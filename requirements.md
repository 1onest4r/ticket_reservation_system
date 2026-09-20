# Global Event Ticket Reservation System

## 1. Product Vision
- **FOR** space enthusiasts, science professionals, and adventurers
- **WHO** need a secure and reliable way to discover and book access to rocket launches, special hackathons and commercial space flights
- **THE** Galactic Gateway Ticket Reservation System
- **IS A** cloud-based specialized event ticketing platform
- **THAT** allows users to discover aerospace events, verify prerequisites (like medical clearances), and reserve launch viewing seats or spacecraft cabins quickly and securely
- **UNLIKE** fragmented space-agency websites and exclusive VIP travel agencies
- **OUR PRODUCT** provides one unified, reliable and accessible reservation experience for the growing commercial space industry


## 2. Users and Stakeholders
- **Space Tourist / Attendee:**
	- The primary user for booking viewing tickets or orbital flights.
- **Launch Provider (e.g. , SpaceX, Blue origin):**
	- Event organizers listing launches and managing capacities.
- **Science Event Organizer:**
	- Groups hosting special hackathons, astronomy conventions, or zero-G flights.
- **Venue / Spaceport Manager:**
	- Personnel managing ground operations, VIP viewing galleries, and security zones.
- **Administrator:**
	- Platform operators managing system health and user disputes.
- **Payment Provider:**
	- External partners handling large amount of fiat or cryptocurrency transactions.

## 3. Personas

### Persona 1: The Astro-Enthusiast (Alex)
- **Age:** 24
- **Role:** Software engineering student / Hackathon competitor
- **Technology:** Mobile-first, highly tech-savvy
- **Context**: Regularly attends science events, coding competitions, and travels to spaceports to watch heavy-lift rocket launches
- **Needs:** Fast event discovery, real-time alerts on launch delays, cheap and reliable booking for hackathon seats or launch viewing stands.
### Persona 2: A Wealthy space tourist (Eleanor)
- **Age:** 55
- **Role:** Entrepreneur
- **Technology:** Prefers desktop or tablet, values clean premium UI
- **Context**: Looking to fulfill a lifelong dream by booking suborbital flight or a lunar flyby module
- **Needs:** High security, privacy, white-glove customer service, and a clear interface for uploading necessary medical/training clearance documents.
### Persona 3: The Event organizer (Dr. Aris)
- **Age:** 42
- **Role:** Mission outreach director at a commercial space agency
- **Technology:** Uses complex dashboard tools on multi monitor desktop setups
- **Context**: Needs to allocate 5'000 viewing tickets for an upcoming Mars rover launch, plus manage VIP seating.
- **Needs:** Ability to create events, update launch windows dynamically, manage seat maps, and track total ticket sales.

## 4. Scenarios

### Scenario 1: Booking a rocket launch viewing
Alex sees an announcement on social media that a new heavy-lift rocket is launching to Mars next month. He opens the ticketing app on his phone, searches for "Mars Launch", and views the interactive seat map for the spaceport viewing gallery. He selects a front row seat (Seat A12), completes the payment, and receives a QR ticket immediately.
### Scenario 2: Reserving a suborbital flight cabin
Eleanor decides she is ready for a suborbital spaceflight. She longs into the platform, selects an upcoming commercial flight, and chooses a premium window seat cabin. Because this is a spaceflight, the system prompts her to upload her medical clearance forms. She reserves the cabin, and the system places a 48-hour hold on her reservation pending medical verification.

### Scenario 3: Creating a special hackathon event
Dr. Aris is organizing a "Lunar base cybersecurity hackathon". He logs into the platform as a organizer. He creates the event, sets the date, defines a custom floor plan for 300 hacker stations, and sets the ticket price to free but requires a university email to register. He publishes the event live to the public.

### Scenario 4: Handling a launch scrub (Delay)
A major solar storm causes a rocket launch to be scrubbed and delayed by 48 hours. Dr. Aris updates the launch window in the platform. The system automatically pushes a notification to Alex and all other holders. Alex checks the new date, realizes he has a university exam, and uses the app to easily cancel ticket and request a refund.


### Scenario 5: Managing VIP areas
A venue manager at the spaceport notices that the VIP section for a lunar launch is overbooked due to a layout change. They use the platform's administrative tools to view Eleanor's reservation, upgrade her to private suite at no extra cost, and message her directly through the system to ensure her luxury experience isn't interrupted.
## 5. User Stories

