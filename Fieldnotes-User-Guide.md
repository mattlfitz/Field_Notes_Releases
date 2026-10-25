# Fieldnotes User Guide

## 1. Welcome

Fieldnotes is a private Android and Windows wildlife photography journal. Save photos with animal names, observation dates, places, identification confidence, habitats, outings, and notes. It supports birds, mammals, reptiles, amphibians, and other animals.

Your journal, the bundled animal-name search, and the US state map work offline. There is no account, automatic photo identification, analytics, or automatic cloud backup. The latest preview reads per-photo EXIF capture details and GPS coordinates automatically and presents Insights as visual cards and charts.

This guide describes the current 1.0.0 preview features. New public builds have separate release tags; always read the release notes before installing.

## 2. Install or update safely

### Android
1. Visit https://github.com/mattlfitz/Field_Notes_Releases/releases on your phone.
2. Open the newest preview release and download its Fieldnotes APK.
3. Before updating an existing installation, export a journal backup and keep it outside app storage.
4. Open the APK from Files or Downloads. Android may ask you to permit that app to install unknown apps.
5. Install Fieldnotes and open it. Disable unknown-app installation afterward.

Builds are now signed with one permanent Fieldnotes key, so later versions install over the top and keep your journal. Copies installed before in-app updates were signed with temporary keys: Android rejects an update over them. For that one-time switch, export your journal, check the ZIP is saved outside the app, uninstall Fieldnotes, install the new APK, and restore the backup.

Uninstalling Fieldnotes or clearing its app data permanently removes the local journal and drafts. After reinstalling, use Backup & restore to merge a saved backup. Drafts cannot be restored from a journal export.

### In-app updates
Fieldnotes checks GitHub for a newer build each time it opens. When one is available, a banner shows the build number and download size; select **Update** or **Later**. You can also check at any time from **About Fieldnotes > Check for updates**, which also shows your current build.

- **Android** downloads only the APK built for your phone's processor and verifies its checksum. The first time, Android asks you to allow Fieldnotes to install apps: turn on **Allow from this source**, then go back. Android then asks **Update this app?** and may run a Google Play Protect scan, because Fieldnotes is not from the Play Store. Your journal stays in place.
- **Windows** downloads only the files that changed since your build, then asks to **Restart to update**. Fieldnotes closes, replaces those files, and reopens. If anything fails, the previous files are put back and Fieldnotes says so on the next launch. Keep Fieldnotes in a folder you can write to, such as `C:\Fieldnotes`; it cannot update itself inside `C:\Program Files`.

Updates need an internet connection only while checking and downloading. Fieldnotes never sends your journal anywhere.

### Windows (desktop)
1. Download `Fieldnotes-Windows-*.zip` from the latest release on GitHub Releases.
2. Extract the ZIP archive into a folder of your choice (e.g. `C:\Fieldnotes`).
3. Run `fieldnotes.exe`. All required Visual C++ runtime libraries and Flutter assets are bundled inside the folder. No installer is required.

#### The Windows welcome screen
Fieldnotes opens on an illustrated welcome screen with the Fieldnotes eagle gliding across a forest, replacing the previous bobbing and click-to-soar effect. The scene is drawn by the app, so it needs no internet connection and no downloaded imagery.

- Lighting starts from your computer's local system time and updates automatically while the screen is open. The sky and forest transition through dawn, daylight, dusk, and night; nighttime includes a moon and stars. This is an illustrative clock-based scene, not a calculation of local sunrise or sunset.
- Each visit shows a randomly chosen scene: a forest, a mountain lake, or a bald eagle nest with eaglets.
- Select the scene button to open a compact **Time and scenery** dialog. Enable **Override time and scenery** there to choose **Forest**, **Lake**, or **Eagle’s nest** and reveal a full-day slider. Drag it to preview another time; the controls stay hidden while system time is in use. Disable override to restore the current system time and the random scene immediately. Select **Done** or click outside the dialog to close it and keep the live preview. The preview does not affect your journal or system clock and resets when you reopen the welcome screen.
- Move the mouse across the scene for a gentle parallax. The eagle glides from left to right and returns after passing beyond the screen edge.
- Select **Wildlife fact** for a short note about bald eagles and field journaling.
- Select **Continue to journal**, or press `Esc`, to open your collection. The journal loads in the background while the welcome screen is open.
- Tick **Skip this screen next time** to go straight to the journal on future launches. This preference is stored separately from your journal, so restoring a backup never changes it.
- Reopen the welcome screen at any time from the forest icon in the journal toolbar.

