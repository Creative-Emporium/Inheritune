# Pre-training Small Base LMs with Fewer Tokens

⚠️ **Warning**

This repository is still under development and may still contain some bugs. 

---

## Abstract
We study the effectiveness of a simple approach to develop a small base language model (LM) starting from an existing large base LM: first inherit a few transformer blocks from the larger LM, and then continually train this smaller model on a very small subset (0.1\%) of the raw pretraining data of the larger model. We call our simple recipe Inheritune and first demonstrate it for building a small base LM with 1.5B parameters using 1B tokens (and a starting larger LM of 3B parameters); we do this using a single A6000 GPU for half a day. Across 9 diverse evaluation datasets as well as the MMLU benchmark, the resulting model compares favorably to publicly available base models of 1B-2B size, some of which have been trained using 50-1000 times more tokens. 

We investigate Inheritune in a slightly different setting where we train small LMs utilizing larger LMs and their full pre-training dataset. Here we show that smaller LMs trained utilizing some of the layers of GPT2-medium (355M) and GPT-2-large (770M) can effectively match the val loss of their bigger counterparts when trained from scratch for the same and double the number of training steps on OpenWebText dataset with 9B tokens. We analyze Inheritune with extensive experiments and demonstrate it efficacy on diverse settings. Our training code will be available soon. 
