# MongoDB Licensing Dramas - Case Study
ACIT3890 - BCIT - Fall 2019

This case study was prepared by the ACIT3890 students as part of a lab.
Some of the grammar has been edited for readability.

## The Story

Every modern developer has come across or heard of MongoDB, in fact the companies 
that we hear on a day-to-day basis, such as Google, Facebook & Adobe, utilize 
MongoDB in their applications. So, what is MongoDB? It’s a an open-source/commercial 
software-as-a-service which provides a NoSQL document-based database built for app 
developers and for the cloud computing era. 

In late October 2018, MongoDB switched their open-source license from GNU’s Affero 
General Public License (GNU AGPLv3) to a MongoDB conceived Server-Side Public License (SSPL) 
to apply to future releases of MongoDB’s Community Server.

The reason for this change was to retaliate from cloud providers across the globe 
that were taking advantage of MongoDB’s open-source code and hosted commercial 
versions of the database to their users without following its open source guidelines.

Similarly, companies like Redis Labs initially implemented changes in the clause 
of licenses to combat the same issue, but Redis Labs created their own license 
Redis Source Available License (RSAL) once MongoDB created SSPL.

The change in license does not affect regular end-users of MongoDB’s Community 
Server, but this change applies to companies who want to run cloud database as a 
publicly available service because the new license states that the companies must 
open-source their software or obtain a commercial license from MongoDB as a way 
of giving back to the open-source community. 

Eliot Horowitz, the Co-Founder of MongoDB spoke on this issue explaining: 

“The market is increasingly consuming software as a service, creating an incredible 
opportunity to foster a new wave of great open source server-side software. 
Unfortunately, once an open source project becomes interesting, it is too easy 
for cloud vendors who have not developed the software to capture all of the 
value but contribute nothing back to the community.” 

This licensing drama caused a debate in the open-source community to reconsider 
the meaning of what open-source really means to the participants of this ever-growing community.

## Server Side Public License (SSPL)

SSPL abbreviated for Server-Side Public License, is an open-source license type 
created by MongoDB that builds on the AGP license. The licenses are generally the same 
except for the last section(13), which MongoDB changed to “terms for offering the 
software as a service”. It added, “If you make the functionality of the Program 
or a modified version available to third parties as a service, you must make the 
Service Source Code available via network download to everyone at no charge.”

This allows for the same permissions as using, modifying, and redistributing code; 
but with the new condition that organizations using the software as a service must 
also release all related software as open source. This came about because MongoDB 
felt that enterprises were using their software, profiting unjustly without giving 
back to the community. 

This new addition would deter large companies from using them for gain, but this 
created a large grey area of what would be considered derived work from the software, 
and what was considered fair use. This issue made OSI reluctant to recognize this 
license and ultimately lead to the withdrawal of its license application.


## How Are They Right?

MongoDB was right in the sense that they wanted to protect their Intellectual Property 
from being abused by cloud vendors like Amazon who sold the
software as a service and were able to monetize on the rapidly gaining popularity of 
MongoDB. Other large cloud vendors were also taking advantage
of the AGPL to profit from open-source creators.

This allowed MongoDB to have an edge over companies that took advantage of the 
Open-Source Software with little to no contributions to the original code.
The intent was to stop companies from testing the boundaries of the AGPL by 
benefiting from the work of others. 

The new license was designed so that companies that wanted to use the software for 
commercial use would have to pay to use it or would have to make their 
software open source. Doing so would allow the creator of the IP to be able to 
make some profit off their product and would encourage other creators to utilize
open-source concepts therefore contributing back to the community.


## How Are They Wrong?

MongoDB are trying to overstep their bounds by changing their 
licensing from AGPL to SSPL. Comparatively, SSPL does not have as  
clear-cut boundaries for anyone using MongoDB to follow, thus giving 
them more control and making it harder for anyone using the service to 
utilize MongoDB as an open source software. By doing this, MongoDB are 
defying the open source practices that they have profited from 
themselves. This creates an ultimatum for anyone looking to use MongoDB 
as they can control whether or not it is compliant with their license, so they 
could potentially force companies to pay for their commercial license or 
open source their entire project. 
 
They’re making China pay money + making mandatory code contributions 
if they want to utilize the MongoDB software. But MongoDB is supposed to 
be free and open source so is this not going against the morals of OPEN 
SOURCE SOFTWARE? They shouldn’t have made it open source if they were 
going to monetize it later, defeats the purpose of open source. 
 
Mongodb wants all of the benefits of being an open source project, such 
as having community developers adding driver support, while wanting to 
retain full control how the product can be and who can use it.   

## Lessons to Learn

*Contribute back to OSS projects you use*  
If you are using an open source project source code, contribute back meaningful 
information to the project or get a commercial license if you are offering a 
hosted commercial version. Comply with current license rules and don’t try to 
cheat the system or else they could make the project closed source or change their license. 
In this case, 

*Choose OSS license carefully*  
From the start, if there is a strong intention to disallow others to profit from the OSS, 
the appropriate license should be applied. If a license change is required, 
there are various licenses that cover the new needs. Moreover, there are precedent 
cases to follow. For example, Redis added a commons clause to prevent the sale of their OSS. 

*Ensure custom licenses are clear*  
If that is not enough and a new license is desired, then it should be written clearly and thoughtfully. 
The SSPL protects the OSS from misuse as intended, but the conditions are overdone; 
if a company were to comply with the conditions, SSPL will maliciously cause 
all of the company's software to become public.
