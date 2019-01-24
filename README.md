# EEG-data-from-basic-sensory-task-in-Schizophrenia

A small project for the [Computational neuroscience](https://courses.cs.ut.ee/2018/neuro/fall) course taught at [University of Tartu](https://www.ut.ee/en).

## Code and setup

Install python, jupyter notebook and the following modules

```bash
# Globally:
pip install jupyter

# In project folder:
python -m pip install matplotlib
python -m pip install pandas
python -m pip install numpy

# Run notebook:
jupyter notebook
```

After the environment is set up, create "data" folder in project folder, download ***demographic.csv*** and ***ERPdata.csv*** from [Kaggle competition data](https://www.kaggle.com/broach/button-tone-sz), and put them into data folder.

Or change read_csv calls if you prefer some other folder :   
```python
demo = pd.read_csv("data/demographic.csv")
demo.columns = [col.replace(' ', '') for col in demo.columns]
erp_data = pd.read_csv("data/ERPdata.csv")
```

## References

### Idea

- [Kaggle competition](https://www.kaggle.com/broach/button-tone-sz/home)  
- [Code references](https://www.kaggle.com/broach/replicating-did-i-do-that-paper-analyses-with-r)   
### Research papers
- [Did I Do That? Abnormal Predictive Processes in Schizophrenia When Button Pressing to Deliver a Tone](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4059422/) 
- [Using concurrent EEG and fMRI to probe the state of the brain in schizophrenia](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5008052/)  
- [Meditation (Vipassana) and the P3a event-related brain potential](https://www.ncbi.nlm.nih.gov/pubmed/18845193)  
- [The N1-suppression effect for self-initiated sounds is independent of attention.](https://www.ncbi.nlm.nih.gov/pubmed/23281832)    

## Overview

### Theory
Our motor actions are preceded by a corollary discharge of the expected sensation in sensory cortex. This copy does not produce movement itself but it's directed to other regions of the brain to inform them of the following action. This mechanism is thought to be allowing animals to suppress responses which are self-generated, which helps to process sensational information more efficiantly.

### Project    
We tried to replicate the results gotten by [Judith M. Ford et al., 2013](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4059422/).   
In was mentioned in that research paper that during talking patients with schizophrenia show less evidence of pretalking activity and less suppression of the speech sound. They tried to replicate the same effect with pressing a button followed by a tone. Their research included 26 schizophrenia patients and 22 healthy control subjects.   

### Data analysis
The data is gotten from [Kaggle](https://www.kaggle.com/broach/button-tone-sz). We use ERP data from 9 electrodes from 32 control subjects and 49 schizophrenia patients.   
As in the research that we follow, we also remove button-press activity from button-press-tone ERPs. We also measured N1 and P2 between 80 and 100 ms and 150 and 190 ms, respectively, as in the paper, after tone onset, relative to baseline (−100 to 0 ms) at frontal (Fz), frontal-central (FCz), and central (Cz).


## Contributors:

[Karl Jääts](https://github.com/karljaats)  
[Mihkel Kruusi](https://github.com/mihkelkruusi)  
[Siim Karel Koger](https://github.com/siimkkoger)  