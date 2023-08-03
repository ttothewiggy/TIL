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