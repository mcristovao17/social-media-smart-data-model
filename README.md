# SocialMediaMetric - Smart Data Model

This Smart Data Model represents a **single metric** collected from a **social media account**, allowing normalized and semantically enriched representation of social KPIs (e.g., followers, likes, reach) across platforms such as Facebook, Instagram, LinkedIn, Twitter, YouTube, and more.

It is designed to be **cross-platform, extensible**, and **compatible with NGSI-LD**, making it suitable for use in **Data Spaces**, **marketing intelligence systems**, and **interoperable analytics tools**.

---

## Entity: `SocialMediaMetric`

### Description

A standardized representation of a single metric for a specific social media account on a specific day. It includes metadata about whether the metric is organic or paid, its granularity, and the associated company name.

---

## Properties

| Property       | Type     | Description                                                                 |
|----------------|----------|-----------------------------------------------------------------------------|
| `id`           | `string` | Unique identifier of the metric entity (must follow NGSI-LD URN convention) |
| `type`         | `string` | Always set to `SocialMediaMetric`                                           |
| `platform`     | `string` | Name of the platform (e.g., Facebook, Instagram)                            |
| `account_id`   | `string` | ID of the account within the platform                                       |
| `metric`       | `string` | Name of the metric collected (e.g., `likes`, `followers`)                   |
| `value`        | `float`  | Numeric value of the metric                                                 |
| `organic`      | `boolean`| `true` if organic, `false` if paid                                          |
| `status_date`  | `date-time` | ISO timestamp when the metric was recorded                              |
| `granularity`  | `string` | Aggregation level of the metric (e.g., `daily`, `weekly`)                  |
| `company_name` | `string` | Name of the company that owns the social media account                      |

---

## JSON-LD Context

The model is compatible with NGSI-LD and uses the following context(s):

```json
[
    "https://uri.etsi.org/ngsi-ld/v1/ngsi-ld-core-context.jsonld",
    "https://raw.githubusercontent.com/mcristovao17/social-media-smart-data-model/main/context.jsonld"
]
