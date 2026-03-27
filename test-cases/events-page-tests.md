# GreenCity Events - Test Cases

---

## Test Case 1: Filter Events by Type

**Title:** Verify filtering of events by type (ECONOMIC, SOCIAL, ENVIRONMENTAL)

**Preconditions:**
- User is on the GreenCity Events page (https://www.greencity.cx.ua/#/greenCity/events)
- Events list is fully loaded with multiple events of different types
- User is not logged in (can view events)

| Step | Action | Data | Expected Result |
|------|--------|------|-----------------|
| 1 | Locate the filter panel | Filter options: Type, Location, Status, Event time, Date range | Filter panel is visible at the top of the events list |
| 2 | Click on "Type" filter | Filter section | Type filter dropdown expands showing available types |
| 3 | Select "ECONOMIC" from the Type filter | Type = ECONOMIC | Only events with ECONOMIC type are displayed |
| 4 | Verify the filtered results | Observe event cards | All displayed events show ECONOMIC tag |
| 5 | Click "Reset all" button | Reset all filters | All events are displayed again, filter is cleared |

---

## Test Case 2: Join an Event

**Title:** Verify user can join an available event by clicking "Join event" button

**Preconditions:**
- User is on the GreenCity Events page
- Events list is fully loaded
- At least one event with "Open" status is visible
- User is not logged in OR is logged in (should handle both cases)

| Step | Action | Data | Expected Result |
|------|--------|------|-----------------|
| 1 | Locate an event card with "Open" status | Observe event status | Event card is visible with "Open" status indicator |
| 2 | Click "Join event" button on the selected event | Event: "Some Event" (May 31, 2026) | Button is clickable and responsive |
| 3 | Verify the action result | Check if user is logged in | If logged out: User is redirected to login page; If logged in: User joins the event, button state changes |
| 4 | Verify participant count update | Participant count icon | Participant count increases by 1 (if user successfully joined) |

---

## Test Case 3: Search and View Event Details

**Title:** Verify user can click "More" button to view event details

**Preconditions:**
- User is on the GreenCity Events page
- Events list is fully loaded with multiple events
- At least one event with complete information is visible (title, date, location, author, ratings)

| Step | Action | Data | Expected Result |
|------|--------|------|-----------------|
| 1 | Locate an event card in the list | Select first event card | Event card is clearly visible with all details (title, date, location, rating) |
| 2 | Click the "More" button on the event card | Event: "Some Event" | "More" button is clickable |
| 3 | Verify navigation to event details page | Check URL and page content | User is navigated to the event details page with full event information |
| 4 | Verify event details are displayed | Event details page content | Page displays: event title, description, date/time, location, author name, ratings, participant count, likes/dislikes, and action buttons |
| 5 | Click back button or GreenCity logo | Navigation | User returns to the events list page |

---
