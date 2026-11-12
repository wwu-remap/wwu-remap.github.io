# ReMAP

**Remote Monitoring Application**

!!! note "Zusammenfassung"

    Die Smartphone-App ReMAP (Remote Monitoring Application) ist eine Anwendung für Android und iOS, die für psychiatrische Forschungszwecke am Institut für Translationale Psychiatrie der Universität Münster entwickelt und eingesetzt wird.

    Derzeit erfassen wir zahlreiche Parameter passiv, darunter die Anzahl der Schritte, die zurückgelegte Strecke, die Geolokalisierung (GPS) und auf dem iPhone die dreidimensionale Beschleunigung.
    Darüber hinaus werden regelmäßig aktive Fragebögen durchgeführt, einschließlich der Bewertung von Affektivität, Schlafqualität und depressiven Symptomen mit dem Beck Depression Inventory (BDI).
    Außerdem erfassen wir je nach Studie Stimmproben, in denen die Teilnehmenden berichten, wie es ihnen geht.
    Welche Daten erhoben werden und wie häufig, hängt von der jeweiligen Studie und von den erteilten Berechtigungen ab.

    Die Daten werden pseudonymisiert und ausschließlich für die wissenschaftliche Forschung verarbeitet.
    Einzelheiten stehen in den [Datenschutzhinweisen](privacy-policy.md); wie Teilnehmende die Löschung ihres Kontos und ihrer Daten anfragen, beschreibt die Seite [Konto und Daten löschen](account-deletion.md).

