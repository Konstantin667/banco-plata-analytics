# AQA calibration: model vs human QA (round 2)

Same meetings labelled by human QA and by the LLM; 68 meetings matched. `agree` = share of meetings where both gave the same answer. S-criteria are sales-behaviour tags.

| Criterion | Meaning | n | Agreement |
|---|---|---:|---:|
| V1 | Audio file exists | 68 | 96% |
| V2 | Transcript is not empty | 68 | 96% |
| V3 | Audio ≥ 60 s | 68 | 96% |
| V4 | Enough speech | 68 | 93% |
| V5 | Not only fragments | 67 | 91% |
| V9 | Someone from the business is on the recording | 67 | 90% |
| V11 | Recording is complete | 67 | 51% |
| H1 | No client on the recording | 65 | 97% |
| H2 | Survey says more than the client | 65 | 78% |
| H3 | Recording paused mid-conversation | 60 | 98% |
| H4 | False product information | 59 | 42% |
| H5 | Promises products that do not exist | 58 | 78% |
| H6 | Price / free period not explained | 0 | 0% |
| H7 | Rude or pressure | 58 | 98% |
| H8 | Suggests false data | 58 | 95% |
| H11 | Asks for money for personal use | 58 | 98% |
| H12 | Sells third-party services | 58 | 100% |
| H18 | Personal phone use | 65 | 91% |
| OBS1 | Profanity not addressed to the client | 65 | 92% |
| OBS2 | Observation 2 | 65 | 92% |
| S2 | Sales behaviour tag | 55 | 80% |
| S3 | Sales behaviour tag | 56 | 93% |
| S5 | Sales behaviour tag | 56 | 55% |
| S7 | Sales behaviour tag | 53 | 58% |
| S8 | Sales behaviour tag | 54 | 72% |
| S12 | Sales behaviour tag | 5 | 80% |
| S14 | Sales behaviour tag | 21 | 57% |
| S17 | Sales behaviour tag | 51 | 65% |
| S19 | Sales behaviour tag | 37 | 73% |
| S20 | Sales behaviour tag | 53 | 74% |

Criteria at ≥ 90%: 16 of the 29 compared (H6 had no human labels in this round). Low-agreement criteria were rewritten or routed to human review in the next prompt version.
