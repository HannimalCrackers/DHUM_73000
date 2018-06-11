# Looking for Factors in Overall Calorie Consumption

#### Introduction

I started with a simple question: does increasing sugar intake one day lead to higher calorie consumption the next day? I had a hunch it did, and – having tracked my eating habits with MyFitnessPal for some time – I had the data to explore my hypothesis.

Upfront, I’ll say I was wrong. My data showed no positive correlation between increased sugar intake and subsequent increased caloric intake. If anything, I tend to eat less the next day. I expanded my question to look at whether protein or fat might have the effect I was looking for. Higher proportional protein intake shows some correlation with steadier low caloric intake, but further investigation is needed.

This research was done primarily for myself, as I was curious about my own cravings, but those looking to see what kind of exploration may be done with downloaded personal MFP data (or those looking for some very tenuous evidence that indulging now and then will not instantly doom their diet) may be interested in reading on. 

&nbsp;

#### Data Source and Preparation

I explored this question with my downloaded personal data from MFP, utilizing fields that captured date along with calories consumed, sugar consumed – which was provided in grams, and protein and fat consumed – both also provided in grams. In order to better compare sugar, protein and fat intake to overall caloric intake, I created calculated fields in Tableau to convert them from grams to calories.

Then I had a look at my data. I had not always been careful about making sure nutritional breakdowns were included for the items I’d logged. I went back to the app and went through day by day updating items where I could, and making note of when the information simply wasn’t available (usually due to eating out at a restaurant that did not provide such information).

I decided to completely exclude the days that I didn’t have complete nutrition details. To accomplish this I set up a separate spreadsheet with a column titled Date and second column titled Nutrition Unknown. I filled this in with the dates for which I lacked complete information, and typed an X into the Nutrition Unknown column. I married this information to the MFP data by performing a left join on the Date field.

Last, I needed to select a date range to analyze. My first completely tracked day using MFP was October 9, 2017. I decided to start my analysis on that date and look at all available information through the end of that year.


&nbsp;

#### Visualization A: Examination of Sugar Intake

Below is a dashboard showing two combination bar and line charts. The pale orange bars show total calories consumed. There is one bar per day. Gaps indicate dates excluded for missing nutritional information. Sugar calories are depicted with a dark blue line chart running over top of the bars. 

The top chart shows total calories and sugar calories mapped to the same scale (both left and right y-axes are identical). This is useful for showing the proportion of sugar calories to total calories. The bottom chart shows the same total and sugar calorie information, but in this chart the y-axes are unsynchronized. This chart is included because having the sugar data proportionally exaggerated makes it easier to pick out trends.

Specific date and calorie counts are available by hovering over the bars or the line chart nodes. The date range is set to the dates I’ve chosen to analyze, but readers are welcome to browse my full range of data. To that end I included dynamic date range filters.

All charts in this blog are colorblind-friendly due to the high contrast in colors used. All charts include a color key for reference. 

These charts make it easy to see that during this time period I was not more likely to consume more calories the day after eating relatively high amounts of sugar.
    
  {% include mfpdash-sugar.html %}
  
  &nbsp; &nbsp;
  
  
  #### Visualization B: Examination of Protein Intake

  &nbsp; &nbsp;
  
  {% include mfpdash-protein.html %}

  &nbsp; &nbsp;
  
  
  
  #### Visualization C: Examination of Fat Intake
  
  &nbsp; &nbsp; 
  
  {% include mfpdash-fat.html %}
  
  &nbsp; &nbsp;

  

  &nbsp; &nbsp; &nbsp; &nbsp;
  

< [There's no place like home](./index.md)
