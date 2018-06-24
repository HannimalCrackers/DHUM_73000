# Instagram Image Exploration and AI Analysis

&nbsp;


## Introduction

This project had two goals. First, I explored methods for including images in Tableau, so that visualizations about Instagram or other image data could include the relevant visual reference. Second, I delved into the research question, how do the results of AI image analysis correspond or differ from my own assignation of labels to my own Instagram photos? Audiences for this analysis are myself, as I like my photos and enjoy working with them, along with those who are interested in the inclusion of imagery in Tableau or the current state of AI assisted image analysis.


&nbsp;


## Data Source

To explore this question I downloaded my personal photos and data from Instagram using their recently implemented Data Download tool. Instagram only recently began making users’ personal data available to them. It did so in order to be compliant with the European Union’s GDPR privacy law which went into effect May 25, 2018. Users may now easily download a package of their personal user data. The data package I downloaded contained multiple JSON files along with subfolders for photos and videos, as shown in the visual below. Photos were in jpeg format, videos were MP4s – both easily accessible formats.

&nbsp;
![screenshot](https://raw.githubusercontent.com/HannimalCrackers/DHUM_73000/master/img/Instagram_download.png)
&nbsp;

My data contained 265 photos and 3 videos. Due to time and resource constraints, I focused on my 50 most recent posts, excluding selfies and videos.

&nbsp;


## Data Preparation

The media.JSON file was the only JSON file I used for this project. The media file contains information on the content of the user’s posts, including fields for caption, location, and timestamp. I prepped the data as follows.
The field giving date and time of the post came in as string. I converted it to a Date & Time field in Tableau as part of general cleanup, though I did not end up making use of that field for this project. Image names for the photos were only provided as part of path, so I split the path to create an image name field. The image names were awkwardly long and unintelligible. I wanted image names that would be quicker to reference and which would provide information on when the image was posted. I determined my desired nomenclature, which would be to add a prefix to each image consisting of a unique serial index key (starting at the number 1 for the first image) and the year and month of the post in YYYYMM format. This yielded image filenames which were somewhat easier to identify from looking at just the first few characters, though they were still clunky, as I’d decided to retain the original image name in the filename in case it came in useful (it was not useful). The exhibit below shows my naming system. I created the new filenames as a Calculated Field in Tableau, then exported the old and desired filenames into a .CSV. I automated the filename changing process by batch renaming using the .CSV and commands in Terminal. Then I copied the 50 renamed images I was using as my dataset for this project into a separate folder.

&nbsp;
![screenshot](https://raw.githubusercontent.com/HannimalCrackers/DHUM_73000/master/img/FilenameKey.png)
&nbsp;


## Visualization A: Top Locations Bar Chart with Images in Tooltip

Visualization A: Top Locations Bar Chart with Images in Tooltip
I was able to accomplish my first aim by embedding images in the Tableau tooltips, as I have done in the segmented bar chart below. This chart shows locations or regions I tagged at least twice times in my 50 most recent posts. 14 records did not have location data, so they were excluded. Three of the four categories in the visualization below are in Iceland (I vacationed there in March), but I preferred to keep them separate rather than lumping them into one large “Iceland” category as that would have made the bar chart imbalanced and hard to read. The non-Icelandic location is the Lloyd Sealy Library at John Jay College of Criminal Justice, where I recently finished a bachelor’s degree. 
Including images in the tooltips makes the visualization more engaging and provides a richer experience than descriptive words or metadata alone.
User note: hover over a section of the bar chart to see images displayed.

&nbsp;

  {% include aidash-locations.html %}

  &nbsp; &nbsp; &nbsp; &nbsp;
 
 
  {% include aidash-clouds-combined.html %} 

  {% include aidash-clouds.html %} 
 
  &nbsp; &nbsp; &nbsp; &nbsp;
  
  
  {% include aidash-labelbar.html %} 
  
  &nbsp; &nbsp; &nbsp; &nbsp;

  
  {% include aistatic-labels.html %} 

  &nbsp; &nbsp; &nbsp; &nbsp;
  

< [There's no place like home](./index.md)
