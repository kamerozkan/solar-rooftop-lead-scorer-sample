# Data Notice

## Purpose

This repository is a technical sample for the [Solar Panel Rooftop Lead Scorer Actor](https://apify.com/kamerozkan/solar-rooftop-lead-scorer). It contains one exact public Example Task input, one inspected live-run input, one current-schema coordinate recipe, two privacy-minimized live provider result projections, and one actual illustrative demo result.

The Actor and this repository are independently maintained. They are not affiliated with, sponsored by, or endorsed by Google, the European Commission, the U.S. Census Bureau, any utility, solar installer, property owner, or address represented in a sample.

## Audit snapshot

The following state was verified through the public Apify API, public Store page, public build records, and authenticated owner console on 2026-07-29, with current build and smoke status refreshed on 2026-08-02:

| Item | Verified value |
|---|---|
| Actor | `kamerozkan/solar-rooftop-lead-scorer` |
| Actor ID | `soaKkDxBAEDY4JSlb` |
| Public | `true` |
| Current latest build | `0.2.13`, build ID `gbdvjcIE50T2LDgXc`, status `SUCCEEDED` |
| Saved tasks | 4 total, 1 public |
| Public Example Task | `wPS3YcoBLSW59YWTg`, slug `preview-rooftop-solar-scoring-with-a-free-demo` |
| Inspected public-task run | `13JAmEk7QtEaEVLsx`, build `0.1.11` |
| Public-task dataset | `p39ebTaNt566cmUh5`, 1 illustrative record |
| Inspected live run | `swIS6orxhytWO51hj`, build `0.2.6`, 2 records |
| Inspected live dataset | `4f7TNIzjbDSneMze5` |
| Current keyless smoke | `wgod85L5wWai35y35`, build `0.2.13`, 1 qualified `OPEN_DATA` record |

Build `0.2.13` completed successfully. The 2026-08-02 smoke produced one qualified Berlin `OPEN_DATA` record and triggered one `property-analyzed` event plus one Actor-start event. The repository's two checked-in live projections still come from build `0.2.6` and remain labeled with that provenance.

## Input provenance

- [`01_public_demo_example_task_input.json`](01_public_demo_example_task_input.json) is the exact input of the sole public Example Task at audit time. `demoMode: true` means it does not perform a real property or provider assessment.
- [`02_verified_open_data_address_run_input.json`](02_verified_open_data_address_run_input.json) reproduces the complete non-secret configuration of successful run `swIS6orxhytWO51hj`.
- [`03_public_berlin_coordinate_recipe_input.json`](03_public_berlin_coordinate_recipe_input.json) is the keyless quick-start recipe published in the current Actor README and accepted by the current input schema. It was verified successfully in run `wgod85L5wWai35y35` on build `0.2.13` during the 2026-08-02 refresh.

The two addresses in inputs 01 and 02 are public corporate campuses or landmarks. No private residential address is included.

## Output provenance

[`01_live_no_geocode_match_output.json`](01_live_no_geocode_match_output.json) and [`02_live_open_data_qualified_output.json`](02_live_open_data_qualified_output.json) are privacy-minimized projections of the two records in dataset `4f7TNIzjbDSneMze5`, produced by successful run `swIS6orxhytWO51hj` on build `0.2.6`.

- Output 01 preserves the failed-closed `NO_GEOCODE_MATCH` result. Estimates remain `null`; no solar conclusion is inferred.
- Output 02 preserves the public landmark match, user-supplied 25 kW scenario, model results, confidence fields, limitations, source names, source URLs, and observation time.

[`03_actual_illustrative_demo_output.json`](03_actual_illustrative_demo_output.json) is a projection of the actual row in public Example Task dataset `p39ebTaNt566cmUh5`, produced by run `13JAmEk7QtEaEVLsx` on build `0.1.11`. Its values are intentionally illustrative. They did not come from a geocoder, imagery source, PVGIS, Google Solar API, a utility, or a real property assessment.

No omitted field was guessed. Long null-only, internal, and redundant structures were removed. One typographic separator in the open-data attribution was normalized from Unicode U+2014 to an ASCII hyphen; its meaning was not changed.

## Interpretation limits

- `qualified` means the Actor's configured screening threshold was met. It is not rooftop suitability, customer intent, marketing consent, engineering approval, a permit, financing approval, or an installation recommendation.
- `leadScore` is an automated pre-screen score. It is not a probability, warranty, or professional opinion.
- `NO_GEOCODE_MATCH` means the configured geocoder did not return an accepted match. It is not a negative solar-resource finding.
- Census TIGER address-range interpolation is not a surveyed rooftop centroid.
- `scenarioPanels` is a panel-equivalent scenario based on supplied assumptions. It is not a measured panel layout.
- PVGIS values are modeled solar-resource and energy estimates. They do not establish current rooftop condition, parcel-level shade, structural capacity, utility interconnection, tariff, incentives, realized savings, or production.
- A public Example Task demo result is illustrative even when its `status` is `qualified`.
- The Google BYOK mode was not sampled in this repository. No claim is made about Google coverage, current imagery, or successful Google matching.

The Actor is a pre-screening tool only. It does not provide engineering, structural, electrical, installation, financial, investment, tax, legal, permit, utility, or consumer-credit advice.

## Privacy and security

The samples preserve public corporate or landmark addresses only where needed to document the inspected run. They contain no private residential address, personal contact details, customer list, account data, API key, Apify token, bearer token, cookie, request signature, proxy credential, IP address, user-agent string, raw request header, or browser metadata.

Users remain responsible for lawful purpose, consent where required, data minimization, access control, retention, deletion, provider terms, marketing rules, and data-subject rights. Do not submit personal property data without a valid lawful basis and necessary rights.

## Availability and sources

Source coverage, models, vintages, APIs, schemas, terms, and pricing can change. These are historical sample records, not a real-time feed. No coverage, accuracy, completeness, freshness, imagery age, uptime, savings, output, or service-level guarantee is provided.

Primary sources:

- [PVGIS API documentation](https://joint-research-centre.ec.europa.eu/photovoltaic-geographical-information-system-pvgis/using-pvgis-5/api-non-interactive-service_en)
- [PVGIS usage conditions and data protection](https://joint-research-centre.ec.europa.eu/photovoltaic-geographical-information-system-pvgis/general-information/usage-conditions-data-protection_en)
- [U.S. Census Geocoder documentation](https://www.census.gov/programs-surveys/geography/technical-documentation/complete-technical-documentation/census-geocoder.html)
- [Google Solar API policies](https://developers.google.com/maps/documentation/solar/policies)

Review the Actor's current Store page, terms, pricing, input schema, provider documentation, and limitations before each production deployment.

## Listing update on September 30, 2026

The Store title, description and search metadata were checked against the owned Actor and synchronized with this repository. This documentation update does not alter executable code, input or output schemas, recorded test outputs, artifact hashes, billing or runtime builds. Existing examples retain their original dates and validation limits. A public listing is not evidence of successful output, network acceptance or an achieved search ranking.
