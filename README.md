# PACT Dataset

This repository contains the source dataset used to generate the PACT website as seen at [pactmatrix.com](https://pactmatrix.com) and the corresponding [STIX 2.0 Dataset](https://github.com/slashsec-Red-Teaming-GmbH/pact-data-stix). The dataset is completely based on JSON, enabling easy editing as well as automation.

## Reporting Issues

If you encounter issues with the dataset, please use the [Github Issue Tracker](https://github.com/slashsec-Red-Teaming-GmbH/pact-data-json/issues).

For any errors, typos or bugs in the website, shoot us an email to [pact@slashsec.at](mailto:pact@slashsec.at). Include a description as well as the URL at which it can be found.

## Contributing

We welcome corrections, new techniques, mitigations, detections, assets, and references. The fastest path is a pull request against this repository. Please open an issue first so we can align on scope and IDs.

### Repository layout

| Directory | ID prefix | Contents |
|-----------|-----------|----------|
| `tactics/` | `PT####` | Tactic columns in the matrix |
| `techniques/` | `P####` | Techniques |
| `subtechniques/` | `P####.###` | Procedures (sub-techniques) |
| `mitigations/` | `PM####` | Mitigations |
| `detections/` | `PET####` | Detections |
| `assets/` | `PA####` | Data sources / assets |

Each object lives in one file named after its ID (for example `techniques/P0007.json`).

Starter templates for each object type are in [templates/](https://github.com/slashsec-Red-Teaming-GmbH/pact-data-json/tree/main/templates).

### Editing rules

- **One object per file.** The top-level `id` must match the filename.
- **Descriptions** should follow this style: start with “Adversaries may …” for techniques and sub-techniques.
- **`metadata.modified`** - set to the date of your change (`YYYY-MM-DD`).
- **`metadata.contributors`** - add your name or handle when you edit an object.
- **`metadata.references`** - cite sources as URL strings where applicable.
- **`metadata.version_permalink`** - site path for the object (for example `/ttps/PT0003/P0007/`). Sub-techniques nest under their parent technique path.
- **Cross-links** - use ID arrays only (`tactics`, `technique`, `techniques`, `related.mitigations`, `related.detections`, `data_components`). Both sides of a relationship should agree where applicable.

### Pull requests

1. Fork the repository and create a branch for your change.
2. Edit or add JSON files; keep valid JSON and consistent indentation (2 spaces).
3. Open a PR with a short summary of what changed and why.
4. By contributing, you agree that your submissions are licensed under the [Apache License 2.0](https://github.com/slashsec-Red-Teaming-GmbH/pact-data-json/blob/main/LICENSE) and your contribution is published by [slashsec](https://slashsec.at).

Questions about structure or new object IDs: [pact@slashsec.at](mailto:pact@slashsec.at) or via the [Discussion Tab](https://github.com/slashsec-Red-Teaming-GmbH/pact-data-json/discussions).

