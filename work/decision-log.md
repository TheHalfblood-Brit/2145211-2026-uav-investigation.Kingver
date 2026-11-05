# My evidence and decision log

Keep this file free of names, IDs, grades and private assessment answers. Use it for practice reasoning only. Duplicate the cycle section as needed.

## Cycle 1
- Released package and version:
- Earlier packages available:
- My initial prediction and reason:
- Exact files and test IDs used:
- Relevant test conditions and why they match the mission:
- Evidence excluded or qualified, and why:
- Analysis or plot used, with units:
- One calculation or observation I checked myself:
- AI suggestion I accepted or rejected, and my reason:
- Current recommendation:
- What changed my mind, or why it did not change:
- Remaining unknown and most useful next check:

## Cycle 2
- Released package and version: ENERGY, NEW-SYNTHETIC-20261105-R2. Released on 5 November 2026.

- Earlier packages available: DATA, in evidence/04_information_quality/. ENERGY is now also released.

- Initial prediction and reason: Initially favoured COVERAGE over ENERGY because coverage efficiency directly determines whether the UAV can map the required 1.60 km². ENERGY was still important for estimating available flight time.

- Exact files and test IDs used:
- E01_telemetry.csv
- E02_telemetry.csv
- E03_telemetry.csv
- E04_telemetry.csv
- E05_telemetry.csv
- E06_telemetry.csv
- test_conditions.csv
- README.md
- Test IDs: E01–E06.
- Relevant test conditions and why they match the mission:
- E01 and E02: 600 g payload, 3 m/s wind, CASE-A. These match the mission's nominal payload and wind conditions, making them the best baseline tests.
- E03: 600 g payload, 6 m/s wind. Useful for examining a higher-wind condition.
- E04: 300 g payload, 3 m/s wind. Useful for examining a lower payload.
- E06: 900 g payload, 3 m/s wind. Useful for examining a higher payload.
- E05: 600 g payload, 3 m/s wind, but only a 600-second record.
- Evidence excluded or qualified, and why:
- E05 was qualified because it covers only 10 minutes, unlike the 20-minute complete intervals. Its average power is usable for that interval, but its total energy cannot be compared directly with the complete runs.
- E03, E04 and E06 were not used as nominal baseline tests because their wind or payload differs from the mission conditions.
- All results were qualified because the package contains synthetic teaching data, not validated aircraft performance measurements.
- Analysis or plot used, with units:
- Power-time plot, with time in seconds and electrical power in watts (W).
- Average-power comparison across all six tests, in watts (W).
- Energy calculated by trapezoidal integration, in watt-hours (Wh).
- Formula: \(P=V\times I\).
- One calculation or observation checked:
- E01 average power = 450 W.
- Duration = 1,200 seconds.
- Energy = \(450\times1,200/3,600=150\text{ Wh}\).
- This agrees with the calculated E01 energy of 150 Wh.
- Suggestion accepted or rejected, and reason: Accepted the suggestion to compare E01 and E02 first. They have matching test conditions, so their difference helps assess variation between repeat runs before interpreting the other tests.

- Current recommendation: Treat E01 and E02 as the nominal energy baseline. Their mean average power is 456 W. Using the mission's 300 Wh usable energy gives an estimated total operating time of approximately 39.5 minutes at that power. If the 10-minute nonproductive period consumes energy at the same average rate, approximately 29.5 minutes remain for mapping. This is a conditional estimate, not flight approval.

- What changed your mind, or why it did not change: ENERGY provides useful evidence about the likely operating-time budget, but it has not displaced COVERAGE as a priority. The mission must produce a map of the full 1.60 km², so sufficient flight time alone does not establish mission feasibility.

- Remaining unknown and most useful next check: The most useful next check is to obtain and analyse the COVERAGE package. We need to determine whether the UAV can map 1.60 km² within the estimated productive flight time. We also need to justify whether using the mapping-phase average power during the nonproductive 10 minutes is reasonable.

Overall decision: ENERGY provides a preliminary estimate of the available mapping time, but COVERAGE evidence is still needed to assess whether the mission can achieve its mapping objective. The synthetic nature of the energy data and the unverified overhead-power assumption remain important limitations.

## Cycle 3
Use the same fields. Show what passes, fails or remains unknown under the instructor's changed condition. Do not erase an earlier result just because the mission changed.
