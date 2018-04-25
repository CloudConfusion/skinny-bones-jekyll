---
layout: article
title: Stop using Vlookup, It's basically garbage
date: '2017-02-13 14:00:09'
tags:
- excel
- index
- microsoft-excel
- office-2007
- intermediate
- office-2013
- office-2010
- office-2016
- office365
- vlookup
---


### Okay that was click bait. Vlookup is merely bad.

Ohhh the controversy. Intermediate Excel Lesson time.  
 I've tried putting plenty of pictures to explain but tbh it's so much easier just to download the sheet and play along. So click [here](https://cloudconfusionsa.blob.core.windows.net/blogimages/2017/vlookupsucks-1.xlsx) and do that.

> I've used Vlookup for years , in a million spreadsheets.  
>  A million? Literally a million ?  
>  Yes.  
>  You are ridiculous and I refuse to engage with you further.

This has now become a monologue.

If you don't know what Vlookup does and how it works I shall tell you.  
 After which, never use it and use the other thing I‘m going to tell you again. Index Match (Match). If you do know what it does then just read it all anyway. I put secret knowledge in amongst the stuff you already know. Hidden in the white spaces.

Below is our sample piece of data, which is a highly classified piece of documentation from my existing work.  
 It's part of the HR departments appraisal process. Only the top left part is the actual data table. The other sections are things I‘ve put in to explain at you.

![vlookup 1](https://cloudconfusionsa.blob.core.windows.net/blogimages/2017/Vlookupsucks1.jpg?resize=525%2C115)

Value 1 and Value 2 are the things we're interested in finding out. However, for Vlookup, only worry about Value 1 as it can't handle 2 Values. (it's garbage)

What Vlookup does for you is to pull the content out of a cell based on matching a row and an entered column number so if you look at syntax above in the green highlighted cell at bottom right or along the bar at the top of the imagr. The lookup_value is 102, the table_array is the bit in red and the col_index_number (number of columns from left) is 3.

So in the sample above, VLookup returns in the highlighted green square Kitchen. It‘s the line with 102 in it and it‘s 3 along. But what if my data isn't to the right of the Value I‘m using to search on? Well, then you‘re stuffed if you‘re using Vlookupª you know why by now.

Time to bring in the competition. **Index Match Match**

I‘ll break it down into the 3 parts. Index first.

INDEX is kind of like an even more crappy Vlookup on it‘s own. You give it an array. In blue below. You then tell it how many rows to come down and then columns to go along and it returns the value. In this case it‘s 1,1 so would return Priscilla Desert.

![vlookup 2](https://cloudconfusionsa.blob.core.windows.net/blogimages/2017/Vlookupsucks2.jpg?resize=525%2C204)

Let‘s give it a buddy. MATCH. With Match, you select a lookup Value (blue below), point it to an array (in red below) and then tell it how accurate a match you want with ÔÇØ -1ÔÇ│,ÔÇØ0ÔÇ│ or ÔÇ£1ÔÇØ in the last comma space.Always use ÔÇ£0ÔÇØ for exact match. ┬áIt then returns the row or column number that it corresponds to. So in the below Match of Value 1 gives you 3. Third row down. ┬á(can you see what‘s coming?)┬á

Column numbers are relative to the array area you select. So it‘s the third column in the array. Not the third in the sheet

![vlookup 3](https://cloudconfusionsa.blob.core.windows.net/blogimages/2017/Vlookupsucks3.jpg?resize=525%2C179)

What about another MATCH┬ábecause you‘re wanting a value that goes left to right (columns) instead of up and down (rows)┬áWe got you covered buddy ! Exactly the same as before. ┬áIn this below example, you get back ÔÇ£1ÔÇØ as it‘s the first column number that matches the number

![vlookup 5](https://cloudconfusionsa.blob.core.windows.net/blogimages/2017/Vlookupsucks4.jpg?resize=525%2C171)

┬á

So to sum up. INDEX returns the contents┬áof a cell based on a row and column number and MATCH gives you a row or column number based on values you put inÔÇª (see where this going NOW? ÔÇª please?)

So check the picture below. In that case we Have INDEX that has the two MATCH functions nested into it. That means it can bring you back the cell content based on two values.

SO in the below, you get back Stefan Legendary as he has Emp No. ÔÇ£102ÔÇØ and We want the ÔÇ£NameÔÇØ column.

If we change Value 2 to Department it would say Kitchen, and so on.

![vlookup 6](https://cloudconfusionsa.blob.core.windows.net/blogimages/2017/Vlookupsucks5.jpg?resize=525%2C192)

Still not convinced it‘s better? okay so here‘s the data below. The Vlookup and Index Match Match are giving back the same value of ÔÇ£Stefan LegendaryÔÇØ.

![vlookup 6](https://cloudconfusionsa.blob.core.windows.net/blogimages/2017/Vlookupsucks6.jpg?resize=525%2C165)

┬á

What if the columns on the top left get switched about. Your data dump gets moved or you have to add columns ?

Now you see, INDEX MATCH MATCH still shows the correct answer of ÔÇ£Stefan LegendaryÔÇØ  
 What about Vlookup that‘s only using Value 1 and a column number though ?

Ah.

ÔÇ£KitchenÔÇØ.

![vlookup 7](https://cloudconfusionsa.blob.core.windows.net/blogimages/2017/Vlookupsucks7.jpg?resize=525%2C164)

ÔÇª guess you better redo all those formulas then.

Told you !

VLOOKUP is basically Garbage.

┬á

*So what can I use IMM┬áfor?*

Well I use it to put together an MI pack from 12,000 lines of data that fills in about 30 graphs. Also used it for making up ÔÇ£Report cardÔÇØ style things for teams from lines of data into nicely organised stuff. I just change the name. I can even change which pieces of data I want to bring through on the fly!

So handy whenever I needed to add new columns to my data.

Always have your data as unbroken columns with headers and boom, life is good.


