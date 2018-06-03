
# Lorem Ipsum Titleum

#### Research question

How does the New York City Department of Parks and Recreation (Parks Dept) respond to citizen complaints about violations of parks rules, and how are enforcement resources allocated? Insights can be gleaned from how the city responds to requests submitted to 311.

#### Audience

Interested audiences for this analysis are (1) Parks Dept management, who might like to see how their employees are choosing to enact enforcement, and (2) the citizens of NYC, who are interested parties in how their taxes are being spent and their public lives are being regulated while in parks.

#### Visualizations intro

To explore this research question, I used a dataset made publicly available by the NYC government which contains all 311 Service Requests made in the year 2015. The dataset filename as downloaded is 311_Service_Requests_from_2015.csv. All visualizations in this post are built from this dataset using Tableau Public. 

Explanations of the data and design decisions made are included in the discussions with each visualization, rather than in a separate section.

#### Visualization A: Number of Complaints Table

This table shows complaints received by 311 about various types of behavior in parks. Complaint types are listed at left, with the total number of complaints received about each in 2015 showninthecolumnatright. The numbers column is color coded as a heat map along a light-to-dark spectrum, with theleast common complaint category (Other Complaints) in the lightest color and the most common complaint category (Obstructing Public Use) in the darkest color.

The “Other Complaints” categoryconsolidatesrelatively few complaints about removing plants or flowers, unauthorized climbing, unauthorized posting of signs, and prohibited use of newly seeded lawns. 
  
  {% include parkschart-table.html %}

  &nbsp; &nbsp;
  
#### Visualization B: Complaints and Response for all NYC Bar Chart

Visualization B is a bar chart showing a horizontal bar for each service request complaint type. The bar length is the total number of records, as shown along the x-axis, and each bar is segmented into colors representing the type of response to the complaint. Hovering over the colored sections in the chart reveals information on the service request complaint type,official response, and number of records in the data segment.

  {% include parksdash-nyc.html %}

This visualization reveals the existence of a very specific response for complaints about smoking. This response is used only and universally for complaints about smoking. The lack of response and enforcement variation in response to smoking demonstrates a deliberate, centralized decision on the part of the Department of Parks and Recreation (Parks Dept) about how to handle these complaints. According to the official response to complaints about smoking, the Parks Dept has determined that it has too limited of resources to enforce the regulation prohibiting it, and has taken steps to be completely consistent in thisenforcementdecision. This concerted effort at enforcement consistency is laudable, as quality of life violations are liable to be selectively enforced against minorities.

The legendshowsan abbreviated version of the Parks Dept’s limited resources response. The full response text in the database reads“The Department of Parks and Recreation has limited resources to follow up on this complaint. Your complaint will help the City schedule patrols and target particular areas for enforcement.”

  &nbsp; &nbsp;
  
  
  This is parksdash-borough

  {% include parksdash-borough.html %}

  &nbsp; &nbsp;
  
  
  This is parksdash-pie

  {% include parksdash-pie.html %}

  &nbsp; &nbsp;



  This is the fail compare image

  {% include parks-failcompare.html %}

  &nbsp; &nbsp;
  
  
  You can see a live version of the messed up overview dashboard at the link below.

  [Link: Dashboard fail](./dashboardfails.md)

  &nbsp; &nbsp;
  

# Lorem ipsum

## Lorem ipsum

### Lorem ipsum

#### Lorem ipsum

&nbsp;

< [There's no place like home](./index.md)
