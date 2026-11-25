# AVD Profile Tools 2611.25.06

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

SHA256 - E476FCB4CD99551F4329A4717C26BA7D3C56BB4F01F5142B4B2D2337CFDA2D1F

**VirusTotal Result**

https://www.virustotal.com/gui/file/e476fcb4cd99551f4329a4717c26ba7d3c56bb4f01f5142b4b2d2337cfda2d1f/detection

0 malicious / 0 suspicious of 69 engines

To check a download: `Get-FileHash .\ProfileTools.exe -Algorithm SHA256`