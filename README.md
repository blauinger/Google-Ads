What this script does: 
For adgroups labeled "Automated negatives" all search terms of the last 7 days will be matched against the keywords in the adgroup.
If the search term is not a exact match in the adgroup, it will be added as a negative. #

Beware: Also very close variants can will be excluded. the script only checks if search_term == any_keyword_in_adgroup

If you do not want to auto exclude: 
Use the script in "preview" mode. the tab "Excluded Search terms" will still be filled and you can choose to add negatives manually and also add more exact matches before automating.

How to use
1. label the adgroups you want to adjust in your account. Add the label "Automate negatives". Beware capitalization!
2. Create a copy of this Gsheet and paste the url in line 6 of the script
3. https://docs.google.com/spreadsheets/d/1HrpFYk7WLV5eWgk0crYkFPgy1oycyuZ-0ZXzkum2gh0/edit#gid=0
4. Click preview and authorize
5. If you manually want to check search terms, go to "excluded search terms" in the gsheet and copy / paste keywords
6. If you want to automatically exclude search terms, run the script. All the keywords shown in the gsheet will be excluded form the adgroup

advanced use: 
- if your adgroups are very big you can also change line 30 to be larger than any other number than 0 (it is the click threshold for filtering)
