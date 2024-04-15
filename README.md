# SIGMORPHON 2024 Shared Task on Subword Tokenization

Subword tokenization is a fundamental preprocessing step for all the state-of-the-art language models. It is designed to avoid Out-Of-Vocabulary (OOV) issues by segmenting OOV words into subwords. This shared task asks participants to develop a subword tokenization system and follow this procedure: 

1.  pre-train baby language models with your tokenizer
2.  fine-tune your BabyLM on the first three subtasks with training and development splits
3.  submit predictions on test splits

+ ***Subtask 1***: [Word and Definition](https://github.com/sigmorphon/2024TokenST#)
+ ***Subtask 2***: [Word and Word](https://github.com/sigmorphon/2024TokenST#)
+ ***Subtask 3***: [Word and Morphology](https://github.com/sigmorphon/2024TokenST#)
+ ***Subtask 4***: [Machine Translation](https://github.com/sigmorphon/2024TokenST#)

Please join our [Google Group TBA] to stay up to date.
Click here to [register for the task TBA]!

Please open the issues if you have any questions.

The average score of all subtasks will determine the shared task winner. Participant teams may submit as many systems as they want.

## Subtask 1: Word and Definition
Classify if a given word and a given definition match semantically.

### Data
Training and development data are UTF-8-encoded tab-separated values files. Each example occupies a single line and consists of the input word, the input definition, and the corresponding output category. The following shows two lines of the training data:
    
    clerking  the activity of recording business transactions  true
    ammo  alternatively placed in genus Martynia  false

## Subtask 2: Word and Morphology
Classify whether a given word contains a given morphology.

### Data
Training and development data are UTF-8-encoded tab-separated values files. Each example occupies a single line and consists of the input word, the input morphology type, and the corresponding output category. The following shows two lines of the training data:
    
    leaderboard  derivation  true
    overpressing  compound  false

## Subtask 3: Word and Word
Classify whether two words in input are semantically related to one another.

### Data
Training and development data are UTF-8-encoded tab-separated values files. Each example occupies a single line and consists of two input words, as well as the corresponding output category. The following shows two lines of the training data:
    
    photocopy  mosaic  true
    poorer  proxy  false


## Evaluation

We will provide Python evaluation scripts, reporting the following evaluation measures:

- TBA

## Submission

Please submit your team's results to khuyagbaatar.b@gmail.com, CCing your teammates by TBA (AoE). Each submission should be a .tar.gz or .zip file.

## Timeline (Tentative)

- April 15, 2023: The task website is complete, and accepting registrations to the mailing list
- April 22, 2024: Baseline systems released to participants
- May 22, 2024: Test data is available for participants
- May 31, 2024: Final Submissions are due
- June 17, 2024: Results announced to participants
- June 24, 2024: System papers due for review
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
- Ryan Cotterell (ETH Zürich)
- Ekaterina Vylomova (University of Melbourne)
