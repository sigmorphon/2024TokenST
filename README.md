# SIGMORPHON 2024 Shared Task on Subword Tokenization

Subword tokenization is a fundamental preprocessing step for all the state-of-the-art language models. It is designed to avoid Out-Of-Vocabulary (OOV) issues by segmenting OOV words into subwords. This shared task asks participants to develop a subword tokenization system and follow this procedure: 

1.  pre-train baby language models with your tokenizer
2.  fine-tune your BabyLM on the first three subtasks with training and development splits
3.  submit predictions on test splits

+ ***Subtask 1***: [Word and Definition](https://github.com/sigmorphon/2024TokenST#)
+ ***Subtask 2***: [Word and Word](https://github.com/sigmorphon/2024TokenST#)
+ ***Subtask 3***: [Word and Morphology](https://github.com/sigmorphon/2024TokenST#)
+ ***Subtask 4***: [Machine Translation](https://github.com/sigmorphon/2024TokenST#)

Please join our [Google Group](https://groups.google.com/forum/#!forum/sigmorphon-subword-tokenization/join) to stay up to date.
Click here to [register for the task TBA]!

Please open the issues if you have any questions.

The average score of all subtasks will determine the shared task winner. Participant teams may submit as many systems as they want.

## Subtask 1: Word and Definition
Classify if a given word and a given definition match semantically.

### Data
Training and development data are UTF-8-encoded tab-separated values files. Each example occupies a single line and consists of the input word, the input definition, and the corresponding output category. The following shows two lines of the training data:
    
    clerking  the activity of recording business transactions  1
    ammo  alternatively placed in genus Martynia  0

## Subtask 2: Word and Morphology
Classify whether a given word contains a given morphology.

### Data
Training and development data are UTF-8-encoded tab-separated values files. Each example occupies a single line and consists of the input word, the input morphology type, and the corresponding output category. The following shows two lines of the training data:
    
    leaderboard  derivation  1
    overpressing  compound  0

## Subtask 3: Word and Word
Classify whether two words in input are semantically related to one another.

### Data
Training and development data are UTF-8-encoded tab-separated values files. Each example occupies a single line and consists of two input words, as well as the corresponding output category. The following shows two lines of the training data:
    
    photocopy  mosaic  1
    poorer  proxy  0

## Allowed Data Sources
For pre-training your baby language models and training your tokenizer, you can only use the 100M word dataset from the [BabyLM Challenge 2023](https://babylm.github.io/archive_2023.html). For training your tokenizer, you can additionally use the English morphological data from the [SIGMORPHON Shared Task 2022 on Morpheme Segmentation](https://github.com/sigmorphon/2022SegmentationST). Please note: this morphological data had some noises and we will release a more clean version of this data soon here. 


## Evaluation

We will provide Python evaluation scripts, reporting the following evaluation measures:

- TBA

## Baseline

Babylm baselines for WaD subtask. The first table shows the tokenizer size and how the test split is divided into three subgroups of [umLabeller](https://github.com/unimorph/umLabeller).

|   model                |   tokenizer size  |   vocab         |   morph          |   alien         |
|------------------------|-------------------|-----------------|------------------|-----------------|
|   babylm-roberta-base  |   50227           |   1001 (33.3%)  |   1050 (35.0%)   |    949 (31.6%)  |
|   lgt-bert-babylm      |   16385           |    347 (11.5%)  |   1078 (35.9%)   |   1560 (52.0%)  |

The second table shows the test accuracies across three subgroups with total.

|   model                |   vocab     |   morph     |   alien     |   total     |
|------------------------|-------------|-------------|-------------|-------------|
|   babylm-roberta-base  |   91.6±0.5  |   61.8±1.2  |   53.2±1.6  |   69.0±0.8  |
|   lgt-bert-babylm      |   93.1±0.5  |   75.2±0.4  |   72.0±0.9  |   75.8±0.4  |


## Submission

Please submit your team's results to khuyagbaatar.b@gmail.com, CCing your teammates by TBA (AoE). Each submission should be a .tar.gz or .zip file.

## Timeline

- April 15, 2023: The task website is complete, and accepting registrations to the mailing list
- April 29, 2024: Baseline systems released to participants
- May 30, 2024: Test data is available for participants
- June 20, 2024: Final Submissions are due
- June 25, 2024: Results announced to participants
- July 7, 2024: System papers due for review
- July 31, 2024: Reviews back to participants
- August 15, 2024: CR deadline; task paper due from organizers.

## Organizers
- Khuyagbaatar Batsuren (University of Melbourne)
- Gábor Bella (University of Trento)
- Verna Dankers (University of Edinburgh)
- Tsetsuukhei Delgerkhuu (National University of Mongolia)
- Omri Uzan (Ben-Gurion University of the Negev)
- Zdeněk Žabokrtský (Charles University)
- Jungyeul Park (University of British Columbia)
- Yuval Pinter (Ben-Gurion University of the Negev)
- Vilém Zouhar (ETH Zürich)
- Ryan Cotterell (ETH Zürich)
- Ekaterina Vylomova (University of Melbourne)
