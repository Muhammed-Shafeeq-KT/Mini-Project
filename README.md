# Mini-Project
Initial mini project utilizing MS Excel and Power Bi

1) DATA CLEANING WITH EXCEL
Filled "N/A" to the missing places in the loan date end column. 
Renamed "Height" and "Weight" to "Height in cm" and "Weight in kg" respectively. Removed cm and kg from their values by extracting values before delimiter and changed their datatypes to number. 
In order to convert value, Wage, and Release Clause columns to number: removed the euro symbol, M, and K by using find and replace, changed the data intially to decimal format, multiplied column that had M with 1000000 and K with 1000 to get whole number format, finally changed the values to whole number, renamed the columns like Value in Euros for clarification. 
In order to convert Hits into number, created a custom column with the following equation //= Table.AddColumn(#"Renamed Columns3", "Custom", each if Text.EndsWith([Hits], "K") then Number.From(Text.Remove([Hits], "K")) * 1000 else Number.From([Hits]))// 
To improve readability, changed value, wage, and release clause columns back to the original format by using custom format like "$" #,##0.0,,"M" and "$" #,##0,"K"

2) DATA VISUALIZATION USING PowerBi
Created a column named "Growth Gap" by subtracting POT from OVA.
Added buttons on each page for navigation.
Created Bookmarks for each page.
Added background image for home page and changed colours appropriately. 
Utilized diverse visuals on each page.
Used conditional formatting to visualize contrast when applicable.
Icons were used to enhance readability. 
Created the following measures for efficient visualization.
•	Average Rating 
•	Most Valuable Player
•	Oldest Player 
•	Top Player OVA
•	Top Player POT
•	Total Market Value.
•	Total Players
•	Youngest Player
•	Fastest Player
•	Strongest Player
•	Most Durable Player
•	Best Aerial Player
