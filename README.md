Privacy Policy for Kepta
Last updated: 12 September 2026

Kepta is an offline Android habit tracker. This policy describes what it does with your information. It is short because there is very little to describe.

The short version
Kepta collects nothing. There is no account, no analytics, no crash reporting, no advertising, and no server. Your habits and your history stay on your phone.

What Kepta stores, and where
All of it lives in Kepta's own private storage on your device, which other apps cannot read. None of it is transmitted anywhere.

What	Where
Your habits, and every entry you record	A private database in the app's own storage
Your settings — when your day starts, theme, default reminder time	Private app storage
When reminders are due and when they last ran	Private app storage
Two counters: how many typed habit sentences the app understood, and how many it did not	Private app storage. The sentences themselves are never stored — only the two numbers
Android's automatic backup is switched off, so none of the above is copied to Google Drive or restored onto another device by the system. Uninstalling Kepta deletes all of it.

Saving a copy of your own data
Kepta can write your habits and history to a file so you can move them to a new phone. You choose where that file goes, through Android's own file picker. Kepta does not upload it, and it has no ability to: see the next section. Once the file is somewhere you chose, it is yours and this policy no longer governs it — if you save it into a cloud folder, that provider's terms apply to the copy you put there.

The offline claim, and how to check it
Kepta does not have the Android INTERNET permission. Without it the operating system will not let the app open a network connection at all. This is enforced by Android, not by a promise in a document.

You do not have to take that on trust. The permission list is part of the shipped app and anyone can read it out of the installed package:

aapt2 dump permissions kepta-release.apk
android.permission.INTERNET will not be listed. What is listed, and why:

Permission	Why it is there
POST_NOTIFICATIONS	To show your reminders
SCHEDULE_EXACT_ALARM	So a reminder arrives at the time you set rather than hours later
RECEIVE_BOOT_COMPLETED	To put your reminders back after the phone restarts
VIBRATE	The small taps you feel when you log something
WAKE_LOCK, FOREGROUND_SERVICE, ACCESS_NETWORK_STATE	Added automatically by androidx.work, a Google library the home-screen widget depends on. Kepta uses none of them directly. ACCESS_NETWORK_STATE only allows an app to ask whether a network exists; it grants no network access, and without INTERNET nothing can be sent regardless
What Kepta does not do
No account, no sign-in, no email address.
No analytics, telemetry, crash reporting, or advertising SDKs.
No advertising identifier.
No ads.
No sale or sharing of personal information.
Purchases
Kepta does not currently sell anything. If a paid feature is added later, the payment is handled by Google Play Billing — Kepta never sees or handles your payment details, and Google's handling of that transaction is covered by Google's own privacy policy and the Google Play Terms of Service. Kepta would store only a local record that the purchase was made.

Children
Kepta is not directed at children and is not designed for or marketed to them. It knowingly collects no information from anyone, children included.

Your rights
Because Kepta holds no data about you on any server, there is nothing to export, correct or delete on request. Everything is on your device and under your control: correct or remove entries inside the app, or uninstall Kepta to remove all of it at once.

Changes
If this policy changes, the date at the top changes with it.

Contact
whirlwind.support@gmail.com
