# SIGMORPHON 2024 Shared Task on Subword Tokenization

Subword tokenization is a fundamental preprocessing step for all the state-of-the-art language models and is designed to avoid Out-Of-Vocabulary (OOV) issues by segmenting OOV words into subwords. This shared task asks participants to develop a subword tokenization system and follow this procedure: 

1.  pre-train baby language models with their tokenizer
2.  fine-tune your BabyLM on 3-5 subtasks with training and development splits
3.  submit predictions on test splits

+ ***Subtask 1***: [Word and Definition](https://github.com/sigmorphon/2024TokenST#)
+ ***Subtask 2***: [Word and Word](https://github.com/sigmorphon/2024TokenST#)
+ ***Subtask 3***: [Word and Morphology](https://github.com/sigmorphon/2024TokenST#)
+ ***Subtask 4***: [TBA](https://github.com/sigmorphon/2024TokenST#)
+ ***Subtask 5***: [TBA](https://github.com/sigmorphon/2024TokenST#)

Please join our [Google Group TBA] to stay up to date.
Click here to [register for the task TBA]!

Please open the issues if you have any questions.

The average score of all subtasks will determine the shared task winner. Participant teams may submit as many systems as they want.

## Part 1: Word and Definition
At the word level, participants will be asked to classify if a given word and a given definition match semantically: true or false.

### Data
Training and development data are UTF-8-encoded tab-separated values files. Each example occupies a single line and consists of the input word, the input defition, and the corresponding output category. The following shows two lines of the training data:
    
    clerking  the activity of recording business transactions  true
    ammo  alternatively placed in genus Martynia  false


