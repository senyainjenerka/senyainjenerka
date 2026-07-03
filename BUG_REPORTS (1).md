# Bug Reports: Client Web Application

> Баг-репорты оформлены в Jira в ходе производственной практики (мануальное функциональное и адаптивное тестирование клиентского веб-приложения). Из соображений NDA конкретное название продукта, компания и внутренние ссылки заменены на нейтральные формулировки. **Скриншоты и видео-вложения к багам не публикуются по этой же причине** — они содержат реальный интерфейс и адрес продукта.

**Author:** Ksenia Sereda | **Total bugs:** 8 | **Type:** Functional / UI-Responsive

## Table of Contents

1. [Search & Browse](#search--browse) — 5 bugs
2. [Profile](#profile) — 3 bugs

## Search & Browse

### BUG-001. Search query parameters are missing in URL
**Environment:** Stage, Chrome 149
**Preconditions:** user is logged off
**Steps to Reproduce:**
1. [relevant application page]
2. Enter valid search criteria and click the Search icon
3. Copy the URL of the opened page
4. Paste the URL into a new browser tab
5. Compare search results on the old and new pages

**Actual Result:** the new page shows the "No lawyers found" placeholder

**Expected Result:** results should be consistent when the URL is copied and reopened

**Requirements:** [see project requirements documentation] (BA & PO discussion in comments)

---

### BUG-002. Search can't be triggered by pressing the Enter key
**Environment:** Stage, Google Chrome 148.0.7778.218
**Preconditions:** [relevant application page] is opened
**Steps to Reproduce:**
1. Enter practice area/name and state
2. Press the Enter key

**Actual Result:** pressing Enter does not trigger the search; the search results page is not displayed

**Expected Result:** pressing Enter should trigger the search; the search results page should open

**Requirements:** [see project requirements documentation]

---

### BUG-003. "Back" button redirects to sign-up form instead of search results list
**Environment:** Stage, Google Chrome 148.0.7778.218
**Preconditions:** [relevant application page] is opened, user is non-logged
**Steps to Reproduce:**
1. Enter practice area/name and state
2. Click the "Search" button
3. Select a Pro and open their full profile
4. Click the browser "back" button

**Actual Result:** clicking "back" navigates the user to the sign-up form instead of the search results list

**Expected Result:** clicking "back" should return the user to the search results list with the previously applied search and filter criteria preserved

---

### BUG-004. The calendar week starts on Sunday instead of Monday
**Environment:** Stage, Google Chrome 148.0.7778.218
**Preconditions:** [relevant application page] is opened
**Steps to Reproduce:**
1. Enter practice area/name and state
2. Click the "Search" button
3. Select any Pro with a connected calendar from the list

**Actual Result:** the calendar week starts on Sunday

**Expected Result:** the calendar week should start on Monday

**Requirements:** [see project requirements documentation]

---

### BUG-005. Filters panel disappears when scrolling through the Pro list instead of staying fixed
**Environment:** Stage, Google Chrome 148.0.7778.218
**Preconditions:**
1. [relevant application page] is opened
2. At least one Pro is listed in the results
3. Filter panel is displayed

**Steps to Reproduce:**
1. Scroll down through the Pro list

**Actual Result:** the filters panel is only visible at the top of the page; scrolling down makes it disappear, leaving only the Pro list visible

**Expected Result:** the filters panel should stay fixed on screen while scrolling through the list, so the user can adjust filters at any point without scrolling back to the top

**Requirements:** [see project requirements documentation]

---

## Profile

### BUG-006. Text in "Add credit card" and "Add bank account" buttons overflows the button border at viewport less than 938 px
**Environment:** Stage, Google Chrome 148.0.7778.218, DevTools
**Preconditions:** [relevant application page] is opened, user is logged in
**Steps to Reproduce:**
1. Click the Profile icon
2. Select "payments"
3. In DevTools responsive mode, set viewport width to 938 px or less

**Actual Result:** the text inside the "Add credit card" and "Add bank account" buttons overflows the button borders

**Expected Result:** button text should stay inside the button at all screen sizes without overflowing

---

### BUG-007. Sidebar menu stays open and covers half the screen on mobile
**Environment:** Stage, Google Chrome 148.0.7778.218, DevTools
**Preconditions:** [relevant application page] is opened, user is logged in
**Steps to Reproduce:**
1. Click the Profile icon
2. Select the "profile" section
3. In DevTools, set the viewport to a mobile width, e.g. 491 px

**Actual Result:** the sidebar menu stays open and doesn't collapse; the user has to scroll horizontally to see and interact with the page content

**Expected Result:** on mobile viewports the sidebar menu should collapse into a hamburger menu, or be hidden by default, so the main content takes up the full screen width and is fully readable without horizontal scrolling

---

### BUG-008. Card details overflow the card container block at viewport less than 689 px
**Environment:** Stage, Google Chrome 148.0.7778.218, DevTools
**Preconditions:** [relevant application page] is opened, user is logged in
**Steps to Reproduce:**
1. Click the Profile icon
2. Select "payments"
3. In DevTools, set viewport width to 689 px or less, e.g. 550 px

**Actual Result:** the card details don't fit inside the card container; text and the card icon overflow the block, making the information cut off and hard to read

**Expected Result:** card details should fit fully inside the container block at all screen sizes

---
