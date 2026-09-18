# SATRUGHAN POS Billing

GitHub Pages-ready PWA built from the SATRUGHAN POS HTML app.

## Offline backup & restore
- Automatic offline snapshot every 1 minute.
- Keeps the latest 10 snapshots on the device.
- **Backup** saves a snapshot locally.
- **Export** downloads a complete JSON backup file that can be copied to another phone.
- **Import Restore** restores a JSON backup without internet.
- **Restore** restores the latest on-device snapshot.
- If the app opens with an empty local database, it attempts to restore the latest on-device snapshot automatically.

The backup contains the app's `localStorage` data. It does not upload private billing data to GitHub or any cloud service.

## GitHub Pages
Upload the files to a repository and enable GitHub Pages. The app can then be installed from the browser as a PWA.


## Auto Restore v3
- On startup, the PWA checks the local offline backup database.
- If browser app data is empty or clearly incomplete, the newest meaningful backup is restored automatically.
- A full-screen “Restoring your data…” message is shown during restore.
- After successful restore, the app reloads automatically.
- Manual Restore and Import Restore remain available.
- Up to 15 recent offline snapshots are retained.
- Data stays on the device/browser unless the user explicitly exports a JSON backup.


## Auto Backup v4
- Automatic snapshot on important POS actions such as bill/save/print/payment/history/invoice actions.
- Automatic snapshot when the PWA goes into the background.
- Automatic snapshot on page hide/unload where the browser permits it.
- Existing periodic 1-minute backup remains active as an additional safety layer.
- The latest 15 offline snapshots are retained locally.


## Final verification
The package includes periodic, data-action, background/pagehide Auto Backup and automatic offline restore, with service-worker cache refresh support.
