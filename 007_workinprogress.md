# WIP: learnings, data prep, notes

#### Things I've learned so far working on the final project

* More markdown features
    * How to make a bulleted list in markdown with an asterisk then a space
    * How to make nested lists in markdown
    * ~~strikethrough~~

&nbsp;
* That my GitHub directory was already getting messy
    * Renamed all blogposts with ###_ prefix to order and sort to top
    
&nbsp;
* How to custom split columns in the Data Source pane in Tableau
    
&nbsp;
* **I used commands I didn't understand in Terminal to batch rename my images, even though it was scary.**
    * [StackExchange source](https://apple.stackexchange.com/questions/236213/renaming-files-names-in-bulk-any-smarter-solution)
    * Update from 2 days later: After all the quality time with Terminal during my Python misadventure, I'm much more comfortable with it
    
&nbsp;
* I can only pivot once per workbook. (<a href="//imgur.com/iWKad22">Picard facepalm</a>)

&nbsp;
* Pivoting is sometimes the entirely wrong move. (<a href="//imgur.com/jiFfM.jpg">Double facepalm</a>)


    
&nbsp; &nbsp; &nbsp; &nbsp;


# Data prep
* Data downloaded from Instagram 180607. Received photos as JPGs, videos as MP4s, multiple JSON files. I excluded videos from this project.

&nbsp;
* Tableau: I used only media.json. Field with date and time came in as string, converted to Date & Time field

&nbsp;
* Image names only provided as part of path, so split path to access name only data

&nbsp;
* Created CALC to create new name field for images with image index # and YYYYMM info at beginning

&nbsp;
* Leaded in the media JSON file and created CALCs to split out hashtags from captions, which removed hashtag character so I created more CALCs to add hashtag back in. Ended up with way too many CALCs probably. Also it added the hashtag character to all fields, not just the ones with data.

&nbsp;
* Batch renamed images to match name CALC from Tableau using commands in Terminal

&nbsp;
* Selecting most recent 50 photos (not including any selfies) to work with. This may be too ambitious. Oldest image in set is from October 2017.

&nbsp;
* Pulling out top 5 results from Google Vision for analysis and pasted into Excel file

&nbsp; 
* Manually entered my 5 labels for each image into another sheet on the Excel file

&nbsp; 
* Could not get my Excel sheets into Tableau with the JSON media data from Instagram loaded, so exported JSON media data along with the field calculations I created into a CSV. Took the opportunity to clean up data in Excel. I deleted the hashtag symbols that were filling what should have been null fields. Fixed some data which had come in in wrong columns. Removed extra words after the hashtags that came in when I used hashtags in the middle of sentences.

&nbsp;
* Loaded the cleaned up data from the formerly JSON media file into Tableau. Then joined the Excel with sheets listing Google Vision's labels and my labels. I used an inner join, so that only the set of 50 images which were labeled would appear. I checked the number of records quickly on Sheet 1 to confirm that there were 50 records.

&nbsp;
* Discovered immediately that there can only be one pivot per workbook in Tableau. I needed both the Google Vision Labels and My Labels sheets to pivot (technically unpivot). Could not find quick way to do it on Excel for Mac, so brought each sheet into Tableau, pivoted, and exported a CSV separately. Brought both CSVs into Tableau and tried joining to the media data, but column header names in one of my CSVs were not being read correctly and wouldn't join. So I opened both CSVs and saved as Excel. Then brought both sheets back into Tableau. It's still bringing in each record 5 times because it's multiplying my labels by Google Vision's labels.

&nbsp;
* Pasting the two labels sheets together into a single Excel sheet. Also fixing the mismatched capitalization while I'm at it. Google Vision used lowercase for labels. I realized when I saw the word clouds that I used initial caps. To fix this I had to use a calculation in Excel to switch all my labels to lowercase, then I went through and manually removed the calculation from the cells that had proper names to preserve those capitalizations.

&nbsp;
* This fixed how many times each label appears. But each image shows 10 records – one record each for every label from Google Vision and myself. Maybe I shouldn't have pivoted (technically unpivoted) the data? Leaving my word clouds dashboard as is because it's already posted and linked, but starting fresh for my locations chart.

&nbsp;
* I brought in data fresh into my Locations workbook without any pivoting action and everything worked correctly. Pivoting was the wrong move.

&nbsp; &nbsp; &nbsp; &nbsp;


# Questions for tech work session
* How to structure Python query to pull image data from Google Cloud

* How could I have done the hashtag splitting and re-adding more accurately and effectively?

* CALC to join all hashtags returning Null when I try to concatenate all hashtags

* ~~Can't get a CALC to only show locations with 2 or more records (I had to manually exclude, sloppy)~~

* Note: can't add more info to image tooltip


&nbsp; &nbsp; &nbsp; &nbsp;

# Process notes so I can retrace my steps later

&nbsp;
6/15
&nbsp;

* Created a Google Cloud account and uploaded my image set into a bucket named dhum73000-imageset-180615
* Google Cloud Vision API setup. Created sample app in tutorial in Google Cloud Shell. Installed Python 2.7.13. Downloaded Brackets and Sublime Text.
* Downloaded Google Cloud SDK. Now I'm back in terminal. Does this all happen in Terminal? It's 1:00am on technically-Saturday and my life just got complicated. Calling it a night soon.
* Used Homebrew to install Python 3 and a Python 2.7.16 via Command line.

&nbsp;
6/16
&nbsp;

* 1pm: [Current questions](https://docs.google.com/presentation/d/1oq3hsq7qOgkFmn7fg6CCQDI_6x2zVZVOMpbbTcDpbSk/edit?usp=sharing)
    * Maybe I don't need to use the SDK. Can I do this all in Google Cloud Shell?
* 1:30pm: setting up a [Python development environment](https://cloud.google.com/python/setup)
* 2:30pm: setting up Python seems complicated and hopefully overkill for what I need. Seeing if I can just make a C# script instead.
* 3:40pm: I kept bashing my head against the Python wall. Trying C# solution in MonoDevelop instead for real now. 
    * Went back to Python. It keeps having trouble finding my Google Cloud SDK when I try to run scripts. Not every time, but often.
* 4:00pm: Set up authentication key for API
* 6:30pm: Giving up on getting batch results through code. Running image links through Interactive API one by one.

&nbsp;
6/17
&nbsp;

* Probably need to wipe my current installs of everything (if possible) and start fresh. Google Cloud SDK isn't in correctly. I don't understand Homebrew and not sure that install went correctly either. Also the EnvWrapper was being weird, and really wanted me to have things in my user directory as opposed to the root level Library > Frameworks place that 2.7.13 was in, but even after I copied into my local directory it couldn't find them there. Best to start fresh.


  &nbsp; &nbsp; &nbsp; &nbsp;
  

< [There's no place like home](./index.md)
