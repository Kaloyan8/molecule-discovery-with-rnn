The goal of this project is to develop a model that can propose new molecules from a database of 15697 SMILES entries. 
The original plan was to develop this model using MolGAN, which was rather difficult to implement in this 60 hour project. 
According to a study I found (https://pmc.ncbi.nlm.nih.gov/articles/PMC8470987/), the recurrent neural network (rnn) model has great capabilities in this regard and is comparable to the general adversarial model (GAN) model.
Due to the ease of access of the rnn model and being able to train the data even with the CPU only (in Google Colab), I opted for using this model instead.
So, I proceeded to adapt a developed model to my database (https://dmol.pub/applied/MolGenerator.html#approach-1-token-sampling)
1000 moledules were generated using this model, after which I moved on to perform the tanimoto analysis. Tanimoto similarity is a widely used metric in chemical similarity analysis to quantify the similarity between two molecular structures based on their chemical fingerprints At least 100 of these molecules have a tanimoto index ranging between 0 and 0.2, as seen in the heatmap.
Further reading:
https://github.com/MunibaFaiza/tanimoto_similarities/blob/main/README.md
https://github.com/codetodiscovery/Tanimoto-similarity/tree/main
