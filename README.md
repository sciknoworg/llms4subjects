# 🚀 Welcome to the LLMs4Subjects 📚 GermEval 2025 Shared Task Dataset Repository!

## 💡 About

The **LLMs4Subjects** shared task invites the research community 🤝 to develop cutting-edge, LLM-based semantic solutions for automated subject indexing and classification 📑 of [TIB](https://www.tib.eu/en/)—the German National Library of Science and Technology’s ever-growing collection of technical records in various natural languages. This task, includes domain classification as well as subject tagging, which leverages the [GND](https://www.dnb.de/EN/Professionell/Standardisierung/GND/gnd_node.html) (Gemeinsame Normdatei in German or Integrated Authority File in English), an international authority file primarily used by German-speaking libraries to catalog and link information on people, organizations, topics, and works.


To support the development of systems for the **LLMs4Subjects** shared task, we provide participants with two types of datasets:

1. **Curated, human-readable form of the GND subjects taxonomy.**
2. **A large-scale dataset of technical records from TIB’s open-access collection, annotated with domains and GND subjects, available in both English and German.**

Although TIB’s technical records span multiple languages, this shared task focuses on the most representative collections in English and German. We have utilized the TIB's open-access catalog of technical records (https://www.tib.eu/en/services/open-data), known as TIBKAT, and restricted it to records that include abstract metadata. This collection can be dynamically browsed on the TIB portal [here](https://www.tib.eu/en/search?tx_tibsearch_search%5Baction%5D=search&tx_tibsearch_search%5Bcnt%5D=20&tx_tibsearch_search%5Bcontroller%5D=Search&tx_tibsearch_search%5BgroupField%5D=matchTitleTypeFirstAuthor_str&tx_tibsearch_search%5Bpg%5D=1&tx_tibsearch_search%5Bquery%5D=prefix%3Atibkat%20%2Babstract%3A%2A%20%2BxmlPath%3Asubject%2F%40type%3Dgnd&cHash=f451c3e5094da4379c764584d10afc8d). While the overall collection includes various types of technical records, this shared task focuses on the most representative types: `article`, `book`, `conference`, `report`, and `thesis`. Therefore, the official shared task dataset comprises only records of these five types.

For the convenience of our participants, both the GND and the TIBKAT datasets have been reorganized, appropriately formatted with human-readable tags, and released as the official shared task dataset in this repository. We recognize that standardized library taxonomies and collections often refer to age-old identifier mechanisms and are filled with codes. Processing and interpreting these codes can be time-consuming ⏳. Therefore, in consultation with TIB subject matter experts, we have preprocessed both the GND and TIBKAT datasets, converting their fine-grained coding into human-readable formats. This should help the **LLMs4Subjects** participants download the relevant data and get started right away.

This shared task offers the research community an opportunity to creatively develop LLMs 🧠 for domain classification and subject tagging 📑 of technical records 📚 based on the GND taxonomy. Systems need to demonstrate bilingual language modeling 🌍 by processing technical records in both German and English. Moreover, successful solutions may be integrated directly into the operational workflows of the TIB Leibniz Information Centre for Science and Technology University Library 🏛️.


## 📂 Repositories Included

- [**shared-task-datasets**](https://github.com/sciknoworg/llms4subjects/tree/main/shared-task-datasets): This subfolder includes the human-readable formatted GND subjects taxonomy and the training and development sets for the TIBKAT records. Participants in the **LLMs4Subjects** shared task are requested to download the relevant files from this folder for system development.

- [**supplementary-datasets**](https://github.com/sciknoworg/llms4subjects/tree/main/supplementary-datasets): This subfolder includes all excluded data from the open-access GND and TIBKAT datasets that are not part of the **LLMs4Subjects** shared task. For instance, this may include records from TIBKAT in languages other than English or German or records where a specific record type is too sparse. Although not part of the official shared task, these records are available for participants to use as needed.

- [**shared-task-eval-script**](https://github.com/sciknoworg/llms4subjects/tree/main/shared-task-eval-script): This subfolder contains the official evaluation script used to generate the quantitative evaluation results for **LLMs4Subjects** participant team submissions.

## 📧 Contact

llms4subjects [at] gmail.com

## 💡 Citation

The recommended citation for this dataset resource is provided below. If you find this resource useful, please consider citing it.

```bibtex
@InProceedings{dsouza-EtAl:2025:SemEval2025,
author    = {D'Souza, Jennifer and Sadruddin, Sameer and Israel, Holger and Begoin, Mathias and Slawig, Diana},
title     = {SemEval-2025 Task 5: LLMs4Subjects - LLM-based Automated Subject Tagging for a National Technical Library's Open-Access Catalog},
booktitle = {Proceedings of the 19th International Workshop on Semantic Evaluation (SemEval-2025)},
month     = {August},
year      = {2025},
address   = {Vienna, Austria},
publisher = {Association for Computational Linguistics},
pages     = {1082--1095},
url       = {https://aclanthology.org/2025.semeval2025-1.139}
}
```

```bibtex
@misc{D_Souza_The_GermEval_2025_2025,
author = {D'Souza, Jennifer and Sadruddin, Sameer and Israel, Holger and Begoin, Mathias},
doi = {10.5281/zenodo.16743609},
month = mar,
title = {{The GermEval 2025 2nd LLMs4Subjects Shared Task Dataset}},
url = {https://github.com/sciknoworg/llms4subjects},
year = {2025}
}
```

## ⭐ Acknowledgements

The **LLMs4Subjects** shared task, organized as GermEval 2025, is jointly supported by the [SCINEXT project](https://scinext-project.github.io/) (BMBF, German Federal Ministry of Education and Research, Grant ID: 01lS22070) and the [NFDI4DataScience initiative](https://www.nfdi4datascience.de/) (DFG, German Research Foundation, Grant ID: 460234259).


This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg