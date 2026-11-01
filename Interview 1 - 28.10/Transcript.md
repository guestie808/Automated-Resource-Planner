Tyler:
So we are the group that will be doing the automated resource planner and we kind of just wanted to get a more full understanding on the project itself. We've read the brief itself and kind of discussed it very shortly.

Hazel:
So I've got some, I can email this to you.

So this comes from a real-world scenario. So this is a real-life problem that we have in Glenside.

For healthcare students, they require a practical session.

We've currently got an export from the timetabling system that comes out in CSV format, which is fed into an old version of Microsoft Outlook, because that old version of Outlook is the only one that can do the upload.

It creates a series of meetings, events, and then they have to assign them to rooms and equipment and technicians.

Different technicians specialise in different types of healthcare practicals, so the rooms are determined by what type of equipment they've got in them and that sort of thing.

It's all a very manual, labourious process.

If we take it back to what we want, and then reverse engineer it.

What we want is a system that can as simply as possible take the timetable information as to when the practicals have to occur, who needs to be in them, and then assign a room, equipment and a technician, and emails out the booking to the person doing the practical, their tutor, and the technician, including a little package that has the information about what it is that they need.

Kyran:
So this is like the university's timetabling system outputs the CSV?

Hazel:
Don't worry about how the CSV just assume that you start with a CSV that's got:

Who needs the practical.

What the practical's about.

What subject/course they're on.

What time that practical has to happen.

Kyran:
Does that imply that there wouldn't be scheduling conflicts because it's already being worked out in advance for the students?

Hazel:
There won't be any scheduling conflicts for the students.

There may well be for the room and the technician.

Because if the timetable just says you've got a practical session, you need it in a room that has this equipment and the student has to be there at this time.

Which room with that equipment they use, they don't necessarily have.

A nice to have, but isn't essential, would be something that:

Automates the matches and only comes back for human intervention from the technician if there is a scheduling conflict.

If either the room isn't available or the technician isn't available or the equipment isn't available.

Then they spend most of their time resolving the conflict and not on the ones that just flow through.

Connor:
So you want an automated system with the option of manual adjustments just in case?

Hazel:
Yeah.

It's really just flagging where you've got problems that people need to fix and where it just is not a problem and can carry on as normal.

Tyler:
Are there any other features you would like in a new system?

Hazel:
No, I'm giving you absolute free rein.

It needs to be simple.

It needs to be robust.

The idea is that it reduces the amount of manual staff intervention time and frees the technicians up to actually do the work.

The end result may well be that we have more practical session time.

There's more time to actually devote to the students.

But for the moment:

The essential bit is to remove that old version of Outlook because that shouldn't really still be in operation.

It must work from our current Microsoft Exchange Online system.

Connor:
A question regarding timing. For example, say there's a class booked at 11 and suddenly there's something urgent. Do you want something that allows urgent changes?

Hazel:
No. If the timetable says 11 it's got to start at 11.

Assume a 50 minute hour.

You've got 5–10 minutes either side to set the room up.

Then 50 minutes to deliver the practical.

Another 5 minutes either side to strike it down afterwards.

And a technician can supervise more than one room at a time.

All the technicians can do that.

Connor:
We were planning on using synthetic data. Is there any actual data?

Hazel:
I'll find out what the actual constraints are.

The only thing that would be nice to have is:

This is just for healthcare appointments, however, there is more than just healthcare taught at the university.

Things like engineering and so on also have practical sessions.

If we can make something that fits for this use case but could be adapted to be rolled out wider, that would be perfect.

They'll all have different rooms, different technicians and different equipment.

But the principle is the same.

If it's all built to the same process then anybody supporting it, whether it's engineering, healthcare or education, can support it.

If you have bespoke answers for each of them then it requires somebody to learn all four systems.

Tyler:
With the current system is there some sort of filter system?

Hazel:
No. It will be done entirely in their heads really.

For different types of appointment they know in their head what type of equipment is required.

This is probably not written down anywhere, but for what you need to do it will have to be.

There will be a list that says for this course you need this equipment.

Another list that says for this course you can operate in these rooms and with these technicians.

And these technicians are assigned to these rooms.

Connor:
You mentioned technicians can do more than one room at once. How many?

Hazel:
If the rooms are side by side, they could cover three rooms.

If not, ideally one.

One or two is more realistic.

Tyler:
For each course topic, is the equipment always the same?

Hazel:
Yes.

If you're doing a particular module in physiotherapy, for example, you will always need X equipment.

If you're doing occupational therapy you will need Y equipment and so on.

Tyler:
Once the events have been made in Outlook after the CSV import...

Hazel:
Currently it's imported into Outlook Classic.

Outlook Classic has to go.

At this point you have totally free rein as to which order you apply the mapping.

Tyler:
And in terms of the output are we outputting to a database or just sending emails?

Hazel:
You are actually making a calendar booking in a shared calendar in Outlook.

Then it sends out appointment invites.

The location is the room.

There is a spot for equipment which lists the equipment.

There is a technician assigned to it.

The technician and the student will be the recipient of that room booking.

Tyler:
So it's kind of automating the process and bringing it to the new Outlook.

Hazel:
Yes.

**Connor's Design Presentation**

Hazel:
Simple is always good.

What you could do is:

Auto generate.

When you've imported the timetable it could try to map as much of the timetable to a room as possible.

Then you've got a review option.

It will show and highlight where you've got clashes or things that are unable to be timetabled or booked in.

Then it's quite clear where the person doing the bookings needs to adjust things.

Maybe an option at the end to actually create the bookings.

You'll probably want to get as much booked in and mapped in as possible first.

Then at the end have the ability to do a mass booking rather than booking each one individually.

Once you've organised the rooms, technicians and so on.

At the end an ability to say "Book" and it will create all the bookings at one go would be great.

Connor:
So these CSV files are based on one student?

Hazel:
No, they're based on a class of students.

Tyler:
Is it the lecturer's timetable or the class timetable?

Hazel:
Part of the practical sessions timetable for that module. 

It's got all the student names.

It's got all the lecturer names.

It's got all the course information.

You'll need a table that maps the equipment to the course or the module.

Whichever module it is, you'll know what equipment is required.

Kyran's Design Presentation

Hazel:
Assume there will be a separate spreadsheet and/or database.

The technician details will be in there.

Name.

UWE email address.

Which modules they support.

Which equipment they support.

For the rooms, there'll be a separate table that lists the room and the equipment available in that room.

That will be one of your limiting factors in which practical sessions you can book in each room.

It then limits which technicians you can assign.

Tyler's Design Presentation

Hazel:
That's an interesting approach because you're modelling this outside Exchange in a database.

That's absolutely fine.

At the moment you lock it in the database.

You need one more step to generate the room bookings in Exchange.

Once you've got everything locked in there you need one more step to take the data and generate the room booking.

Tyler:
I think I assumed it would just be converted back to CSV.

Hazel:
We are removing the CSV route.

You've got to start with the timetable and finish with the calendar invitation, the attachments, the room bookings and the technician allocation.

Tyler:
And you'll email us the process information?

Hazel:
I will email this to you.

The initial bit only relates to healthcare, but we want a system that could be scaled out to support other courses that have practicals.

Connor:
If we get it polished and working, would it actually be used?

Hazel:
Yes, we're taking the old system out.

Connor:
Really?

Hazel:
If this works, we could well put it into practice.