ReMAP is a smartphone application for continuous assessment of affective symptoms and activity in psychiatric research. Developed at the [Institute for Translational Psychiatry](https://www.medizin.uni-muenster.de/itp/), University of Münster, Germany, ReMAP combines **active** self-reports with **passive** sensor data to build high-resolution longitudinal profiles of mood, behavior, and daily functioning.

The app runs natively on **iOS** and **Android** and is used in longitudinal studies, where it can complement assessments such as neuroimaging, genetics, neuropsychological tests, and clinical interviews.

---

## Data Collection

ReMAP collects two complementary streams of data. **Active data** requires participant involvement and captures subjective experience. **Passive data** is recorded in the background, providing objective behavioral markers with no user effort. Which tasks and data types are part of an assessment, and how often tasks are due, depends on the study.

<div style="display: flex; gap: 1em; flex-wrap: wrap; margin: 1.5em 0;">
<div style="flex: 1; min-width: 280px; border: 2px solid #3f51b5; border-radius: 8px; padding: 1.2em; background: #f5f5ff;">
<div style="text-align: center; font-weight: bold; font-size: 1.1em; color: #3f51b5; margin-bottom: 0.5em;">Active Data</div>
<div style="text-align: center; color: #666; font-size: 0.85em; margin-bottom: 1em;">User-initiated &middot; Reminders by push notification</div>
<div style="border-left: 3px solid #3f51b5; padding-left: 0.8em; margin-bottom: 0.6em;">
<strong>BDI Questionnaire</strong><br>
<span style="font-size: 0.9em;">21-item Beck Depression Inventory</span>
</div>
<div style="border-left: 3px solid #3f51b5; padding-left: 0.8em; margin-bottom: 0.6em;">
<strong>Mood Rating</strong><br>
<span style="font-size: 0.9em;">Single item, scale 1&ndash;10</span>
</div>
<div style="border-left: 3px solid #3f51b5; padding-left: 0.8em; margin-bottom: 0.6em;">
<strong>Sleep</strong><br>
<span style="font-size: 0.9em;">Short items on sleep duration and quality</span>
</div>
<div style="border-left: 3px solid #3f51b5; padding-left: 0.8em;">
<strong>Voice Diary</strong><br>
<span style="font-size: 0.9em;">1&ndash;3 min free-form recording, depending on the study</span>
</div>
</div>
<div style="flex: 1; min-width: 280px; border: 2px solid #4caf50; border-radius: 8px; padding: 1.2em; background: #f5fff5;">
<div style="text-align: center; font-weight: bold; font-size: 1.1em; color: #4caf50; margin-bottom: 0.5em;">Passive Data</div>
<div style="text-align: center; color: #666; font-size: 0.85em; margin-bottom: 1em;">Background &middot; No user effort</div>
<div style="border-left: 3px solid #4caf50; padding-left: 0.8em; margin-bottom: 0.6em;">
<strong>Activity</strong><br>
<span style="font-size: 0.9em;">Steps, distance, walking speed, step length, stand time</span>
</div>
<div style="border-left: 3px solid #4caf50; padding-left: 0.8em; margin-bottom: 0.6em;">
<strong>Heart</strong><br>
<span style="font-size: 0.9em;">HR, HRV, resting HR, walking HR</span>
</div>
<div style="border-left: 3px solid #4caf50; padding-left: 0.8em; margin-bottom: 0.6em;">
<strong>Environment</strong><br>
<span style="font-size: 0.9em;">Audio exposure (iOS only), GPS location</span>
</div>
<div style="border-left: 3px solid #4caf50; padding-left: 0.8em;">
<strong>Motion</strong><br>
<span style="font-size: 0.9em;">Accelerometer (x, y, z), iOS only</span>
</div>
</div>
</div>

---

## Active Data

Active data captures the participant's subjective experience. The app reminds participants of pending tasks with push notifications, and participants choose when to respond. Which tasks a participant receives, and whether they are due daily, weekly or at longer intervals, depends on the study. The study team manages tasks and their schedules centrally, so they can be adjusted without an app update.

!!! info "Surveys"

    The questionnaires depend on the study. Typical examples:

    - **BDI (Beck Depression Inventory)** -- Full 21-item digital questionnaire on depressive symptoms.
    - **Mood rating** -- Single-item self-report ("How is your mood today?") on a scale from 1 ("very bad") to 10 ("very good").
    - **Sleep** -- Short items on sleep duration and sleep quality.

    Questionnaire answers are checked automatically for indications of suicidal intent. In that case the app asks the participant to seek help, and the study team contacts the participant by phone. Voice samples are not screened in this way.

    No partial events are stored -- if a participant cancels a survey, the answers are discarded.

!!! info "Voice Samples"

    Participants record a **1--3 minute** free-form voice diary in which they report how they are doing. During the recording, the app shows the sound level as visual feedback to support recording quality. Recordings are transmitted in encrypted form as soon as an internet connection is available, including over mobile data. Whether voice samples are part of the assessment depends on the study.

---

## Passive Data

Passive data is collected in the background without user interaction. This provides activity profiles with high temporal resolution while minimizing participant burden and attrition. Health metrics are retrieved from **Apple HealthKit** (iOS) or **Health Connect** (Android). Which data is collected depends on the study and on the permissions the participant grants.

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
    | Heart rate variability | ms | iOS (SDNN), Android (RMSSD) |
    | Resting heart rate | bpm | iOS, Android |
    | Walking heart rate average | bpm | iOS only |

=== "Environment & Location"

    | Metric | Unit | Platform |
    |--------|------|----------|
    | Environmental audio exposure | dB(A) | iOS only |
    | GPS location | lat/lon | iOS, Android |

=== "Accelerometer"

    Acceleration data is collected in the background on iOS only.

!!! info "Additional data starting with app version 2.3.0"

    Starting with app version 2.3.0, a study can enable further passive data types. What is collected depends on the study and on the permissions granted.

    - **Further sensors** -- steps and activity type, places visited, barometric pressure, network type with a non-reversible Wi-Fi identifier, battery and device status, screen brightness and time zone, ringer mode and Do Not Disturb or Focus, the number of nearby Bluetooth devices without names or addresses, and ambient sound level as a level value without any audio recording.
    - **Android only** -- when the screen was switched on, switched off and unlocked, how long other apps were used per hour (app names, no content), sleep phases detected by the phone, and ambient light.
    - **Use of the app itself** -- when a reminder arrived, when a task was opened or finished, and when and for how long ReMAP was open; no screen contents or input.

    The complete list is part of the [privacy notice](privacy-policy.md) (in German).

---

## Architecture

The app works in the background and collects passive sensor data without active participant involvement. Data is first stored on the device and transferred in encrypted form to the ReMAP server once an internet connection is available. Tasks and their reminder schedules are managed centrally, so a study can be adjusted on both platforms without an app update.

Health and activity data is read from **Apple HealthKit** (iOS) or **Health Connect** (Android) once the participant has granted access. Location and motion access are handled through standard OS-level permissions. Participants can withdraw permissions at any time in the device settings.

---

## Privacy and Data Deletion

Study data is processed in pseudonymised form and used exclusively for scientific research, on the basis of the participant's voluntary consent. Participation can be ended at any time without giving reasons.

- [Datenschutzhinweise](privacy-policy.md) -- the privacy notice (in German): which data is collected and why, pseudonymisation, the optional email backup for switching phones, retention and participants' rights.
- [Konto und Daten löschen](account-deletion.md) -- how participants request the deletion of their account and study data, in the app or by email (German, with an English summary).

---

## References

Emden, D., Goltermann, J., Dannlowski, U., Hahn, T., & Opel, N. (2021). Technical feasibility and adherence of the Remote Monitoring Application (ReMAP) for the assessment of affective symptoms. *Journal of Affective Disorders*, 294, 652--660. [doi:10.1016/j.jad.2021.07.030](https://doi.org/10.1016/j.jad.2021.07.030)

Goltermann, J., Emden, D., Leehr, E.J., Dohm, K., Redlich, R., Dannlowski, U., Hahn, T., & Opel, N. (2021). Smartphone-Based Self-Reports of Depressive Symptoms Using the Remote Monitoring Application (ReMAP): Interformat Validation Study. *JMIR Mental Health*, 8(1), e24333. [doi:10.2196/24333](https://doi.org/10.2196/24333)
