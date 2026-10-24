# UI preview

Actual screenshots of the current web application, captured October 23, 2026. The app is shown with no saved patient records. The assessment's pain slider is its default form value, not a patient observation. Screenshots show one responsive viewport; layouts adapt to screen size.

## My day

The overview provides entry points to recording pain, the latest record, seven-day average and comfort activities.

![My day overview](images/ui-overview.webp)

## Record pain

Six assessment groups cover intensity and timing, location and character, pattern and triggers, medication records, symptoms and daily life, and comfort activities and notes.

![Pain assessment form](images/ui-assessment.webp)

## Find comfort

Optional breathing, imagery and music/distraction activities. The reason for highlighting an activity appears above the cards when the user's records or preferences apply.

![Comfort activity library](images/ui-comfort.webp)

## My insights

The empty diary is shown intentionally. With records, this screen displays individual pain observations, period summaries, follow-up scores and export controls.

![Insights and diary empty state](images/ui-insights.webp)

## Screen map

```mermaid
flowchart LR
    A[My day] --> B[Record pain]
    B --> C[Saved record]
    C --> D[Find comfort]
    C --> E[My insights]
    E --> F[Follow-up score]
    E --> G[CSV / print]
    A --> H[Care plan]
    H --> D
    I[Care-team support] --> H
```

## Refreshing screenshots

Serve the repository root on a local HTTP server, open it with a clean browser profile, and capture the `#home`, `#record`, `#comfort`, and `#insights` screens. Replace the corresponding WebP images in `docs/images/`. Never publish screenshots containing real patient information.