If Windows is set to minimize animations, the eagle and forest stay still. Time-of-day controls and the continue button still work.

## 3. Understand the main screens

Collection is your photo journal. Search, filter, sort, and open sightings here.

Locations leads with a **Sighting map** that pins every GPS-tagged sighting in the lower 48, then a live preview of the offline US state life-list map, then groups recorded places and opens their sightings. On wide windows, the map preview and saved places sit side by side. External map actions hand a selected place or coordinates to another app or browser. Android uses a native `geo:` map intent for coordinates with an HTTPS fallback; Windows opens an HTTPS Google Maps link directly.

On wide Windows and iPad layouts, the navigation rail adds a State map destination that fills the window with the map. On Windows, press Ctrl+M to open it.

Insights shows totals, a States explored map preview, habitats, confirmed life lists, and named outings.

New sighting opens the editor. Backup & restore is available from the main app bar.

Tap the eagle in the app bar or About dialog to view the larger 2048-pixel artwork offline. Pinch to zoom, drag to pan, and use Reset eagle zoom to fit it again. Back returns to the previous screen.

For a few quiet surprises, long-press the eagle icon for a wildlife fact, tap the Insights heading for a discovery message, or double-tap the enlarged eagle to watch it gently soar. The brief animation respects the device's reduced-motion setting. These extras work offline and never change your journal.

## 4. Add your first sighting

1. Tap New sighting.
2. Choose Photo library for one or more photos, or Camera for a new photo.
3. Enter an Animal / species name, or tap Search animal names.
4. Check the Animal group. Bird is the default; choose Mammal, Reptile, Amphibian, or Other animal when appropriate.
5. Set Date observed and Identification. If the first imported photo has an EXIF capture date, Fieldnotes suggests that date until you choose one yourself.
6. Add an optional location name, coordinates, or manual US state.
7. Open More details for optional fields.
8. Tap Save sighting.

At least one photo and a nonempty animal name are required for a new sighting. To log animals without photos, use **Checklist** instead: tap names to count them and save each as its own photo-less sighting under one outing. Location is optional. If a field is invalid, the editor explains what needs correcting. Observation dates cannot be in the future.

For each imported photo, Fieldnotes records supported embedded EXIF details: capture date/time, camera make/model, lens make/model, focal length, shutter speed, aperture, ISO, exposure compensation, flash status, and GPS coordinates. Open a sighting and swipe between photos or use its thumbnail strip, then expand **Photo details** to see the matching metadata. The card differentiates a photo with no embedded details from a file Fieldnotes could not read. Metadata is stored per photo, preserved when photos are reordered, and included in journal backups.

Use Unknown bird or Unknown animal if you cannot identify the subject. These placeholders are saved as unknown identifications and excluded from life lists.

### Import many photos at once

After a big day in the field, tap **Import many photos** (the photo-plus icon in the top app bar) and choose your photos. Fieldnotes reads each photo's capture time and GPS and groups photos taken within 30 minutes and about 1 km of each other into one sighting. Photos without a capture date each become their own sighting. Turn off **Group photos taken together** to import every photo separately, and uncheck any group you do not want. Tap **Import** to save each group as an **Unknown bird** sighting with its date, time, and location filled in, then open each one to add the animal name and identification.

## 5. Search the offline animal checklist

Tap Search animal names in the editor. Search by part of a common name, such as cardinal, or a scientific name, such as Cardinalis cardinalis. Search is case-insensitive. Use Animal group to narrow results or choose All animals.

The bundled snapshot includes 2,570 active species observed in the United States or Canada through iNaturalist research-grade observations. Birds, mammals, reptiles, and amphibians are included. Previously saved names are also available.

Selecting a result fills the common name, scientific name, and animal group. It does not examine your photo and does not mark the sighting Confirmed. Check all values before saving. Previously saved names can retain the scientific spelling you entered earlier.

