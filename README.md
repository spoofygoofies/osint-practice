# OSINT practice

Write-ups of open-source verification and geolocation exercises (Gralhix, Trace Labs weekly challenges), by Bohdan Yakovliev.

Each write-up records the method step by step, what failed as well as what worked, the sources used, the limits of the conclusion, and — where I got something wrong — what the error was and the countermeasure I adopted.

## Exercises

| Exercise | Question | Techniques | Status |
|----------|----------|------------|--------|
| [Gralhix #002](exercises/gralhix-002-writeup.md) | Train station and tallest structure in a photo | Signage, skyline matching, independent corroboration | (a) solved; (b) incorrect — errors analysed |
| [Gralhix #003](exercises/gralhix-003-writeup.md) | Where was a 2017 state-visit photo taken? | Event research, pivot from still to video, reverse image search | Solved |
| [Gralhix #004](exercises/gralhix-004-writeup.md) | Identify an island resort from an aerial photo | Reverse image search, first-party provenance | Solved; camera bearing outstanding |
| [Gralhix #009](exercises/gralhix-009-writeup.md) | Time and place of a sunset video in Tirana | Metadata check, solar azimuth as a street filter, chronolocation | Solved |
| [Trace Labs — camera](exercises/tracelabs-weekly-camera.md) | Which camera took this photo? | Earliest-instance reverse search, Wayback Machine, pivot to author | Solved |
| [Trace Labs — church](exercises/tracelabs-weekly-church.md) | Where was this church photographed? | Reverse image search, source independence | Solved; independent verification not done |

## How I work

- **Claims are not facts.** Captions, labels and posting accounts are treated as claims until something independent confirms them.
- **Corroboration must be independent.** The feature that confirms a hypothesis should not be the one that produced it; copies of one image across many sites count as one source.
- **Narrow before searching.** Use the strongest constraint first (e.g. sun azimuth to filter street orientation) before enumerating candidates.
- **Bounded answers over skipped ones.** An incomplete answer with stated limits is a result; a skipped question is not.
- **Errors are logged.** Mistakes get a named cause and a countermeasure, so they are not repeated.

## Notes

- Exercise material belongs to the respective challenge organisers (Gralhix, Trace Labs).
- Write-ups reflect my reasoning at the time of solving; corrections are added, not silently edited.
