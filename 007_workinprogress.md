# Learnings, data prep, notes

#### Things I'm learning working on the final project

* How to make a bulleted list in markdown with an asterisk then a space
    * How to make nested lists in markdown
    * That bulleted lists work with either an asterisk or a hyphen

&nbsp;
* That my GitHub directory was already getting messy
    * Renamed all blogposts with ###_ prefix to order and sort to top
    
&nbsp;
* How to custom split columns in the Data Source pane in Tableau
    * Photo taken info came in as a mashed together string field / separated into identifiable date and time
    * Realized late that just changing field format worked fine, but now I know how to split if I ever need to

&nbsp;
* Current challenge: how to split caption string to get hashtags isolated
    * Ok, got all hashtags split off and the hash character readded but it probably took too many CALCs and it's adding hashtag characters to the empty fields as well. Not best use of time to keep going at this. Tabling and moving on.
    
&nbsp;
* I used commands I didn't understand in Terminal to batch rename my images, even though it was scary.
    * [StackExchange source](https://apple.stackexchange.com/questions/236213/renaming-files-names-in-bulk-any-smarter-solution)
    
    
    
&nbsp; &nbsp; &nbsp; &nbsp;


#### Data prep
* Field with date and time came in as string, converted to Date & Time field

&nbsp;
* Image names only provided as part of path, so split path to access name only data

&nbsp;
* Created CALC to create new name field for images with image index # and YYYYMM info at beginning

&nbsp;
* Created CALCs to split out hashtags from captions, which removed hashtag character so I created more CALCs to add hashtag back in. Ended up with way too many CALCs probably.

&nbsp;
* Batch renamed images to match name CALC from Tableau using commands in Terminal



&nbsp; &nbsp; &nbsp; &nbsp;

#### Other notes




  &nbsp; &nbsp; &nbsp; &nbsp;
  

< [There's no place like home](./index.md)
