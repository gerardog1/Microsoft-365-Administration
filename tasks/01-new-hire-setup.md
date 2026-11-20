# Scenario 1: New hire setup

- [ ] Reproduced in a Microsoft 365 trial tenant

## Ticket

> "Hi, we have a new hire starting Monday, Sofia Ramirez, in Sales. Can you set up her account and email, and give her the same access as the rest of the sales team? Thanks."

## First checks

1. I'd first check if the requester is allowed to ask for this. I'd check the client documentation for the list of people who can request new accounts.
2. Also on the client documentation; I would look for what the standard setup is for someone in Sales (Licenses, Group)
3. I'd check if we have licenses to give out.

## Steps

1. Sign into Microsoft 365 Admin Center.
2. Click Users, then Active Users, then Add a User.
3. On the Basics section, I enter the first name, last name, display name, and username. I'd also leave Automatically create a password and Require this user to change their password when they first sign in ticked.
4. On Product licenses, choose the standard license. Skip Optional settings and click Finish adding.
5. Copy the temp password from the confirmation page.
6. Go to Teams & groups, then Active teams & groups, then the team's group (Sales). Click Membership, then View all and manage members, then Add members. Search for the newly created user, tick them and add them.
7. Call the requester and read the temporary password over the phone.
8. Tell the requester that on the first sign-in the new hire will be asked to change the password and set up their Authenticator app, and that the mailbox may take a few minutes to be ready after the license is assigned.

## Screenshots
[See Screenshots Here](../screenshots/01-screenshots.md)

## Ticket note

> New hire account requested by an authorized contact per client documentation. Created the user in the Microsoft 365 admin center, assigned the standard license, and added the user to the team group. Temporary password given to the requester by phone. User must change the password at first sign-in. 

## Key takeaways

- Verify the requester, and check the license count before creating anything.
- Passwords are shared by phone only.
- Adding the user to the team's group is how "same access as the team" gets done.
