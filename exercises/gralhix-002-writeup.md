# OSINT Exercise #002 — Write-up

**Analyst:** Bohdan
**Date of research:** 14 August 2026
**Time spent:** ~30 minutes
**Status:** Task (a) solved and verified. Task (b) partially incorrect — see Corrections.

---

## 1. Task

Source material: a photograph shared on social media, depicting a train station.

Questions:
- a) Name of the train station.
- b) Name and height of the tallest structure visible in the photo.

---

## 2. Key findings

| # | Finding | Confidence |
|---|---|---|
| a | Flinders Street Station, Melbourne, Victoria, Australia | High — verified |
| b | Initial answer incorrect. See Corrections. | — |

---

## 3. Methodology — Task (a)

**Initial lead.** Street name legible on signage within the frame.

**Hypothesis.** Search engine query on the street name returned results pointing to
Australia.

**Hypothesis held as provisional.** Street names are frequently duplicated across
cities and countries; a name match alone is not sufficient for identification. The
hypothesis was therefore treated as unconfirmed pending independent corroboration.

**Verification.** Satellite and street-level imagery consulted for the candidate
location. The relative positions and skyline profile of three high-rise buildings
visible in the background of the original photograph matched the candidate site.

**Corroboration basis.** The confirming feature (building arrangement) was not used
in forming the hypothesis, and is therefore independent of it.

**Result.** Flinders Street Station, Melbourne — confirmed.

---

## 4. Methodology — Task (b)

**Approach taken.** Visually identified the apparently tallest building in frame,
read the tenant signage on its facade, and searched on that basis.

**Object reached.** 60 City Road, Southbank VIC 3006, Australia — a tower within the
Southgate commercial complex, commonly referred to by tenant-derived branding.

**Height.** Open sources returned a range of approximately 110–113 m. No authoritative
primary source located. Discrepancy likely reflects differing measurement bases
(roof height / architectural height / height to tip).

**Outcome:** incorrect. See below.

---

## 5. Corrections and errors

Three distinct errors were made in Task (b). All are systemic rather than incidental.

**5.1 — Category substitution.**
The brief asked for the tallest *structure*. This was read as the tallest *building*.
A pole/mast on the left of the frame was consequently filtered out at the perception
stage and never considered as a candidate.

*Countermeasure adopted:* read the brief literally, noun by noun, and check for
substitution of the stated term with a more familiar one.

**5.2 — Perspective error.**
Objects at differing distances from the camera cannot be compared for height by
apparent size, as angular size decreases with distance. A building further from the
camera appeared shorter than a nearer one and was discounted; it was in fact taller.

*Countermeasure adopted:* determine camera position and bearing, establish object
distances from mapping data, and rank heights from published figures only — never
from the image.

**5.3 — Tenant signage treated as identification.**
Facade branding identifies an occupant at the time of capture, not the building.
Tenants change; the structure does not. Identification should proceed from signage
to official building name and street address, and only then to technical data.

*Countermeasure adopted:* the address is the identifier, not the name. (Direct
analogue in corporate research: the registration number is the identifier, not the
company name.)

---

## 6. Limitations

- Task (b) was not resolved correctly and the correct structure was identified only
  after consulting the published walkthrough.
- Camera position and bearing were not recorded during the exercise.
- No definitive height source (e.g. CTBUH) was consulted; the 110–113 m range rests
  on secondary aggregators of unverified provenance.

---

## 7. Sources

- Google Maps / satellite and street-level imagery — accessed 14 August 2026
- Open web search on street signage — accessed 14 August 2026
- Gralhix published walkthrough (consulted after answers were recorded)

---

## 8. Lessons carried forward

1. A name is not an identifier. An address or registration number is.
2. An incomplete answer with stated bounds is a result. A skipped answer is not.
3. Read the brief literally; watch for silent substitution of terms.
4. Never compare heights across depth by eye.
