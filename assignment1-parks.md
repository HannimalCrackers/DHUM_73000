
# NYC Parks Violations Complaints to 311 in 2015

#### Introduction

How does the New York City Department of Parks and Recreation (Parks Dept) respond to citizen complaints about violations of parks rules, and how are enforcement resources allocated? Insights can be gleaned from official responses to requests submitted to the 311 citizen hotline.

Interested audiences for this analysis include (1) Parks Dept management, who might like to see how their employees are choosing to enact enforcement, and (2) the citizens of NYC, who are interested parties in how their taxes are being spent and their public lives are being regulated while in parks.

To explore this research question, I used a dataset made publicly available by the NYC government which contains all 311 Service Requests made in the year 2015. The dataset filename as downloaded is 311_Service_Requests_from_2015.csv. All visualizations in this post are built from this dataset using Tableau Public. 

Explanations of the data and design decisions made are included in the discussions with each visualization, rather than in a separate section.

  &nbsp; &nbsp;

#### Visualization A: Number of Complaints Table

This table shows complaints received by 311 about various types of behavior in parks. Complaint types are listed at left, with the total number of complaints received about each in 2015 shown in the column at right. The numbers column is color coded as a heat map along a light-to-dark spectrum, with the least common complaint category (Other Complaints) in the lightest color and the most common complaint category (Obstructing Public Use) in the darkest color. A table is sufficient for displaying this top-level information, while the color coding provides a quick reference for how close to the minimum or maximum any given value is.

The “Other Complaints” category consolidates the relatively few complaints about removing plants or flowers, unauthorized climbing, unauthorized posting of signs, and prohibited use of newly seeded lawns. 
  
  {% include parkschart-table.html %}

  &nbsp; &nbsp;
  
#### Visualization B: Complaints and Response for all NYC Bar Chart

Visualization B is a bar chart showing a horizontal bar for each service request complaint type. The bar length is the total number of records, as shown along the x-axis, and each bar is segmented into colors representing the type of response to the complaint. Hovering over the colored sections in the chart reveals information on the service request complaint type, official response, and number of records in the data segment. Using a bar chart allows for an organized presentation and comparison of the categories, and segmenting the bars gives an extra layer of information. I have been unable to control legend placement the way I’d like.

  {% include parksdash-nyc.html %}

This visualization reveals the existence of a very specific response for complaints about smoking. This response is used only and universally for complaints about smoking. The lack of response and enforcement variation in response to smoking demonstrates a deliberate, centralized decision on the part of the Parks Dept about how to handle these complaints. According to the official response to complaints about smoking, the Parks Dept has determined that it has too limited of resources to enforce the regulation prohibiting it, and has taken steps to be completely consistent in this enforcement decision. This concerted effort at enforcement consistency is laudable, as quality of life violations are sometimes liable to be selectively enforced against minorities.

The legend shows an abbreviated version of the Parks Dept’s limited resources response. The full response text in the database reads “The Department of Parks and Recreation has limited resources to follow up on this complaint. Your complaint will help the City schedule patrols and target particular areas for enforcement.”

  &nbsp; &nbsp;
  
#### Visualization C: Complaints and Response by Borough Bar Chart

This bar chart shows each complaint type broken out by number of service requests per borough, and each borough’s bar is sectioned by response type. Hovering over the colored sections in the chart reveals information on the service request complaint type, borough, official response, and number of records in the data segment.

I chose to place the legend above the bar chart because it is easier to get familiarized with parsing the chart data when the key is close to the beginning of the chart. Again, however, I don't have an ideal level of control over placement and formatting.

  {% include parksdash-borough.html %}
  
This visualization shows that Manhattan has the most complaints in all categories, though by varying degrees. Manhattan has far more complaints than any other borough about obstructing public use and smoking, but is nearly even with the Bronx and Brooklyn in number of complaints about barbequing outside authorized areas, and nearly even with the Bronx and Queens in complaints about unauthorized vendors.

This visualization does not reveal many significant differences in enforcement between boroughs. There were two summons issued as a result of complaints about barbequing in Brooklyn and one in the Bronx. No summons for barbecue complaints were issued in other boroughs. Two summons were issued for biking or rollerblading off-path complaints in Manhattan, with none in any other borough. Overall, enforcement looks proportionally fairly even across boroughs.

  &nbsp; &nbsp;
    
#### Visualization D: Complaint Type Proportions Pie Chart

This pie chart is the final visualization in this series. It represents the same data as Visualization A, the numbers table that was the first visualization in the series. Hovering over wedge sections reveals the number of complaints in each segment. Showing the numbers data in this simple proportional chart provides a quick visual reference and focus for a discussion tying together findings from the previous visualizations.

  {% include parksdash-pie.html %}

We see quickly from this chart that obstructing public access is the most common area of public complaint, comprising 33%, or one in three, of all complaints. It was a significant problem in every borough, as shown in Visualization C. This is also the category, referring back to Visualization B, in which the Parks Dept took the largest number of actions to remedy or correct the situation, up to and including issuing a summons. This is inline with the Parks Dept mission to provide spaces available for public use.

Unlicensed vendors are the next largest category, making up 20%, or one in five, of all complaints. This is also the only other category in which a large number of summons were written. Again, the Parks Dept enforcement priorities are in line with the public’s priorities.

Barbequing outside of authorized areas, the third largest category (17%), shows a different enforcement profile. In over half of the cases the Parks Dept did not take action, usually due to the reason, “resources allocated to other critical services at this time.” This was the most common use of the resources allocated elsewhere response.

The last category that occurred with a frequency above 10% is complaints about smoking. As discussed earlier, smoking complaints have their own category of official response that cite limited resources, and Parks Dept resources are not used to respond to complaints about smoking in any park.

Visualizing the 311 data on parks violations complaints reveals that the Parks Dept does allocate resources in response to the two most common public complaints, but that barbequing and smoking, despite being the third and fourth most common complaints, are not enforcement priorities.

  &nbsp; &nbsp;

#### Next Steps

Having written this assignment and placed my visuals, I now see it would be useful to include a simple bar chart that shows an overview of just the number of complaints by borough, before showing my current Visualization C borough chart with the greater level of detail. Showing overall proportions of complaints per borough first would provide context for interpreting the differences in complaint type and response type by borough shown in Visualization C. Actually, it might make sense to eliminate Visualization C entirely and instead show only a simplified visualization of complaint type by borough.

Another next step is to work on my dashboard execution. The first dashboard I made for this project ended up not being usable. It looks great in Tableau Public, both on desktop and web, but once embedded into this blog it looks terrible. Everything is crashing together unless viewed in full screen mode.

  {% include parks-failcompare.html %}
  
You can see a live version of the messed up overview dashboard at the link below.

  [Link: Dashboard fail](./dashboardfails.md)


My current theories on what may be causing the issues I’m encountering are that they may be the result of using floating containers for the dashboard segments,and/or perhaps GitHub blog pages are not able to display elements this wide.

For this assignment, I ended up creating single-chart dashboards because I wanted to control legend placement, which I believe can only be done on dashboards, but I haven’t yet solved how to get a multi-chart dashboard to display well on the GitHub page.* However, I would like to continue trying to solve this issue, so that I can show a multi-chart overview dashboard. I would like to improve my Tableau formatting abilities overall to be better able to achieve clearer, cleaner, and more compelling visualizations.

  &nbsp;
  &nbsp;
  - - - - - - 
 *post-assignment update: I had a multi-chart dashboard success! [Link: Dashboard success](./dashboardsuccess.md)

  &nbsp; &nbsp; &nbsp; &nbsp;
  

< [There's no place like home](./index.md)
