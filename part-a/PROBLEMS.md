# IRCTC Problem Discovery — Part A

## Summary

* Total Problems: 6 (3 Given + 3 Self-Discovered)
* Platform: IRCTC Web
* Devices: Desktop Chrome, Mobile Chrome

---

## Problem 1: Tatkal Booking Crashes at 10:00 AM [Given]

### What is broken

Tatkal booking becomes extremely slow or fails during peak demand at opening time.

### Affected Users

Passengers booking emergency or last-minute travel tickets.

### Frequency

Daily during Tatkal booking hours.

### Current Flow

1. User logs into IRCTC.
2. Searches train.
3. Selects Tatkal quota.
4. Enters passenger details.
5. Waits for booking window.
6. Clicks Book at 10:00 AM.
7. Page freezes or times out.
8. Ticket becomes unavailable.

### Where it breaks

During booking submission when traffic spikes.

---

## Problem 2: Search Filters Do Not Work Reliably [Given]

### What is broken

Applied filters sometimes reset or do not update results consistently.

### Affected Users

Users comparing multiple train options.

### Frequency

Common during train search.

### Current Flow

1. Search trains.
2. View results.
3. Apply Sleeper filter.
4. Apply availability filter.
5. Open train details.
6. Return to results.
7. Filters disappear or reset.

### Where it breaks

Filter state is not maintained after navigation.

---

## Problem 3: Seat Selection Resets [Given]

### What is broken

Selected berth preference is not always reflected later in booking.

### Affected Users

Senior citizens, families, and users with berth preferences.

### Frequency

Observed during seat selection flow.

### Current Flow

1. Select train.
2. Enter passenger details.
3. Choose Lower Berth.
4. Continue booking.
5. Reach review page.
6. Preference is missing or changed.

### Where it breaks

Between berth selection and booking review.

---

## Problem 4: Session Timeout Without Warning [Self-Discovered]

### How I Found It

While entering passenger information during booking.

### What is broken

The session expires without notifying the user.

### Affected Users

First-time users and users booking for multiple passengers.

### Frequency

Occurs during longer booking sessions.

### Current Flow

1. Search train.
2. Select train.
3. Fill passenger details.
4. Spend time reviewing information.
5. Session expires.
6. User loses progress.

### Where it breaks

At session timeout due to missing warning system.

---

## Problem 5: PNR/TDR Information Is Difficult To Understand [Self-Discovered]

### How I Found It

While exploring PNR Status and TDR sections.

### What is broken

Railway terminology is difficult for new users to understand.

### Affected Users

First-time and infrequent travelers.

### Frequency

Every visit to PNR or TDR pages.

### Current Flow

1. Open PNR page.
2. Enter details.
3. View status.
4. Encounter abbreviations and technical terms.
5. Search elsewhere for explanations.

### Where it breaks

Information is presented without sufficient guidance.

---

## Problem 6: Mobile Booking Flow Requires Excessive Scrolling [Self-Discovered]

### How I Found It

Using IRCTC on mobile browser.

### What is broken

Booking forms are lengthy and difficult to navigate on mobile.

### Affected Users

Mobile users and elderly passengers.

### Frequency

Throughout the booking process.

### Current Flow

1. Search train.
2. Select train.
3. Open passenger form.
4. Scroll through multiple sections.
5. Review details.
6. Scroll repeatedly to fix errors.

### Where it breaks

During passenger information entry and review.

---

## Conclusion

The six documented issues impact booking success, usability, user confidence, and mobile accessibility. These findings will be used in Part B to design targeted feature improvements and workflow enhancements.
