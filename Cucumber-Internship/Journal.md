# Journal

## 31/07/23

I'll write a little bit here about what I've been learning at Cucumber. It'll serve as a reference guide for myself to keep track of the path I've taken incase I take a wrong turn. 

Today is my first day, I've dived into the analysis tools used here to try and get more familiar with what they can do. The more I can understand the scope of the software, the more I can figure how to utilise it. 

I've started on: 
- Raven SEO Tools
- Raven site auditor studio (branch of Raven tools)
- Google Analytics 4
- TAG Manager
- Looker Studio
- Search Console

And things I need to familiarise myself with are:
- SquareSpace
- HubSpot


## 01/08/23

Day 2 has been spent using Raven Tools to identify which pages on the cucumber website had links with redirects attached to them. I then went on squarespace and edited the links to use the new new link instead of the old redirect one. 
The I did the Looker Studio for beginners course on LinkdIn, followed by half of the Advanced GA4 course. 
Today was spent combing through the cucumber website fixing redirects and wrong links. 
I used Raven software to crawl a website that had fairly recently migrated to a new management software. The crawl flagged a number of errors, including redirects. This was because the old addresses of the links on the website were still being used, even though they had been redirected to the new addresses.

I combed through the website and found all of the links that were using the old addresses. I then changed these links to the new addresses. This will make the website slightly more efficient, as it will no longer need to redirect users from the old addresses to the new ones.

This was a relatively straightforward task, but it was important to ensure that all of the links were changed correctly. I also took the opportunity to review the website's overall structure and make sure that it was still easy to navigate.

I then spent the afternoon doing a variety of linkedIn Leanring courses on the various software I'm trying to master. 
We have:

- **Google Analytics:** Helps track and measure website traffic. It collects data such as visits, views, location, device, browser and behaviour such as clicks, scrolls and loads of other actions. This data can be used to improves website performance, increase conversions (importrant activity such as purchases, game level completion or scroll activity as well as the user doing the thing you made the website for e.g. newsletter download, email signup, free trial sign up, completing survey) and track marketing campaigns. 
- **Google TAG Manager:** tag management system that allows you to add and mange trackig codes on your website. Useful for tracking things like conversions, social media engagement ,email marketing campaigns. 
- **Google Search Console:** is a free service that helps you monitor and maintain your site's presence in Google Search results. It provides data on how your site is performing in search, such as the number of impressions and clicks your site receives, as well as the keywords that people are using to find your site. You can also use Google Search Console to troubleshoot problems with your site's indexing and crawling.
- **Google Looker Studio:** a data visualisation and analysis tool (like Power BI). Can create interactive dashboards and report from data collected from the above sources. Makes it easier to analyse the data and share insights. 

You can use Google Analytics to track the overall traffic to your website, Google Search Console to track the traffic from Google Search, and Google Tag Manager to track the traffic from other sources, such as social media and email marketing campaigns.
Then Google Looker Studio can be used to visualize and analyze the data. 

**How they differ:**

Google Analytics and Google Search Console are both used to track website traffic, but they track different things. Google Analytics tracks all traffic to your website, while Google Search Console only tracks traffic that comes from Google Search.

I've been given a list of various tasks on Google Keep to crack o with. 

## 02/08/23

Rainy day this morning, traffic was terrible. The office is really quiet as a side effect, lots of people WFH. 
But I have my tasks today, which is to continue the list assigned to me. 
I started on Raven crawling both the Cucumebr site and the Bayer site. 
The Cucumber site was done first as it's so much smaller and I finished fixing the link redirects I missed from yesterday, which was a time consuming process. 

The Bayer crawl was done by the time I was finished so I opened that up in the Raven Tools auditor. It has no critical issues, and a higher score than the Cucumber site, but by no means perfect. I've explored all the issues and I'll narrow it down to attempt to fix some of them. I'll check with Nick before I change anything though as I don't want to break the website. 
Nick advised to leave it for now as it was trickier than the cucumber stuff I've been doing for now. 

