# Privacy Policy for Inkstep

**Last updated: 14 October 2026**

Inkstep is an offline Android app for filling and signing documents. This policy
describes what it does with your information. It is short because there is very
little to describe.

## The short version

**Inkstep collects nothing. It has no account system, no analytics, no crash
reporting, and no server.** Your documents, your signatures and your settings
stay on your device.

## What Inkstep stores, and where

All of it is in Inkstep's own private storage on your device, which other apps
cannot read. None of it is transmitted anywhere.

| What | Where | How long |
|---|---|---|
| Your saved signatures and company stamps, including the cleaned-up picture of one you photographed | The app's private files directory | Until you delete them in the app (a deleted picture is removed the next time the app starts) |
| A working copy of each document you opened | The app's private files directory | While it is in the Recent list |
| The Recent list itself: file names and when you opened them | Android shared preferences | Until a document drops off the list, or you clear it |
| The marks on the document that is open right now, so they survive Android closing the app in the background | The app's private files directory | Deleted when you close the document; ignored after 24 hours |
| Settings: theme, language, date format, haptics | Android shared preferences | Until you uninstall |
| A flag recording that Premium was bought, and a count of how often you were asked to rate the app | Android shared preferences | Until you uninstall |

**Inkstep never writes to your original file.** Everything happens on a copy.

**The Recent list is short on purpose.** It holds the last few documents only.
When a document leaves the list its working copy is deleted, and **Clear recent
documents** in Settings deletes all of them at once.

**Android's cloud backup is switched off for Inkstep.** Android can copy an
app's private files to your Google account; Inkstep opts out, so your signatures
and working copies are not included in that backup. The cost is that they do not
move to a new phone on their own.

Uninstalling the app deletes all of the above.

## Files you choose to give it, and files it gives back

- **Opening.** Inkstep sees a document only when you share it to Inkstep from
  another app or pick it in Android's own file picker. It has no permission to
  browse your storage or your photos.
- **Photos of a signature or a stamp.** *Choose a photo* opens Android's picker
  and Inkstep receives the one picture you pick. What it stores is the ink it
  lifts from that picture, not the photo.
- **Sharing and saving.** A finished document goes only where you send it: to
  the app you choose in Android's share sheet, or to the folder you choose with
  *Save to device*. What that other app does with it is up to that app.

## Password-protected PDFs

- A password you type to open a PDF, or to protect one you are sending, is held
  in memory while that document is open. **It is never written to storage.**
- To work on a protected PDF, Inkstep makes an unprotected working copy in its
  private storage, like any other document. It stays there while the document is
  in the Recent list. If that matters to you, clear the list when you are done.

## Redaction

A page you redact is rebuilt so that what is under the black box is removed from
the file you share, not merely covered. The working copy inside Inkstep, and
your original file, still contain it.

## What Inkstep does not do

- No account, no sign-in, no email address.
- No analytics, telemetry, crash reporting, or advertising SDKs.
- No advertising identifier.
- No ads.
- No sale or sharing of personal information.

## The offline claim, and how to check it

Inkstep contains no networking code, and the Android `INTERNET` permission is
**removed** from the release build. Without it the operating system will not let
Inkstep open a network connection at all — this is enforced by Android, not by a
promise in a document.

None of this has to be taken on trust. The permission list is part of the
shipped app and anyone can read it out of the installed package:

```
aapt2 dump permissions <inkstep-release.apk>
```

`android.permission.INTERNET` will not be listed. What is listed is Google Play
billing, for the one purchase, and `ACCESS_NETWORK_STATE`, explained below.
Neither lets Inkstep send anything. There is no camera, storage, contacts or
location permission.

## The one thing that deserves a straight answer: the scanner

If you use **Scan document**, or **Take a photo** for a signature or a stamp,
the camera, edge detection and image filters are provided by **Google ML Kit,
which runs inside Google Play services — a separate Google app on your phone,
not inside Inkstep.** Inkstep itself does not request the camera permission.

What that means honestly:

- **Your scan does not leave your device.** ML Kit's document scanner processes
  on-device, and the finished scan is handed back to Inkstep in Inkstep's private
  storage.
- **Google Play services is Google's software, running under Google's own privacy
  policy, not this one.** Anything Google may record about your use of its
  scanner is outside Inkstep's control and is not governed by this document. See
  <https://policies.google.com/privacy>.
- Including ML Kit causes Android to merge the `ACCESS_NETWORK_STATE` permission
  into Inkstep's manifest. That permission only allows an app to *ask whether a
  network exists*. It does not permit any network access, and Inkstep does not
  have `INTERNET`, so Inkstep cannot upload anything regardless.

If you would rather not involve Google Play services at all, do not use those two
features. Every other part of Inkstep works without them, including drawing a
signature and choosing a photo you already have.

## Purchases and ratings

Inkstep Premium is a single one-time purchase. It is processed by **Google Play
Billing**; Inkstep never sees or handles your payment details. Google's handling
of that transaction is covered by Google's privacy policy and the Google Play
Terms of Service. Inkstep stores only a local flag recording that the purchase
was made.

Now and then Inkstep asks Google Play to show its rating sheet. The sheet is
Google Play's: Inkstep is not told whether you rated the app or what you wrote.
*Rate Inkstep* and *Share Inkstep* in Settings open Google Play and Android's
share sheet, and send nothing themselves.

## Children

Inkstep is not directed at children and is not designed for or marketed to them.
It knowingly collects no information from anyone, children included.

## Your rights

Because Inkstep holds no data about you on any server, there is nothing to
export, correct or delete on request. All data is on your device and under your
control: delete individual signatures and stamps inside the app, clear the
Recent list in Settings, or uninstall Inkstep to remove everything at once.

## A note on what a signature in Inkstep is

Inkstep applies a **visual electronic signature** — the digital equivalent of ink
on paper. It is **not** a certified or cryptographic digital signature (X.509 /
eIDAS QES) and it makes no cryptographic authenticity claim. This is stated in
the app as well.

## Changes

If this policy changes, the date at the top changes with it.

## Contact

whirlwind.support@gmail.com
