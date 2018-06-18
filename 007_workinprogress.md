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
    

&nbsp; &nbsp; &nbsp; &nbsp;


#### Questions for tech work session
* How to structure Python query to pull image data from Google Cloud

* Can't seem to add any other data sources to JSON


    
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
* Created CALCs to split out hashtags from captions, which removed hashtag character so I created more CALCs to add hashtag back in. Ended up with way too many CALCs probably.

&nbsp;
* Batch renamed images to match name CALC from Tableau using commands in Terminal

&nbsp;
* Selecting most recent 50 photos (not including any selfies) to work with. This may be too ambitious. Oldest image in set is from October 2017.

&nbsp;
* Pulling out top 5 results from Google Vision for analysis and pasted into Excel file

&nbsp; 
* Manually entered my 5 labels for each image into another sheet on the Excel file

&nbsp; 
* Cannot get my Excel sheets into Tableau with the JSON data from Instagram loaded, so exporting JSON data, along with the field calculations into a CSV.



&nbsp; &nbsp; &nbsp; &nbsp;

#### Results notes

&nbsp;
* Non-American spellings and terms (neighbourhood, loch, archaeological, jewellery) mixed in with American spellings (jewelry)

&nbsp;
* Some images returned fewer than 5 results. One image returned no results.



&nbsp; &nbsp; &nbsp; &nbsp;

#### Process notes

&nbsp;
* Created a Google Cloud account and uploaded my image set into a bucket named dhum73000-imageset-180615
&nbsp;
* Google Cloud Vision API setup. Created sample app in tutorial in Google Cloud Shell. Installed Python 2.7.13. Downloaded Brackets and Sublime Text.
&nbsp;
* Downloaded Google Cloud SDK. Now I'm back in terminal. Does this all happen in Terminal? It's 1:00am on technically-Saturday and my life just got complicated. Calling it a night soon.
&nbsp;
* 6/16 at 1pm: [Current questions](https://docs.google.com/presentation/d/1oq3hsq7qOgkFmn7fg6CCQDI_6x2zVZVOMpbbTcDpbSk/edit?usp=sharing)
    * Maybe I don't need to use the SDK. Can I do this all in Google Cloud Shell?
* 1:30pm: setting up a [Python development environment](https://cloud.google.com/python/setup)
* 2:30pm: setting up Python seems complicated and hopefully overkill for what I need. Seeing if I can just make a C# script instead.
* 3:40pm: I kept bashing my head against the Python wall. Trying C# solution in MonoDevelop instead for real now.
* 6:30pm: Giving up on getting batch results through code. Running image links through Interactive API one by one.


  &nbsp; &nbsp; &nbsp; &nbsp;
  

< [There's no place like home](./index.md)
