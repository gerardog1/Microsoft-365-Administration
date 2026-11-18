# Scenario 8: MFA reset after a new phone

- [ ] Reproduced in a Microsoft 365 trial tenant

## Ticket

> "Hi, I got a new phone and now I can't sign in to my email or Teams. It keeps asking me to approve on the Authenticator app but that's on my old phone and I don't know how to move it over. Can you help?"

## First checks

1. **Verify the user's identity.** I call the number already on file. Attackers like MFA resets, so this step is not optional.
2. **Was the phone upgraded, or lost or stolen?** If it was lost or stolen, I also reset the password and revoke sessions, and tell the security team.
3. **Is the user at their computer?** I need them there to set up the new phone.

## Steps

1. Sign in to the Entra admin center (`entra.microsoft.com`).
2. Click **Entra ID**, then **Users**, then **All users**. Search for the user and open their page.
3. Click **Authentication methods** in the left menu.
4. Click **Require re-register multifactor authentication**, then **OK**. The old Authenticator entry disappears.
5. Walk the user through it by phone: sign in at `office.com`, click **Next** at "More information required", and get to the QR code.
6. On the new phone, open the Authenticator app, tap **+**, tap **Work or school account**, and scan the QR code.
7. The user types the number shown on the laptop into the phone notification and approves it.
8. Ask the user to open Teams to confirm everything works.

## Root cause

The Authenticator app was registered on the old phone, so the user could not approve sign-ins on the new one.

## Ticket note

> User upgraded phone and could not approve MFA prompts. Verified identity by calling the number on file. Cleared registered MFA methods in the Entra admin center (Require re-register). User registered Authenticator on the new phone and confirmed sign-in to Microsoft 365 and Teams. Follow-up: check with the user in two days to confirm MFA prompts are working.

## Key takeaways

- Identity first. An MFA reset is a favorite social-engineering target.
- Re-registering removes the old method, so the old phone no longer works for sign-in.
- A lost or stolen phone needs extra steps.