Instead I compressed a bunch of  large images on the cucumber website and reuplaoded them. Waiting to hear if there's a more efficient way to do it, as there's 1600 over 100kb.

I've begun to use google Bard today, which has been fun. It's got live data pretty much so it's much better to ask current questions. As an AI assistant it's been great. 


## 03/08/23

Today was a late start as I was making my contribution to the christmas dinner, cauliflower cheese and maple glazed carrots and parsnips. 

Once at work I continued on from yesterady, checking over the SEO tools and trying to figure out why squarespace tends to incrase images sizes to up to 4mb. 

Next challenge was to great my own trigger in Tag manager that will fire when a particular button was clicked. The button clicked to a page with a lot of paths to it so I needed to make the trigger only fire when i was leaving one particular page, going to the one particular page. This way you can measure specific traffic that has been guided to that button and the content has proven effective as they have clocked the button navigating to the contact page. 
It was a little tricky but got there in the end. 
First I created a trigger that when a link is clicked it checks agains a few parameter/filters. These were:
Click ID contains yui - This was the first few characters of the css id for the button. 
Page Path contains /news/the-importance-of-ga4-in-todays-data-driven-business-landscape - this is the path of the origin URL
Click URL contains /contact - this is the path of the destination/click URL. 

Next creating a tag for the information from this trigger to go to. 
The trigger and tag work hand-in-hand to track and collect data. Without a specific tag, the trigger would not have any instructions on what to do when the conditions are met. The trigger would activate, but it wouldn't have anywhere to send the information it gathered.
In other words, the tag is the destination for the trigger's data. When the trigger says, "Hey, I found a user clicking the specific button and going to the 'Contact Us' page from that particular blog post," the tag takes that information and delivers it to Google Analytics.

Tomorrow I'm going to be analyzing the Cucumber website analytics, the tags being sent to GA4 and what they tell me about how the site is being used.
I need to think up some more ways we could be tracking the company website. 

## 04/08/23

Started the day trying to get a GA4 report made but I don't have permissions for that so I'm going to crack on with some advanced GA4 course material and possibly some JavaScript. 
Did a couple Java30 challenges to get the blood flowing and now I'm doing the google analytics skillshop course made by google themselves.
Questions: What's the purpose of cucumbers website? - sales, information, what are the conversions?


## 07/08/23 

Today I've been tasked with beggining to understand Bayers SEO. 
Combing through the data to find the top pests and evaluate SEO against competitors popular keywords. 
It's been tricky as there's a few red herrings where there's lots of impressions on really broad queries which when I try to recreate them, it's not behaving the same way. 
For example, on the webpage for cabbage cluster catapillar, it got tens of thousands of impressions and 40 clicks, most of those impressions were on the query keyword catapillar, which when I searched for that it brings up dozens of other webpages before Bayers, which the search console seems to think is coming up second from the top. 

Spent some time looking at careers paths for data analysts and python comes up a lot. So I've got it runing on the work computer and I'll do a few little side projects to explore python a bit. 

## 08/08/23

Continuing to analyse the Bayer data to evaluate low/high performing web pages and identify popular keywords. 
Currently I've been ordering the data by lowest CTR and identifying pages with high impressions but no clicks then analysing why. Mainly getting meta descriptions lacking decent descriptions and keywords. 
But also quite a few anomolies where a lot of impressions are from the Bayer result appearing high up on a generic term assosiated with the pest in question. 
eg "cabbage cluster caterpillar" got almost 10000 impressions from a google search for "caterpillar". When I made the search with my location set to rural australia, I got the result sub 20th position, with the brand caterpillar and actual caterpillars filling the spaces up high. As expected. So how did this page get 10000 impressions off that keyword search? 

Today I'll comb through yesteradys work and list pages that need to improve their meta description and then move onto high performing pages and analyse why they're performing so well and see if I can use that information to improve the lowest ones. 

