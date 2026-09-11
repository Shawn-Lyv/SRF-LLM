A Multimodal Neuroimaging Large Language Model for Transdiagnostic Suicidal Risk Assessment Across Developmental Stages
=========================

Suicidal Risk Forewarning Large Language Model (SRF-LLM) was dedicated to provide timely and preliminary assessment of suicidal risk for young people. By encoding resting-state fMRI (rsfMRI) dynamic functional connectivity into Chinese texts, SRF-LLM was trained to ‘translate’ latent rsfMRI abnormalities into dysfunctional task-based connectivity representations (evoked by interoception-exteroception-emotion transition task in this research, which were correlated with suicidal risk). There are two different SRF-LLM developed for adolescent group and young adult group, including binary SRF-LLM to distinguish subjects with suicidal risks from healthy ones and triplet SRF-LLM (BSS SRF-LLM) to stratify suicidal risks into three levels. Data needed for the replication of model performances on independent datasets were provided in this repository.


Data
----------
For each SRF-LLM, independent datasets applied in model training, test and generalization verification were arranged separately in four folders, including encoded Chinese textural representations (.json) and labels specifying suicidal risks in multiple timescales (assessed by scores of Beck Scale for Suicide Ideation, BSS) of each sample.

SRF-LLM consists of a Bert layer and a linear layer. The Bert layer was fine-tuned on the pretrained Bert-base-Chinese model, which was presented in ‘bert_base_chinese\\’ folder. The coefficients of trained Bert layer and linear layer were presented in four folders corresponding to each SRF-LLM.

We found adult SRF-LLM inputted with feature analyzed from the first-6-minute rsfMRI responses (since data collection onset) performed the best upon different datasets. Regarding adolescent SRF-LLM, the best performances were based on the rsfMRI responses collected during the first 3 minutes. The Chinese texts arranged in this repository were encoded from these rsfMRI response segmentations.

Performance Replication
------------------
The four Jupyter notebook files in the base directory, corresponding to the four SRF-LLM, were used to replicate model performances on independent datasets. These files were compiled on Python 3 environments, and numpy, transformers, torch, sklearn and scipy libraries were also required in running.
 
