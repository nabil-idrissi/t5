The dataset was reconstructed to match the needed format. One that let us finetune the T5 model on instructions.
The first column (article) of the initial 'cnn_dailymail' dataset is turned into this:

> > A randomly chosen instruction from a list + initial cnn_dailymail column

For example:

> > > LONDON, England (Reuters) -- Harry Potter star Daniel Radcliffe gains access to a reported £20 million...

Turns into:

> > > Summarize this text: LONDON, England (Reuters) -- Harry Potter star Daniel Radcliffe gains access to a reported £20 million...

Also, I save this new data to make a fair comparison later on, when evaluating all models, as randomly choosing instructions would make training/testing on the huggingface dataset differ between models, and one version that can be used across all of them would solve this.
