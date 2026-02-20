# ReMAP

**Remote Monitoring Application in Psychiatry**

ReMAP is a smartphone application for continuous assessment of affective symptoms and activity in psychiatric research. Developed at the [Institute for Translational Psychiatry](https://www.medizin.uni-muenster.de/itp/), University of Munster, Germany, ReMAP combines **active** self-reports with **passive** sensor data to build high-resolution longitudinal profiles of mood, behavior, and daily functioning.

The app runs natively on **iOS** and **Android** and serves as an add-on assessment for ongoing longitudinal deep phenotyping studies, complementing neuroimaging, genetics, microbiome data, neuropsychological tests, and clinical interviews.

---

## Data Collection

ReMAP collects two complementary streams of data. **Active data** requires participant involvement and captures subjective experience. **Passive data** is recorded continuously in the background, providing objective behavioral markers with no user effort.

<div style="display: flex; gap: 1em; flex-wrap: wrap; margin: 1.5em 0;">
<div style="flex: 1; min-width: 280px; border: 2px solid #3f51b5; border-radius: 8px; padding: 1.2em; background: #f5f5ff;">
<div style="text-align: center; font-weight: bold; font-size: 1.1em; color: #3f51b5; margin-bottom: 0.5em;">Active Data</div>
<div style="text-align: center; color: #666; font-size: 0.85em; margin-bottom: 1em;">User-initiated &middot; Weekly prompts</div>
<div style="border-left: 3px solid #3f51b5; padding-left: 0.8em; margin-bottom: 0.6em;">
<strong>BDI Questionnaire</strong><br>
<span style="font-size: 0.9em;">21-item Beck Depression Inventory, every 2 weeks</span>
</div>
<div style="border-left: 3px solid #3f51b5; padding-left: 0.8em; margin-bottom: 0.6em;">
<strong>Mood Rating</strong><br>
<span style="font-size: 0.9em;">Single item, scale 1&ndash;10, weekly</span>
</div>
<div style="border-left: 3px solid #3f51b5; padding-left: 0.8em; margin-bottom: 0.6em;">
<strong>Sleep Duration</strong><br>
<span style="font-size: 0.9em;">Single item, 0&ndash;13 hours, weekly</span>
</div>
<div style="border-left: 3px solid #3f51b5; padding-left: 0.8em;">
<strong>Voice Diary</strong><br>
<span style="font-size: 0.9em;">1&ndash;3 min free-form recording, weekly</span>
</div>
</div>
<div style="flex: 1; min-width: 280px; border: 2px solid #4caf50; border-radius: 8px; padding: 1.2em; background: #f5fff5;">
<div style="text-align: center; font-weight: bold; font-size: 1.1em; color: #4caf50; margin-bottom: 0.5em;">Passive Data</div>
<div style="text-align: center; color: #666; font-size: 0.85em; margin-bottom: 1em;">Background &middot; Continuous</div>
<div style="border-left: 3px solid #4caf50; padding-left: 0.8em; margin-bottom: 0.6em;">
<strong>Activity</strong><br>
<span style="font-size: 0.9em;">Steps, distance, walking speed, step length, stand time</span>
</div>
<div style="border-left: 3px solid #4caf50; padding-left: 0.8em; margin-bottom: 0.6em;">
<strong>Heart</strong><br>
<span style="font-size: 0.9em;">HR, HRV (SDNN), resting HR, walking HR</span>
</div>
<div style="border-left: 3px solid #4caf50; padding-left: 0.8em; margin-bottom: 0.6em;">
<strong>Environment</strong><br>
<span style="font-size: 0.9em;">Audio exposure, GPS location</span>
</div>
<div style="border-left: 3px solid #4caf50; padding-left: 0.8em;">
<strong>Motion</strong><br>
<span style="font-size: 0.9em;">Accelerometer (x, y, z), aggregated per 4h</span>
</div>
</div>
</div>

---

## Active Data

Active data captures the participant's subjective experience. The app sends weekly push notifications during daytime, with a two-day variance window. Participants choose when to respond, and all surveys function fully offline. Surveys are defined as configuration files on the ReMAP backend and can be modified at runtime without requiring an app update.

!!! info "Surveys"

    - **BDI (Beck Depression Inventory)** -- Full 21-item digital questionnaire administered every two weeks. Includes a safety protocol: participants scoring 2 or higher on the suicide item are instructed to contact their local Department of Psychiatry.
    - **Mood rating** -- Single-item self-report ("How is your mood today?") on a scale from 1 ("very bad") to 10 ("very good"), prompted weekly.
    - **Sleep duration** -- Single-item question ("How many hours did you sleep last night?") on a scale from 0 to 13 hours, prompted weekly.

    No partial events are stored -- if a participant cancels a survey, the answers are discarded.

!!! info "Voice Samples"

    Participants record a **1--3 minute** free-form voice diary about their well-being, responding to the prompt "How did you feel last week?". The app monitors background noise and sound levels in real-time, providing visual feedback to ensure recording quality. Audio is stored in encrypted MP4 format and transmitted when WiFi is available.

    Built with Apple ResearchKit (iOS) and [SurveyKit](https://github.com/quickbirdstudios/SurveyKit) (Android).

---

## Passive Data

Passive data is collected continuously in the background without user interaction. This provides high temporal resolution activity profiles while minimizing participant burden and attrition. Health metrics are retrieved from **Apple HealthKit** (iOS) or **Health Connect** (Android).

=== "Activity"

    | Metric | Unit | Platform |
    |--------|------|----------|
    | Step count | count | iOS, Android |
    | Distance | meters | iOS, Android |
    | Walking speed | m/s | iOS only |
    | Walking step length | meters | iOS only |
    | Stand time | minutes | iOS only |

=== "Heart"

    | Metric | Unit | Platform |
    |--------|------|----------|
    | Heart rate | bpm | iOS, Android |
    | Heart rate variability (SDNN) | ms | iOS, Android |
    | Resting heart rate | bpm | iOS, Android |
    | Walking heart rate average | bpm | iOS only |

=== "Environment & Location"

    | Metric | Unit | Platform |
    |--------|------|----------|
    | Environmental audio exposure | dB(A) | iOS only |
    | GPS location | lat/lon | iOS, Android |

=== "Accelerometer"

    Acceleration data is collected in the background on both iOS and Android.

---

## Architecture

The app works in the background and collects passive sensor data without active participant involvement. Data is encrypted on-device and transferred to the ReMAP server. Surveys and their notification schedules are managed centrally through the backend, enabling runtime configuration changes across both platforms.

ReMAP requires access to **Apple HealthKit** (iOS) or **Health Connect** (Android) for health and activity data. GPS and accelerometer access are handled through standard OS-level permissions.

---

## References

Emden, D., Goltermann, J., Dannlowski, U., Hahn, T., & Opel, N. (2021). Technical feasibility and adherence of the Remote Monitoring Application in Psychiatry (ReMAP) for the assessment of affective symptoms. *Journal of Affective Disorders*, 294, 652--660. [doi:10.1016/j.jad.2021.07.030](https://doi.org/10.1016/j.jad.2021.07.030)

Goltermann, J., Emden, D., Leehr, E.J., Dohm, K., Redlich, R., Dannlowski, U., Hahn, T., & Opel, N. (2021). Smartphone-Based Self-Reports of Depressive Symptoms Using the Remote Monitoring Application in Psychiatry (ReMAP): Interformat Validation Study. *JMIR Mental Health*, 8(1), e24333. [doi:10.2196/24333](https://doi.org/10.2196/24333)
