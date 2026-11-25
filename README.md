# AVD Profile Tools 2611.25.03

**Release Date** 25 November 2026

---

**Overview**

FSLogix profile tools for Azure Virtual Desktop, as one stand-alone Windows app (the Profile Tools of the AVD Live
Dashboard, without the dashboard). For profile shares on Azure Files and on Windows file servers:

- **Find Profile** - find a user's profile folders on every location.
- **Profile Locks** - see who has a profile VHDX open, and release the locks.
- **Delete Profile** - delete a user's profile folders.
- **Profile Sizes** - folder sizes per location.
- **Profile Cleanup** - list and delete stale profiles (no activity for N days), with folders to exclude.
- **Storage Locations** - the configured shares, with their share and NTFS permissions and an FSLogix check.

Everything is set up in Settings (no config file). It updates itself: a new version is offered when it starts.

**Requirements**

- Windows 10 or 11 (64-bit), or Windows Server 2016 or later. Nothing to install - the .NET runtime is inside the exe.
- Azure Files: an Azure account (Microsoft Entra ID sign-in, MFA supported) with access to the storage accounts.
- Windows file servers: no Azure sign-in; the Windows account needs access to the share. Listing and closing open
  files (profile locks) needs administrator rights on the file server.
- Internet access to GitHub for updates.

---

**Executable**

ProfileTools.exe (59.3 MB, standalone - nothing to install)

Download: https://github.com/virtualwebber/Profile-Tools/releases/latest

**Digital signature**

Digitally signed using DigiCert.

**Checksums**

SHA256 - DC1D5D320021E4D9194EA0E4D617C39F9113853406702F68B9F172B00CB3DD9B

**VirusTotal Result**

https://www.virustotal.com/gui/file/dc1d5d320021e4d9194ea0e4d617c39f9113853406702f68b9f172b00cb3dd9b/detection

0 malicious / 0 suspicious of 68 engines

To check a download: `Get-FileHash .\ProfileTools.exe -Algorithm SHA256`