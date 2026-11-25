# Setup and usage notes

## Requirements

- A current version of Chrome, Edge, Firefox, or Safari.
- Optional: Python 3 for running a local development server.

There are no third-party JavaScript dependencies and no package manager is required.

## Start the app

From the project root (the directory containing `index.html`):

```bash
python -m http.server 8000
```

Open `http://localhost:8000` in your browser. If port 8000 is already in use, choose another port, for example `python -m http.server 8080`, and open `http://localhost:8080`.

You can also open `index.html` directly, although a local server provides a more consistent browser environment.

## Where data is stored

The app stores its state in browser local storage using these keys:

- `ss_subjects_v2` — subjects
- `ss_tasks_v2` — tasks
- `ss_profile_v1` — profile name and email

Data is scoped to the browser and origin. For a clean first-run test, clear the site's local storage in browser developer tools and reload. This also removes user-created content.

## Troubleshooting

- **Page looks unstyled:** make sure `style.css` remains beside `index.html`.
- **Buttons do not respond:** make sure `app.js` remains beside `index.html` and check the browser console for errors.
- **Changes did not persist:** ensure browser storage is enabled and not being cleared automatically; private browsing may have different persistence rules.
- **Port is busy:** use a different port number in the server command.

## Scope

This deliverable is a frontend-only prototype. It does not include production authentication, server-side validation, cloud backup, multi-user accounts, or cross-device synchronisation.
