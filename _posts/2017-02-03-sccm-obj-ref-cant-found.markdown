---
layout: article
title: SCCM Solved -Task Sequence Error - objects referenced in the task sequence
  cannot be found
date: '2017-02-03 13:42:29'
tags:
- sccm
- solved
- task-sequences
- system-center-config-manager
---



## ┬áSystem Center Config Manager CB┬áTask Sequences (SCCM).

##### Version: 1610

Mostly used for deploying Operating Systems through SCCM, these cheeky guys bring some fresh hell to your learning burden.

I had a sequence much like the below (apologies this is not my actual screen shot as I donÔÇÖt get the error anymore,┬á I took this off Microsoft.com somewhere).

ÔÇ£The objects referenced in the task sequence cannot be found. Verify that the objects exists and that the task sequence references the correct object name and location.ÔÇØ

<figure class="wp-caption aligncenter" style="width: 662px">![The objects referenced in the task sequence cannot be found. Verify that the objects exists and that the task sequence references the correct object name and location.](https://social.microsoft.com/Forums/getfile/3306/)<figcaption class="wp-caption-text">What you mean canÔÇÖt be found. I added it from a list you nugget!</figcaption></figure>┬á

So I googled, much as you are doing now o humble seeker of knowledge.  
 I found a lot of smart people with a lot of great solutions that worked for lot of other people but my solution was not there.

It turned out to be surprisingly simple.

You might not know but I learnt from the great [Mick Pletcher ](http://mickitblog.blogspot.co.uk/)that you could create an application that didnÔÇÖt have any content location.

<figure class="wp-caption alignnone" id="attachment_200" style="width: 300px">![SCCM Application Deployment Type](https://cloudconfusionsa.blob.core.windows.net/blogimages/2017/image-7-e1486128868260-300x66.png?resize=300%2C66)<figcaption class="wp-caption-text">This bit. SCCM Application Deployment Type</figcaption></figure>Like so.┬á This means you donÔÇÖt actually pull anything down to the local machine to install. ItÔÇÖs handy for v fat apps.  
 That being said, it causes the above error in task sequences.  
 So all I did was make the content location a folder with a┬á small text file, just so it had something and boom. Task Sequence in SCCM was all fine.

┬á

AWWWWW YISSSSSS!

┬á


