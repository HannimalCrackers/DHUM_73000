
# Data is in the Eye of the Beholder: Instagram Image Exploration and AI Analysis



## Introduction

In this project I explore my 50 most recent Instagram posts (excluding selfies) and delve into the research question, how do the results of AI image analysis correspond or differ from my own assignation of labels to my own Instagram photos? Audiences for this analysis are myself, as I like my photos and enjoy working with them, along with those who are interested in the current state of AI assisted image analysis.

To explore this question I downloaded my personal photos and data from Instagram. My data prep is detailed (messily) in this supplemental post: [Work in progress](./007_workinprogress.md). Data prep will be more cleanly detailed in my upcoming white paper, to be published on this blog by June 25, 2018.

  &nbsp; &nbsp; 


## Data is in the eye of the beholder

  {% include aistatic-beholder.html %}
  
(That thing is a Dungeons & Dragons monster called a beholder)  

  &nbsp; &nbsp; 
  
  
## Visualization A: Top Locations Bar Chart with Images in Tooltip

Below is a segmented bar chart showing the locations I tagged at least three times in my 50 most recent posts. 14 records did not have location data, so they were excluded. Three of the four categories in the visualization below are in Iceland (I vacationed there in March), but I preferred to keep them separate as the content was quite distinct between them. The fourth location is the library at John Jay College of Criminal Justice, which is one of my favorite places in NYC. In this visualization I was experimenting with incorporating the images of my Instagram posts into Tableau. 

User note: hover over a section of the bar chart to see the relevant image displayed. 

  {% include aidash-locations-preso.html %}
  
  &nbsp; &nbsp; 
  

## Visualizations B & C: Word Clouds of AI Labels vs My Labels

I was curious about the capability of an artificial intelligence to assign appropriate labels to images. To explore this, I uploaded my 50 most recent images to a bucket in Google Cloud, then used the Interactive API embedded on a Google webpage to run each image one by one through the Google Vision AI and copied the labels it returned into a spreadsheet. Separately, I selected five labels myself for each image. 

I then created word clouds to compare the labels the AI came up with to labels I assigned. As shown below, the AI and I agreed that I often take photos of architecture, sky and water. There was very little overlap, however, otherwise. All word clouds show only labels used twice or more.

User notes: more commonly used words appear larger and darker. Hover over words to see how many times they were used as labels. 

&nbsp;

 {% include aidash-clouds-combined.html %} 

 {% include aidash-clouds-preso.html %} 
 

  
  &nbsp; &nbsp; 
  
  
## Visualization C: Select Images Comparing AI Labels vs My Labels

There is a degree of subjectivity in labeling, and my labels are not inherently correct. Still, it's interesting to more closely examine exactly what the AI and I chose for each image. Below is a sampling of images with Vision's top five labels and my own five labels shown alongside. In some instances our labeling was closely aligned. In others, Vision made clear errors or failed to identify the main subject matter. Vision did not always return at least five labels. In one instance shown below it did not venture any labels at all.

User note: the images below are static.
  
  {% include aistatic-labels.html %} 



  &nbsp; &nbsp; &nbsp; &nbsp;
  

< [There's no place like home](./index.md)

