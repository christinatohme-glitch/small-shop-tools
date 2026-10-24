# Northstar Shop Tools — Windows installer build

This project packages the offline HTML prototype in Electron and builds a Windows x64 NSIS `.exe` installer.

## Build directly on Windows
1. Install Node.js 22 LTS from https://nodejs.org/.
2. Extract this folder to a normal writable folder.
3. Open PowerShell in this folder.
4. Run `npm install`.
5. Run `npm run dist-win`.
6. Find the installer in `dist/Northstar-Shop-Tools-Setup-1.0.0.exe`.

## Build using GitHub Actions
1. Create a GitHub repository and upload these project files to the `main` branch.
2. Open the repository's **Actions** tab.
3. Select **Build Northstar Windows Installer** and click **Run workflow** (or push a commit to `main`).
4. When the workflow completes, open the run and download the artifact named `Northstar-Shop-Tools-Windows-Installer`.

## Important limitations
- This is an offline desktop wrapper around the current HTML prototype, not a certified Microsoft Store submission.
- The prototype uses browser local storage. Keep regular exported backups; test data persistence and backup/restore before using it for important business records.
- The installer is unsigned unless you sign it with a certificate. Microsoft Store distribution may require a different package format and store-specific identity/metadata.
- The build workflow produces an `.exe` installer, not an `.msi`.
