# Learnings, data prep, notes

#### Things I'm learning working on the final project

* How to make a bulleted list in markdown with an asterisk then a space
    * How to make nested lists in markdown

&nbsp;
* That my GitHub directory was already getting messy
    * Renamed all blogposts with ###_ prefix to order and sort to top
    
&nbsp;
* How to custom split columns in the Data Source pane in Tableau

&nbsp;
* Current challenge: how to split caption string to get hashtags isolated
    * Ok, got all hashtags split off and the hash character readded but it probably took too many CALCs and it's adding hashtag characters to the empty fields as well. Not best use of time to keep going at this. Tabling (haha is that a pun?) and moving on.
    
&nbsp;
* **I used commands I didn't understand in Terminal to batch rename my images, even though it was scary.**
    * [StackExchange source](https://apple.stackexchange.com/questions/236213/renaming-files-names-in-bulk-any-smarter-solution)
    
&nbsp;
* In Google Cloud Vision API setup. Created sample app in tutorial. Downloading Google Cloud SDK. Need Python 2.7.0 first. Downloading that. Oh ok, should be 2.7.13. 

&nbsp;
* Downloaded Google Cloud SDK. Now I'm back in terminal. Does this all happen in Terminal? It's 1:00am on technically-Saturday and my life just got complicated. Calling it a night soon.
    
    
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





&nbsp; &nbsp; &nbsp; &nbsp;

#### Other notes

&nbsp;
* Created a Google Cloud account and uploaded my image set into a bucket named dhum73000-imageset-180615


  &nbsp; &nbsp; &nbsp; &nbsp;
  

< [There's no place like home](./index.md)
