# Sensor Log File Problem

*A compact temperature log must survive a write–append–read round trip as one exact filesystem artifact.*

*Estimated prepared-cell time: 10–15 minutes.*

## Setting

Three sensor readings arrive five minutes apart. The first two are written together, and the third arrives later and must be appended.

## Analytical Question

The file workflow must preserve the header and row order, then recover the reading count and basic temperature range from the saved text.

## Given Data

| Timestamp | Temperature (°C) | Arrival Stage |
| --- | ---: | --- |
| 2026-03-02T09:00 | 21.4 | Initial write |
| 2026-03-02T09:05 | 21.8 | Initial write |
| 2026-03-02T09:10 | 22.1 | Append |

## Constraints

The case must construct paths with `Path`, write only under the case's `output/` directory, declare UTF-8 explicitly, and use a focused `with ... as` block for the append operation. Repeated execution must replace the same exact file rather than create additional artifacts.

## Required Output

The executed notebook must show `output/sensor_log.csv`, its complete text, and the recovered count, minimum, maximum, and mean. The practice notebook applies Paths and Filesystem State and Text and Structured File Round Trips to one bounded file effect.
