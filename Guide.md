# Simple Data Entry App User Guide

## 1. App Overview
**Simple Data Entry** is an Android app for DHIS2 that supports:
- **Aggregate (Dataset) data entry**
- **Tracker enrollments and events**
- **Standalone event programs**
- **Offline-first work** (save locally, sync when internet is available)

The app is designed for fast field data capture with controlled, user-initiated sync.

## 2. Minimum Requirements
- Android **7.0+ (API 24+)**
- Internet for first login and syncing
- Valid DHIS2 account credentials:
  - Server URL
  - Username
  - Password

## 3. Install the APK
1. Copy the APK file to the Android device.
2. Open the APK from Files/Downloads.
3. If Android blocks installation, allow install from that source:
   - Go to `Settings > Security` (or `Apps > Special app access > Install unknown apps`)
   - Select the app you used to open the APK (Files, Chrome, WhatsApp, etc.)
   - Enable **Allow from this source**
4. Retry installation.

## 4. If Play Protect Blocks the APK (Temporary)
If Play Protect warns or blocks installation, temporarily disable scanning:

1. Open **Google Play Store**
2. Tap profile icon (top-right)
3. Tap **Play Protect**
4. Tap the settings icon (top-right)
5. Turn off:
   - **Scan apps with Play Protect**
   - (If shown) **Improve harmful app detection**
6. Install the APK
7. **Immediately re-enable both options after installation**

Notes:
- Menu labels can vary slightly by Android version.
- This should only be temporary for trusted APKs from your team.

## 5. First-Time Setup
1. Open **SimpleDataEntry**.
2. Enter:
   - **Server URL** (example: `https://your-dhis2-server.org`)
   - **Username**
   - **Password**
3. Tap **Login**.
4. Wait for initial metadata/data loading to finish.
5. The app opens the main list of programs (Datasets, Tracker, Events).

## 6. How Data Entry Works

### 6.1 Dataset (Aggregate) flow
1. Open a dataset.
2. Pick instance context (typically period, org unit, and attribute option combo if applicable).
3. Open an existing instance or create new entry.
4. Enter values in form sections.
5. Tap **Save**:
   - Values are stored locally as drafts.
   - They are not guaranteed uploaded yet.
6. Optional: run validation and review warnings/errors.
7. Mark dataset **Complete** when ready.

### 6.2 Tracker flow
1. Open a tracker program.
2. Create or open an enrollment.
3. Fill tracked entity profile/attributes.
4. Add/edit stage events.
5. Save changes; sync when online.

### 6.3 Event program flow
1. Open an event program.
2. Create or edit event(s).
3. Fill event form values.
4. Save and sync.

## 7. Save, Complete, and Sync (Important)
These are different actions:

- **Save**
  - Writes changes to local draft storage.
  - Safe for offline work.

- **Complete (Dataset)**
  - Marks the dataset instance as complete.
  - Completion registration is uploaded to DHIS2 when operation succeeds.

- **Sync**
  - Transfers local unsynced values and downloads latest server updates.
  - On dataset entry sync dialog:
    - **Upload & Download**: sends local drafts first, then pulls latest server data.
    - **Download Only**: refreshes from server without uploading local drafts.

## 8. How Sync to DHIS2 Happens After Form Completion
Recommended sequence for reliable DHIS2 updates:
1. Enter values
2. **Save** (local drafts)
3. **Complete** dataset (if submission is final)
4. **Sync (Upload & Download)** to push remaining drafts and refresh local copy

If offline:
- Local data remains queued locally.
- Sync when internet is back.

## 9. Sync and Status Indicators
- Draft/unsynced status is shown in dataset instance lists.
- Sync progress is shown during user-initiated sync.
- Last sync information appears on the home/program screens.

## 10. Common Issues and Fixes
- **Login fails**: verify URL format, credentials, and internet.
- **No programs shown**: run metadata/data sync from Settings or Home sync action.
- **Entry not visible on server**: run **Upload & Download** sync and confirm network.
- **Cannot edit completed dataset**: mark it incomplete first, edit, then complete again.
- **Play Protect keeps blocking**: confirm APK source, temporarily disable scan, install, then re-enable.

## 11. Security and Good Practice
- Use only trusted APK builds from your deployment team.
- Re-enable Play Protect immediately after installation.
- Do not share credentials.
- Sync before switching devices or uninstalling the app.

## 12. Quick Daily Workflow
1. Open app and confirm account/session
2. Sync (recommended at start of day)
3. Enter data (dataset/tracker/event)
4. Save frequently
5. Complete final reports/events as needed
6. Sync (Upload & Download) before end of day

