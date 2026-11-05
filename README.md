# Thesis Companion v0.1

A small, local-first thesis planning companion. It is designed to sit alongside LaTeX, not replace it.

## Features in this first version
- Create and edit your own thesis chapters and track progress/status.
- Record daily word and page totals, with a configurable daily word target.
- Time focused work sessions or enter them manually; link sessions to chapters.
- Keep a small reference library and export it as a `.bib` file.
- Export/import a complete JSON backup.
- Responsive layout and installable PWA structure for Android.

## Run it on your computer
1. Unzip the project.
2. Open the folder in Visual Studio Code.
3. Install the **Live Server** extension (if you do not already have it).
4. Right-click `index.html` and choose **Open with Live Server**.

For offline/PWA installation, serve it over HTTPS (or localhost). Opening the HTML file directly with `file://` does not enable service workers.

## Put it on Android
The simplest route is to publish the folder to a GitHub repository and enable GitHub Pages:
1. Create a GitHub repository and upload the contents of this folder.
2. In the repository settings, enable **Pages** and deploy from the main branch / root folder.
3. Open the resulting HTTPS address in Chrome on Android.
4. Open Chrome's menu and choose **Install app** or **Add to Home screen** (wording varies).

The repository contains the app source. Do not put private thesis text, unpublished results, or sensitive data in a public repository. The app's data is stored locally in the browser, separately from the source code.

## Important data note
This version stores information in browser localStorage on the device. It does not sync between devices. Clearing site data, changing browser, or uninstalling/clearing app data may remove the information. Use **Data & backup → Download backup** regularly. Store the backup somewhere separate from the phone.

## Current limitations / next improvements
- Chapter progress is entered manually; it is not inferred from your LaTeX files.
- Daily writing totals are entered manually to avoid pretending the app can reliably inspect your LaTeX project.
- Reference details are entered manually; DOI lookup and automatic BibTeX retrieval are not included yet.
- The focus timer runs while the app page is open. If Android suspends the browser, timing may be inaccurate.
- This is a first prototype; test it with a small amount of data and keep backups.


## Manuscript PDF reader (v0.2)

Open **My manuscript** and choose a compiled PDF. The file is stored locally in IndexedDB on that device and can be reopened after closing the app or restarting the phone. The reader uses the browser's built-in PDF viewer; on some Android browser versions, use **Open separately** if the embedded viewer is not displayed correctly.

The reader remembers the page when you use the page-number control and press **Go**. The PDF is stored separately from the JSON workspace backup and is not included in that export. Keep the original PDF and a separate copy. Clearing browser/site data or uninstalling the PWA can remove the locally stored PDF. The app does not upload the PDF to GitHub Pages or any other server.
