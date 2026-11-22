# Scenario 5: Offboarding

- [x] Reproduced in a Microsoft 365 trial tenant

## Ticket

> "Hi, today is Brian Foster's last day. He's in Dispatch. Please disable his account at 5pm today. I'll also need access to his email afterwards. Thanks, Linda"

## First checks

1. **Is the requester allowed to ask for this?** I check the client's list of authorized contacts.
2. **When should it happen?** The ticket says 5:00 PM, so I set a reminder and do it then.
3. **What should happen to the email?** Here it is kept and given to the requester. If it is not clear, I ask before removing anything.

## Steps

1. Sign in to the Microsoft 365 admin center. Click **Users**, then **Active users**, search for the user, and click their name.
2. **Block sign-in:** click **Block sign-in**, tick **Block this user from signing in**, and click **Save changes**.
3. **Sign out of all sessions:** Go to EntraID, Users, Find Brian Foster. Click **Sign out of all sessions**, then **Yes**.
4. **Convert the mailbox:** go to the Exchange admin center (`admin.exchange.microsoft.com`), click **Recipients**, then **Mailboxes**, click the user, and click **Convert to shared mailbox**. Wait a few minutes and refresh until the type next to the user's name says **Shared**. I only remove the license after I see that. (When I converted from the Microsoft 365 admin center's Mail tab, it did not take effect, and I had to redo it here.)
5. **Give the requester access:** under **Mailbox permissions**, click **Manage mailbox permissions**, then **Read and manage permissions**, then **Add permissions**. Tick the requester and click **Add**.
6. **Remove the license:** click **Licenses and apps**, untick the license, and click **Save changes**. I do this only after step 4 shows a shared mailbox.
7. Reply on the ticket: give it about 30 minutes, then close Outlook completely and reopen it. If the mailbox is still not there after an hour, reply here and I will take another look.

## Screenshots
[See Screenshots Here](../screenshots/05-screenshots.md)

## If it's urgent

For an immediate lockout, like a termination, I also reset the user's password and don't share the new one, so the old password stops working right away.

## Result

The user can no longer sign in, the license is freed, and the requester can read the old mailbox.

## Sample ticket note

> Offboarding requested by an authorized contact per client documentation. At 5:00 PM blocked sign-in and signed the user out of all sessions. Converted the mailbox to a shared mailbox, gave the requester read and manage access, then removed the license. Requester confirmed mailbox access. Follow-up: check with the requester in two days to confirm they can still see the mailbox.

## Key takeaways

- Order matters: block, sign out, convert the mailbox, give access, then remove the license.
- If the license is removed before the mailbox is converted, the mailbox starts a 30-day countdown to deletion. Reassigning the license recovers it within that window.
- A mailbox over the shared size limit or under a legal hold may still need a license. I follow the client's offboarding checklist or escalate.
