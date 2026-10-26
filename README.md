# High-Tide Detection for Coastal Monitoring in Connecticut

**Research by Hiral Choksi | Graduate Research Assistant, CIRCA | Advisor: Dr. Yaprak Onat**

## Overview

How can coastal monitoring teams identify unusually high tides across locations with different tidal behavior? I developed an automated, zone-aware framework that processes modeled water levels, identifies candidate high-tide events, connects them to monitoring locations, and compares their timing with NOAA tide predictions.

This work was completed as part of my graduate research assistantship at the Connecticut Institute for Resilience and Climate Adaptation (CIRCA), under the guidance of Dr. Yaprak Onat.

## My contribution

I independently developed the analysis workflow, including data preparation, statistical event selection, geospatial site assignment, validation, and visualizations. The project connects modeled tidal information with 16 coastal monitoring sites in Groton, New London, and Stonington.

## Approach

1. Prepare hourly predicted water levels for four coastal zones.
2. Calculate a monthly regional 90th-percentile threshold and identify high-water candidates.
3. Apply zone-specific fallback thresholds where the regional threshold yields too few candidates.
4. Assign monitoring sites to zones using geographic boundaries and check assignments against nearest-zone distances.
5. Compare selected high-tide times with the nearest NOAA-predicted high tide on the same day.

## Reported validation results

The project report gives the following comparison with NOAA **predicted** high-tide times in two zones. These are comparisons between predictions, not errors against observed flood events.

| Zone | Mean absolute timing difference | Root mean square difference | Reported bias |
|---|---:|---:|---:|
| 2 | 7.00 minutes | 7.90 minutes | +7.00 minutes |
| 3 | 3.75 minutes | 4.15 minutes | +3.75 minutes |

The report describes positive bias as the model timing earlier than the NOAA prediction. The report refers to both December 2025 and a full-year comparison; the validation period and sample size should be confirmed before publication.

![Timing comparison chart](assets/timing_comparison.png)

*Chart recreated from the report’s summary metrics. Validation period and sample size remain to be confirmed.*

## Research report

The full research report is available privately upon request.

## Tools and skills

Python · data processing · statistical thresholding · geospatial analysis · mapping · time-series comparison · data visualization

## Project status

Research conducted at CIRCA. Source code and underlying research materials are private. Contact Hiral to discuss the project.

## Acknowledgments

Project advisor: Dr. Yaprak Onat. Supported by Connecticut Sea Grant, CIRCA, and CT NERR.
