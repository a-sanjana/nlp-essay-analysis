# Analyzing Argumentative Student Essays

### Based on the Kaggle Contest - Feedback Prize : Evaluating Student Essays

#### Dataset
The dataset contains argumentative essays from U.S. students in grades 6-12.There are a total of 15594 essays in the training dataset. The openly available test dataset consists of 5 essays, while the hidden test set used by Kaggle to evaluate our model has 10402 essays.

#### Model
Our model is an ensemble that employs WBF of DeBERTa-Large and DeBERTa-XLarge.

#### Training
Maximum sequence length is set to 1536. Number od epochs is 5 and batch size is 4. Each model is trained for 5 folds; the first three folds of DeBERTa-Large and the last two folds of DeBERTa-XLarge are used for ensembling.

#### Loss and Evaluation
The loss used in this project is cross-entropy loss. The final score is determined by calculating each class's TP/FP/FN and taking the macro F1 score across all classes.

#### Results
The model achieve a CV score of 0.727. The results are visualized below:
