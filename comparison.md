# KWS Google Speech Commands v2 35
An audio dataset of spoken words designed to help train and evaluate keyword spotting systems. Its primary goal is to provide a way to build and test small models that detect when a single word is spoken, from a set of ten target words, with as few false positives as possible from background noise or unrelated speech.

# Model Training
## Supervised Learning
In simple words, supervised learning provides a set of input-output pairs such that we can learn an intermediate system that maps inputs to correct outputs.

## Semi-supervised Learning
While supervised learning assumes the entire dataset to be trained on a task has the corresponding labels for each input, reality may not always be like this. 

*Labelling is a labour-intensive processing task and often input data comes in unpaired.*

## Unsupervised Learning
Unsupervised learning is at other end of the spectrum, where only input data have no corresponding classifications or labelling. The goal is to find underlying patterns with each dataset.

## Self-Supervised Learning
Self-supervised learning is in some sense a type of unsupervised learning as it follows the criteria that no labels were given. However, instead of finding high-level patterns for clustering, self-supervised learning attempts to still solve tasks that are traditionally targeted by supervised learning (e.g., image classification) without any labelings available.

# Evaluation Type
## One-shot learning
each new class has one labeled example. The goal is to make predictions for the new classes based on this single example.

## Few-shot learning
there is a limited number of labeled examples for each new class. The goal is to make predictions for new classes based on just a few examples of labeled data.

## Zero-shot learning
there is absolutely no labeled data available for new classes. The goal is for the algorithm to make predictions about new classes by using prior knowledge about the relationships that exist between classes it already knows. In the case of large language models (LLMs) like ChatGPT, for example, prior knowledge is likely include semantic similarities.

# Findings
| Model                                                  | Accuracy      | Model Training    | Evaluation Type |
|--------------------------------------------------------|---------------|-------------------|-----------------|
| ImageBind Demo                                         | ~2.5%         | Supervised        | Zero-shot       |
| kws_demo                                               | 94.5%         | Supervised        | Few-shot        |
| Masked Modeling Duo (M2D)                              | 98.5%         | Self-supervised   | Few-shot        |
| End-to-End Audio Strikes Back (EAT-S)                  | 98.15%        | Supervised        | Few-shot        |
| Audio Spectrogram Transformer (AST)                    | 98.11%        | Self-supervised   | Few-shot        |
| Hierarchical Token-Semantic Audio Transformer (HTS-AT) | 98%           | Weakly supervised | Few-shot        |
| Keyword Transformer (KWT-2)                            | 97.74% ±0.03% | Self-supervised   | Few-shot        |

- the performance of the SOTA models indicate the rising prevalence of Self-supervised models as well as the important of few-shot evaluation 
- it is also intriguing to observe that although advancements in KWS have emerged, the performance of SOTA models is still not 100%. This trend may be changed with the arrival of more advanced models such as OpenAI's whisper, that can be used to enrich training data as well as numerous other speech generation models out there. 

# References
- https://www.tensorflow.org/datasets/catalog/speech_commands
- https://www.techopedia.com/definition/34949/zero-shot-one-shot-few-shot-learning
- https://towardsdatascience.com/supervised-semi-supervised-unsupervised-and-self-supervised-learning-7fa79aa9247c
- https://paperswithcode.com/sota/keyword-spotting-on-google-speech-commands?metric=Google%20Speech%20Commands%20V2%2035
