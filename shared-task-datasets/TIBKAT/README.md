# 📑 The **LLMs4Subjects** Shared Task TIBKAT Dataset

## 🔍 About

TIB subject matter experts index the library’s technical records based on the GND subjects taxonomy. Early in the development of TIB's record annotation guidelines, certain GND subject classes were identified as core to TIB’s focus. However, as technical sciences have advanced, TIB records are now annotated with GND subjects that go beyond those original core subject classes.

Since the TIBKAT dataset compiled for this shared task contains over 100,000 records, we offer participants the option of using a smaller subset. This subset includes only records annotated with at least one GND subject from TIB’s core subject classification scheme.

## 📂 Repositories Included

- [**all-subjects**](https://github.com/sciknoworg/llms4subjects/tree/main/shared-task-datasets/TIBKAT/all-subjects) **dataset:** The `train dataset` contains 81,937 records, and the `dev dataset` contains 13,666 records. This dataset is a superset of the dataset linked below and includes all annotated records without restrictions.

- [**tib-core-subjects**](https://github.com/sciknoworg/llms4subjects/tree/main/shared-task-datasets/TIBKAT/tib-core-subjects) **dataset:** The `train dataset` contains 41,902 records, and the `dev dataset` contains 6,980 records. In this subset, records are included only if at least one of the annotated GND subjects belongs to TIB's original core subject classification.

For Sub-task 1 - Multi-domain Classification, participants are required to use only the all-subjects dataset, as it encompasses all 28 predefined domains, providing systems with a broader distribution of data records. However, there are some exceptions. Specifically, a small subset of records does not include domain information in its metadata. Out of the 95,603 records in the train and development splits, only 278 records lack domain details. The list of these records can be found [here](all-subjects/data-statistics/Records_without_Domains.json).

For Sub-task 2 - Subject Indexing, participants can choose between the two datasets based on their project needs—whether to work with the larger, more comprehensive set or focus on a smaller, more manageable subset of records within TIB’s core subject classes for subject indexing.

Each dataset folder is organized into two directories: `data`, which contains the actual dataset files, and `data-statistics`, which provides detailed statistical analyses on various aspects of the dataset.

## 🧐 A Guide to Reading TIBKAT Records

Each TIBKAT technical record in the repositories is provided in `json-ld` format. You can view an example English record [here](https://github.com/sciknoworg/llms4subjects/blob/main/shared-task-datasets/TIBKAT/all-subjects/data/train/Article/en/3A1499846525.jsonld) and an example German record [here](https://github.com/sciknoworg/llms4subjects/blob/main/shared-task-datasets/TIBKAT/all-subjects/data/train/Article/de/3A168396733X.jsonld). These files contain various property annotations, with the four most relevant to **LLMs4Subjects** being `title`, `abstract`, `dcterms:subject` and `subject`. Participants are free to use other properties as needed. This guide provides an overview of how to interpret a TIBKAT record, focusing on the `dcterms:subject` and `subject` properties.

### Understanding the Subject Properties


Each TIBKAT technical record contains the properties `subject` and `dcterms:subject`, which describes the domains and topics covered by a given resource. These properties are essential for ensuring that systems perform effectively in both Sub-task 1 and Sub-task 2.

#### [The TIBKAT Domain Property for Sub-Task 1 - Multi-domain Classification](#how-to-domains)

The `subject` property includes keywords, phrases, or classification codes that reflect the content. Subject annotations in TIBKAT records are provided by a team of 17 expert subject specialists, covering 28 different subjects, including:

- Architecture, Civil Engineering, Biochemistry, Biology, Chemistry, Chemical Engineering, Electrical Engineering, Energy Technology, Educational Science, Earth Sciences, History, Information Technology, Literary Studies and Linguistics, Mechanical Engineering, Mathematics, Medical Technology, Plant Sciences, Philosophy, Physics, Law, Study of Religions, Social Sciences, Sports Sciences, Theology, Environmental Engineering, Traffic Engineering, Materials Science, and Economics.

For this edition of the shared task and specifically for Sub-task 1, only domains related to Fachsystematik LinSearch should be considered. More information about Fachsystematik LinSearch can be found [here](https://terminology.tib.eu/ts/ontologies/linsearch).

#### [The `dcterms:subject` Property for Sub-Task 2 - Subject Indexing](#how-to-subjects)

The `dcterms:subject` property (often represented as `<dc:subject>` in XML or similar formats) describes the subjects or topics covered by the resource. 

#### How to Read the `dcterms:subject` Property

1. **Access the TIBKAT Record:** Start by accessing the JSON-LD TIBKAT records in the dataset or supplementary dataset folders.

2. **Locate the `dcterms:subject` Property:** Find the `dcterms:subject` property in the record. This property may contain one or more subject headings, each sourced from the GND Sachbegriff (subject headings) taxonomy. More information on GND and its role in TIBKAT can be found in the GND shared task dataset subfolder.

3. **Interpret the Subject Entries:** Each entry under the `dcterms:subject` property represents a subject or topic relevant to the resource. These are typically classification codes from the GND subject headings.

4. **Use the Subjects for Research:** The subject codes listed under the `dcterms:subject` property, when mapped to their corresponding labels, are useful for understanding the focus of the resource, conducting research, or finding related materials in the library catalog.

### Conclusion

Understanding the `dcterms:subject` and `subject` property within TIBKAT records is crucial for researchers, librarians, and anyone working on categorizing or finding resources by subject. By focusing on this property, users can gain insights into the content and relevance of the resources cataloged in the TIBKAT system.