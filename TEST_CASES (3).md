# Test Cases: Search, Filters & Specialist Profile (Client Web App)

> Тест-кейсы разработаны и оформлены в TestRail в ходе производственной практики (мануальное функциональное тестирование клиентского веб-приложения). Раздел покрывает поиск специалиста, фильтрацию и сортировку результатов, карточку и полный профиль специалиста с календарём. Из соображений NDA конкретное название продукта, компания и внутренние ссылки заменены на нейтральные формулировки.

**Author:** Ksenia Sereda | **Total cases:** 74 | **Type:** Functional

## Table of Contents

1. [Pro Search](#pro-search) — 15 cases
2. [Search Results Filters](#search-results-filters) — 18 cases
3. [Pro List, Card & Sorting](#pro-list-card-sorting) — 23 cases
4. [Full Pro Profile & Calendar](#full-pro-profile-calendar) — 10 cases
5. [Additional Negative Scenarios: Search](#additional-negative-scenarios-search) — 8 cases


## Pro Search

### TC-001. Check that the user can search a Pro by practice area
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Enter practice area in search field
3. Click to the "Search" icon

**Expected Result:** Search results page opens with matching Pros

---

### TC-002. Check that the user can search a Pro by sub-specialty
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Enter sub-specialty in search field
3. Click to the 'Search' icon

**Expected Result:** Search results page opens with matching Pros

---

### TC-003. Check that the user can search a Pro by name
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Enter name in search field
3. Click to the 'Search' icon

**Expected Result:** Search results page opens with matching Pros
[see project requirements documentation]
The user should be able to type Pro name and trigger search.
The system should perform search
by Pro First name and Last name on ‘start with’ principle(e.g. user types Mar and trigger search, then the system should show all Pros whose First and/or Last name starts with Mar)
starting from 3 symbols. If the user types less symbols or no symbols at all, then the system should ask to provide name
no autosuggest should be implemented
If there are no Pros found, the placeholder should be presented.
By reloading, the typed search request should be saved.

---

### TC-004. Check that the "practice area or legal topic" search field provides auto-suggestions
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Start typing in the "practice area or legal topic" search field
3. Verify auto-suggestions dropdown appears

**Expected Result:** Auto-suggestions dropdown is displayed
[see project requirements documentation]
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

### TC-005. Check that the "state" search field provides auto-suggestions
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Start typing in the "state" search field
3. Verify auto-suggestions dropdown appears

**Expected Result:** Auto-suggestions dropdown is displayed
[see project requirements documentation]
Autocomplete should work in the same way as for the practice area.

---

### TC-006. Check that "practice area" displays in alphabetical order with sub-specialties sorted alphabetically
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Start typing in the "practice area or legal topic" search field
3. Verify auto-suggestions dropdown appears

**Expected Result:** B y click on the search area system should show the list of practice areas in alphabetical order with related sub-specialties sorted in alphabetical order. The user should be able to choose one sub-specialty.
[see project requirements documentation]

---

### TC-007. Check that "state" displays in alphabetical order
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Start typing in the "state" search field
3. Verify auto-suggestions dropdown appears

**Expected Result:** The system should present the list with USA states to the user sorted alphabetically.
[see project requirements documentation]

---

### TC-008. Check that the user informed if Platform is not officially launched in a specified state
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. Enter "practice area or legal topic/name" search field
2. Enter specified state, for example Alaska
3. Click to the "Search" icon

**Expected Result:** According to the search results, the user should be informed if Platform is not officially launched in a specified state. The message " We have not officially launched in Alaska . Once we are in Alaska, there will be a larger selection of Alaska lawyers available to you. " is displayed
[see project requirements documentation]

---

### TC-009. Check the search by pressing the Enter key
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Enter practice area or legal topic/name in the search field
3. Enter/select state
4. Press "Enter" key

**Expected Result:** The user should be navigated to the page with ‘ advanced search ’
[see project requirements documentation]
To search for a Pro, the user should be able to:
trigger searching(button on the page + Enter)

---

### TC-010. Сheck that the placeholder is displayed when no Pros are found
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Enter a non-existing Pro name in the search field, for example Meow
3. Click to the 'Search' icon

**Expected Result:** The list of Pros is empty. The system shows placeholder with message " No lawyers were found meeting your criteria. Please modify some of the search parameters and start a new search "
[see project requirements documentation]
if no results found, the placeholder should be presented.

---

### TC-011. Check that the "practice area" search type is pre-selected by default
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Verify the search type field

**Expected Result:** By default, practice area should be selected.
[see project requirements documentation]

---

### TC-012. Check that the selected search type is saved after page reload
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Select the search type, for example "Name"
3. Reload the page

**Expected Result:** By reloading, selected search type should be saved.
[see project requirements documentation]

---

### TC-013. Check that the search is not case-sensitive
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Enter practice area or legal topic/name in the search field in UPPERCASE
3. Enter/Select state
4. Click to the 'Search' icon
5. Repeat with lowercase
6. Verify same results returned

**Expected Result:** Same results are returned

---

### TC-014. Check that the user can select a US state from the dropdown before searching
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Click to the state dropdown
3. Select a US state

**Expected Result:** State is selected

---

### TC-015. Check that only states with at least one active Pro are shown in the dropdown
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Click to the state dropdown

**Expected Result:** Only states with active Pros are displayed

---


## Search Results Filters

### TC-016. Check that the user can filter Pros by State
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Click to the state dropdown
3. Select a US state
4. Click to the "Search" icon

**Expected Result:** Results list is displaed with Pros from the selected state

---

### TC-017. Check that the user can filter Pros by Price range
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is open
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Set Price range filter

**Expected Result:** Results list updates with the selected price
[see project requirements documentation]
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

### TC-018. Check that the average price value indicator is displayed
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is open
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Verify average price indicator is displayed

**Expected Result:** Value indicator is shown on the price filter

---

### TC-019. Check that the user can filter Pros by Initial consultation availability
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is open
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Enable ' no charge initial consult ' filter

**Expected Result:** Results list updates to show only Pros with free initial consultations
[see project requirements documentation]
The user should be able to filter Pro by the ‘free’ consultation .(true/false control)
By default, the filter should not be applied.

---

### TC-020. Check that the user can filter Pros by Languages spoken
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is open
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Select any language

**Expected Result:** Results list updates according to selected language
[see project requirements documentation]
The user should be able to see the list of languages and search for languages that are presented in the system and select the desired( only one language can be selected) . By search the found fragment should be highlighted.
By default, English should be predefined.

---

### TC-021. Check that the user can filter Pros by Fee types
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is open
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Select "contingency" fee type
5. Select "flat fee" fee type

**Expected Result:** Results list updates according to selected fee type
[see project requirements documentation]
The user should be able to select price methods what Pro are provided:
contingency(true/false control)
fixed price(true/false control)
By default, the filter should not be applied.

---

### TC-022. Check that the user can filter Pros by Rating
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is open
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Select a rating value

**Expected Result:** Results list updates according to selected rating.
[see project requirements documentation]
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

### TC-023. Check that the user can toggle "Lawyers in my state only"
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Toggle ' lawyers in my state only '

**Expected Result:** Results list updates according to toggle state

---

### TC-024. Check that the availability time slider is available
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Verify the availability time slider

**Expected Result:** Availaility time slider is displayed

---

### TC-025. Check that the default slider position is set now to 30 days ('anytime')
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Verify the availability time slider
5. Verify default position is 'now' to 30 days

**Expected Result:** Slider shows range from now to 30 days by default
[see project requirements documentation]
default from now to 30 days('anytime' wording)

---

### TC-026. Check that the user can filter Pros by availability time using the slider
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Verify the availability time slider
5. Regulate time range

**Expected Result:** Results list updates according to selected time range
[see project requirements documentation]
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

### TC-027. Check that filters are applied dynamically without page refresh
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Apply multiple filters

**Expected Result:** Results list updates on each filter change
[see project requirements documentation]
Once the user updates any of the filter parameters, the Pros list should be updated.

---

### TC-028. Check that the user can reset all filters to defaults
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Apply multiple filters
5. Click to the 'Reset all' button

**Expected Result:** All filters return to default values, results list updates
[see project requirements documentation]
The user should be able to reset all filters. All filters should be in the default state.

---

### TC-029. Check that filters are reset after the page/card is reloaded
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Apply multiple filters
5. Reload the page

**Expected Result:** All filters return to default state after reload
[see project requirements documentation]
Filters should not be saved and be r eset after each card reloading

---

### TC-030. Check that the number of currently displayed Pros is shown according to applied filters
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Apply multiple filters

**Expected Result:** The count of Pros updates
The user should be able to see the number of Pros that are currently displayed according to filters.
[see project requirements documentation]

---

### TC-031. Check that the filters panel stays fixed on screen while scrolling through the Pro list
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Scroll down through the Pro list

**Expected Result:** Filters panel should be fixed and not disappear by scrolling
[see project requirements documentation]

---

### TC-032. Check that average price is not displayed if no Pros are found
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is open
2. No one Pros in the search results
3. Filter panel is displayed
4. Verify the price rage filter

**Expected Result:** The average price indicator is not displayed
\ [see project requirements documentation]
If the are no Pros, average price can be calculated for, the average price should not be displayed.

---

### TC-033. Check that average price is not calculated when searching by Pro name
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. Enter "name" search field
2. Click to the "Search" icon
3. At least one Pros listed in the results
4. Filter panel is displayed
5. Verify the price rage filter

**Expected Result:** The average price indicator is hidden
[see project requirements documentation]
By searching by name the average price should not be calculated and presented.

---


## Pro List, Card & Sorting

### TC-034. Check that the user can sort Pros by Price
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Sort dropdown is displayed
4. Open sort dropdown
5. Select "highest standard hourly rate" and check the results
6. Select "lowest standard hourly rate" and check the results

**Expected Result:** Results list is sorted correctly
[see project requirements documentation]
price (highest first) Pros in the list should be sorted by the price for practice areas.
If Pros are filtered by a practice area, the only price for the selected practice areas should be considered by sorting
If Pros are filtered by a sub-specialty, the only price for the practice area of a selected sub-specialty should be considered by sorting
price (lowest first) . Pros in the list should be sorted by the price for practice areas.
If Pros are filtered by a practice area, the only price for the selected practice areas should be considered by sorting
If Pros are filtered by a sub-specialty, the only price for the practice area of a selected sub-specialty should be considered by sorting

---

### TC-035. Check that the user can sort Pros by nearest available time slot
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Sort dropdown is displayed
4. Open sort dropdown
5. Select "earliest availability" slot

**Expected Result:** Results list is sorted from earliest to latest available slot
[see project requirements documentation]
availability time (sooner available time first) Pros in the list should be sorted by availability time. Pros that have no availability time, should be presented at the end of the list in any order.

---

### TC-036. Check that the user can sort Pros by Rating
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Sort dropdown is displayed
4. Open sort dropdown
5. Select "highest star ranking" slot

**Expected Result:** Results list is sorted by rating from highest
[see project requirements documentation]
rating(highest first) Pros in the list should be sorted by rating. Pros that have no rating, should be presented at the end of the list in any order.

---

### TC-037. Check that Pros without a connected calendar are placed at the end when sorting by availability time
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Sort dropdown is displayed
4. Open sort dropdown
5. Select "earliest availability" slot

**Expected Result:** Results list is sorted from earliest to latest available slot. Pros without calendar are at the bottom of the list
[see project requirements documentation]
Pros that have no availability time, should be presented at the end of the list in any order.

---

### TC-038. Check that the non-logged user can access the list of Pros by triggering search from the main page
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. User is non-logged
3. Enter practice area or legal topic/name in search field
4. Select state
5. Click to the "Search" icon

**Expected Result:** Search results page opens with Pro short-profile cards
[see project requirements documentation]
Non-logged user should be able to view the list of Pros by triggering search on the Platform main page

---

### TC-039. Check that each Pro card displays the Pro's photo
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results

**Expected Result:** Pro photo is displayed on the card

---

### TC-040. Check that each Pro card displays the Pro's first and last name
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results

**Expected Result:** Pro name is displayed on the card

---

### TC-041. Check that each Pro card displays rating and review count
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results

**Expected Result:** Rating and review count are displayed on the card

---

### TC-042. Check that each Pro card displays price for initial consultation
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results

**Expected Result:** Price for initial consultation is displayed on the card

---

### TC-043. Check that the nearest available time slot is displayed on Pro card (if calendar connected)
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Verify a Pro with connected calendar

**Expected Result:** Date and time in am/pm format (e.g. Jan 23 · 2:00 pm) are displayed on the Pro card

---

### TC-044. Check that the nearest free time slot is 30 min for initial meeting on the Pro card
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the result s
3. Verify a Pro with connected calendar

**Expected Result:** The nearest free time 30-minute slot is displayed on the Pro card

---

### TC-045. Check that clicking the nearest free time slot asks the user to log in
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with connected calendar
5. Click to the "Meet at [time]" button

**Expected Result:** Login form opens
[see project requirements documentation]
Once the user selects a time slot, the system should check if the user is logged in. If the user is not logged in, the system should navigate the user to the login form

---

### TC-046. Check that after signing up via nearest free time slot the user is navigated to the full Pro profile with the selected date and time
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with connected calendar
5. Click to the "Meet at [time]" button on the Pro card
6. Sign up in to the system

**Expected Result:** the full Pro profile with the selected date and time opens
[see project requirements documentation]
After the user follows the verification link(it should have a certain redirect URL if the user comes from the ‘booking time’ process) , they should be navigated to the full Pro profile with the selected date and time

---

### TC-047. Check that a logged-in user is navigated to meeting details page after selecting a time slot
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. User is logged in
3. At least one Pros listed in the result s
4. Verify a Pro with connected calendar
5. Click to the "Meet at [time]" button on the Pro card

**Expected Result:** Meeting details page opens with selected Pro

---

### TC-048. Check that after logging in (not connected) via nearest free time slot the user is navigated to meeting details page
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with not connected calendar
5. Click to the "Contact" button on the Pro card
6. Log in to the system

**Expected Result:** Meeting details page opens after log in

---

### TC-049. Check that after logging in (connected) via nearest free time slot the user is navigated to full Pro profile with confirmation popup
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with connected calendar
5. Click to the "Meet at [time]" button on the Pro card
6. Log in to the system

**Expected Result:** Full Pro profile opens with booking confirmation popup

---

### TC-050. Check that the user is navigated to meeting details page after logging in via Email
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with connected calendar
5. Click to the "Meet at [time]" button on the Pro card
6. Log in with Email

**Expected Result:** Meeting details page opens

---

### TC-051. Check that the user is navigated to meeting details page after logging in via Google/Facebook
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with connected calendar
5. Click to the "Meet at [time]" button on the Pro card
6. Log in to the system via Google/Facebook

**Expected Result:** Meeting details page opens

---

### TC-052. Check that a non-logged user is redirected to sign-up when triggering the contact button on the Pro card
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Verify a Pro with not connected calendar
5. Click to the "Contact" button on the Pro card

**Expected Result:** Sign-up form opens

---

### TC-053. Check that a non-logged user is redirected to login form after selecting a time slot
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. User is non-logged
3. At least one Pros listed in the result s
4. Open a Pro profile with connected calendar
5. Select a time slot with available date

**Expected Result:** Login form opens

---

### TC-054. Check that the user can access the full profile by clicking "see bio and more times"
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the result s
3. Click to the "see bio and more times" button on the Pro card

**Expected Result:** Full Pro profile page opens
[see project requirements documentation]
Non-logged users should be able to go to a PRO full profile by triggering “see bio and more times“ button, Pro name or Pro photo

---

### TC-055. Check that the user can access the full profile by clicking the Pro's name
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the result s
3. Click to the Pro's name on the Pro card

**Expected Result:** Full Pro profile page opens
[see project requirements documentation]
Non-logged users should be able to go to a PRO full profile by triggering “see bio and more times“ button, Pro name or Pro photo

---

### TC-056. Check that the user can access the full profile by clicking the Pro's photo
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the result s
3. Click to the Pro's photo on the Pro card

**Expected Result:** Full Pro profile page opens
[see project requirements documentation]
Non-logged users should be able to go to a PRO full profile by triggering “see bio and more times“ button, Pro name or Pro photo

---


## Full Pro Profile & Calendar

### TC-057. Check that the Pro full profile displays all information
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the result s
3. Any Pros profile is opened

**Test Data / Variations:**

| Action | Expected Result |
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

### TC-058. Check that the user can see available dates on the Pro's full profile page
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the result s
3. Open a Pro profile with connected calendar

**Expected Result:** Available dates are displayed per month
[see project requirements documentation]
The user should be able to see available dates of Pro.

---

### TC-059. Check that the first available date is pre-selected by default
**Priority:** Minor | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the result s
3. Open a Pro profile with connected calendar

**Expected Result:** First available date is selected by default in the calendar
[see project requirements documentation]
By default, the month with the first available date should be opened.

---

### TC-060. Check that days with no free slots are shown but are not selectable
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the result s
3. Open a Pro profile with connected calendar

**Expected Result:** Days without free slots are visible but not clickable

---

### TC-061. Check that the user can navigate forward through months
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the result s
3. Open a Pro profile with connected calendar
4. Switch calendar to the next month

**Expected Result:** Next month calendar is displayed.
[see project requirements documentation]
The user should be able to switch between months.

---

### TC-062. Check that the user can navigate backward through months
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the result s
3. Open a Pro profile with connected calendar
4. Switch calendar to the next month
5. Swith calendar to the previuos month

**Expected Result:** Previous month's calendar is displayed
[see project requirements documentation]
The user should be able to switch between months.

---

### TC-063. Check that selecting a date displays available time slots for that date
**Priority:** Critical | **Scenario Type:** Positive

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the result s
3. Open a Pro profile with connected calendar
4. Select any available date

**Expected Result:** Time slots are displayed for the selected date
[see project requirements documentation]
The user should be able to see available time slots for a certain date.

---

### TC-064. Check that 30-minute time slots are shown for the initial meeting
**Priority:** Major | **Scenario Type:** Positive

**Steps to Reproduce:**
1. The user is on the page with search results
2. At least one Pro s listed in the results
3. The user is not logged in
4. The user selects the desired Pro
5. The system navigates the user to the Pro profile full view and displays available dates
6. The user finds the availability time of Pro and selects the desired date
7. The system displays the available time slots for the selected date

**Expected Result:** [see project requirements documentation]
Time slots should be presented:
in am/pm format
by 30 minutes
The time intervals should be shown ONLY from the beginning of an hour and from half an hour (e.g., if user’s current time is 10:12 am, the system should show nearest available slot - 10:30 am OR if user’s time is 10:31 am, the system should show nearest available slot - 11:00 am )
Only the first 16 available time slots should be displayed by default for a selected date. Ff there are more than 16 available time slots, ‘show more’ button should be presented.

---

### TC-065. Check that the time zone is determined by the user's browser geolocation
**Priority:** Major | **Scenario Type:** Positive

**Expected Result:** Correct time zone is displayed

---

### TC-066. Check that both calendar and time slots are shown in the user's local time zone
**Priority:** Major | **Scenario Type:** Positive

**Expected Result:** All times are in user's local TZ

---


## Additional Negative Scenarios: Search

### TC-067. Check that the user can't search with empty search field
**Priority:** Critical | **Scenario Type:** Negative

**Steps to Reproduce:**
1. [relevant application page] opened
2. Click to the Search icon

**Expected Result:** Validation error " please enter a legal topic " is displayed

---

### TC-068. Check that Search by name doesn't trigger search when less than 3 symbols entered
**Priority:** Minor | **Scenario Type:** Negative

**Steps to Reproduce:**
1. [relevant application page] opened
2. Select "name" search type
3. Enter less than 3 characters
4. Click to the Search icon

**Expected Result:** Validation error " Please provide more then 3 symbols " is displayed
[see project requirements documentation]
starting from 3 symbols. If the user types less symbols or no symbols at all, then the system should ask to provide name

---

### TC-069. Check that the user can't search without selecting a state
**Priority:** Major | **Scenario Type:** Negative

**Expected Result:** Search is blocked

---

### TC-070. Check that the availability time filter is not applied to Pros without a connected calendar
**Priority:** Major | **Scenario Type:** Negative

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Verify the availability time slider
5. Regulate time range

**Expected Result:** Pros without connected calendar are not displayed

---

### TC-071. Check that the slider bullets can't overlap each other on the availability time filter
**Priority:** Minor | **Scenario Type:** Negative

**Steps to Reproduce:**
1. [relevant application page] is opened
2. At least one Pros listed in the results
3. Filter panel is displayed
4. Verify the availability time slider
5. Regulate time range

**Expected Result:** Bullets stop before overlapping

---

### TC-072. Check that slots already booked are not shown
**Priority:** Critical | **Scenario Type:** Negative

**Steps to Reproduce:**
1. [relevant application page] is opened
2. User is logged in
3. At least one Pros listed in the result s
4. Open a Pro profile with connected calendar
5. Select any tome slot from any available date
6. Schedule a meeting
7. Open the same Pro profile

**Expected Result:** Booked slot is not displayed

---

### TC-073. Check that slots in the past are not shown
**Priority:** Critical | **Scenario Type:** Negative

**Steps to Reproduce:**
1. [relevant application page] is opened
2. User is logged in
3. At least one Pros listed in the result s
4. Open a Pro profile with connected calendar

**Expected Result:** Past time slots are not displayed

---

### TC-074. Check that search by name doesn't implement autocomplete
**Priority:** Minor | **Scenario Type:** Negative

**Steps to Reproduce:**
1. [relevant application page] is opened
2. Start typing in the "name" search field
3. Verify auto-suggestions dropdown doesn't appears

**Expected Result:** Auto-suggestions dropdown is not displayed

[see project requirements documentation]
no autosuggest should be implemented

---
