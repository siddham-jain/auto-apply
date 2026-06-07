# Auto Apply

## Workflow

Applies to jobs automatically from Google Sheets with status tracking. Reads job listings from your sheet, filters by priority and status, and applies to jobs on LinkedIn, Indeed, and other platforms. Updates application status in real-time and checks every 2 days for status changes. Sends email notifications for successful applications, status updates, and interview invites. Prevents duplicate applications and manages rate limiting to keep your accounts safe.

## Who's it for

Job seekers who want to streamline their application process, save time on repetitive tasks, and never miss following up on applications. Perfect for anyone managing multiple job applications across different platforms.

## How it works

The workflow runs on two schedules:

**Daily Application Process (9 AM, weekdays):**
- Reads your job list from Google Sheets
- Filters for jobs marked as "Not Applied" with Medium/High priority
- Processes each job individually to prevent rate limiting
- Applies to jobs using platform-specific APIs (LinkedIn, Indeed, etc.)
- Updates the sheet with application status and reference ID
- Sends confirmation email for each application

**Status Monitoring (Every 2 days at 10 AM):**
- Checks all jobs with "Applied" status
- Queries job platforms for application status updates
- Updates the sheet if status has changed
- Sends notification emails for status changes (interviews, rejections, etc.)
