# raceday-system
description 
RaceDay is a race event management system that allows organizers to create events and participants to enrol in races. The system manages events, categories, enrolments, payments, and results.

section a
business rules 
RACEDAY BUSINESS RULES

1. USERS
   - Unique email required
   - Role: Participant or Organizer
   - Passwords must be hashed

2. ORGANISER
   - Can create multiple events
   - Owns events they create

3. EVENT
   - Must have date and location
   - Status: Upcoming/Ongoing/Completed/Cancelled
   - Belongs to one organiser

4. CATEGORY
   - Belongs to one event
   - Must have distance (>0) and entry fee (>=0)

5. ENROLMENT
   - One per participant per category
   - Status: Pending/Confirmed/Completed/Cancelled

6. PAYMENT
   - Linked to one enrolment
   - Amount > 0
   - Status: Pending/Completed/Failed/Refunded

7. RESULT
   - One result per enrolment
   - Must have finish time

8. ROLE ACCESS
   - Public: View only events, categories, results
   - Participant: Enrol, pay, view own enrolments
   - Organizer: Create events, manage categories, capture results
