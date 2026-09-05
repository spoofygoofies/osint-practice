# OSINT Exercise #003 — Meeting Location

**Analyst:** Bohdan  
**Status:** Solved.

---

## Task

In April 2017, Mohamed Abdullahi Farmaajo, then President of Somalia, visited Turkey.
A news agency published a photograph of him shaking hands with President Recep Tayyip
Erdoğan. The article did not disclose where the photograph was taken.

Objective: identify the location.

---

## Answer

**Presidential Complex (Cumhurbaşkanlığı Külliyesi), Ankara, Turkey**

Coordinates: 39.9308°N, 32.7989°E

---

## Method

**1. Establish what is already known.**
The caption gives the two individuals and the approximate date. Both are public
figures and the visit was a state occasion, so it will be documented.

**2. Search the event, not the image.**
Open-source search on the visit established that the meeting took place in Ankara.
This narrows the problem from "somewhere in Turkey" to one city before any image
analysis begins.

**3. Pivot from still to video.**
The original photograph is framed tightly on the two men in a doorway — very little
of the building is visible. Located news footage of the same event on Getty Images,
which shows the building in full at 4:07.

*This is the key step.* The still photo did not contain enough of the building to
identify it. Rather than trying to extract more from an image that does not hold the
answer, the search moved to different coverage of the same event.

**4. Reverse image search on the building.**
Ran the video frame through reverse image search. Returned the Presidential Complex,
with coordinates.

**5. Attempted satellite verification.**
Google Earth imagery of the site is obscured. Coordinates taken from the reference
entry instead.

---

## Notes

**Different coverage of the same event is a distinct source, not a duplicate.** A
press still, agency video, and official photography of one occasion frame different
things. When the material in hand does not contain the answer, look for other
material from the same moment before concluding the answer is unobtainable.

**The obscured satellite imagery is itself informative.** Sensitive government sites
are frequently blurred or degraded in commercial satellite products. Encountering
this at a candidate location is weak supporting evidence that the identification is
correct, and is worth recording rather than treating purely as an obstacle.

---

## Note on verification

Final confidence rested partly on the exercise itself appearing in search results for
the identified location.

This is circular: the exercise appearing in results confirms that others have
searched the same terms, not that the answer is correct. It should not carry weight
in the conclusion.

The identification is sound on its own merits — the building in the video frame
matches the Presidential Complex, and the event is independently documented as having
taken place in Ankara. Better verification would be a direct visual match between the
video frame and reference photography of the complex: roofline, column spacing,
entrance geometry.

---

## Limitations

- Satellite verification not possible; imagery of the site is obscured.
- Coordinates taken from a reference entry rather than measured.
- Camera position and bearing not established.

---

## Sources

| Source | Used for | Accessed |
|---|---|---|
| Open web search — Farmaajo Turkey visit April 2017 | Establishing city | — |
| Getty Images news footage (ref. 673667442) | Building visible at 4:07 | — |
| Reverse image search | Building identification | — |
| Wikipedia — Presidential Complex | Coordinates | — |
