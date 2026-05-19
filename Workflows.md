Create a workflow that runs every day at 6:00 PM in my local time zone.

When it runs, review my Microsoft 365 activity for the current day across:
- Outlook email
- Outlook calendar / Teams meetings
- Teams chats

Identify all pending tasks, follow-ups, and action items that are still open as of today.

Use these rules:
1. From Outlook email:
   - Scan emails received and sent today.
   - Find messages that contain requests, commitments, deadlines, promised follow-ups, unanswered questions, or action items assigned to me.
   - Flag emails that still need a reply from me or where I committed to do something today and it is not yet completed.

2. From meetings:
   - Review today’s calendar events and Teams meetings.
   - Extract action items, owners, due dates, and follow-ups mentioned in meeting subject, body, notes, recap, or transcript if available.
   - Include only tasks assigned to me or clearly requiring my action.

3. From Teams chats:
   - Review my 1:1 chats, group chats, and meeting chats with activity today.
   - Identify messages that contain asks, decisions requiring my follow-up, pending deliverables, reminders, or unresolved questions directed to me.
   - Exclude casual conversation unless it contains a clear work task or follow-up.

Output:
- Create a concise end-of-day summary with these sections:
  1. Urgent pending today
  2. Needs response
  3. Follow-up required
  4. Waiting on others
  5. Completed / no action needed

For each pending item include:
- Source (Email / Meeting / Teams Chat)
- Title or topic
- Who requested it / owner
- Short summary
- Due date or expected timeline if mentioned
- Recommended next step
- Priority: High / Medium / Low

Also include:
- A total count of pending items
- A separate section called “Top 3 things to close tomorrow morning”
- Links to the original email, meeting, or chat whenever available

Send the final summary to me in Teams chat and also email it to me.
