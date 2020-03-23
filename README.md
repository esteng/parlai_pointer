# parlai_pointer

Gradescope won't let me upload my ParlAI fork, so here is a [pointer to it](https://github.com/mitchellgordon95/ParlAI) 

# Evaluation 

Our model tended to produce degenerate outputs, both with and without MMI decoding. 

Pre-training seemed to go fine, we had to do some minor hyper-parameter search
to get things to start converging. We implemented the data filtering from
DialoGPT, because it seemed a lot less involved than the Entropy Based Filtering. However, we don't think that's the reason why the model is degenerate.

The most likely failure is the fine-tuning on dailydialog. We tried a couple hyper-parameter settings, but couldn't get the model to converge. The perplexity didn't go down much from initialization. I suspect if we did a more thorough grid search we could have gotten reasonable results.

# Eval Examples

![alt text](https://github.com/esteng/parlai_pointer/blob/master/mturk/screen1.png "Qualification Task")

![alt text](https://github.com/esteng/parlai_pointer/blob/master/mturk/screen2.png "Example Dialog")
