## Submission Guidelines 📄

### Task 1 Overview Recap

Given a human-readable record, the developed system must classify it into one or more of the 28 predefined domains. The primary target of this task is to predict the values of `subject` property, where the available annotations will be hidden in the test dataset.

#### Data For Evaluation 📚

During the evaluation phase, the participants will receive the test dataset consisting of technical records similar to those found in the training set, but with the subject domains removed, i.e. the `subject` property will be removed.

#### Evaluation Phase Submission

For the test dataset provided, the participant's systems should predict and classify the technical records into one or more of the 28 predefined subject domains.

##### Output Format

The expected output from participants should be a simple list of formatted domains as a list in `json` format. Each participant must submit their predictions in a file named identically to the corresponding test file, but containing only the predicted subject domains as a list in a json file.

##### Output Example

We use an example training file to illustrate this. 

Consider  [shared-task-datasets/TIBKAT/all-subjects/data/train/Book/de/3A01265597X.jsonld](../shared-task-datasets/TIBKAT/all-subjects/data/train/Book/de/3A01265597X.jsonld),

A sample output file can be found in this repository. Refer to the following link: [3A01265597X.json](3A01265597X.json).

### Task 2 Overview Recap 

The primary focus of LLMs4Subjects is on predicting the values of the `dcterms:subject` property, where the available annotations will be hidden in the test dataset. The list of GND subject term IDs predicted for `dcterms:subject` is treated as the subject classification of technical records.

#### Data for Evaluation 📚

During the evaluation phase, starting in June, participants will receive a dataset consisting of technical records similar to those found in the training set, but with the subject classifications removed, i.e. the `dcterms:subject` property will be an empty list.

We use an example training file to illustrate this. 

Consider  [shared-task-datasets/TIBKAT/all-subjects/data/train/Article/de/3A168396733X.jsonld](https://github.com/sciknoworg/llms4subjects/blob/main/shared-task-datasets/TIBKAT/all-subjects/data/train/Article/de/3A168396733X.jsonld),

in the test dataset, the section highlighted below will be blank:

<img src="https://github.com/sciknoworg/llms4subjects/blob/main/img/classification-target.png" width="500" height="350" alt="Example of blank subject classification area in test data">

#### Evaluation Phase Submissions

For the test dataset provided in the evaluation phase, participants need to apply their systems to predict or classify the `gnd` subject tag IDs for each record in the test dataset.

##### Output Format

The expected output from participants should be a simple list of `gnd` subject tag IDs as a list in `json` format. Each participant must submit their predictions in a file named identically to the corresponding test file, but containing only the predicted subject tags as a list of gnd ids in a json file.

###### Output Example

A sample output file can be found in this repository. Refer to the following link: [submission-format/3A168396733X.json](3A168396733X.json).

Each output file must include the top 50 GND tag predictions made by your system, arranged in descending order based on model confidence. This order is crucial, as evaluations will be conducted using top-k ranking methods. Ensure that the tags predicted with the highest confidence are listed at the top.