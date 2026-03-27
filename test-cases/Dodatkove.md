# GreenCity Events - Negative Test Cases 

---

## Test Case 1: Attempt to Join Event Without Authentication

**Title:** Verify that unauthenticated user is prompted to login when attempting to join an event

**Preconditions:**
- User is on the GreenCity Events page
- User is NOT logged in (not authenticated)
- Events list is fully loaded with at least one "Open" event
- Browser cookies and session storage are cleared

| Step | Action | Data | Expected Result |
|------|--------|------|-----------------|
| 1 | Locate an event with "Open" status | Select event: "Some Event" | Event card is visible |
| 2 | Click "Join event" button without being logged in | Click button | User is redirected to login page OR authentication popup appears |
| 3 | Verify login requirement message | Check page/modal content | Message indicates user must login first |
| 4 | Verify user is NOT added to event participants | Check original event page | User is not listed as a participant, original participant count remains unchanged |

---

## Test Case 2: Search Events with Empty or Invalid Search Query

**Title:** Verify system behavior when filtering with empty or invalid search parameters

**Preconditions:**
- User is on the GreenCity Events page
- Events list is fully loaded
- Search/filter functionality is accessible

| Step | Action | Data | Expected Result |
|------|--------|------|-----------------|
| 1 | Open the filter panel | Click on filter section | Filter options are visible (Event time, Location, Status, Type) |
| 2 | Enter empty value in search field | Input: (blank/empty string) | System displays either: "No results found" message OR shows all events by default |
| 3 | Enter special characters in filter field | Input: !@#$%^&*() | No events are filtered; system shows "No results found" OR displays appropriate error message |
| 4 | Attempt to filter by non-existent location | Input: "XYZ City 12345" | No events are displayed; "No results found" message appears |
| 5 | Clear invalid filters | Click "Reset all" button | All events are displayed again; filters are cleared |

---

## Test Case 3: Rate Event Without Login Credentials

**Title:** Verify that unauthenticated user cannot rate events and is prompted to login

**Preconditions:**
- User is on the GreenCity Events page
- User is NOT logged in
- At least one event card with star rating system is visible
- Event has empty or partially filled star ratings

| Step | Action | Data | Expected Result |
|------|--------|------|-----------------|
| 1 | Locate an event card with star rating display | Observe star icons on event card | Star rating section is visible (5 empty stars or mixed stars) |
| 2 | Attempt to click on a star to rate | Click on 4th star to give 4-star rating | System displays login prompt or disables rating for non-authenticated users |
| 3 | Verify no rating was recorded | Check event card | Star rating remains unchanged; no new rating is saved |
| 4 | Observe error message or tooltip | Hover or check for message | Message indicates: "Please login to rate this event" or similar authentication requirement |
| 5 | Verify like/dislike buttons are also locked | Attempt to click Like button | Like/Dislike buttons are disabled or redirect to login page |

---
