# Trace Labs Weekly OSINT Challenge — Camera Identification

**Date:** 1 September 2026
**Task:** Identify the camera a photograph was taken with.
**Flag format:** `flag{Xxx_Xxxxx_Nx_xxxx_N}`
**Status:** Solved.

---

## Source material

Photograph of cattle and working dogs in a dusty yard. No metadata available in the
image as posted.

---

## Method

**1. Reverse image search.**
Ran the image through reverse image search and sorted results by date to surface the
earliest publication rather than the most popular one.

*Why this matters:* the earliest instance is closest to the origin. Later copies
strip metadata, crop, and lose attribution. Sorting by date instead of relevance is
the step most people skip.

**2. First result was a dead site.**
The oldest hit pointed to a site that no longer resolves.

**3. Wayback Machine.**
Retrieved the archived version of the dead page. It belonged to an Australian
photographer.

**4. Pivot to social media.**
Located the photographer's Facebook account from the archived site.

**5. Found the answer in the caption.**
The photograph appeared in a post where the photographer mentioned the camera he had
used, by name.

---

## Answer

The exact flag value was not recorded in these notes. The camera model came from the photographer's own post (see Method, step 5).

---

## Notes

**The chain worked because each step preserved provenance.** Image → earliest
publication → archived page → author → author's own statement. The final answer came
from the photographer himself, which is the strongest possible source for this
question.

**Dead links are not dead ends.** A site that no longer resolves is still readable
through the Wayback Machine. Worth treating "404" as a routing instruction rather
than a stop.

**Metadata absent ≠ information absent.** The EXIF was gone, but the camera model was
recoverable through the human who took the photo.

---

## Limitations

- The answer rests on the photographer's own claim in a social media post. Not
  independently verified against EXIF or any other source.
- Archived pages capture a moment; content may have differed before or after the
  snapshot date.

---

## Sources

| Source | Used for | Accessed |
|---|---|---|
| Reverse image search | Locating earliest publication | 1 Sep 2026 |
| web.archive.org | Retrieving dead photographer site | 1 Sep 2026 |
| Facebook post (photographer) | Camera model | 1 Sep 2026 |