Highest performing pages seems to be ones with "control" in their name. People who searched "Fleabane" for example had a CTR of less that 2% whereas "fleabane control" (although had way fewer impressions) had a CTR of 16%. Bayers pages had more success when the users intent was clear which indicates they're targeted well. 

I've moved on to Looker Studio now, I want to make a chart to view the Tag and trigger I made last week on the blog posts contact button. It seems I have to create a custom dimension and I don't have permissions for that. I've tried to find a work around with the help of some AI but no luck, all attempts have hit a wall blocked by lack of permissions. 

Also, I've been using the Pomodoro technique to try and help with focus. It's been working great, I've done 3 sets of 25 mins where I worked non stop and took my 5 mins rest between. 


## 09/08/23

Continuing to analyse the Bayer SEO data. I'm going to review my current notes and check they're all relevant. 
I'm going to do some more research into SEO keywords and see if I can expand and elaborate on the data even more. 

Short tail - more general words getting lots of impressions but less clicks. 
Longtail words - more specific, often stating towards what the user wants. eg: shorttail = vollyball longtail = vollyball nets for backyard. 

Wireweed = ST
wireweed control = LT
Think of more longtail keywords. These people know what they want so get bayer there to give them that. 

Gave the google analytics 4 certification a go today and just passed it with 82% (80% being a pass). It was fairly strightforward, though for the sake of honestly, I did google some answers. 
Now just to keep on it so it all sinks in. 

Continued to analyse the Bayer data, got some good stuff I rekcon, so I was just thinking of condensing it into an easier to digest format incase it actually gets sent to whoever can make these changes at Bayer. 
I was just having a break from it before doing that so it may be a job for tomorrow. 


## 10/08/23

Today has been spent combing through the presvious analysis of the Bayer pests I've done and creating a table stating what changes need to be done. It's a fairly slow process of going through each individual page, bringing up the search console for that page and checking over the popular queries/keywords and seeing if any improvement to the age is needed. 
Analysing the meta descriptions, page titles, competitors ranking and any other factors I can think of that might assit in the page getting more clicks and rising through the ranks. 

Got started on the tui website, creating redirects for 404 pages. Did 54 out of 110. Quite simple work. 

## 11/08/23

Started the day off with some redirects. Now going to move onto the Bayer stuff one more time to try and figure out a way to get new people clicking on the links. As Nick pointed out, people that are looking for the site will find it. We want to get people who weren't looking for it clicking those links. We want to increase traffic from less likely people. 

Finished the day with some redirects after spending a while watching SEO videos trying to figure out the problem above. 
Happy Friday!

## 14/08/23

Started a Monday morning with some redirects while a lot of meetings and morning tea's were going on as it's easier to make the most of the time. 
Followed ths up with some google analytics, trying to figure out why there was a huge bump in traffic on the cucumber website on Sunday, where it came from and why there was a large increace in referrals. Made some reports that measured the clcik events and outlined their origins. 

I have some web design tasks to complete next along with some updating of content for the website. Quite excited to be collaborating with some other staff members now. 

I also started analysing the BayerNZ data, to begin trying to improve the SEO for that, though I've been assured it should be pretty tight. It'll be a challenge to find something to improve in amongst it so I'm interested to try! 

## 15/08/23

Started the day with some organizing of my notes from yesterday and creating a plan of action. Made a Kanban board and populated it with a few tasks for the website update.
Had a meeting with Tom at 10 to discuss the plan of action.

Taking the info from the meeting, I then spent the day making changes to the website.
I signed up for a free trial of Jasper AI, a content creation tool, which I hoped to use for creating custom images for the site.
Maybe it was my prompting skills, but I was underwhelmed with the tool, and soon moved on to a more old-fashioned way of obtaining images from stock websites, etc. Just a few to test some ideas.
Made some changes to the copied website page, as well as some accidental edits to the actual live home page (which were swiftly corrected), and I've got a bit of a fresh look for the home page. Or at least an idea that we can assess the direction from.