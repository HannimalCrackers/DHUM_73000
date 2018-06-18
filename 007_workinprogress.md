# WIP: learnings, data prep, notes

#### Things I'm learning working on the final project

* How to make a bulleted list in markdown with an asterisk then a space
    * How to make nested lists in markdown

&nbsp;
* That my GitHub directory was already getting messy
    * Renamed all blogposts with ###_ prefix to order and sort to top
    
&nbsp;
* How to custom split columns in the Data Source pane in Tableau

&nbsp;
* Challenge: how to split caption string to get hashtags isolated
    * Ok, got all hashtags split off and the hash character re-added but it probably took too many CALCs and it's adding hashtag characters to the empty fields as well. Not best use of time to keep going at this. Tabling (haha is that a pun?) and moving on.
    
&nbsp;
* **I used commands I didn't understand in Terminal to batch rename my images, even though it was scary.**
    * [StackExchange source](https://apple.stackexchange.com/questions/236213/renaming-files-names-in-bulk-any-smarter-solution)
    * Update from 2 days later: After all the quality time with Terminal during my Python misadventure, I'm much more comfortable with it
    
&nbsp;
* [I can only pivot once per workbook.](<a href="//imgur.com/iWKad22">Picard facepalm HD</a>)
    

&nbsp; &nbsp; &nbsp; &nbsp;


#### Questions for tech work session
* How to structure Python query to pull image data from Google Cloud

* Can't seem to add any other data sources to JSON

* How could I have done the hashtag splitting and readding more accurately and effectively?


    
&nbsp; &nbsp; &nbsp; &nbsp;


#### Data prep
* Data downloaded from Instagram 180607. Received photos as JPGs, videos as MP4s, multiple JSON files. I excluded videos from this project.

&nbsp;
* Tableau: I used only media.json. Field with date and time came in as string, converted to Date & Time field

&nbsp;
* Image names only provided as part of path, so split path to access name only data

&nbsp;
* Created CALC to create new name field for images with image index # and YYYYMM info at beginning

&nbsp;
* Created CALCs to split out hashtags from captions, which removed hashtag character so I created more CALCs to add hashtag back in. Ended up with way too many CALCs probably. Also it added the hashtag character to all fields, not just the ones with data.

&nbsp;
* Batch renamed images to match name CALC from Tableau using commands in Terminal

&nbsp;
* Selecting most recent 50 photos (not including any selfies) to work with. This may be too ambitious. Oldest image in set is from October 2017.

&nbsp;
* Pulling out top 5 results from Google Vision for analysis and pasted into Excel file

&nbsp; 
* Manually entered my 5 labels for each image into another sheet on the Excel file

&nbsp; 
* Could not get my Excel sheets into Tableau with the JSON data from Instagram loaded, so exported JSON data, along with the field calculations into a CSV. Took the opportunity to clean up data in Excel. I deleted the hashtag symbols that were filling what should have been null fields. Fixed some data which had come in in wrong columns. Removed extra words after the hashtags that came in when I used hashtags in the middle of sentences.

&nbsp;
* Loaded the cleaned up data from the formerly JSON media file into Tableau. Then joined the Excel with sheets listing Google Vision's labels and my labels. I used an inner join, so that only the set of 50 images which were labeled would appear. I checked the number of records quickly on Sheet 1 to confirm that there were 50 records.



&nbsp; &nbsp; &nbsp; &nbsp;

#### Results notes
&nbsp;
* Non-American spellings and terms (neighbourhood, loch, archaeological, jewellery) mixed in with American spellings (jewelry)

&nbsp;
* Some images returned fewer than 5 results. One image returned no results.



&nbsp; &nbsp; &nbsp; &nbsp;

#### Process notes - so I can retrace my steps later and do Python right

&nbsp;
* Created a Google Cloud account and uploaded my image set into a bucket named dhum73000-imageset-180615
&nbsp;
* Google Cloud Vision API setup. Created sample app in tutorial in Google Cloud Shell. Installed Python 2.7.13. Downloaded Brackets and Sublime Text.
&nbsp;
* Downloaded Google Cloud SDK. Now I'm back in terminal. Does this all happen in Terminal? It's 1:00am on technically-Saturday and my life just got complicated. Calling it a night soon.
* Used Homebrew to install Python 3 and a Python 2.7.16 via Command line.
* 6/16
* 1pm: [Current questions](https://docs.google.com/presentation/d/1oq3hsq7qOgkFmn7fg6CCQDI_6x2zVZVOMpbbTcDpbSk/edit?usp=sharing)
    * Maybe I don't need to use the SDK. Can I do this all in Google Cloud Shell?
* 1:30pm: setting up a [Python development environment](https://cloud.google.com/python/setup)
* 2:30pm: setting up Python seems complicated and hopefully overkill for what I need. Seeing if I can just make a C# script instead.
* 3:40pm: I kept bashing my head against the Python wall. Trying C# solution in MonoDevelop instead for real now. 
    * Went back to Python. It keeps having trouble finding my Google Cloud SDK when I try to run scripts. Not every time, but often.
* 6:30pm: Giving up on getting batch results through code. Running image links through Interactive API one by one.
* Probably need to wipe my current installs of everything (if possible) and start fresh. Google Cloud SDK isn't in correctly. I don't understand Homebrew and not sure that install went correctly either. Also the EnvWrapper was being weird, and really wanted me to have things in my user directory as opposed to the root level Library > Frameworks place that 2.7.13 was in.


  &nbsp; &nbsp; &nbsp; &nbsp;
  

< [There's no place like home](./index.md)
