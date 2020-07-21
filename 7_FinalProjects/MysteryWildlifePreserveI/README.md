# Mystery at the Wildlife Preserve I

## Background
Mistford is a mid-size city is located to the southwest of a large nature preserve. The city has a small industrial area with four light-manufacturing endeavors.  Mitch Vogel is a post-doc student studying ornithology at Mistford College and has been discovering signs that the number of nesting pairs of the Rose-Crested Blue Pipit, a popular local bird due to its attractive plumage and pleasant songs, is decreasing! The decrease is sufficiently significant that the Pangera Ornithology Conservation Society is sponsoring Mitch to undertake additional studies to identify the possible reasons. Mitch is gaining access to several datasets that may help him in his work, and he has asked you (and your colleagues) as experts in visual analytics to help him analyze these datasets.

## Task 1:  Vehicle Patterns of Life

As part of his investigation, ornithology student Mitch Vogel needs to examine the movement of traffic through the Boonsong Lekagul Nature Preserve. His first working hypothesis is that there is some link between the traffic going through the preserve and the decline in the nesting Rose-crested Blue Pipit—maybe the traffic noises are drowning out mating calls! Or perhaps he can discover some odd goings on in the traffic patterns—perhaps campers are invading the bird’s habitat areas?

There are park rangers working as caretakers of the nature preserve, and they have been collecting traffic data for their annual reporting to the local government. They have provided Mitch with some data, explanations about the data, and a map. Mitch feels unprepared to analyze this information alone and is asking you to help with your data analytics prowess. Use data analytics to explore the available data and develop responses to the questions below. 

### Data - *[Download](https://github.com/emmanueliarussi/DataScienceCapstone/tree/master/7_FinalProjects/MysteryWildlifePreserve/data/task1.zip)*

You are provided with a description of how traffic through the Preserve occurs and how traffic was measured through
the sensors. You are also given some background information about the Preserve and bitmapped files describing the gridded map against which the data is provided. The data contains a timestamp of when the vehicle passed a sensor location, a car-id, a car type (as described in the background information), and a sensor identification.


### Goals

1. “Patterns of Life” analyses depend on recognizing repeating patterns of activities by individuals or groups. Describe up to six daily patterns of life by vehicles traveling through and within the park. Characterize the patterns by describing the kinds of vehicles participating, their spatial activities (where do they go?), their temporal activities (when does the pattern happen?), and provide a hypothesis of what the pattern represents (for example, if I drove to a coffee house every morning, but did not stay for long, you might hypothesize I’m getting coffee “to-go”).
2. Patterns of Life analyses may also depend on understanding what patterns appear over longer periods of time (in this case, over multiple days). Describe up to six patterns of life that occur over multiple days (including across the entire data set) by vehicles traveling through and within the park. Characterize the patterns by describing the kinds of vehicles participating, their spatial activities (where do they go?), their temporal activities (when does the pattern happen?), and provide a hypothesis of what the pattern represents (for example, many vehicles showing up at the same location each Saturday at the same time may suggest some activity occurring there each Saturday).
3. Unusual patterns may be patterns of activity that changes from an established pattern, or are just difficult to explain from what you know of a situation. Describe up to six unusual patterns (either single day or multiple days) and highlight why you find them unusual.
4. What are the top 3 patterns you discovered that you suspect could be most impactful to bird life in the nature preserve? 

## Task 2: Plume Analysis

The primary job for Mitch is to determine which (if any) of the factories may be contributing to the problems of the Rose-crested Blue Pipit. Often, air sampling analysis deals with a single chemical being emitted by a single factory. In this case, though, there are four factories, potentially each emitting four chemicals, being monitored by nine different sensors. Further, some chemicals being emitted are more hazardous than others. These factories were supposed to be compliant with recent years’ environmental regulations but Mitch had his doubts that the actual data has been closely reviewed. Substances of concern include:

* *Appluimonia* – In general, most substances that cause odors in the outdoor air are not at levels that can cause serious injury, long-term health effects, or death to humans or animals. However, odors may affect quality of life and sense of wellbeing. Several odor-producing substances, including Appluimonia, are monitored.
* *Chlorodinine* – Corrosives are materials that can attack and chemically destroy exposed body tissues. They might be hazardous in other ways too, depending on the particular corrosive material. An example is the chemical Chlorodinine which is harmful if inhaled or swallowed.
* *Methylosmolene* – This is a trade name for a family of volatile organic solvents. This chemical was strictly regulated in the manufacturing sector. Liquid forms of Methylosmolene are required by law to be chemically neutralized before disposal.
* *AGOC-3A* – New environmental regulations and consumer demand have led to the development of low-VOC (Volatile Organic Compounds) and zero-VOC solvents. Most manufacturers now use one or more low-VOC substances and Mistford’s plants have wholeheartedly signed on. These new solvents, including AGOC-3A, are less harmful to human and environmental health.

