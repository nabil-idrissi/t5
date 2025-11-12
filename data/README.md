I'm reconstructing the dataset to match the needed format to finetune the T5 model using instructions.
The article column of the initial 'cnn_dailymail' is turned into this format:

> > A randomly chosen instruction from a list + initial cnn_dailymail column

For example:

> > > LONDON, England (Reuters) -- Harry Potter star Daniel Radcliffe gains access to a reported £20 million...

Turns into

> > > Summarize this text: LONDON, England (Reuters) -- Harry Potter star Daniel Radcliffe gains access to a reported £20 million...

Also, I save this new data to have a fair comparison later on, when i'll need to evaluate all models. As randomly choosing instructions would make training/testing on the huggingface dataset differ between models, that's why I'm saving one version that can be used across all of them.
