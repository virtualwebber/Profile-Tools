# AVD Profile Tools 2611.25.02

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

ProfileTools.exe (59.2 MB, standalone - nothing to install)

Download: https://github.com/virtualwebber/Profile-Tools/releases/latest

**Digital signature**

Digitally signed using DigiCert.

**Checksums**

SHA256 - 8040EA5C5014D9A2B6DD9ED642B3DEA9B25744C55EEB9CCB80C655429CCA74A8

**VirusTotal Result**

https://www.virustotal.com/gui/file/8040ea5c5014d9a2b6dd9ed642b3dea9b25744c55eeb9ccb80c655429cca74a8/detection

0 malicious / 0 suspicious of 66 engines

To check a download: `Get-FileHash .\ProfileTools.exe -Algorithm SHA256`