- **US-01:** As an attendee, I want to search for events by celestial destination (e.g. , Moon. Mars, Leo) so that I can easily find specific spaceflight missions. 
- **US-02:** As a tourist, I want to view an interactive map of the spacecraft or viewing gallery so that I can choose my exact seat.
- **US-03:** As an attendee, I want to securely reserve an available seat so that I can guarantee my spot at the event.
- **US-04:** As a tourist, I want to upload my medical clearance documents so that I can meet the legal requirements for orbital flights.
- **US-05:** As an attendee, I want to receive real time push notifications so that I am instantly aware if a launch is scrubbed or delayed. 
- **US-06:** As an attendee, I want to cancel my reservation easily so that I can get a refund if the new launch date conflicts with my schedule.
- **US-07:** As an organizer, I want to create and publish a new event so that users can begin booking tickets.
- **US-08:** As an organizer, I want to dynamically update the date and time of an event so that I can adjust for weather related launch delays.
- **US-09:** As an organizer, I want to view real time reservation statistics so that I know how close we are to maximum capacity.
- **US-10:** As a payment provider, I want the system to process high value transactions with two factor authentication so that expensive spaceflight tickets are securely funded.

## 6. Features

- **F-01:** Interplanetary event search & filtering
- **F-02:** Interactive Spacecraft/Venue seat mapping
- **F-03:** Real time seat reservation & transaction processing
- **F-04:** Medical & training document upload portal
- **F-05:** Launch status & automated delay notifications
- **F-06:** Organizer dashboard (Event creation & capacity management)

## 7. Acceptance Criteria

- **AC-01:** *Given* an available seat, *When* a user makes a valid reservation request, *Then* the reservation succeeds and the seat status changes to unavailable.
- **AC-02:** *Given* a seat is already booked, *When* another user attempts to reserve it, *Then* the system rejects the request and prompts them to choose another seat.
- **AC-03:** *Given* an orbital flight requiring clearance, *When* a user books without uploading documents, *Then* the booking is marked as "Pending" until documents are verified.
- **AC-04:** *Given* a launch delay is entered by the organizer, *When* the update is saved, *Then* all registered attendees receive an automated email and push notification within 60 seconds.
- **AC-05:** *Given* a user requests cancellation of an active booking, *When* the request is processed, *Then* the seat becomes immediately available in the system for others to book.

## 8. Functional Requirements

- **FR-01:** The system shall allow users to search for events using keyboards, dates, and mission types (e.g., Orbital, Suborbital, Ground viewing, Event).
- **FR-02:** The system shall display visual, interactive floor plans or spacecraft schematics indicating available, pending, and reserved seats.
- **FR-03:** The system shall allow users to reserve a seat and hold it for exactly 10 minutes while payment is completed (can't cancel)
- **FR-04:** The system shall allow organizers to cerate, edit, and cancel events.
- **FR-05:** The system shall provide a secure portal for users to upload PDF or JPEG files for flight clearance requirements.

## 9. Non-functional Requirements

- **NFR-01 (Performance):** 95% of event search queries shall return results within 500 milliseconds.
- **NFR-02 (Reliability/Integrity):** The system shall enforce strict database isolation to ensure a specific seat can never have more than one active reservation, even if thousands of users request it at the exact same millisecond.
- **NFR-03 (Security):** All uploaded medical and personal identification documents must be encrypted at rest using AES-256 encryption.
- **NFR-04 (Availability):** The production service shall maintain 99.99% uptime, specifically crucial during heavily trafficked "ticket drop" days for rare Mars launches.
- **NFR-05 (Observability):** All payment failures and double booking attempts shall be automatically logged and flagged for the system administrator.

## 10. AI Use Statement

## AI Tool Used

Gemini pro 3.1


## I Used AI For

Brainstorming space-related themes, writing user scenarios, and formatting the markdown structure.


## What AI Produced
AI generated the initial ideas for the "Wealthy Space Tourist" and "Hackathon Organizer" personas, as well as drafted the initial Given-When-Then phrasing for the acceptance criteria based on standard Agile frameworks.

## What I Changed
I adjusted the AI's generic product vision to specifically align with the Geoffrey Moore template taught in Week 1 (FOR / WHO / THE / IS A...). I also modified the Non-functional Requirements to ensure they were strictly measurable (e.g., adding "within 500 milliseconds" and "AES-256 encryption") rather than accepting the AI's initial vague suggestion of "the system should be fast and secure."

## What I Rejected
The AI suggested adding a "Social Media Feed" and "In-app games to play during launch delays" feature. I rejected these based on the Feature Creep principle discussed in the lecture, as they do not directly support the core Product Vision of quick and reliable seat reservation.