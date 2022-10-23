# BIOL3207_Assignment2

The generally workflow of the study utilises the dataset "OA_activitydat_20190302_BIOL3207.csv". **If replicating the study, use this dataset**. Initially the dataset 
is loaded in in Task 1. This is to load the dataset object into the R studio space allowing more data wrangling and manipulation of the dataset. Github was 
used to track changes to the R studio document throughout the study and saved to my person Github account.

The goal of the study was to conduct a meta-analysis on ocean acidification effects on behaviour. This involved taking data from the Clark et al. (2020) paper named under
"clark_paper_data.csv" and incorporating it in the larger dataset within "OA_activitydat_20190302_BIOL3207.csv" in Task 1.

The dataset is on ocean acidification effects on fish behaviour that was published in Nature in 2020. The dataset includes several columns including loc, species, treatment, animal_id, sl, size, activity and a comment. More details can be found below:

loc			Location, and year, where the data were collected. AIMS = Australian Institute of Marine Science; LIRS = Lizard Island Research Station
species			Species name: acantho = Acanthochromis; Ambon = Pomacentrus amboinensis; Chromis = Chromis atripectoralis; Humbug = Dascyllus aruanus; Lemon = Pomacentrus moluccensis	
treatment		Elevated CO2 [CO2] (850-1,050 µatm) or control [Control] (400 - 450 µatm) groups
animal_id		Fish identity
sl			Standard length of the fish in mm
size			Size grouping of the fish, separated at 15 mm standard length into 'big' or 'small'
activity		Number of seconds the fish was active per minute, averaged across the duration of the trial
comment			Comment with notes on the origin of the data

The combination dataset between "OA_activitydat_20190302_BIOL3207.csv" and "clark_paper_data.csv" was further merged with a larger meta-analysis dataset in Task 3 called "meta-data_ocean_meta.csv" which contained further studies, summary statistics and other metadata. These three datasets, in combation, was used for the meta-analysis tasks
presented in the study. The combined dataset had the following metadata columns:

Study   Unique identifer for each study
Authors   Authors surname in relation to each study
Year    (online)	Year the final paper was made available online
Year    (print)	Year the final paper was included in a journal volume/issue
Title	    Title of each paper
Journal	    Journal the paper was published in
Pubyear IF	    The journal impact factor for the year the paper was published; obtained from InCites Journal Citation Reports
2017 IF	    The journal impact factor for 2017 (i.e., most recent journal impact factor); obtained from InCites Journal Citation Reports
Average n	    Average sample size for the study; average of indiviudal sample sizes for the contol and experimental groups
Effect    type	The type of effect concluded by the study regarding the effect of OA on behaviour; strong, weak, or no effect (see Supplementary Methods for details)
Species	    The species used in each individual experiment
Climate     (FishBase)	Climatic region for each species; obtained from FishBase
Env     cue/stimulus?	Whether or not the experiment included a cue or stimulus in the experiment (olfactory, visual, auditory, or physical)
Cue/stimulus    type	The type of cue or stimulus used
Behavioural metric	    The specific measure of behaviour tested
Life stage	    Life stage of the fish tested
ctrl.n	    Sample size of the control group
ctrl.mean	    Mean of the control group
ctrl.sd	    The standard deviation of the control group, calculated from ctrl.vartype
oa.n	    Sample size of the experimental group
oa.mean	    Mean of the experimental group
oa.sd	    The standard deviation of the experimental group, calculated from ctrl.vartype

The data was initially cleaned up by removing missing data. The data was used to calculate the necessary statistics for study this included removing all negative control and oa 
means for the calculation of the log response ratio for each study.

This study was an experimental study across 5-6 different reef fish that looked
at comparing the effect of elevated CO2 (in ppm) relative to some control on fish behaviour and investigate the three outcomes:

- estimate the overall effect of ocean acidification on behaviour and determine if these effects are general across studies conducting similar experiments;
- understand how variable the effect size is within the literature
- what factors (biological, methodological, publication practices) explain variation in effect size.

The study uses a range of different libraries including pacman, dplyr, bookdown, tidyverse, ggforce, flextable, latex2exp, png, magick. 
These packages enable library loading/installing, rendering and datatable capabilites.
