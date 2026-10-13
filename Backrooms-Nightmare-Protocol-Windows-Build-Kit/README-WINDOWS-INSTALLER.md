# The Backrooms — Nightmare Protocol: Windows Installer

This kit adds an Electron desktop window and a GitHub Actions workflow to the Vite/React game. GitHub Actions builds the Windows installer and portable executable, so Node.js is only needed on the remote build runner—not on the PC that plays the finished game.

## Upload to GitHub

1. Create a **new, empty GitHub repository** for this game.
2. Extract this ZIP on your computer.
3. Upload **all of the contents inside the extracted folder** directly to the repository's top level. `package.json`, `index.html`, `src`, `electron`, `electron-builder.yml`, and `.github` should be visible at the repository root. Do not upload just the outer folder as one nested directory.
4. Commit the files.
5. Open the repository's **Actions** tab and choose **Build Backrooms Windows Launcher**. A push to `main`/`master` should start it automatically; otherwise use **Run workflow**.
6. When the workflow succeeds, open its **Summary** and download `Backrooms-Nightmare-Protocol-Windows-Installers` from **Artifacts**.
7. Extract the artifact ZIP. It contains the Windows installer and portable executable.

## Output

- An NSIS Windows setup executable, which installs the game and creates shortcuts.
- A portable executable for testing without running the installer.

## If it fails

Open the failed step in Actions and copy the first meaningful error, not just the final `Process completed with exit code 1` line. The build kit has not been able to verify a full Windows build in this environment, so the GitHub Actions result is the final check.
