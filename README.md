# Effects of the maternal social environment on the mating signals and mate preferences of adult offspring in *Enchenopa* treehoppers

[https://doi.org/10.5061/dryad.bcc2fqzk8](https://doi.org/10.5061/dryad.bcc2fqzk8)

## **Study summary**

Using the treehopper *Enchenopa binotata* we manipulated the egg-laying density of mothers to determine if there would be an effect on the traits of courtship signals or in the mate preference of their offspring. Juvenile offspring were reared in standardized aggregations until adulthood and then sorted by sex to prevent experience and/or mating. Males signaled spontaneously and were recorded. Females were provided artificial playbacks of males, which varied in frequency, and their responses were recorded to determine preference. We detected a strong effect in male signals, with sons of mothers that experienced low aggregation density signaling more. We also detected a weak effect on female mate preferences, with daughters of mothers that experienced low aggregation density being less selective.

## **Software, packages, and versions**

* female playbacks were created in MATLAB 7.5.0 (R2007b)

- analysis was run in R version 4.3.2

*  Rstudio version RStudio 2023.12.1+402 "Ocean Storm" Release (4da58325ffcff29d157d9264087d4b1ab27f7204, 2024-01-28) for windows Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) RStudio/2023.12.1+402 Chrome/116.0.5845.190 Electron/26.2.4 Safari/537.36

- **Used R packages**

1.  glmmTMB # version 1.1.8
2. ggplot2 # version 3.4.4
3. ggpubr # version 0.6.0
4. bbmle # version 1.0.25.1
5. car # version 3.1-2
6. correlation # version 0.8.4

### **Female Data**

**Enchenopa maternal effects pref indv function traits**
This file contains measurements of female Enchenopa binotata mate preferences across three maternal treatments. The individuals in this dataset, represented by a Female ID, are the daughters of mated females who were subject to one of three aggregation densities (3 females/aggregation, 8 females/aggregation, or 15 females/aggregation) during egg-laying. It is important to note as well that this data has been generated from a spline (made in PFunc) of the original female responses across a range of stimuli. For the original response data, please see the holistic data set.

Here, we describe the contents of each column

* Female ID: the number assigned to each female who was assayed in the experiment
* Peak_pref: short for peak preference. This measurement refers to the signal trait value (in this case male dominant signal frequency) which elicits the greatest response ( defined as number of responses in this data)
* peak_height: The height (number of responses) produced at the peak preference
* tolerance: width of the function at a given drop from the peak
* strength: how much female response drops between the most and least preferred male signals
* responsiveness: overall mean elevation of the function
* plant_replicate: the nymph replicate plant the individual came from. As an example of how naming of plant replicates worked, if maternal plant O produced 60 offspring. These offspring would have been split into two replicate plants of 30 upon second instar. These replicates would then be named O1 and O2 respectively.
* treatment: the density treatment the offspring's mother was assigned to
* temp: temperature (Celsius) taken within 40cm of individual at time of recording
* mass: mass (mg) of females after recording
* selectivity_PC1: a selectivity score generated using a principal component comprised of responsiveness, tolerance, and strength

**Enchenopa maternal effects holistic pref analysis**
*This dataset contains the individual response data of each female.*

*Here we describe the contents of each column*

* playback.nb: the playback number. This number refers to a specific random sequence of synthetic playbacks which was unique to each female tested. This way the order of advertisement signals was randomized.
* freq: the dominant frequency of the bout
* resp: the number of times a female responded within a bout of three male signals
* treat: the density treatment the individual's mother was subject to (low, medium, or high)
* plant: the nymph replicate plant the individual came from
* temp: temperature (Celsius) taken within 40cm of individual at time of recording
* mass: mass (mg) of females after recording

### **Male Data**

**Enchenopa maternal effects males**
This data contains all the measurements of the male advertisement signals. Measurements were taken from the third signal produced in a bout. If there was no third signal we measured the last signal in the bout. This dataset also includes general information about survivorship and sex ratio.

Here, we describe the contents of each column

* file: Refers to the name of the original audacity file from which the measurements were taken. File names include the replicate, sex, and the order in which the male was tested in regards to other males from the same replicate plant.
* treatment: the density treatment the individual's mother was subject to (low, medium, or high)
* replicate: the nymph replicate plant the individual came from. As an example of how naming of plant replicates worked, if maternal plant O produced 60 offspring. These offspring would have been split into two replicate plants of 30 upon second instar. These replicates would then be named O1 and O2 respectively.
* egg_mass_count: the number of egg masses present on the original maternal plant at the end of the season. For example, plant O had 46 egg masses from which all O nymph replicates are hatched from.
* number_nymphs_per_replicate: the number of second instar nymphs initially placed on the replicate plant. All but four plant replicates start at 30. Two started at 7, one at 25, and one is marked at 32. The replicate which started at 25 (and was a low density treatment named Y2) is not in the datasheet because no nymph survived to adulthood and thus it was not attributed to any male in the sheet. The other replicate which is listed as starting at 32 was initially 30, but after two nymphs died within 6 hours of sorting we found it prudent to replace them. Thus, we list that there were 32 nymphs, but in reality no more than 30 were ever living on the replicate plant at the same time.
* adult_molts_per_replicate: the number of individuals which survived to the adult stage
* survivorship: the percent of adults that survived to adulthood, male and female
* sex_ratio: proportion of adult males to females (M:F)
* nb.calls: the number of advertisement signals the male produced in the measured bout
* intercall.dur: the time elapsed between signals. Measured as the time between the peak of the measured signal and the peak of the previous signal
* dom.freq: the frequency of the male signal (taken at the highest amplitude of the signal)
* whine.dur: the length of the call whine (male signals are composed of two parts, a whine and a pulse)
* pulse.rate: the number of pulses produced a second in the latter half of the signal
* nb.pulse: the number of pulses produced in the measured signal
* mass: mass (mg) of females after recording
* temp: temperature (Celsius) taken within 40cm of individual at time of recording

### **Survivorship data**

**Plant replicate data**

This data includes the survivorship and final number of sexually receptive adults from each of the plant replicates

*Here, we describe the contents of each column*

**For NA values**: NA values indicate that a count was not recorded that date for whatever reason. As well, if all individuals died on a replicate, subsequent counts and calculations based on those counts were marked as NA

* treatment: the density treatment the individuals' mother was subject to (low, medium, or high)
* replicate: the nymph replicate plant. As an example of how naming of plant replicates worked, if maternal plant O produced 60 offspring. These offspring would have been split into two replicate plants of 30 upon second instar. These replicates would then be named O1 and O2 respectively.
* sex: the sex (male or female) which corresponds with a row for each replicate plant
* initial nymphs: the number of nymphs placed on the replicate plant
* number of adults (date): the count of males and females that day
* final adult count: the total number of adults of each sex from the replicate plant
* total adults: the sum of adult males and females from each replicate plant
* \# of adults that called: the total number of adults which were responsive (e.g. called and/or responded to playbacks) of each sex from the replicate plant
* total responsive adults: the sum of adult males and females which were responsive from each replicate plant
* survivorship: the proportion of adults (male and female) which molted to adulthood from each replicate plant
* proportion called: the proportion of adults (male and female) which were responsive from each replicate plant
* proportion male: the proportion of adult males from each replicate plant

