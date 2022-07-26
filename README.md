# HMM_SteinmetzDataset
A project for NMA_CN _2022 by Chaosfan group (Farnaz, Jing, Peng, Ula, Yidan, Yuyang)

**Question:**
- What's the difference of state transitions in different brain areas? (motor_areas or vis_ctx)
- How are state transitions correlated across brain areas? Which areas lead/follow?
- How are state transitions changed across different trial types(correct/miss/passive)? 
- Can we predict trial_types from hidden state sequences?

**Dataset:**
- Steinmetz dataset

**Work plan:**

7/25
- decoder using hidden state sequence to predict behaviour/trial_types  Jing
- statistal features in different trial_types/different event_periods   Yuyang
- !!! what the meaning of the hidden states
    - wheel speed focus on motor    Ula
    - pupil area focus on vis        Farnaz
    - reward   Yidan
- !!! organize our data/results/code together  peng
- !!! logic of explaining our results

7/22
- hidden states across areas (vis, motor, thalamus) Ula
- hidden states across trial types  Peng
- best num of hidden states  Jing, Yidan
    - cross-validation
    - BIC
- analysis statistical features of hidden states sequences farnaz, Yuyang

7/15:
- HMM intro: Yuyang, Jing, Yidan
- Accessing data: Ula, Peng, Farnaz

**To do list:**
- explore how to use Steinmetz dataset, refer to [dataset notebook](https://colab.research.google.com/github/NeuromatchAcademy/course-content/blob/main/projects/neurons/load_steinmetz_decisions.ipynb)
- explore how to use PossionHMM to find hidden states, refer to [ssm notebook](https://github.com/lindermanlab/ssm/blob/master/notebooks/Poisson%20HMM%20Demo.ipynb); and how to analysis hidden states, refer to [this one](https://github.com/mazzulab/ANDA_HMM_Course/blob/main/HMM-Introduction_ANDA_Solutions.ipynb)
    - ssm packages
- find the hidden states across different areas
    - focus on certain areas, eg, motor areas, visual cortex
    - quantify the difference of state sequence across different areas
        - transition time
        - interval distribution
    - quantify the time delay (lead/follow relation) across different areas
- find the fidden states across different trial_types
    - quantify the difference of state sequence across trial_types
        - transition time
        - interval distribution
- construct a decoder for predicting trial_types from hidden state sequences
- compare the state sequence difference in different trial types across different brain areas
    - to find which areas play a important role in defferent trials