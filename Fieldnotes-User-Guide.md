# Fieldnotes User Guide

## 1. Welcome

Fieldnotes is a private Android wildlife photography journal. Save photos with animal names, observation dates, places, identification confidence, habitats, outings, and notes. It supports birds, mammals, reptiles, amphibians, and other animals.

Your journal, the bundled animal-name search, and the US state map work offline. There is no account, automatic photo identification, analytics, or automatic cloud backup. The eagle artwork now has the refined compact beak and softer head based on the owner's flight and perched-eagle photos.

This guide describes the current 1.0.0 preview features. New public builds have separate release tags; always read the release notes before installing.

## 2. Install or update safely

1. Visit https://github.com/mattlfitz/Field_Notes_Releases/releases on your phone.
2. Open the newest preview release and download its Fieldnotes APK.
3. Before updating an existing installation, export a journal backup and keep it outside app storage.
4. Open the APK from Files or Downloads. Android may ask you to permit that app to install unknown apps.
5. Install Fieldnotes and open it. Disable unknown-app installation afterward.

These APKs are debug-signed previews, not production-signed Play Store releases. GitHub builds can use different signing keys. If Android rejects an update because its signature differs, do not immediately uninstall: first export your journal and verify that the ZIP is saved somewhere accessible.

Uninstalling Fieldnotes or clearing its app data permanently removes the local journal and drafts. After reinstalling, use Backup & restore to merge a saved backup. Drafts cannot be restored from a journal export.

## 3. Understand the main screens

Collection is your photo journal. Search, filter, sort, and open sightings here.

Locations groups recorded places and opens their sightings. External map actions hand a selected place or coordinates to another app or browser.

Insights shows totals, habitats, confirmed life lists, named outings, and the US state map.

New sighting opens the editor. Backup & restore is available from the main app bar.

Tap the eagle in the app bar or About dialog to view the larger 2048-pixel artwork offline. Pinch to zoom, drag to pan, and use Reset eagle zoom to fit it again. Back returns to the previous screen.

For a few quiet surprises, long-press the eagle icon for a wildlife fact, tap the Insights heading for a discovery message, or double-tap the enlarged eagle to watch it gently soar. The brief animation respects the device's reduced-motion setting. These extras work offline and never change your journal.

## 4. Add your first sighting

1. Tap New sighting.
2. Choose Photo library for one or more photos, or Camera for a new photo.
3. Enter an Animal / species name, or tap Search animal names.
4. Check the Animal group. Bird is the default; choose Mammal, Reptile, Amphibian, or Other animal when appropriate.
5. Set Date observed and Identification.
6. Add an optional location name, coordinates, or manual US state.
7. Open More details for optional fields.
8. Tap Save sighting.

At least one photo and a nonempty animal name are required. Location is optional. If a field is invalid, the editor explains what needs correcting. Observation dates cannot be in the future.

Use Unknown bird or Unknown animal if you cannot identify the subject. These placeholders are saved as unknown identifications and excluded from life lists.

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

For an older photograph, enter the actual observation coordinates under More details. Latitude must be between -90 and 90, longitude between -180 and 180. Supply both fields or leave both blank. Use decimal degrees; western US longitudes are negative.

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

In the editor, add more photos, remove unwanted ones, use the star to choose the cover, and use arrows to move a photo earlier or later. Save the sighting to apply changes.

Open a sighting to swipe through its photos. Tap a photo to open fullscreen. Pinch to zoom and drag around the enlarged image.

Double-tap toggles between fit-to-screen and actual size, centered on the tapped point. Actual size means one original photo pixel per physical screen pixel, not a fixed visual enlargement. Small photos can therefore appear smaller at actual size than at fit.

Fullscreen includes previous/next controls, a photo counter, and reset zoom. Journal cards use small cached previews for efficiency; fullscreen and backups retain originals.

## 10. Find, edit, favorite, or delete sightings

Collection search matches names, scientific names, places, notes, habitats, and outings. Combine search with favorite and habitat filters. Sort by observation date or animal name.

Tap a card to view details. Use the heart to favorite or unfavorite it and the pencil to edit it. Save after editing.

The sighting menu offers deletion with confirmation. Cancel keeps the entry. Deleting removes the saved sighting and its app-managed photo references; it does not delete original library photographs.

If an image is unavailable, try the retry control. If the private file is missing or damaged, add a replacement from the original library. Merge restore skips already-existing sighting IDs, so it does not overwrite an existing damaged entry.

## 11. Read Insights and outings

Sightings counts saved journal entries. Animal names counts distinct entered name/group combinations, including entries that do not qualify for confirmed life lists. Places counts recorded place labels. Saved photos counts photo copies; favorites and GPS-tagged totals reflect saved metadata.

Animals observed adds the entered animal counts. It is different from the distinct-name total.

Expand Bird life list or Overall life list to see confirmed names, first-seen dates, and sighting counts. Tap a name to see its sightings.

Expand Outings to see trips grouped by your outing names. Habitat bars describe saved sightings, not regional species abundance.

## 12. Explore the US state map

Open Insights > US state map. Birds is selected by default each time the map is opened. Choose All animals for the overall confirmed life list.

Each state label shows its abbreviation and distinct confirmed-name count. Boundaries remain visible. Color bands are fixed across both modes:

- 0: no confirmed names assigned.
- 1-5: light green.
- 6-20: medium-light green.
- 21-50: darker green.
- 51 or more: deepest green.

Pinch to zoom, drag to pan, or use Zoom in map and Zoom out map. Reset map zoom returns to the initial fit. Tap a state or one of the small-state labels to open its list.

The State totals and lists section provides a text-based alternative to map tapping, including states with zero names. It is useful for small states, larger text settings, and assistive technology.

### State drilldown

The state screen shows confirmed names for the selected mode. Expand a name to see the associated sightings, dates, and places. Tap a sighting to view its details or edit it. Returning refreshes the lists and map totals.

A repeat sighting of the same confirmed name in one state does not increase its distinct-name count. The same name in two states counts once in each. Do not sum state totals to calculate your national life-list total.

The unmapped message counts eligible confirmed sightings that cannot be assigned, not distinct animal names. Add coordinates or a manual state to eligible no-GPS entries to include them.

### Scope and accuracy

The map covers the 48 contiguous states only. Alaska, Hawaii, DC, Canada, and territories are excluded, but sightings there can still be saved and included in overall journal and life-list totals.

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

Saved data resides in app-private storage. No sign-in, analytics, cloud sync, or background location is used. Android automatic backup is disabled.

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
