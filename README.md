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
- [Using concurrent EEG and fMRI to probe the state of the brain in schizophrenia](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5008052/)  
- [Meditation (Vipassana) and the P3a event-related brain potential](https://www.ncbi.nlm.nih.gov/pubmed/18845193)  
- [The N1-suppression effect for self-initiated sounds is independent of attention.](https://www.ncbi.nlm.nih.gov/pubmed/23281832)    

## Summary
bacon ipsum...

## Contributors:

[Karl Jääts](https://github.com/karljaats)  
[Mihkel Kruusi](https://github.com/mihkelkruusi)  
[Siim Karel Koger](https://github.com/siimkkoger)  