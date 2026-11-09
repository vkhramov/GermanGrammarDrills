# GermanGrammarDrills

A mobile-first, installable PWA study interface for the supplied *German Grammar Drills* PDF.

## Important: keep the book data private

The app code is separate from the extracted book text and Answer Key. The file `GermanGrammarDrills-book-data.json` contains copyrighted book content and is intentionally **not included** in this GitHub Pages source folder. Do not commit that data file or the original PDF to a public repository. Keep it on your own device and import it inside the app.

## Deploy to GitHub Pages

1. Create a GitHub repository for the app shell.
2. Upload the files in this folder (`index.html`, `styles.css`, `app.js`, `manifest.webmanifest`, `sw.js`, and this README).
3. In repository **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`.
4. Open the published Pages URL in Chrome on your Galaxy S24 Ultra.
5. Import the separate `GermanGrammarDrills-book-data.json` file from your device. It is stored locally in the browser and is not sent to a server.
6. In Chrome, use **⋮ → Add to Home screen** or the app's Install control if offered.

The Pages repository contains only the application code. The private JSON contains the book's extracted page text, exercises and original Answer Key sections. It must remain separate from the public repository.

## Features

- Book-wide reading progress: the current PDF page and exact scroll position are saved automatically, including when you switch to exercises or leave the app. Resume reading from the same place.
- Book page reader with chapter navigation and page-by-page controls.
- 215 numbered exercises extracted from the PDF.
- Each answer field appears directly below its corresponding numbered prompt.
- Answers are saved automatically as you type; checking uses only the extracted Answer Key, without adding external answers.
- Exercises marked as sample answers are never automatically graded; they are sent to manual review.
- Mistake review, saved drafts, completion status and progress.
- Offline app shell after the first visit; book data and progress are saved in the browser's local storage.

## Checking policy

Automatic checking compares the entered response with the corresponding Answer Key entry after case/whitespace normalization. Explicit alternatives printed in the key are accepted. It does not try to infer other valid German answers. Where the book labels answers as samples, the app shows the original key and requests manual comparison.

## Device storage

The book data and learning progress are stored locally in this browser. Clearing site data, changing browsers, or changing devices can remove or separate that data. Keep a backup copy of the private JSON file.


## App version
The current app version is shown at the bottom of the navigation menu. This release is **v1.0.1**. The service-worker cache version was also bumped so deployed browsers can fetch the updated files.
