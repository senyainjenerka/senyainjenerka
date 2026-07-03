# Тест-кейсы: клиентское веб-приложение (legal-tech платформа)

> Тест-кейсы разработаны и оформлены в TestRail в ходе производственной практики (мануальное функциональное тестирование клиентского веб-приложения). Из соображений NDA конкретное название продукта, компания и внутренние ссылки заменены на нейтральные формулировки.

**Автор:** Ксения Середа | **Всего кейсов:** 207 | **Тип:** Functional

## Оглавление

1. [Профиль пользователя](#профиль-пользователя) — 9 кейсов
2. [Способы оплаты: карты и банковские счета](#способы-оплаты-карты-и-банковские-счета) — 31 кейсов
3. [Recurring Billing (регулярные платежи)](#recurring-billing-регулярные-платежи) — 6 кейсов
4. [Удаление аккаунта](#удаление-аккаунта) — 5 кейсов
5. [Смена пароля](#смена-пароля) — 2 кейсов
6. [Дополнительные негативные сценарии: платежи, пароль, доступ](#дополнительные-негативные-сценарии-платежи-пароль-доступ) — 17 кейсов
7. [Запись на встречу (календарь специалиста)](#запись-на-встречу-календарь-специалиста) — 11 кейсов
8. [Вход и регистрация](#вход-и-регистрация) — 37 кейсов
9. [Поиск специалиста](#поиск-специалиста) — 15 кейсов
10. [Фильтры результатов поиска](#фильтры-результатов-поиска) — 18 кейсов
11. [Список и карточка специалиста, сортировка](#список-и-карточка-специалиста-сортировка) — 23 кейсов
12. [Полный профиль специалиста и календарь](#полный-профиль-специалиста-и-календарь) — 10 кейсов
13. [Дополнительные негативные сценарии: поиск](#дополнительные-негативные-сценарии-поиск) — 8 кейсов
14. [Отзывы и комментарии](#отзывы-и-комментарии) — 15 кейсов


## Профиль пользователя

### TC-001. Check that user can see their profile
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. Open [открыта нужная страница приложения]
2. log in to the system
3. open account menu
4. select ‘profile’ option in the menu

**Ожидаемый результат:** The profile page is displayed with all personal, contactinformation

---

### TC-002. Check that user can update Profile information
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. log in to the system
2. open account menu
3. select ‘profile’ option in the menu

**Проверяемые варианты:**

| Действие | Ожидаемый результат |
|---|---|
| update "First Name" | The updated information is saved successfully |
| update "Last Name" | The updated information is saved successfully |
| update "Country" | The updated information is saved successfully |
| update "Address" | The updated information is saved successfully |
| update "City" | The updated information is saved successfully |
| update " Zip Code / Postal Code " | The updated information is saved successfully |
| update " Apartment, Suite, PO Box " | The updated information is saved successfully |
| update " State / Province " | The updated information is saved successfully |
| update " Mobile phone " | The updated information is saved successfully |

---

### TC-003. Check input validation in profile
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. log in to the system
2. open account menu
3. select ‘profile’ option in the menu

**Проверяемые варианты:**

| Действие | Ожидаемый результат |
|---|---|
| The "First Name" accepts 1 character | The field accepts the input |
| The "First Name" accepts 2 characters | The field accepts the input |
| The "First Name" accepts 25 characters | The field accepts the input |
| The "First Name" accepts 49 characters | The field accepts the input |
| The "First Name" accepts 50 characters | The field accepts the input |
| The "Last Name" accepts 1 character | The field accepts the input |
| The "Last Name" accepts 2 characters | The field accepts the input |
| The " Last Name" accepts 25 characters | The field accepts the input |
| The " Last Name" accepts 49 characters | The field accepts the input |
| The " Last Name" accepts 50 characters | The field accepts the input |
| The "First Name" can't be submitted empty | The field doesn't accept the input. |
| The "Last Name" can't be submitted empty | The field doesn't accept the input. |
| The "First Name" can't accepts 51 characters | The field doesn't accept the input. |
| The "Last Name" can't accepts 51 characters | The field doesn't accept the input. |
| The "Country" can't be submitted empty | The field doesn't accept the input. The error "Please fill in the fiel d" is displayed |
| The "Address" accepts 1 character | The field accepts the input |
| The "Address" accepts 2 c haracters | The field accepts the input |
| The "Address" accepts 50 c haracters | The field accepts the input |
| The "Address" accepts 99 c haracters | The field accepts the input |
| The "Address" accepts 100 c haracters | The field accepts the input |
| The "Address" can't accepts 101 characters | The field doesn't accept the input |
| The "Address" can't be submitted empty | The field doesn't accept the input. The error "Please fill in the field" is displayed |
| The "City" accepts 1 c haracter | The field accepts the input |

---

### TC-004. Check that State/Province dropdown is populated with US states when USA is selected
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. Open [открыта нужная страница приложения]
2. log in to the system
3. open account menu
4. select ‘profile’ option in the menu

**Ожидаемый результат:** The list of US states is displayed

---

### TC-005. Check that State/Province dropdown is populated with Canadian provinces when Canada is selected
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. Open [открыта нужная страница приложения]
2. log in to the system
3. open account menu
4. select ‘profile’ option in the menu

**Ожидаемый результат:** The list of Canadian provinces is displayed

---

### TC-006. Check that switching country resets all other fields to default state
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** All fields are cleared when the country is changed

---

### TC-007. Check that the Country dropdown contains USA and Canada sorted alphabetically
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Ожидаемый результат:** USA and Canada are displayed in alphabetical order

---

### TC-008. Check that user can cancel their changes in the profile
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** Changes are not saved and the original information is displayed

---

### TC-009. Check that user can add contact information
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** Contact information is saved successfully and displayed in the profile

---


## Способы оплаты: карты и банковские счета

### TC-010. Check that user can see List of Cards
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The list of added cards is displayed with all required elements

---

### TC-011. Check that user can see List of Bank accounts
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The list of added bank accounts is displayed with all required elements

---

### TC-012. Check that placeholder is displayed when no payment methods are added
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The placeholder is shown in the payment methods section

---

### TC-013. Check that user can check and uncheck ‘default’ status of payment methods
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The default status is updated and displayed correctly

---

### TC-014. Check that user can delete any card at any time
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The card is deleted and no longer displayed in the card list

---

### TC-015. Check that user can delete any bank account at any time
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The bank account is deleted and no longer displayed in the list

---

### TC-016. Check that the system asks the user to confirm card deletion
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** A confirmation dialog is displayed before the card is deleted

---

### TC-017. Check that the system asks the user to confirm bank account deletion
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** A confirmation dialog is displayed before the bank account is deleted

---

### TC-018. Check that pending payments remain valid after the card is deleted
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** Pending payments are still processed successfully using the deleted card

---

### TC-019. check that only one payment method can be the default
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** Only one payment method is marked as default at a time

---

### TC-020. Check that one payment method should be always marked as default
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** At least one payment method is always marked as default

---

### TC-021. Check that bank account should be automatically marked as default once it’s status becomes ‘ready’
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The bank account is automatically marked as default when its status becomes "Ready"

---

### TC-022. Check that the default payment method is used for auto charges and pre-selected for manual payment
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The default payment method is automatically charged and pre-selected on the manual payment screen

---

### TC-023. Check that user can add the card
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Проверяемые варианты:**

| Действие | Ожидаемый результат |
|---|---|
| add Visa | The card is saved successfully |
| add MasterCard | The card is saved successfully |
| add American Express | The card is saved successfully |
| add Discovery | The card is saved successfully |
| add Dinners Club | The card is saved successfully |
| add JCB | The card is saved successfully |
| add China Union Pay | The card is saved successfully |
| Enter 16 digits in the "Card number" field | The field accepts the input |
| Enter less than 16 digits in the "Card number " field | The field doesn't accepts the input |
| "Card number" field is empty | The form is not submitted |
| Enter letters i n the "Card number" field | The field doesn't accepts the input |
| Enter special symols i n the "Card number" field (e.g. #@) | The field doesn't accepts the input |
| Enter valid date in the past in the "Card expire date" field | The field accepts the input |
| Enter a date in the past in the "Card expire date" field | The form is not submitted |
| Enter special symols i n the "Card expire date" field (e.g. #@) | The field doesn't accepts the input |
| Enter letters i n the "Card expire date field | The field doesn't accepts the input |
| Enter invalid date i n the "Card expire date" field (e.g. 13/25) | The field doesn't accepts the input |
| Enter 3 digits in the "CVC" field | The field accepts the input |
| Enter 4 digits in the "CVC" field for American Express | The field accepts the input |
| Enter 2 digits in the "CVC" field | The field doesn't accepts the input |
| Enter more than 3 digits in the "C VC" field | The field doesn't accepts the input |
| Enter 3 digits in the "CVC" field for American Express | The field doesn't accepts the input |
| "CVC" field is empty | The form is not submitted |
| Enter letters i n the "CVC" field | The field doesn't accepts the input |

---

### TC-024. Check that user can add the bank account
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The bank account is saved successfully and displayed in the bank accounts list

---

### TC-025. Check that user can see card details
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Проверяемые варианты:**

| Действие | Ожидаемый результат |
|---|---|
| see Type of the Card |  |
| see Last 4 numbers of the Card number |  |
| see Card label |  |
| see Mark if the card is the default |  |
| see expiration date |  |
| see option to delete the card |  |
| see option to edit the card |  |

---

### TC-026. Check that the Default card checkbox is unchecked by default
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The checkbox state is false

---

### TC-027. Check that the user can mark the card as default during adding
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The card is saved and marked as default

---

### TC-028. Check that the user can cancel card adding
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The card is not saved

---

### TC-029. Check that the user can cancel bank account adding
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The bank account is not saved and the form is closed

---

### TC-030. Check that clicking "Add credit card" button opens the card adding form
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The card adding form is displayed with all required fields: Card number, Card expire date, CVC, Card label, Default card checkbox

---

### TC-031. Check that user can edit the card label
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The updated label is saved and displayed in the card list

---

### TC-032. Check that the user can add a US bank account (ACH)
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The US bank account is added and displayed in the bank accounts list

---

### TC-033. Check that the user can add a Canadian bank account (PAD)
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The Canadian bank account is added and displayed in the bank accounts list

---

### TC-034. Check that the bank accounts are sorted by date added descending
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The most recently added bank account appears first in the list

---

### TC-035. Check that the cards are sorted by date added descending
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The most recently added card appears first in the list

---

### TC-036. Check that the bank accounts have the following elements
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Проверяемые варианты:**

| Действие | Ожидаемый результат |
|---|---|
| see Last four digits of the account number |  |
| see Bank name |  |
| see Account Status |  |
| see Mark if bank account is default |  |
| see Option to delete the bank account |  |

---

### TC-037. Check that clicking "Add bank account" button opens the bank account adding form
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The bank account adding form is displayed

---

### TC-038. Check that the user can verify a US bank account via instant verification
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The bank account status becomes "Ready" after instant verification

---

### TC-039. Check that the user can verify a Canadian bank account via instant verification
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The bank account status becomes "Ready" after instant verification

---

### TC-040. Check that the user can verify a Canadian bank account via micro-deposits
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The bank account status becomes "Ready" after entering correct deposit amounts

---


## Recurring Billing (регулярные платежи)

### TC-041. Check that the client receives an email with a link to the "Recurring Billing" approval screen
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The email is received and the link opens the approval screen

---

### TC-042. Check that all "Recurring Billing" details are displayed on the approval screen
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** Provider Name, Project name, Amount, Invoicing schedule, First billing date are displayed

---

### TC-043. Check that the "Recurring Billing" details are not editable on the approval screen
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** All fields are disabled and can't be edited

---

### TC-044. Check that the client can approve recurring billing
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** Status "Approved" is shown on the approval screen

---

### TC-045. Check that the client can decline recurring billing
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** Status "Rejected" is shown on the approval screen

---

### TC-046. Check that the status "Stopped" is shown when Pro stops billing
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** Status "Stopped" is displayed on the approval screen

---


## Удаление аккаунта

### TC-047. Check that the user can request account deletion
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The deletion request is submitted, emails are sent to connected Pros and Admin

---

### TC-048. Check that the system asks the user to confirm account deletion
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** Confirmation dialog with message M0072 is displayed

---

### TC-049. Check that the user can cancel the account deletion request
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The deletion request is removed and email E0043a is sent to Admin

---

### TC-050. Check that the system asks the user to confirm cancellation of account deletion
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** Confirmation dialog with message M0069 is displayed

---

### TC-051. Check that the user can request account deletion again after cancelling it
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The deletion request is submitted successfully

---


## Смена пароля

### TC-052. Check update password validation
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Проверяемые варианты:**

| Действие | Ожидаемый результат |
|---|---|
| Enter current password with valid data | The password is updated, the user is logged out and receives an email notification |
| Enter the current password with more than 50 characters | The field does not accept input |
| Enter current password field empty | The form is not submitted and error M0001 is shown |
| Enter new password field empty | The form is not submitted and error M0001 is shown |

---

### TC-053. Check that the user can cancel password updating
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The password is not changed and the user stays on the profile page

---


## Дополнительные негативные сценарии: платежи, пароль, доступ

### TC-054. Check user can't delete contact information
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** The delete option is not available for contact information

---

### TC-055. Check that user can't delete default bank account
**Приоритет:** Критический | **Тип сценария:** Негативный

**Ожидаемый результат:** The delete option is not available for the default bank account

---

### TC-056. Check that user can't delete default card
**Приоритет:** Критический | **Тип сценария:** Негативный

**Ожидаемый результат:** The delete option is not available for the default card

---

### TC-057. Check that user can't uncheck the card as default
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** The uncheck option is not available for the default card

---

### TC-058. Check that user can't uncheck the bank account as default
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** The uncheck option is not available for the default bank account

---

### TC-059. Check that the user cannot edit card details
**Приоритет:** Важный | **Тип сценария:** Негативный

**Проверяемые варианты:**

| Действие | Ожидаемый результат |
|---|---|
| Edit card number | The card number editing option is not available |
| Edit card expiration date | The expiration date editing option is not available |
| Edit CVC | The CVC editing option is not available |

---

### TC-060. Check that the system shows an error if the bank account is already added
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** An error message is displayed and the bank account is not added again

---

### TC-061. Check that the user cannot add more than 5 bank accounts
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** The option is disabled and a tooltip about the limit is shown

---

### TC-062. Check that the bank account with status "Verification Failed" cannot be used for payment
**Приоритет:** Критический | **Тип сценария:** Негативный

**Ожидаемый результат:** The account is not available as a payment option

---

### TC-063. Check that micro-deposit verification fails after 3 incorrect attempt
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** The bank account status becomes "Verification Failed"

---

### TC-064. Check that the "Approve" button is disabled when no default payment method exists
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** The Approve button is disabled

---

### TC-065. Check that the user cannot schedule new meetings after requesting account deletion
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** The meeting scheduling option is not available

---

### TC-066. Check that the Pro cannot create cases or activities with the client after account deletion is requested
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** The option to create cases/activities is not available for the Pro

---

### TC-067. Check that the system shows an error if the retyped password doesn't match the new password
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** Error M0006 is displayed

---

### TC-068. Check that the system shows an error if the new password is the same as the current password
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** Error M0011 is displayed

---

### TC-069. Check that the system shows an error if the password doesn't meet minimum length requirement
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** Error M0004 is displayed

---

### TC-070. Check that the system shows an error if the password doesn't meet the required rules
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** Error M0005 is displayed

---


## Запись на встречу (календарь специалиста)

### TC-071. Сheck that the user can see available dates in Pro's calendar
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** Available dates are displayed in the user's time zone

---

### TC-072. Check that the user can select a date in Pro's calendar
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** Available time slots for the selected date are displayed

---

### TC-073. Check that 30-minute time slots are available for initial meeting
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** 30-minute slots are displayed in Pro's calendar

---

### TC-074. Check that 30 and 60-minute time slots are available for connected users
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** Both 30 and 60-minute options are displayed

---

### TC-075. Check that 30-minute option is selected by default
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The 30-minute option is pre-selected

---

### TC-076. Check that selecting 60-minute meeting shows only 60-minute slots
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** Only 60-minute available slots are displayed

---

### TC-077. Check that the user is navigated to meeting details page after selecting a time slot
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The meeting details page opens at the same tab

---

### TC-078. Check that the user is navigated to login form if not logged in when selecting a time slot
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** The login form opens with Client role pre-selected and Pro option disabled

---

### TC-079. Check that the user is navigated to meeting details page after logging in via Email
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The meeting details page opens

---

### TC-080. Check that the user is navigated to meeting details page after logging in via Google/FB
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The meeting details page opens

---

### TC-081. Check that the user is navigated to meeting details page after signing up via Google/FB
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The meeting details page opens

---


## Вход и регистрация

### TC-082. Check that the user can open the sign-in form from the main page?
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** The sign-in form opens correctly after clicking the corresponding control

---

### TC-083. Check that the user can select the "Client" role on the sign-up form?
**Приоритет:** Важный | **Тип сценария:** Позитивный

---

### TC-084. Check that user can signing in via Email and Password
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Enter valid Email (e.g myasobulka+13@gmail.com)
3. Enter vslid password (e.g. 1qaz!QAZ)
4. Click to the "Continue" button

**Ожидаемый результат:** The user is successfully logged into the system

---

### TC-085. Check that user can signing in via Google account
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. The user has previously logged in to Google account
3. Click to the "Google" button
4. Complete Coogle OAuth

**Ожидаемый результат:** The user is successfully logged into the system

---

### TC-086. Check that the user can sign in via Facebook account?
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. The user has previously logged in to Facebook account
3. Click to the "Google" button
4. Complete Facebook OAuth

**Ожидаемый результат:** The user is successfully logged into the system

---

### TC-087. Check that the user can enter an Email in the input field
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Enter an Email (e.g. myasobulka+13@gmail.com)

**Ожидаемый результат:** The "Email" field accepts text input

---

### TC-088. Check that the user can enter a Password in the input field
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Enter a Password (e.g. 1qaz!QAZ)

**Ожидаемый результат:** The Password field accepts text input and masks it.

---

### TC-089. Check the "Forgot Password" link
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Click to the "Forgot Password" link

**Ожидаемый результат:** The "Forgot Password" form opens

---

### TC-090. Check the "New to Платформа? Sign Up" button
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Click to the "New to Платформа? Sigh Up" button

**Ожидаемый результат:** The "Sign Up" form opens

---

### TC-091. Check that the user can sign in as Pro with valid email and password
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Enter Pro Email (e.g. kbparamonov+lawyer@gmail.com)
3. Enter vslid password (e.g. 1qaz!QAZ)
4. Click to the "Continue" button

**Ожидаемый результат:** The user is successfully logged in as Pro and navigated to the Dashboard/Events or profile creation step

---

### TC-092. Check that the user can sign in as Client with valid email and password
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Enter Client Email (e.g. myasobulka+13@gmail.com )
3. Enter vslid password (e.g. 1qaz!QAZ)
4. Click to the "Continue" button

**Ожидаемый результат:** The user is successfully logged in as Client and navigated to the welcome screen/ events

---

### TC-093. Check that a signed-in user returning to the Платформа URL is auto-authenticated
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. The user has previously logged in
2. Open a new tab and navigate to the Платформа application URL

**Ожидаемый результат:** The user is redirected to Dashboard without login form

---

### TC-094. Check that the system sends a password-reset link to a registered email
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Click to the "Forgot password" link
3. Enter an Email
4. Click to "Reset password" button

**Ожидаемый результат:** Password-reset email i sent to the provided address

---

### TC-095. Check the "Back to Log in" link on the "Forgot password" form
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Click to the "Back to Log in" link

**Ожидаемый результат:** The "Log in" form opens

---

### TC-096. Check that the system shows a success message after submitting a registered email
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Click to the "Forgot password" link
3. Enter an Email
4. Click to "Reset password" button

**Ожидаемый результат:** Success message is displayed

---

### TC-097. Check that clicking the reset link opens the new password form
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. Complete password reset on the "Forgot password" form
2. Following the link from the Email

**Ожидаемый результат:** The "restore password" form opens

---

### TC-098. Check that the user can set a new valid password
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. The "restore password" form is opened
2. Enter new valid password (e.g. 1qaz!QAZ)

**Ожидаемый результат:** The password is updated

---

### TC-099. Check that the user is navigated to the sign-in page with success notification after reset
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. The "restore password" form is opened
2. Complete reset password

**Ожидаемый результат:** Sigh in page opens with success notification

---

### TC-100. Check that an unregistered user can open sign-up form via invitation link
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** Sign-up form opens with the Client role preselected and the Pro role option disabled

---

### TC-101. Check that the system establishes Client-Pro connection after email verification
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** the connection is created between the new Client and the Pro

---

### TC-102. Check that both parties are notified after connection is established
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** Notifications are sent to oth Client and Pro

---

### TC-103. Check that a registered but not-connected user is navigated to sign-in when clicking invite link
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** Sign in form opens

---

### TC-104. Check that the system establishes connection after registered user signs in via invite link
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Ожидаемый результат:** Connection is established

---

### TC-105. Check that the new Client is navigated to the relevant next step after sign-up via invite
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. Click expired invitation link
2. Verify error message displayed

**Ожидаемый результат:** The meeting details or connections opens

---

### TC-106. Check that the user can't sign in with empty email field
**Приоритет:** Важный | **Тип сценария:** Негативный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. The "Email" field is empty
3. Click to the "Continue" button

**Ожидаемый результат:** The field doesn't accept the input. The message " please type your email " is displayed

---

### TC-107. Check that the user can't sign in with empty password field
**Приоритет:** Критический | **Тип сценария:** Негативный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. The "Password" field is empty
3. Click to the "Continue" button

**Ожидаемый результат:** The field doesn't accept the input. The message " please type your password " is displayed

---

### TC-108. Check invalid Email and Password combination
**Приоритет:** Важный | **Тип сценария:** Негативный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Enter valid Email( e.g. myasobulka+13@ )
3. Enter invalid Password ( e.g. aaa)
4. Click to the "Continue" button

**Ожидаемый результат:** Error message M0020(" Your login info is incorrect. Please check and try again. ") is displayed, and sign-in is blocked for invalid credentials.

---

### TC-109. Check that the user can't sign in with a blocked account
**Приоритет:** Критический | **Тип сценария:** Негативный

---

### TC-110. Check that the system offers to sign up when the account doesn't exist
**Приоритет:** Важный | **Тип сценария:** Негативный

---

### TC-111. Check that the user can't submit the forgot password form with empty email
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---

### TC-112. Check that the user can't submit the forgot password form with invalid email format
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---

### TC-113. Check that an expired reset link shows an appropriate error
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---

### TC-114. Check that the user can't set a password less than 8 symbols
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---

### TC-115. Check that the user can't set a password that does not meet complexity rules
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---

### TC-116. Check that the user can't set a password when confirmation does not match
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---

### TC-117. Check that the user can't set the same password as the current one
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---

### TC-118. Check that an expired invitation link shows an appropriate error
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---


## Поиск специалиста

### TC-119. Check that the user can search a Pro by practice area
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Enter practice area in search field
3. Click to the "Search" icon

**Ожидаемый результат:** Search results page opens with matching Pros

---

### TC-120. Check that the user can search a Pro by sub-specialty
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Enter sub-specialty in search field
3. Click to the 'Search' icon

**Ожидаемый результат:** Search results page opens with matching Pros

---

### TC-121. Check that the user can search a Pro by name
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Enter name in search field
3. Click to the 'Search' icon

**Ожидаемый результат:** Search results page opens with matching Pros
[см. документацию требований проекта]
The user should be able to type Pro name and trigger search.
The system should perform search
by Pro First name and Last name on ‘start with’ principle(e.g. user types Mar and trigger search, then the system should show all Pros whose First and/or Last name starts with Mar)
starting from 3 symbols. If the user types less symbols or no symbols at all, then the system should ask to provide name
no autosuggest should be implemented
If there are no Pros found, the placeholder should be presented.
By reloading, the typed search request should be saved.

---

### TC-122. Check that the "practice area or legal topic" search field provides auto-suggestions
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Start typing in the "practice area or legal topic" search field
3. Verify auto-suggestions dropdown appears

**Ожидаемый результат:** Auto-suggestions dropdown is displayed
[см. документацию требований проекта]
The search should be performed on the 'starts' principle:
each word in the Practice area/sub-specialty name should be considered
exceptions are articles and conjunctions: a, the, or, of, with and.
The search should be performed starting with the first letter.
Autocomplete by practice area and subspeciality should be introduced by searching.
if there are more than 6 TBD items in the list, vertical scroll bar should be introduced in the list
first 10 results should be displayed in the list
The found fragment of the search request should be highlighted in the word
the system should display First and Last name of the user in the list
items should be displayed alphabetically
if practice area matches the search request, it should be displayed with related sub-specialties
if a sub-specialty and practice area matches the search request, it should be displayed with their ‘parent’ practice area. Matching sub-specialty should be on the top in the practice area. All other related sub-specialties in alphabetical order

---

### TC-123. Check that the "state" search field provides auto-suggestions
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Start typing in the "state" search field
3. Verify auto-suggestions dropdown appears

**Ожидаемый результат:** Auto-suggestions dropdown is displayed
[см. документацию требований проекта]
Autocomplete should work in the same way as for the practice area.

---

### TC-124. Check that "practice area" displays in alphabetical order with sub-specialties sorted alphabetically
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Start typing in the "practice area or legal topic" search field
3. Verify auto-suggestions dropdown appears

**Ожидаемый результат:** B y click on the search area system should show the list of practice areas in alphabetical order with related sub-specialties sorted in alphabetical order. The user should be able to choose one sub-specialty.
[см. документацию требований проекта]

---

### TC-125. Check that "state" displays in alphabetical order
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Start typing in the "state" search field
3. Verify auto-suggestions dropdown appears

**Ожидаемый результат:** The system should present the list with USA states to the user sorted alphabetically.
[см. документацию требований проекта]

---

### TC-126. Check that the user informed if Платформа is not officially launched in a specified state
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. Enter "practice area or legal topic/name" search field
2. Enter specified state, for example Alaska
3. Click to the "Search" icon

**Ожидаемый результат:** According to the search results, the user should be informed if Платформа is not officially launched in a specified state. The message " We have not officially launched in Alaska . Once we are in Alaska, there will be a larger selection of Alaska lawyers available to you. " is displayed
[см. документацию требований проекта]

---

### TC-127. Check the search by pressing the Enter key
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Enter practice area or legal topic/name in the search field
3. Enter/select state
4. Press "Enter" key

**Ожидаемый результат:** The user should be navigated to the page with ‘ advanced search ’
[см. документацию требований проекта]
To search for a Pro, the user should be able to:
trigger searching(button on the page + Enter)

---

### TC-128. Сheck that the placeholder is displayed when no Pros are found
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Enter a non-existing Pro name in the search field, for example Meow
3. Click to the 'Search' icon

**Ожидаемый результат:** The list of Pros is empty. The system shows placeholder with message " No lawyers were found meeting your criteria. Please modify some of the search parameters and start a new search "
[см. документацию требований проекта]
if no results found, the placeholder should be presented.

---

### TC-129. Check that the "practice area" search type is pre-selected by default
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Verify the search type field

**Ожидаемый результат:** By default, practice area should be selected.
[см. документацию требований проекта]

---

### TC-130. Check that the selected search type is saved after page reload
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Select the search type, for example "Name"
3. Reload the page

**Ожидаемый результат:** By reloading, selected search type should be saved.
[см. документацию требований проекта]

---

### TC-131. Check that the search is not case-sensitive
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Enter practice area or legal topic/name in the search field in UPPERCASE
3. Enter/Select state
4. Click to the 'Search' icon
5. Repeat with lowercase
6. Verify same results returned

**Ожидаемый результат:** Same results are returned

---

### TC-132. Check that the user can select a US state from the dropdown before searching
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Click to the state dropdown
3. Select a US state

**Ожидаемый результат:** State is selected

---

### TC-133. Check that only states with at least one active Pro are shown in the dropdown
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Click to the state dropdown

**Ожидаемый результат:** Only states with active Pros are displayed

---


## Фильтры результатов поиска

### TC-134. Check that the user can filter Pros by State
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Click to the state dropdown
3. Select a US state
4. Click to the "Search" icon

**Ожидаемый результат:** Results list is displaed with Pros from the selected state

---

### TC-135. Check that the user can filter Pros by Price range
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is open
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Set Price range filter

**Ожидаемый результат:** Results list updates with the selected price
[см. документацию требований проекта]
The user should be able to select the desired price range between the highest and the lowest for the practice area.
The highest bound should be equal to the $1000 + (all Pros that have hourly rate 1000 and more should be displayed)
The lowest bound should be equal to $0
The user should be able to update both boundaries.
The user should be able to enter bounds value by moving UI control or enter the values in the two fields.
Two fields should be presented for lowest and highest bound (Numeric, max value 1000)
the user should not be able to enter a value for the lowest bound more than for highest and vice versa
if the user leaves one of the fields empty, the default value should be set
if the user enter ‘1000’ value, ‘1000+’ should be presented and ll Pros that have hourly rate 1000 and more should be displayed
By default, the filter should not be applied.

---

### TC-136. Check that the average price value indicator is displayed
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is open
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Verify average price indicator is displayed

**Ожидаемый результат:** Value indicator is shown on the price filter

---

### TC-137. Check that the user can filter Pros by Initial consultation availability
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is open
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Enable ' no charge initial consult ' filter

**Ожидаемый результат:** Results list updates to show only Pros with free initial consultations
[см. документацию требований проекта]
The user should be able to filter Pro by the ‘free’ consultation .(true/false control)
By default, the filter should not be applied.

---

### TC-138. Check that the user can filter Pros by Languages spoken
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is open
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Select any language

**Ожидаемый результат:** Results list updates according to selected language
[см. документацию требований проекта]
The user should be able to see the list of languages and search for languages that are presented in the system and select the desired( only one language can be selected) . By search the found fragment should be highlighted.
By default, English should be predefined.

---

### TC-139. Check that the user can filter Pros by Fee types
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is open
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Select "contingency" fee type
5. Select "flat fee" fee type

**Ожидаемый результат:** Results list updates according to selected fee type
[см. документацию требований проекта]
The user should be able to select price methods what Pro are provided:
contingency(true/false control)
fixed price(true/false control)
By default, the filter should not be applied.

---

### TC-140. Check that the user can filter Pros by Rating
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is open
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Select a rating value

**Ожидаемый результат:** Results list updates according to selected rating.
[см. документацию требований проекта]
The user should be able to select rating of a Pro that should be presented in the Pros list:
more or equal to 1 star
more or equal to 2 stars
more or equal to 3 stars
more or equal to 4 stars
equal to 5 stars
When User applies filtering by rating, the system should display result based on available rating.
If a Pro doesn’t have connected calendar, the system still should display the highest rating first. If two Pros have the same exact rate then the one with connected calendar should be shown first.
If no rating is available, the system displays those Pro at the end of the search.

---

### TC-141. Check that the user can toggle "Lawyers in my state only"
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Toggle ' lawyers in my state only '

**Ожидаемый результат:** Results list updates according to toggle state

---

### TC-142. Check that the availability time slider is available
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Verify the availability time slider

**Ожидаемый результат:** Availaility time slider is displayed

---

### TC-143. Check that the default slider position is set now to 30 days ('anytime')
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Verify the availability time slider
5. Verify default position is 'now' to 30 days

**Ожидаемый результат:** Slider shows range from now to 30 days by default
[см. документацию требований проекта]
default from now to 30 days('anytime' wording)

---

### TC-144. Check that the user can filter Pros by availability time using the slider
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Verify the availability time slider
5. Regulate time range

**Ожидаемый результат:** Results list updates according to selected time range
[см. документацию требований проекта]
The user should be able to filter Pros with connected calendar by availability time.
The user should be able to use slider to filter Pros.
default from now to 30 days('anytime' wording)
Do not allow bullets to overlap
Make infinite slider (no separate slices)
Intervals:
now
4 hours
8 hours
12 hours
16 hours
24 hours
2 days
3 days
4 days
5 days
6 days
7 days
14 days
30 days
When User applies filtering by earliest available time, the system should display result based on available time.
If no calendar is available, the system displays those Pro at the end of the search.

---

### TC-145. Check that filters are applied dynamically without page refresh
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Apply multiple filters

**Ожидаемый результат:** Results list updates on each filter change
[см. документацию требований проекта]
Once the user updates any of the filter parameters, the Pros list should be updated.

---

### TC-146. Check that the user can reset all filters to defaults
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Apply multiple filters
5. Click to the 'Reset all' button

**Ожидаемый результат:** All filters return to default values, results list updates
[см. документацию требований проекта]
The user should be able to reset all filters. All filters should be in the default state.

---

### TC-147. Check that filters are reset after the page/card is reloaded
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Apply multiple filters
5. Reload the page

**Ожидаемый результат:** All filters return to default state after reload
[см. документацию требований проекта]
Filters should not be saved and be r eset after each card reloading

---

### TC-148. Check that the number of currently displayed Pros is shown according to applied filters
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Apply multiple filters

**Ожидаемый результат:** The count of Pros updates
The user should be able to see the number of Pros that are currently displayed according to filters.
[см. документацию требований проекта]

---

### TC-149. Check that the filters panel stays fixed on screen while scrolling through the Pro list
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Scroll down through the Pro list

**Ожидаемый результат:** Filters panel should be fixed and not disappear by scrolling
[см. документацию требований проекта]

---

### TC-150. Check that average price is not displayed if no Pros are found
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is open
2. No one Pros in the search results
3. Filter panel is displayed
4. Verify the price rage filter

**Ожидаемый результат:** The average price indicator is not displayed
\ [см. документацию требований проекта]
If the are no Pros, average price can be calculated for, the average price should not be displayed.

---

### TC-151. Check that average price is not calculated when searching by Pro name
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. Enter "name" search field
2. Click to the "Search" icon
3. At least one Pros listed in the results
4. Filter panel is displayed
5. Verify the price rage filter

**Ожидаемый результат:** The average price indicator is hidden
[см. документацию требований проекта]
By searching by name the average price should not be calculated and presented.

---


## Список и карточка специалиста, сортировка

### TC-152. Check that the user can sort Pros by Price
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Sort dropdown is displayed
4. Open sort dropdown
5. Select "highest standard hourly rate" and check the results
6. Select "lowest standard hourly rate" and check the results

**Ожидаемый результат:** Results list is sorted correctly
[см. документацию требований проекта]
price (highest first) Pros in the list should be sorted by the price for practice areas.
If Pros are filtered by a practice area, the only price for the selected practice areas should be considered by sorting
If Pros are filtered by a sub-specialty, the only price for the practice area of a selected sub-specialty should be considered by sorting
price (lowest first) . Pros in the list should be sorted by the price for practice areas.
If Pros are filtered by a practice area, the only price for the selected practice areas should be considered by sorting
If Pros are filtered by a sub-specialty, the only price for the practice area of a selected sub-specialty should be considered by sorting

---

### TC-153. Check that the user can sort Pros by nearest available time slot
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Sort dropdown is displayed
4. Open sort dropdown
5. Select "earliest availability" slot

**Ожидаемый результат:** Results list is sorted from earliest to latest available slot
[см. документацию требований проекта]
availability time (sooner available time first) Pros in the list should be sorted by availability time. Pros that have no availability time, should be presented at the end of the list in any order.

---

### TC-154. Check that the user can sort Pros by Rating
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Sort dropdown is displayed
4. Open sort dropdown
5. Select "highest star ranking" slot

**Ожидаемый результат:** Results list is sorted by rating from highest
[см. документацию требований проекта]
rating(highest first) Pros in the list should be sorted by rating. Pros that have no rating, should be presented at the end of the list in any order.

---

### TC-155. Check that Pros without a connected calendar are placed at the end when sorting by availability time
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Sort dropdown is displayed
4. Open sort dropdown
5. Select "earliest availability" slot

**Ожидаемый результат:** Results list is sorted from earliest to latest available slot. Pros without calendar are at the bottom of the list
[см. документацию требований проекта]
Pros that have no availability time, should be presented at the end of the list in any order.

---

### TC-156. Check that the non-logged user can access the list of Pros by triggering search from the main page
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. User is non-logged
3. Enter practice area or legal topic/name in search field
4. Select state
5. Click to the "Search" icon

**Ожидаемый результат:** Search results page opens with Pro short-profile cards
[см. документацию требований проекта]
Non-logged user should be able to view the list of Pros by triggering search on the Платформа main page

---

### TC-157. Check that each Pro card displays the Pro's photo
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results

**Ожидаемый результат:** Pro photo is displayed on the card

---

### TC-158. Check that each Pro card displays the Pro's first and last name
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results

**Ожидаемый результат:** Pro name is displayed on the card

---

### TC-159. Check that each Pro card displays rating and review count
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results

**Ожидаемый результат:** Rating and review count are displayed on the card

---

### TC-160. Check that each Pro card displays price for initial consultation
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results

**Ожидаемый результат:** Price for initial consultation is displayed on the card

---

### TC-161. Check that the nearest available time slot is displayed on Pro card (if calendar connected)
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Verify a Pro with connected calendar

**Ожидаемый результат:** Date and time in am/pm format (e.g. Jan 23 · 2:00 pm) are displayed on the Pro card

---

### TC-162. Check that the nearest free time slot is 30 min for initial meeting on the Pro card
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the result s
3. Verify a Pro with connected calendar

**Ожидаемый результат:** The nearest free time 30-minute slot is displayed on the Pro card

---

### TC-163. Check that clicking the nearest free time slot asks the user to log in
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with connected calendar
5. Click to the "Meet at [time]" button

**Ожидаемый результат:** Login form opens
[см. документацию требований проекта]
Once the user selects a time slot, the system should check if the user is logged in. If the user is not logged in, the system should navigate the user to the login form

---

### TC-164. Check that after signing up via nearest free time slot the user is navigated to the full Pro profile with the selected date and time
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with connected calendar
5. Click to the "Meet at [time]" button on the Pro card
6. Sign up in to the system

**Ожидаемый результат:** the full Pro profile with the selected date and time opens
[см. документацию требований проекта]
After the user follows the verification link(it should have a certain redirect URL if the user comes from the ‘booking time’ process) , they should be navigated to the full Pro profile with the selected date and time

---

### TC-165. Check that a logged-in user is navigated to meeting details page after selecting a time slot
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. User is logged in
3. At least one Pros listed in the result s
4. Verify a Pro with connected calendar
5. Click to the "Meet at [time]" button on the Pro card

**Ожидаемый результат:** Meeting details page opens with selected Pro

---

### TC-166. Check that after logging in (not connected) via nearest free time slot the user is navigated to meeting details page
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with not connected calendar
5. Click to the "Contact" button on the Pro card
6. Log in to the system

**Ожидаемый результат:** Meeting details page opens after log in

---

### TC-167. Check that after logging in (connected) via nearest free time slot the user is navigated to full Pro profile with confirmation popup
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with connected calendar
5. Click to the "Meet at [time]" button on the Pro card
6. Log in to the system

**Ожидаемый результат:** Full Pro profile opens with booking confirmation popup

---

### TC-168. Check that the user is navigated to meeting details page after logging in via Email
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with connected calendar
5. Click to the "Meet at [time]" button on the Pro card
6. Log in with Email

**Ожидаемый результат:** Meeting details page opens

---

### TC-169. Check that the user is navigated to meeting details page after logging in via Google/Facebook
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with connected calendar
5. Click to the "Meet at [time]" button on the Pro card
6. Log in to the system via Google/Facebook

**Ожидаемый результат:** Meeting details page opens

---

### TC-170. Check that a non-logged user is redirected to sign-up when triggering the contact button on the Pro card
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with not connected calendar
5. Click to the "Contact" button on the Pro card

**Ожидаемый результат:** Sign-up form opens

---

### TC-171. Check that a non-logged user is redirected to login form after selecting a time slot
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Open a Pro profile with connected calendar
5. Select a time slot with available date

**Ожидаемый результат:** Login form opens

---

### TC-172. Check that the user can access the full profile by clicking "see bio and more times"
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the result s
3. Click to the "see bio and more times" button on the Pro card

**Ожидаемый результат:** Full Pro profile page opens
[см. документацию требований проекта]
Non-logged users should be able to go to a PRO full profile by triggering “see bio and more times“ button, Pro name or Pro photo

---

### TC-173. Check that the user can access the full profile by clicking the Pro's name
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the result s
3. Click to the Pro's name on the Pro card

**Ожидаемый результат:** Full Pro profile page opens
[см. документацию требований проекта]
Non-logged users should be able to go to a PRO full profile by triggering “see bio and more times“ button, Pro name or Pro photo

---

### TC-174. Check that the user can access the full profile by clicking the Pro's photo
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the result s
3. Click to the Pro's photo on the Pro card

**Ожидаемый результат:** Full Pro profile page opens
[см. документацию требований проекта]
Non-logged users should be able to go to a PRO full profile by triggering “see bio and more times“ button, Pro name or Pro photo

---


## Полный профиль специалиста и календарь

### TC-175. Check that the Pro full profile displays all information
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the result s
3. Any Pros profile is opened

**Проверяемые варианты:**

| Действие | Ожидаемый результат |
|---|---|
| Check that the full profile displays the Pro's photo | Pro photo is displayed |
| Check that the full profile displays the Pro's first and last name | Pro name is displayed |
| Check that the full profile displays practice area and sub-specialties | Practice area and sub-specialties are displayed |
| Check that the full profile displays firm name (if applicable) | Firm name is displayed |
| Check that the full profile displays the Pro's bio | Bio text is displayed |
| Check that the full profile displays rating and reviews | Rating and reviews are displayed |
| Check that the full profile displays languages | Languages are displayed |
| Check that the full profile displays fee types | Fee types are displayed |
| Check that the full profile displays price for initial consultation | Price is displayed |
| Check that the full profile displays available dates and time slots (if calendar connected) | Available dates and time slots are displayed |
| Check that the full profile displays "Book initial consultation" action | "Book initial consultation" button is displayed |
| Check that the full profile displays "Contact via email" action | "Contact via email" button is displayed |

---

### TC-176. Check that the user can see available dates on the Pro's full profile page
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the result s
3. Open a Pro profile with connected calendar

**Ожидаемый результат:** Available dates are displayed per month
[см. документацию требований проекта]
The user should be able to see available dates of Pro.

---

### TC-177. Check that the first available date is pre-selected by default
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the result s
3. Open a Pro profile with connected calendar

**Ожидаемый результат:** First available date is selected by default in the calendar
[см. документацию требований проекта]
By default, the month with the first available date should be opened.

---

### TC-178. Check that days with no free slots are shown but are not selectable
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the result s
3. Open a Pro profile with connected calendar

**Ожидаемый результат:** Days without free slots are visible but not clickable

---

### TC-179. Check that the user can navigate forward through months
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the result s
3. Open a Pro profile with connected calendar
4. Switch calendar to the next month

**Ожидаемый результат:** Next month calendar is displayed.
[см. документацию требований проекта]
The user should be able to switch between months.

---

### TC-180. Check that the user can navigate backward through months
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the result s
3. Open a Pro profile with connected calendar
4. Switch calendar to the next month
5. Swith calendar to the previuos month

**Ожидаемый результат:** Previous month's calendar is displayed
[см. документацию требований проекта]
The user should be able to switch between months.

---

### TC-181. Check that selecting a date displays available time slots for that date
**Приоритет:** Критический | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the result s
3. Open a Pro profile with connected calendar
4. Select any available date

**Ожидаемый результат:** Time slots are displayed for the selected date
[см. документацию требований проекта]
The user should be able to see available time slots for a certain date.

---

### TC-182. Check that 30-minute time slots are shown for the initial meeting
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Шаги воспроизведения:**
1. The user is on the page with search results
2. At least one Pro s listed in the results
3. The user is not logged in
4. The user selects the desired Pro
5. The system navigates the user to the Pro profile full view and displays available dates
6. The user finds the availability time of Pro and selects the desired date
7. The system displays the available time slots for the selected date

**Ожидаемый результат:** [см. документацию требований проекта]
Time slots should be presented:
in am/pm format
by 30 minutes
The time intervals should be shown ONLY from the beginning of an hour and from half an hour (e.g., if user’s current time is 10:12 am, the system should show nearest available slot - 10:30 am OR if user’s time is 10:31 am, the system should show nearest available slot - 11:00 am )
Only the first 16 available time slots should be displayed by default for a selected date. Ff there are more than 16 available time slots, ‘show more’ button should be presented.

---

### TC-183. Check that the time zone is determined by the user's browser geolocation
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** Correct time zone is displayed

---

### TC-184. Check that both calendar and time slots are shown in the user's local time zone
**Приоритет:** Важный | **Тип сценария:** Позитивный

**Ожидаемый результат:** All times are in user's local TZ

---


## Дополнительные негативные сценарии: поиск

### TC-185. Check that the user can't search with empty search field
**Приоритет:** Критический | **Тип сценария:** Негативный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] opened
2. Click to the Search icon

**Ожидаемый результат:** Validation error " please enter a legal topic " is displayed

---

### TC-186. Check that Search by name doesn't trigger search when less than 3 symbols entered
**Приоритет:** Незначительный | **Тип сценария:** Негативный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] opened
2. Select "name" search type
3. Enter less than 3 characters
4. Click to the Search icon

**Ожидаемый результат:** Validation error " Please provide more then 3 symbols " is displayed
[см. документацию требований проекта]
starting from 3 symbols. If the user types less symbols or no symbols at all, then the system should ask to provide name

---

### TC-187. Check that the user can't search without selecting a state
**Приоритет:** Важный | **Тип сценария:** Негативный

**Ожидаемый результат:** Search is blocked

---

### TC-188. Check that the availability time filter is not applied to Pros without a connected calendar
**Приоритет:** Важный | **Тип сценария:** Негативный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Verify the availability time slider
5. Regulate time range

**Ожидаемый результат:** Pros without connected calendar are not displayed

---

### TC-189. Check that the slider bullets can't overlap each other on the availability time filter
**Приоритет:** Незначительный | **Тип сценария:** Негативный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Verify the availability time slider
5. Regulate time range

**Ожидаемый результат:** Bullets stop before overlapping

---

### TC-190. Check that slots already booked are not shown
**Приоритет:** Критический | **Тип сценария:** Негативный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. User is logged in
3. At least one Pros listed in the result s
4. Open a Pro profile with connected calendar
5. Select any tome slot from any available date
6. Schedule a meeting
7. Open the same Pro profile

**Ожидаемый результат:** Booked slot is not displayed

---

### TC-191. Check that slots in the past are not shown
**Приоритет:** Критический | **Тип сценария:** Негативный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. User is logged in
3. At least one Pros listed in the result s
4. Open a Pro profile with connected calendar

**Ожидаемый результат:** Past time slots are not displayed

---

### TC-192. Check that search by name doesn't implement autocomplete
**Приоритет:** Незначительный | **Тип сценария:** Негативный

**Шаги воспроизведения:**
1. [открыта нужная страница приложения] is opened
2. Start typing in the "name" search field
3. Verify auto-suggestions dropdown doesn't appears

**Ожидаемый результат:** Auto-suggestions dropdown is not displayed

[см. документацию требований проекта]
no autosuggest should be implemented

---


## Отзывы и комментарии

### TC-193. Check that approved comments are visible to non-logged users on the Pro's public profile
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

---

### TC-194. Check details of the Comment List (the number of reviews, Платформа rating, and last 4 comments)
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

---

### TC-195. Check that "See all reviews" control loads the full list of comments
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

---

### TC-196. Check that comments are sorted by date (newest first)
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

---

### TC-197. Check that each comment displays star rating (1–5)
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

---

### TC-198. Check that each comment displays comment text
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

---

### TC-199. Check that each comment displays reviewer's first name and last-name initial
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

---

### TC-200. Check that each comment displays the date of the comment
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

---

### TC-201. Check that Pro's reply is shown beneath the comment
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

---

### TC-202. Check that non-logged users can read replies
**Приоритет:** Незначительный | **Тип сценария:** Позитивный

---

### TC-203. Check that a non-logged user can't leave a rating
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---

### TC-204. Check that a non-logged user can't leave a comment
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---

### TC-205. Check that a non-logged user can't flag a comment
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---

### TC-206. Check that a non-logged user can't report a Pro
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---

### TC-207. Check that triggering any interaction redirects non-logged user to sign-up/sign-in
**Приоритет:** Незначительный | **Тип сценария:** Негативный

---
