# CancerCare+

A new browser-based companion for breakthrough cancer pain records, optional comfort activities and care-team visit summaries. Plain HTML, CSS and JavaScript; no packages, build step, secrets or external font requests.

## Run and publish
Open index.html in a modern browser, or serve this folder with a static HTTP server. For GitHub Pages, upload these files at the repository root, then choose Settings > Pages > Deploy from a branch > main > / (root) > Save. The app works under a repository subpath.

## Research foundation
Adapted from the user-provided thesis **Designing a Mobile Application for Breakthrough Cancer Pain Assessment and Personalized Pain Relief**, Julaluck Tantipaswasin, Faculty of Medical Technology, Mahidol University, academic year 2566; advisor Dr. Nutta Homdee, and the accompanying presentation dated December 12, 2023.

Source documents informed these requirements:
- Thesis PDF p. 15 (printed p. 4): intensity, location, character, duration, triggers, daily life and medication timing.
- Thesis PDF pp. 24, 33–39: patient/caregiver audience, assessment, personalized suggestions and visual summaries.
- Thesis PDF p. 37 (printed p. 26): anxiety-to-meditation example.
- Thesis PDF pp. 40–41: limitations and need for clinician review and usability evaluation.
- Presentation pp. 11, 33–36: assessment parameters, medication records and core feature set.

The implementation is independently authored. No PDFs, screenshots, student identifiers, signatures, or original research assets are included in this repository. This is not the original FlutterFlow code, an endorsement by the university, or a clinically validated reproduction.

## Implemented
Six assessment areas: intensity/timing; location/character; pattern/triggers; medication record; symptoms/daily life; comfort activity/notes. Includes patient/caregiver attribution, event timestamps, follow-up scores, diary filtering, per-event plot, seven-day summary, CSV export, print visit summary, care-plan notes, optional timed comfort exercises, and explicit local-data deletion.

### Transparent personalization
The latest record with anxiety value 2 or 3 highlights quiet breathing. Otherwise a user-selected preference is highlighted, or all activities have equal priority. Thresholds are implementation choices, not a validated research algorithm. The research's full intervention dataset and clinical decision rules were not available as machine-readable resources. Suggestions are optional coping support; no treatment efficacy or causal effect is inferred from follow-up scores.

### Deliberate scope
No diagnostic classification, medication recommendations, dose calculations, authentication, cloud database, provider portal, notifications, emergency monitoring, or automated clinical alerts. Unlike the research prototype's Firebase/authentication architecture, this version is a static, browser-local prototype. A real clinical deployment requires separate clinical, security, accessibility, usability and privacy review.

## Clinical education checked October 21, 2026
- NCI, Pain and Cancer Treatment: https://www.cancer.gov/about-cancer/treatment/side-effects/pain
- NCI, Meditation and Relaxation: https://www.cancer.gov/about-cancer/coping/feelings/relaxation
- American Cancer Society, Non-medical Ways to Manage Pain: https://www.cancer.org/cancer/side-effects/pain/cancer-pain/non-medical-treatments-for-cancer-pain.html

Optional comfort activities complement the prescribed plan. New/different or severe reported pain shows care-team contact guidance, not a clinical triage result. No local emergency number is guessed.

## Data and security
Entries and the plan are stored as unencrypted JSON in localStorage under cancercare-plus-v1, scoped to this browser profile and origin. People using the same profile can access records. There is no transmission, login, cloud sync or automatic backup. External education links navigate to third-party services only when clicked. Clearing site data removes records; export before changing devices. No sample patient records ship with the app. Do not commit diary exports or real patient information.

Free-text output is HTML-escaped. CSV cells are quoted and formula-leading content is neutralized. Storage failures retain the form; unreadable prior data is not silently overwritten. Event dates in the future are rejected. The chart shows only recorded observations, without interpolation across missing time.

## Files
index.html — accessible screens and dialogs
styles.css — responsive styling, reduced-motion and print support
app.js — persistence, summaries, personalization and interactions

## Verification
JavaScript syntax and targeted logic checks cover filtering, averages, personalization, HTML escaping, CSV serialization and storage failure handling. Browser verification is documented in the delivery message. Not clinically validated.
