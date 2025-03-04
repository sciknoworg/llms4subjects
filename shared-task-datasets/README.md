# 📚 The **LLMs4Subjects** Shared Task Datasets

The LLMs4Subjects shared task consists of two subtasks: multi-domain classification of library records and subject indexing.

1. **Subtask 1 - Multi-Domain Classification of Library Records**: Given a human-readable record, the system must classify it into one or more of the 28 predefined domains. The list of predefined subject domains can be found [here](https://terminology.tib.eu/ts/ontologies/linsearch/individuals?iri=https%3A%2F%2Fpurl.org%2Flinsearch).
2. **Subtask 2 - Subject Indexing**: Given a human-readable record, the system must generate relevant subject suggestions that accurately reflect its content.

## 🔍 About the Datasets

The **LLMs4Subjects** shared task provides participants with two main data files for developing LLM-based solutions:

1. **GND Subjects Taxonomy**: A comprehensive knowledge base of GND subjects, serving as a foundational resource for LLMs.
2. **Training and Development Dataset for Subtask 1 - Multi-domain classification**: Technical records (all-subjects only) annotated with domains, guiding the LLMs for classifying the records.
2. **Training and Development Datasets for Subtask 2 - Subject Indexing**: Technical records (all-subjects and tib-core-subjects) annotated with GND subjects, providing supervision signals for aligning LLMs.

These datasets are organized into repositories, where participants can visit and download the corresponding GND subjects file or folders containing annotated technical records.

## 📂 Repositories Included

- [**GND**](https://github.com/sciknoworg/llms4subjects/tree/main/shared-task-datasets/GND) **folder:** This folder contains the preprocessed GND subjects file in human-readable form, designed for use in the development of **LLMs4Subjects** shared task systems. Participants should download the relevant GND subjects file from this repository. The [GND](https://www.dnb.de/EN/Professionell/Standardisierung/GND/gnd_node.html) (Gemeinsame Normdatei in German or Integrated Authority File in English) is an international authority file primarily used by German-speaking libraries to catalog and link information on people, organizations, topics, and works. Among the files in the GND, the TIB subject matter experts use the **GND Sachbegriff** (subject terms file) to catalog the TIB’s technical records.

- [**TIBKAT**](https://github.com/sciknoworg/llms4subjects/tree/main/shared-task-datasets/TIBKAT) **folder:** This folder contains a selected portion of the subject-indexed (or subject-annotated) TIBKAT dataset, limited to German and English records, and focused on the following five record types: `article`, `book`, `conference`, `report`, and `thesis`. The dataset is provided with training and development set splits.