The checklist is not a complete or authoritative fauna dictionary. It may omit species with no qualifying observations and include introduced or escaped animals. Only factual species names and group assignments are bundled, not observation records, descriptions, or photographs.

If a species is missing, close search and type a custom name. Use Other animal for animals outside the four bundled groups. Consistent spelling matters because counts use your entered names rather than verified taxon IDs.

## 6. Identification and life-list eligibility

Confirmed means you have chosen to treat the identification as reliable. Tentative is useful when a name is a working guess. Unknown is appropriate when you do not have an identification.

Only Confirmed, nonempty names enter the life lists. Unknown bird and Unknown animal are excluded even if marked Confirmed in older data. Selecting a catalog result does not confirm identification.

Bird life list includes only confirmed entries in the Bird group. Overall life list includes confirmed entries from every animal group.

Within a group, case differences and surrounding spaces are ignored when counting names. Different entered names remain separate. The same entered name in different animal groups remains separate in the overall list.

Older entries without animal-group information default to Bird. Edit older mammal or other-animal entries to choose their correct group. Legacy entries without identification information default to Tentative; the app does not guess confidence.

## 7. Record locations correctly

Location name is an optional descriptive place, such as Riverside Nature Preserve. It can be used without coordinates, but a name alone does not automatically assign a state.

Use current GPS location requests your phone's location when you tap it. Enable Android location services and grant location permission. This is your current position, not an older photo's capture location. No background location is collected.

### Coordinates from the photo itself

Many phones and GPS-equipped cameras store the capture position inside the photo's EXIF data. When you import a photo and both coordinate fields are empty, Fieldnotes reads that position and fills Latitude and Longitude for you, then shows a message so you can review them. If several photos are imported together, the first photo with GPS data is used.

Existing coordinates are never overwritten by a photo import, and nothing is read from the internet; the EXIF data is decoded on your device from the private copy. Photos without GPS data, screenshots, and images exported with location stripped leave the fields blank. Treat the filled values as a starting point: cameras can record the position where the photo was processed rather than where the animal was, so check the detected state and adjust if needed.

For an older photograph without embedded GPS, enter the actual observation coordinates under More details. Latitude must be between -90 and 90, longitude between -180 and 180. Supply both fields or leave both blank. Use decimal degrees; western US longitudes are negative.

The coordinate preview shows the values being saved without loading an online map. Clear coordinates removes both fields.

Saved places reuses a location from your journal. Confirm the replacement: it can replace the name and coordinates, or clear existing coordinates when the chosen place has none. The saved manual state is reused as well.

### Manual state and coordinate priority

If a sighting has no coordinates, choose US state (without GPS) from the editor. This is optional and supports the 48 contiguous US states. Leave Not recorded / outside map selected when appropriate.

If you enter valid coordinates, the editor detects the state offline. Coordinates always take priority over the saved manual state. A coordinate outside the contiguous-US map stays unmapped even if a manual state was previously chosen.

Deleting coordinates makes the saved manual state relevant again. Check the selector after clearing coordinates. The app never infers a state from a place name.

## 8. Optional observation details

Scientific name can be filled by the catalog or entered manually.

Habitat is selected from the available habitat categories and contributes to the Insights breakdown.

Outing groups sightings under a name you choose. Grouping is case-insensitive; use a distinct name for each trip if you want separate outings.

Animal count records the number of animals observed in that sighting. It accepts whole numbers from 1 through 100000. It does not multiply distinct-name life-list totals.

Observation time records an optional time of day. Field notes can describe behavior, weather, identification clues, or anything you want to remember.

Example: two sightings of Northern Cardinal in Texas, with animal counts 2 and 3, produce two sightings and five animals observed, but one confirmed bird name in Texas if both identifications are confirmed.

## 9. Manage photographs

Fieldnotes copies imported photographs into its private storage at original quality. Your original library files are not modified or deleted.

In the editor, add more photos, remove unwanted ones, and use the star to choose the cover. Hold and drag a handle on mobile, drag it directly on Windows, or use the arrow controls to move a photo earlier or later. Save the sighting to apply changes.

Open a sighting to swipe through its photos. Tap a photo to open fullscreen. Pinch to zoom and drag around the enlarged image.