Your task, as supported by data analytics that you apply, is to detangle the data to help Mitch determine where problems may be. Use data analytics to explore the available data and develop responses to the questions below. 

### Data - *[Download](https://github.com/emmanueliarussi/DataScienceCapstone/tree/master/7_FinalProjects/MysteryWildlifePreserve/data/task2.zip)*

Mitch discovered that the state government has been monitoring the gaseous effluents from the factories through a set of sensors, distributed around the factories, and set between the smokestacks, the city of Mistford and the nature preserve. The state gave Mitch access to their air sampling data, meteorological data, and locations map. Data includes meteorological data that provided wind speed and direction for certain periods of time and sensor data for three months’ worth of readings with the chemical detected, the sensor id, the reading in parts per million, and the
date/time. 

### Goals

1. Characterize the sensors’ performance and operation. Are they all working properly at all times? Can you detect any unexpected behaviors of the sensors through analyzing the readings they capture?
2. Now turn your attention to the chemicals themselves. Which chemicals are being detected by the sensor group? What patterns of chemical releases do you see, as being reported in the data? 
3. Which factories are responsible for which chemical releases? Carefully describe how you determined this using all the data you have available. For the factories you identified, describe any observed patterns of operation revealed in the data.

## Task 3: Multispectral Imagery

Mitch Vogel, the ornithology student who is most concerned about the plight of the Rose-crested Blue Pipit, is able to get around some of the nature preserve to study the bird, but because of the terrain and the vegetation he is not able to cover the entire preserve with a car or on foot. Drones and air vehicles would scare the birds making it difficult to assess the extent of the possible problem. While he puzzles out how to get a more complete picture, he talked with one of his professors at Mistford College who suggested he look at imagery over the area over the past few years.

Perhaps, the professor mused, there have been changes in the flora that are related to issues with fauna. Mitch thought this kind of associated study may be informative, so the professor provided him with some images of the preserve collected by the National Space Service. However, they are multi-spectral image files, which Mitch had never dealt with before. The image analysis packages he found online were very complicated to work with, so he has asked you, a data analytics expert, to help him view and understand this data. Use data analytics to explore the available data and develop responses to the questions below.

### Data - *[Download](https://github.com/emmanueliarussi/DataScienceCapstone/tree/master/7_FinalProjects/MysteryWildlifePreserve/data/task3.zip)*

A challenging component of this image dataset is that it is multispectral, that is, there are three other wavelength channels included beyond red, green, and blue. As mentioned, we provide a multispectral analysis primer to assist you with the analysis. We are specifically looking for you to go beyond simple displays of the image data and that employ interesting data and visual analytics to support investigation into the changes in the area over time. 

### Goals

1. Boonsong Lake resides within the preserve and has a length of about 3000 feet (see the Boonsong Lake image file). The image of Boonsong Lake is oriented north-south and is an RGB image (not six channels as in the supplied satellite data). Using the Boonsong Lake image as your guide, analyze and report on the scale and orientation of the supplied satellite images. How much area is covered by a pixel in these images? 
2. Identify features you can discern in the Preserve area as captured in the imagery. Focus on image features that you are reasonably confident that you can identify (e.g., a town full of houses may be identified with a high confidence level). 
3. There are most likely many features in the images that you cannot identify without additional information about the geography, human activity, and so on. Mitch is interested in changes that are occurring that may provide him with clues to the problems with the Pipit bird. Identify features that change over time in these images, using all channels of the images. Changes may be obvious or subtle, but try not to be distracted by easily explained phenomena like cloud cover. 

## Deliverables

Please prepare __a single python notebook__ with the answers __for each task__. However, feel free to use more than a single python file to solve tasks. If necessary, some results may be pre-computed and stored in separate files. Notebooks must clearly explain the answers to each question, supported by evidence derived from the data and visualized using the tools seen in the course. Describe the characteristics of the data you were given as well as your reasoning process leading to each answer. Use the following structure template for the answers notebook:

- project title, task name
    - description and data characterization 
    - answer question 1
    - answer question 2
    - ...

