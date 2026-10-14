# Fieldnotes for Android & Windows

An offline wildlife photo journal for birds, mammals, reptiles, amphibians, and other animals.

The latest preview adds privacy-safe sighting sharing with live image and caption previews, makes the offline US state life-list map central to Locations, reads per-photo EXIF details automatically, and presents Insights as visual cards and charts. Public downloads include an Android APK and a native 64-bit Windows portable edition. Read the [detailed user guide](Fieldnotes-User-Guide.md) for complete instructions, examples, privacy information, and troubleshooting. PDF editions of the quick start and detailed guide are included in release downloads.

Tap the eagle icon to open its larger artwork; pinch to zoom and use Reset eagle zoom to fit again. Long-press the icon for a wildlife fact, tap the Insights heading for a discovery message, or double-tap the enlarged eagle for a gentle soaring animation. These extras work offline, respect reduced-motion settings, and never change journal data.

## Downloads and installation

Download the latest Android APK or native 64-bit Windows portable ZIP from [Releases](https://github.com/mattlfitz/Field_Notes_Releases/releases). Public downloads require no GitHub sign-in. This repository distributes application binaries and documentation only; application source remains private.

### Android
Open the APK on your Android phone using Files or Downloads. Allow installation from that source if prompted, install Fieldnotes, then disable unknown-app installation again. No account is needed.

Builds are debug-signed previews, not Play Store releases. Signing keys may differ between builds and prevent an in-place update. **Export a journal backup before changing installations.** Uninstalling or clearing app data deletes the journal and drafts.

### Windows (desktop)
Download `Fieldnotes-Windows-*.zip`, extract the archive to any folder, and run `fieldnotes.exe`. Visual C++ runtime DLLs and required Flutter engine files are bundled inside the folder. No installer is required.

On Windows, Fieldnotes opens on an interactive welcome screen: the Fieldnotes eagle glides across an illustrated forest. Lighting follows your computer's local time, with moonlight and stars at night. Select the time button to open a compact **Time of day** dialog. Enable **Override time of day** there to reveal the full-day slider and explore other lighting; disable it to return to system time. Select **Done** to close the dialog and keep your preview. The override resets when you reopen the welcome screen. Move the mouse for a gentle parallax or ask for a wildlife fact. Choose **Continue to journal** (or press Escape) when you are ready. Tick **Skip this screen next time** to go straight to the journal; you can always reopen it from the forest icon in the journal toolbar. The scene is drawn in the app, so it works entirely offline, and it respects the Windows "show animations" accessibility setting.

## Save a wildlife sighting

1. Tap **New sighting** and import photos from **Photo library**, or use **Camera**.
2. Tap **Search animal names** to search 2,570 bundled names by common or scientific name. Filter by animal group if helpful. Selecting a result fills the name, scientific name, and group, but does not confirm identification.
3. Custom names remain supported. Choose the appropriate **Animal group** and **Identification**. Use `Unknown bird` or `Unknown animal` when needed.
4. Set the observation date and location. When an imported photo contains EXIF data, its capture date is suggested unless you already chose a date, and its GPS coordinates fill the location fields only when they are empty. Check both before saving. **Use current GPS location** records your device's current location, not an older photo's location. You can also enter coordinates manually or reuse **Saved places**.
5. For sightings without coordinates, optionally choose **US state (without GPS)**.
6. Expand **More details** for scientific name, habitat, outing, animal count, observation time, and notes. Tap **Save sighting**.

The offline checklist is based on iNaturalist research-grade US/Canada observations, not a complete or authoritative fauna list. It may omit unobserved species or include introduced/escaped animals. No photographs or observation records are bundled, and there is no automatic photo identification.

## Explore your journal and map

Search and filter your collection, favorite sightings, and browse locations. Tap a sighting for details; tap its photo for fullscreen pinch zoom. Double-tap switches between fit and actual size. Android opens coordinates with a native map intent; Windows uses an HTTPS Google Maps link.

The per-photo **Photo details** card shows embedded capture time, camera and lens, focal length, shutter speed, aperture, ISO, exposure compensation, and flash status. It explicitly reports when details are not embedded or cannot be read. These details survive photo reordering, journal edits, and backup/restore.

Tap **Share sighting** while viewing a sighting. Choose a social-ready **Branded card** or **Photo + caption**, then select which details to include and inspect the live preview. Use **Copy caption**, **Save image**, or open the system share sheet. Installed apps such as Facebook, Threads, Instagram, Messages, and Mail may appear depending on the device. Precise coordinates are never offered or included, the location name and notes start off, and Fieldnotes strips EXIF metadata and hidden GPS from every exported image.

**Insights** uses persistent **Overview**, **Life lists**, and **Outings** sections. Overview presents collection, photo, and life-list totals with icons, an animal-group bar, and colored habitat bars. Open the other sections and expand the confirmed **Bird life list**, **Overall life list**, or **Outings** card to drill into sightings. Counts use entered names, not verified taxonomy; unknown names and tentative identifications do not enter life lists.

Open **Locations > Explore state map** from the prominent state-life-list card to launch the offline, zoomable **US state map** for the 48 contiguous states. The card summarizes mapped sightings and confirmed names. **Birds** is selected by default; switch to **All animals** for the overall list. State boundaries and labels show distinct confirmed-name totals. Color bands are **0, 1-5, 6-20, 21-50, and 51+**. Repeat sightings do not increase the distinct-name count.

Pinch or use zoom buttons, drag to pan, and reset zoom to fit the map. Tap a state or small-state label to open its list. Expand a name, then tap a sighting to view or edit it. **State totals and lists** is an alternative to tapping the map.

Coordinates determine a state offline and take priority over a manual state, even outside the map. No state is guessed from a place name. Missing locations and confirmed sightings outside the map are reported as unmapped. Alaska, Hawaii, DC, Canada, and territories are excluded. The same name can appear in multiple states; state totals should not be summed to calculate a national life list.

Map boundaries are public-domain U.S. Census Bureau generalized ACS 2024 data, simplified to 0.005 degrees and displayed using an Albers equal-area projection. Near-border assignments are approximate, not legal boundary determinations. The map uses no online tiles and sends no coordinates to a service.

## Protect your journal

Use **Backup & restore > Export journal** to save a ZIP with saved metadata and original-quality photos. Restore previews the backup and merges new sighting IDs without overwriting existing entries.

Backups are unencrypted, may include precise locations, exclude drafts, and are limited to 256 MB. There is no automatic cloud backup. Keep exports somewhere you trust, and retain your original photo library separately.

Animal groups and manual states persist in drafts and backups. Older entries and backups without an animal group default to Birds; edit previously saved non-bird entries manually. Older entries without coordinates or a state remain unmapped.

## Printable guide

The refreshed color quick-start PDF covers wildlife search and state maps with the current eagle branding. The detailed user guide is also available as a printable PDF. These are current text-based guides, not screenshot walkthroughs.