Double-tap toggles between fit-to-screen and actual size, centered on the tapped point. Actual size means one original photo pixel per physical screen pixel, not a fixed visual enlargement. Small photos can therefore appear smaller at actual size than at fit.

Fullscreen includes previous/next controls, a photo counter, and reset zoom. Journal cards use small cached previews for efficiency; fullscreen and backups retain originals.

### Share a sighting safely

Open a sighting, swipe to the photo you want, and tap **Share sighting** in the top bar. Fieldnotes shares the currently displayed photo and opens the operating system's share sheet, where installed apps such as Facebook, Threads, Instagram, Messages, or Mail may be available.

Choose **Branded card** for a portrait Fieldnotes card with the photo and selected details, or **Photo + caption** for a clean copy of the photo plus selected text. You can include the animal name, scientific name, observation date, location name, habitat, identification status, animal count, outing, field notes, and available camera/exposure details. The image and caption previews update as you change these choices.

Use **Copy caption** when a social app does not accept text from the system share sheet. Use **Save image** to put the currently previewed, privacy-safe PNG in the device photo gallery for later posting. **Open share sheet** sends the same image and caption to the operating system's installed sharing targets.

Precise latitude and longitude are never offered or added to the card or caption. The location name and field notes are off by default and must be selected each time. Before sharing either format, Fieldnotes decodes and re-encodes the image as a new PNG, removing the original EXIF metadata, including any hidden GPS coordinates. The shared photo is therefore visually the same image rather than the original file bytes. Sharing is an explicit action and may send the selected content to the app or service you choose.

## 10. Find, edit, favorite, or delete sightings

Collection search matches names, scientific names, places, notes, habitats, outings, animal types, and US state names (or an exact state code such as `OH`). Combine search with the filter chips: **Favorites**; an animal-type chip such as **Birds** or **Mammals** when your journal has more than one type; and the **Year**, **State**, and **Habitat** menus. **All sightings** clears every filter. Sort by observation date or animal name.

Tap a card to view details. Use the heart to favorite or unfavorite it and the pencil to edit it. Save after editing.

The sighting menu offers deletion with confirmation. Cancel keeps the entry. Deleting removes the saved sighting and its app-managed photo references; it does not delete original library photographs. Right after deleting, tap **Undo** in the message at the bottom of the screen (shown for about 8 seconds) to restore the sighting with its photos.

If an image is unavailable, try the retry control. If the private file is missing or damaged, add a replacement from the original library. Merge restore skips already-existing sighting IDs, so it does not overwrite an existing damaged entry.

## 11. Read Insights and outings

Insights keeps an **Overview**, **Life lists**, and **Outings** switcher visible while you browse. Overview shows three stat cards: Your collection shows Sightings, Animal names, and Places; Photos shows Saved photos, Favorites, and GPS tagged; Life lists shows confirmed bird and overall totals, Named outings, and Animals observed. Each figure has an icon so you can scan the page quickly. Life lists and Outings move their detailed expandable lists into focused sections.

Sightings counts saved journal entries. Animal names counts distinct entered name/group combinations, including entries that do not qualify for confirmed life lists. Places counts recorded place labels. Saved photos counts photo copies; favorites and GPS-tagged totals reflect saved metadata.

Animals observed adds the entered animal counts. It is different from the distinct-name total.

The Animal groups card draws a single bar split by Bird, Mammal, Reptile, Amphibian, and Other animal, with a legend showing each group's sighting count. The Habitats explored card shows a colored bar per habitat, sized by its share of your saved sightings. Both describe your journal, not regional abundance.

Expand the Bird life list or Overall life list card to see confirmed names and first-seen dates; the badge on each row and on the card header shows sighting counts. Tap a name to see its sightings.

### Year lists and goals

Life lists opens with a **Year list** card. Pick a year from the menu and choose **Birds** or **All animals** to count the distinct confirmed names observed that year. Select **Set goal** to enter an annual target; a progress bar shows how many names remain, and the goal is remembered for that year (enter 0 to clear it). Expand the list to see each name with its **First of year** date, then tap a name to open those sightings. Overview also shows the current year's bird year-list total.

### New lifer celebrations

