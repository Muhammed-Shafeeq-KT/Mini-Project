# Mini-Project
Initial mini project utilizing MS Excel and Power Bi

Filled "N/A" to the missing places in the loan date end column. 
Renamed "Height" and "Weight" to "Height in cm" and "Weight in kg" respectively. Removed cm and kg from their values by extracting values before delimiter and changed their datatypes to number. 
In order to convert value, Wage, and Release Clause columns to number: removed the euro symbol, M, and K by using find and replace, changed the data intially to decimal format, multiplied column that had M with 1000000 and K with 1000 to get whole number format, finally changed the values to whole number, renamed the columns like Value in Euros for clarification. 
In order to convert Hits into number, created a custom column with the following equation //= Table.AddColumn(#"Renamed Columns3", "Custom", each if Text.EndsWith([Hits], "K") then Number.From(Text.Remove([Hits], "K")) * 1000 else Number.From([Hits]))// 
To improve readability, changed value, wage, and release clause columns back to the original format by using custom format like "$" #,##0.0,,"M" and "$" #,##0,"K"
