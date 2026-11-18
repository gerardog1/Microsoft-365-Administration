# Scenario 4: Outlook closes at startup (add-in)

- [ ] Practiced the steps in a Microsoft 365 trial tenant (the crash itself was not reproduced)

## Ticket

> "Hi, Outlook won't open this morning. It just sits on a loading screen for a while and then closes. I have a meeting at 11 and need my calendar."

## First checks

1. **What exactly happens?** Does it show an error, or does it just close?
2. **Did anything change recently?** An update or new software.
3. **Is anything else broken?** Teams and the internet both work, so this is Outlook, not the network.

## Steps

1. Connect to the PC with the user's permission.
2. Press **Windows key + R**, type `outlook.exe /safe`, and press Enter. Choose the Outlook profile and click **OK**.
3. Outlook opens and the title bar says **(Safe Mode)**. Safe mode starts Outlook with its add-ins off, so an add-in is the likely cause.
4. Click **File**, then **Options**, then **Add-ins**. Next to **Manage**, choose **COM Add-ins** and click **Go...**.
5. Untick the non-Microsoft add-in and click **OK**. Close Outlook.
6. Open Outlook normally from the Start menu and confirm it loads.
7. Tell the user which add-in is turned off, so a missing button is not a surprise.

## Root cause

A third-party add-in was crashing Outlook at startup.

## If the user needs the add-in

I explain that it cannot go back on yet, because it would crash Outlook again, and give a workaround. Then I open a new ticket to update or reinstall the add-in, and escalate with my notes if that does not help.

## Sample ticket note

> User reported Outlook closing at startup while loading. Teams and internet worked. Started Outlook in safe mode (outlook.exe /safe) and it opened normally. Disabled the third-party add-in under File > Options > Add-ins > COM Add-ins. Outlook now opens normally and the user confirmed mail and calendar. User informed the add-in is turned off. Follow-up: check with the user in two days that Outlook is still stable.

## Key takeaways

- Safe mode splits the problem in two: Outlook itself, or something added to it.
- Turning off an add-in has a cost, so tell the user.
- This applies to classic Outlook, not the newer "new Outlook".

## Reproduce it (practice only)

1. Install the desktop apps from the trial tenant and sign in as a test user with classic Outlook.
2. Run `outlook.exe /safe` and confirm the title bar says Safe Mode.
3. Open **COM Add-ins**, untick one add-in, click **OK**, then reopen the box and tick it again.
4. I did not reproduce the crash itself, so this scenario stays a practiced walkthrough.
