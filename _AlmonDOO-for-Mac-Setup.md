# AlmonDOO for Mac — setup and updates

Current version: **1.7** (includes the phone-merge logic from the Android work).

## Install or update
1. Quit AlmonDOO: click its window and press **⌘Q**.
2. Unzip the AlmonDOO package and run **Install AlmonDOO.command**. On the first run, right-click it and choose **Open**.
3. AlmonDOO opens. If it's linked to your CSV already, the list loads with no questions.

**Always update with the installer.** Don't swap `AlmonDOO.html` by hand. The page and its helper have to match. This replaces step 4 of *AlmonDOO Android setup*.

## How the Mac version reaches the CSV
- A small helper app, **AlmonDOO Helper** (in `~/Library/Application Support/AlmonDOO`), reads and writes the CSV. It remembers which file you chose, so Chrome never asks for file permission.
- The CSV lives in **Google Drive**. The first time, macOS may ask whether *AlmonDOO Helper* can access Google Drive. Click **Allow**.
- If AlmonDOO can't read the file, a bar at the top explains why and offers **Retry**. It also keeps retrying on its own. It never asks you to pick the file again, and it never overwrites the file while it can't read it. Edits you make in the meantime are kept and merged in once the file is readable.
- If no macOS prompt appears and the bar says macOS hasn't allowed access, add **AlmonDOO Helper** under **System Settings → Privacy & Security → Full Disk Access**, then Retry.

## Where things live
- App: `~/Applications/AlmonDOO.app` (your home folder's Applications). Drag it to the main Applications folder or the Dock if you like.
- Helper, settings and a backup of the previous CSV version (`backup.csv`): `~/Library/Application Support/AlmonDOO`
- Your to-dos: only in the CSV you chose.