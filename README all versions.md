What this script does: 

If auto exclude in "Script Settings" is set to true: 
For adgroups labeled "Automated negatives" all search terms of the last 7 days will be matched against the keywords in the adgroup, If the search term is not a exact match in the adgroup, it will be added as a negative, Only search terms with clicks > 0 in past 7 days are considered.
The script will only exclude close variants of exact matches (so you are safe to use phrase and broad matches in the same adgroup)

if auto exclude is set to false: The script will not make changes in the account, just report what "would have been done".


How to use

1. label the adgroups you want to adjust in your account, Add the label "Automate negatives", Beware capitalization!
2. Create a copy of this Gsheet and paste the url in line 3 of the script
3. Ghseet: https://docs.google.com/spreadsheets/d/1jz8t4fbX_R6N3oZDjJkvI-RmmN3U5J4kE9-uiDWwI1U/edit#gid=6886337
4. Click "run" and authorize
5. In the first two graphs in "Overview graphs" you can see cost and conversions triggered by match type. 
In the two thereafter you can see which search terms are excluded and which ones are not (all non exact matches get excluded)
6. In "Performance deepdive you can also check performance of adgroups on CPL and ROAS Level
7. If the data and exclusion make sense to you, you can change the setting in "script setting" to automatically exclude the queries


Data Analysis info

It can be the case that %exact match (close variant) is higher than the actually excluded cost when the script runs. This happens when a exact match was recently added. In the query report it still appears as close variant match type for past data. But actually it is already a exact match. 

Changes v2:

- search terms are only excluded if the setting is set
- no phrase match search terms are excluded
- a paid MCC version is available


_________________________


README of v1:
What this script does: 
For adgroups labeled "Automated negatives" all search terms of the last 7 days will be matched against the keywords in the adgroup.
If the search term is not a exact match in the adgroup, it will be added as a negative. 

Beware: Also very close variants will be excluded. the script only checks if search_term == any_keyword_in_adgroup

If you do not want to auto exclude: 
Use the script in "preview" mode. the tab "Excluded Search terms" will still be filled and you can choose to add negatives manually and also add more exact matches before automating.

How to use
1. label the adgroups you want to adjust in your account. Add the label "Automate negatives". Beware capitalization!
2. Create a new Script in Google Ads and name it: "Automate Negatives". Use the code from "Automated negatives - Script" here in github.
3. Create a copy of this Gsheet and paste the url in line 3 of the script: https://docs.google.com/spreadsheets/d/1HrpFYk7WLV5eWgk0crYkFPgy1oycyuZ-0ZXzkum2gh0/edit#gid=0
4. Click preview and authorize
5. If you manually want to check search terms, go to "excluded search terms" in the gsheet and copy / paste keywords. They will be filled with preview mode too (but not excluded)!
6. If you want to automatically exclude search terms, run the script. All the keywords shown in the gsheet will be excluded form the adgroup. 

advanced use: 
- if your adgroups are very big you can also change line 30 to be larger than any other number than 0 (it is the click threshold for filtering)
