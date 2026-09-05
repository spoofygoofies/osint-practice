# OSINT Exercise #009 — Write-up

**Analyst:** Bohdan
**Date of research:** 14 August 2026
**Status:** Solved. Location established and independently corroborated.

---

## 1. Task

Source material: a video posted to social media by the account @VisitTirana, captioned
as a sunset in Tirana, Albania, credited to Eriseld Myrto. Post timestamp: 10:07 PM,
16 February 2023.

Objectives: establish the time and the location of filming.

---

## 2. Key findings

| # | Finding | Confidence |
|---|---|---|
| 1 | Filming location: Tirana, Albania | High — verified |
| 2 | Camera position: 41.32683, 19.80680 | High |
| 3 | Camera bearing: approx. 254° (WSW), along street axis | High |
| 4 | Filmed after sunset, during civil twilight | High |
| 5 | Time window: 17:15–17:43 local, 16 February 2023 | Medium-high |
| 6 | Video and image metadata stripped — no embedded location or timestamp | Confirmed |

---

## 3. Methodology

### 3.1 Initial assessment

Caption and posting account both indicated Tirana. Treated as a claim requiring
verification, not as an established fact — caption text is asserted by the publisher
and is not independent evidence.

Visual character of the scene (street width, density, commercial frontage) suggested
a central or arterial location rather than a peripheral one.

### 3.2 Metadata examination

Performed before image analysis, as embedded data would render further work
unnecessary if present.

- MP4 file — examined with ExifTool. No location or timestamp data; metadata stripped.
- Accompanying JSON — no relevant fields.
- JPG stills — no EXIF of value.

**Result: negative.** Recorded as a finding: absence of metadata is itself
informative, indicating the material passed through a platform or process that
removes it.

### 3.3 Feature-based search — pharmacies

Identified pharmacy signage within the frame, later refined to two pharmacies in
sequence along the same stretch of street. Enumerated pharmacies in central Tirana
manually (approx. 10–15 candidates) and checked each against the frame.

**Result: negative at this stage.** No match found. Search continued.

### 3.4 Feature-based search — tallest buildings

Cross-referenced the tall structures visible in the background against known
high-rise buildings in Tirana.

**Result: negative.**

### 3.5 Vehicle identification

Reviewed the video repeatedly and attempted to read the route number of a bus in
frame. Resolution insufficient — number not legible.

**Result: negative.** Recorded rather than discarded.

### 3.6 Solar positioning

Approach reconsidered. Two facts were already established: the location city
(claimed) and the date (from post timestamp). Rather than deriving position from the
sun directly — which yields an unusably broad area — the sun was used as a
**directional filter** on candidate streets.

Source: timeanddate.com, sun data for Tirana, February 2023.

For 16 February 2023:

| Event | Time (local) | Azimuth |
|---|---|---|
| Sunrise | 06:34 | 106° ESE |
| Solar noon | 11:54 | 180° S |
| Sunset | 17:15 | 254° WSW |
| Civil twilight ends | 17:43 | — |

In the source video the sun sets within the corridor of the street, along its axis.
The street therefore runs on a bearing of approximately 254°/74°, within a tolerance
of roughly ±10–15° to allow for the sun being slightly off-axis.

This reduced the search from "streets in Tirana" to "streets in Tirana on a bearing
of approximately 254°", eliminating the large majority of candidates.

### 3.7 Candidate identification

A street matching the required bearing was located, presenting three further
consistent features:

- a cycle lane running centrally within the planted median
- a double row of mature trees along the median
- ornamental multi-globe street lighting

One feature did **not** match: the building stock along the candidate street was
lower and more varied than the tall, uniform residential blocks appearing in the
source video. This discrepancy was recorded as unresolved at the time rather than
disregarded.

### 3.8 Confirmation

The pharmacy identified at 3.3 was located on the candidate street, confirming the
identification through a feature independent of the solar bearing used to find it.

**Camera position:** 41.32683, 19.80680
**Camera bearing:** approx. 254° (WSW)

### 3.9 Timing

The video shows no solar disc, strong orange glow at the horizon transitioning to
pink at altitude, and sufficient ambient light for pedestrians, road markings and
vehicle colours to be distinguished without artificial illumination. Street lighting
is active but is not the principal light source.

This corresponds to **civil twilight**: after sunset (17:15), before the end of civil
twilight (17:43).

**Estimated window: 17:15–17:43 local time, 16 February 2023.**

Consistent with, though not proven by, the post timestamp of 10:07 PM the same day.

---

## 4. Limitations

- Precision beyond "civil twilight" is not achievable from a single frame. Perceived
  brightness is affected by atmospheric clarity and by camera exposure processing;
  mobile devices lift shadows substantially, rendering scenes lighter than observed.
- The date rests on the post timestamp. Publication date and filming date are
  ordinarily but not necessarily the same; no independent confirmation was obtained.
- The building-height discrepancy noted at 3.7 remains unexplained. A plausible
  cause is focal-length compression: footage shot at longer focal length flattens
  depth and causes distant structures to appear taller and closer than they are.
  Not tested.
- No metadata was available; all conclusions rest on image content and open sources.

---

## 5. Sources

| Source | Used for | Accessed |
|---|---|---|
| timeanddate.com/sun/albania/tirana (Feb 2023) | Solar azimuth, sunset, twilight phases | 12 Aug 2026 |
| Google Earth — Photo Sphere imagery | Street verification, camera position | 14 Aug 2026 |
| Google Maps — satellite | Street bearing, layout | 14 Aug 2026 |
| ExifTool | Metadata examination | 12 Aug 2026 |
| Original social media post (@VisitTirana) | Claimed location, date, credit | 12 Aug 2026 |

---

## 6. Assessment of method

**What worked:** using solar azimuth as a filter on street orientation rather than
as a positioning method in its own right; checking metadata before image analysis;
retaining the pharmacy lead after it initially failed, which ultimately provided
independent confirmation.

**What cost time:** exhaustive manual enumeration of pharmacies was attempted before
the search space had been narrowed. Sequencing the solar filter first would have
reduced the candidate set before the feature search began.

**Open question:** whether the building-height discrepancy is explained by focal
compression, by a different segment of the same street, or by an error in
identification.
