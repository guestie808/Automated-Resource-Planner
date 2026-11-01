Project based on real problem at UWE Glenside Campus involving scheduling of healthcare practical sessions.

Current System:
- University timetabling system exports practical-session data as CSV file.
- CSV is imported into older version of Outlook.
- Staff manually assign:
  - Rooms
  - Equipment
  - Technicians
- Calendar bookings are created, sent to relevant people.
- Process is highly manual, time-consuming, relies heavily on staff knowledge.

System should aim to remove dependency on Outlook Classic.

The CSV will contain following info:
- Practical session date, time
- Course/module information
- Student information
- Tutor/lecturer information
- Practical session requirements (suitable rooms, equipment, technicians)

No student timetable clashes.

Potential clashes may exist for:
- Rooms
- Equipment
- Technicians

Technicians can supervise:
- Up to 3 adjacent rooms.
- 1-2 (ideally 1) non-adjacent rooms.

Modules will always require same equipment.

Timetable should allow for room-preparation time (assume 50 minute hour)

System should:
- Automatically process straightforward bookings.
- Only require human intervention for conflicts.

Users should be able to:
- Review allocations.
- Modify room assignments.
- Modify technician assignments.
- Resolve flagged conflicts manually.

Final output must be:
- Calendar bookings in Microsoft Exchange/Outlook.
- Automatic invitation emails sent to:
  - Students
  - Tutors
  - Assigned technicians

Bookings should include:
- Location (room)
- Equipment details
- Technician assignment
- Supporting documentation where required

Aim for scalability, e.g. suitability for other courses with practicals.