When a new sighting adds a confirmed name you have never recorded, Fieldnotes celebrates with a **New lifer!** message showing its number on your bird or overall life list. Select **View** to open the sighting. Confirming an existing entry later updates the life lists without a celebration.

Expand the Outings card to see trips grouped by your outing names, then tap a trip to open its sightings.

## 12. Explore the US state map

### Sighting pin map

The **Sighting map** card at the top of Locations places a pin for each sighting with GPS coordinates. It is drawn on your device from the bundled state outlines, so no map service receives your locations. Nearby sightings merge into a numbered group. Tap a single pin to open its sighting, or tap a group to zoom in until its pins separate; sightings at the same spot open as a list. Pinch, use the mouse wheel, or use the **+** and **-** buttons to zoom, and choose **Show all pins** to reset. GPS sightings outside the 48 contiguous states are counted below the map and still appear under Saved places.

### State life-list map


Open Locations > Explore state map from the prominent US state life-lists card. The card shows a live preview of your colored states and summarizes states explored, mapped sightings, and confirmed names before opening the map. On wide Windows and iPad layouts, you can also choose State map in the navigation rail, press Ctrl+M on Windows, or select Open state map on the Insights States explored card. Birds is selected by default each time the map is opened. Choose All animals for the overall confirmed life list.

Each state label shows its abbreviation and distinct confirmed-name count. Boundaries remain visible. Color bands are fixed across both modes:

- 0: no confirmed names assigned.
- 1-5: light green.
- 6-20: medium-light green.
- 21-50: darker green.
- 51 or more: deepest green.

Pinch to zoom, scroll the mouse wheel, drag to pan, or use Zoom in map and Zoom out map. Reset map zoom returns to the initial fit. With a mouse, hover a state to highlight it and see its name and total. Tap a state or one of the small-state labels to open its list.

On wide layouts, the map fills most of the window and a side panel sits beside it. Summary cards above the map show states explored, your top state (or a tie between states), and mapped names; on short windows the cards are hidden to give the map more room. With no state selected, the panel offers a Find a state search, ranks explored states with progress bars, and lists the remaining states under Still to explore. Click a state on the map or in the panel to show its list. Select Show all states to return to the overview.

With a keyboard, press Tab to move focus to the map, use the arrow keys to move between states in alphabetical order, and press Enter or Space to open the highlighted state.

The State totals and lists section on phones provides a text-based alternative to map tapping, including states with zero names. It is useful for small states, larger text settings, and assistive technology.

### State drilldown

The state screen shows confirmed names for the selected mode. Expand a name to see the associated sightings, dates, and places. Tap a sighting to view its details or edit it. Returning refreshes the lists and map totals.

A repeat sighting of the same confirmed name in one state does not increase its distinct-name count. The same name in two states counts once in each. Do not sum state totals to calculate your national life-list total.

The unmapped message counts eligible confirmed sightings that cannot be assigned, not distinct animal names. Add coordinates or a manual state to eligible no-GPS entries to include them.

### Scope and accuracy

The map opens on the 48 contiguous states. Use the **Region** picker above the map to switch to Alaska, Hawaii, or Canada's provinces and territories. DC and US territories are not mapped, but sightings there can still be saved and included in overall journal and life-list totals.

Boundaries are public-domain U.S. Census Bureau generalized ACS 2024 data, simplified to 0.005 degrees. Display uses an Albers equal-area projection. Detection near borders is approximate, not a legal boundary determination. No online map tiles are requested and coordinates are not sent to a service for state detection.

## 13. Protect unsaved work with drafts

Editor changes are saved to a local draft after a short delay. Back navigation offers Keep editing, Discard, or Keep draft when there are unsaved changes.

Keep editing returns to the editor. Keep draft leaves and retains the draft for reopening that editor. Discard removes unsaved work without changing an existing saved sighting. Save sighting clears the corresponding draft after saving.

Drafts retain animal groups, manual states, metadata, and staged photo selections. A draft can be restored when the editor is reopened. Interrupted Android photo-picker selections are also recovered when possible.

Drafts are not backups, do not transfer to another installation, and are not included in journal ZIP exports. Abrupt device failure can still lose the latest keystrokes.

## 14. Export and restore backups

### Export

