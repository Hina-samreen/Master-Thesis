# Master-Thesis
Comprehensive Overview of Sentiment Analysis for German: Data Collection, Model Fine-tuning, Interpretability, Token-classification and and Evaluation.

## Sequence and Token Classification of German texts

An experiment, where we find which models perform better with Seqeunce and Token classfication of German texts. One of the approaches to token classification is 'Captum interpretability' where its 'Layer integrated gradient' is explored and Feature attributions are used to compute the label of each token/word. All the results of different approaches are then compared. Learn more about it on our wiki page.

### Reproduce the results

To reproduce the results , you can follow the below instructions:

 * To get started, pre-process your data by following the steps in the file DataPreprocessing.ipynb
 * You can then fine tune your desired model using the code in the file [FineTuningXLMRobertaWithNeutral.ipynb](FineTuningXLMRobertaWithNeutral.ipynb)
 * Next is computing feature attributions using Captum and evaluating it using NER evaluation technique(
   [Conlleval](#ner-evaluation-with-conlleval)). Learn More about it in [CaptumTrainingXLMRobertaWithNeutral.ipynb](CaptumTrainingXLMRobertaWithNeutral.ipynb) and [DataCreationNEREvaluationCaptum.ipynb](DataCreationNEREvaluationCaptum.ipynb)
 * Finally, create your own instruct/prompt for your desired LLM model, and evaluate the sequence classification results like in [LLMTestingSequenceClassification.ipynb](LLMTestingSequenceCalssification.ipynb)

### NER Evaluation with Conlleval:

To evaluate the results of token classification, we use the conlleval approach. Download the available file and use the following code snippet to run it:

```
python conlleval_perl.py -r < 'Your_file'

```
For more information on this script , visit https://github.com/sighsmile/conlleval?tab=readme-ov-file
