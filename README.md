# NER sequence tagging using BiLSTM and CRF model 

# NER sequence tagging using BERT Encoding and CRF model 

```
Prerequistes
```
* nltk
* pytorch

```
Data
https://cogcomp.seas.upenn.edu/page/resource_view/81
```

```
Steps
```
* Follow the steps in the notebook
* Vocab used is numberbatch embedding(https://www.kaggle.com/nholloway/conceptnet-numberbatch-vectors) + training words with frequency > 20   


```
How it works
```

* Encodes tokens using BiLSTM layer
* there are 3 sets of transition matrices ,which are learnt:
  start transition - probability of starting with each of the tags
  end transition - probability of each of the tags being the last tag
  transition - probability of transition from 1 tag to another
* forward function calculates forward score which is sum of probalities for all possible paths of tags
* gold score is the probability which the model assigns to the true path
* loss is the difference between above scores, as all values are learnt in the log space
* viterbi algorithm is used for prediction
* here for demonstration purposes, only 10 sentences are used for training
* training with full dataset is underway on a tesla GPU and results are awaited

```
Future Enhancements
```
* BERT could be used to fetch encoding instead of LSTM (should provide better encoding, with
 time saving in training)

## Any questions 👨‍💻
<p> If you have any questions, feel free to ask me: </p>
<p> 📧: "nirmalendu@outlook.com"</p>