1. Open Backup & restore from the main app bar.
2. Choose Export journal.
3. Save the ZIP outside Fieldnotes private storage, using a destination you trust.
4. Confirm that the file exists and keep another copy if the journal is important.

Exports include saved metadata and original photo copies, including animal groups and manual states. Drafts are excluded. Backups are unencrypted and may contain precise coordinates.

### Share with eBird

Tap **Export eBird CSV** on Backup & restore to save your confirmed bird sightings as an eBird Record Format file (no header row). Tentative and unknown sightings and other animals are skipped, and Fieldnotes tells you how many were exported. Each sighting is exported as an incidental observation with its count, notes, location, coordinates, date, time, and state. Fieldnotes never uploads anything: you choose where the file is saved, and you import it yourself at ebird.org/import using the **eBird Record Format (Extended)** option, where eBird asks you to confirm each location before submitting.

### Backup reminders

Backups never run automatically, so Collection shows a reminder card when work is at risk: after your first three sightings if you have never exported, or once a backup is two weeks old (or ten sightings behind) and newer sightings exist. Choose **Back up now** to open Backup & restore, or **Remind me later** to hide the card for seven days. The card disappears after a successful export.

The uncompressed backup content is limited to 256 MB. Keep original photographs backed up separately; export is not an unlimited photo-archive service.

### Restore

1. Open Backup & restore and choose Restore backup.
2. Select a Fieldnotes ZIP.
3. Review the preview before confirming restoration.
4. Check the resulting journal and life lists afterward.

The selected ZIP and its uncompressed content must each be at most 256 MB. Invalid or unsafe backups are rejected.

Restore merges new sighting IDs and skips IDs already in the journal. It does not overwrite edits to existing sightings. Restoring the same backup again does not duplicate those existing IDs.

Older backups without animal groups default to Bird; older backups without manual states remain unassigned unless coordinates identify a state. Edit metadata when necessary.

## 15. Privacy and offline behavior

Saved data resides in app-private storage. No sign-in, analytics, cloud sync, or background location is used. Android automatic backup is disabled. Photo GPS data is read locally from your imported copy and is only stored if you save the sighting with those coordinates. Sharing and saving an image are user-initiated; precise coordinates are excluded and exported images are re-encoded without EXIF or hidden GPS before they leave app-private storage.

Core journaling, animal-name search, life lists, and state-map detection work offline. External map apps and named-place searches may require internet access and receive the location you choose to open.

Selecting a cloud-backed file destination for an export can upload the ZIP through that provider. This is your explicit action, not automatic Fieldnotes cloud storage.

Export before uninstalling, clearing data, changing phones, or testing a differently signed APK. Do not treat a local draft as disaster recovery.

## 16. Troubleshooting

Cannot save: add at least one photo, enter an animal name, and check both coordinates and the whole-number animal count.

GPS unavailable: enable Android location services, check permission, and try outdoors. Enter a place or coordinates manually if necessary.

Name not found: try a scientific name, clear the group filter, or enter a custom name. The checklist is observational and not exhaustive.

Missing from the bird list: verify Confirmed identification, Bird group, and a non-placeholder name.

Missing from a state's list: check the mode, identification, coordinates, and manual state. Coordinates override manual state; outside-map locations are excluded.

State total seems too low: repeated sightings and animal counts do not multiply distinct names. Tentative and unknown entries are excluded.

State total seems too high: check inconsistent spellings and animal groups. Counts are entered-name based, not taxonomically reconciled.

No map or name results after a load error: use Retry. Loading failures are shown explicitly rather than treated as empty data.

Android rejects an update: check the signing warning in section 2 and export before uninstalling. No backup can recover drafts after uninstall.

Restore did not replace an entry: merge restore skips existing IDs by design. It is not an overwrite operation.

Maps do not open: install a map app or browser; named-place lookups can require internet.

## 17. A practical field workflow

Before a trip, install and open Fieldnotes, check that offline name search and the map load, and export the existing journal.

During a trip, save photos with the actual observation date and place. Use a consistent outing name. Keep uncertain identifications Tentative.

After a trip, review scientific names and groups, confirm reliable identifications, choose photo covers, and check the bird/overall and state lists.

Finally, export a fresh backup and keep the original photographs separately. Check that the ZIP was saved successfully before deleting anything or changing installations.
