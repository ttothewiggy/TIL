## Notes on LinkdIn Learning Google Analytics 4 Course

 ## Intro & Chapter 1

Google Analytics is a free tool from Google that's going to let you install a little bit of JavaScript on your site and it's going to unearth a treasure trove of information about your visitors. 
Its all about continued performance through detailed analysis and optimisation. 
It's a process. Perform the measurement, for we can't manage what we can't measure. And apply the analysis, learn from what we see, and then take action. 
Metrics = Quantitative numbers that are measuring data in counts, ratios, percentages.
Dimensions =  Qualitative categories that describe the data in segments or breakouts.
Event = Any interaction with the page. clicks, scrolls, views etc. 

Event > Parameter > Value model. 

Conversion = Measures if your business objective has been met. 

Source = Where user traffic originated from. 
Medium = The avenue they took took to get from the source to your site. 

GA4 is the new, complete rewrite of google analystics. 

1. Urchin
2. GA.JS
3. Universal Analystics
4. GA4

Changes: Comlpetely event driven, automatic tracking + enchnaced measurements, cross-device tracking, sessions mroe robust, improved funnels and pathing, time based analysis, flexible conversion goals, export all data to cloud via Big Query. 

What's missing: Attribution, Multichannel funnels, stream-level user permissions and filters (views), page and site load times, intergration with full GMP tool suit, ecommerce features. 


## Chapter 2 - Installation

- The instructor recommends using Google Tag Manager (GTM) for installing Google Analytics 4 (GA4) code.
- They assume that viewers already have a GTM account and have installed the Tag Manager code snippet.
- The process involves copying the Measurement ID from the GA4 property.
- In GTM, a new GA4 Configuration tag is created with the copied Measurement ID and set to trigger on all pages.
- The tag is saved and published, sending data back to Google for processing.
- The instructor demonstrates how to verify that the data is being sent correctly using the developer console and Realtime reports in Google Analytics.


## Chapter 3 - Fundamentals

- Demo data from Google Analytics 4 is used for the purpose of the course, allowing analysis without waiting for new data to populate.
- The demo data is from Google's own merchandise store and a mobile app game called Flooded, providing real-time, real-life data.
- Accessing the demo account can be done by searching "Google analytics demo account" on Google and following the link to the article explaining how to gain access.
- The demo account contains two GA4 accounts: Flooded and the merchandise store.
- Users have read access to the demo account, allowing them to analyze data but not make configuration changes or add users.

### Structure


- Google Analytics structure starts with the overall Google account, which is separate from the Google Analytics account used for login.
- Multiple Google Analytics accounts can be created under one Google account, depending on business needs.
- Each account contains at least one property, recommended to have a property for each site or platform.
- Properties are tied to streams, representing data sources such as web, iOS apps, and Android apps.
- An example of Google's structure includes one GA4 account (Google Demos) with two properties: the merchandise store (web stream) and Flood It (web, Android, and iOS streams).


- Campaign tracking in Google Analytics helps measure traffic sources and mediums.
- Google Analytics automatically captures some info, like referrals, organic search, and direct visits.
- Manual tagging (using UTM parameters) allows adding extra info about clicks, like for marketing campaigns.
- Campaign tracking uses source, medium, and campaign name to differentiate different initiatives.
- UTM parameters are added to the URL using Google's URL builder tool, providing specific tracking details.
- Consistent campaign tagging allows for better analysis of click performance and conversions.

## Chapter 4 - UI and Reports


- The left navigation in Google Analytics 4 is streamlined, containing four main areas (Acquisition, Engagement, Monetization, Retention) and admin settings.
- Pre-built template reports are available in the Reports section, organized under life cycle reports for customer acquisition, engagement, monetization, and retention.
- The User section provides information about users, including demographics and technology used to access content, with improved cross-device tracking.
- The Explore reports allow for advanced analysis, especially for digital advertising optimization.
- The home screen includes a dashboard with card-based data and real-time reports, and an Insights section that uses machine learning and AI to highlight spikes and unusual behavior in data.
- The home screen gives a quick overview of site or app performance, serving as a jumping-off point for deeper analysis.

- Realtime reports in Google Analytics 4 provide a snapshot of what's happening on the site or app at any given minute, similar to walking into a brick and mortar store for observation.
- Realtime reports show active users' locations, devices used, and various configuration options and dimensions.
- The "View User Snapshot" feature allows observing a random user's browsing session in detail, including events, screens, properties, and parameters.
- Realtime reports are useful during significant events like app launches or advertising campaigns for immediate monitoring, although heavy analysis is usually not done here.
- Realtime reports offer a unique view of customer behavior that cannot be replicated by other reports.

## Chapter 5 - Filtering and Segmenting Data

### Segmentation

- Segmentation is crucial for true analysis in Google Analytics, allowing users to group and cluster visitors based on similar characteristics.
- The "comparisons" tool helps create segments to compare different groups, enabling better understanding and optimization of the site/business.
- Users can add comparisons from the home screen by including or excluding dimensions, such as country, gender, etc.
- The tool sometimes requires refreshing the page to work properly due to potential beta issues.
- Users can compare different segments side by side, analyzing metrics like total users, new users, average engagement time, and total revenue for each segment.
- Tables and charts in various reports reflect the selected comparisons, making it easier to analyze specific audience groups' behaviors and characteristics.

### Filter and Secondary Dimensions 

- Google Analytics uses secondary dimensions to customize tables and provide more detailed insights.
- Users can add secondary dimensions to any table to compare data based on different criteria.
- For example, in a session medium report, users can add a secondary dimension for session acquisition, such as campaigns.
- For app-related data, users can use app version as the primary dimension and further add secondary dimensions like OS versions or platforms (iOS, Android, Web) to analyze user behavior across different app versions and operating systems.
- Filters can be applied to limit the data displayed in the table, making it easier to focus on specific subsets of data, such as iOS users in a platform comparison.
-  By using comparisons, secondary dimensions, and filters, users can efficiently analyze data and gain deeper insights into user behavior and interactions with the site or app.

### Audiences

- Audiences in Google Analytics are similar to the old "advanced segments" in the previous version.
- Audiences help create custom groups based on specific criteria for targeted analysis or remarketing purposes.
- To create an audience, head to "Configure" and select "Audiences," then choose from suggested options or create a custom audience.
- Custom audiences can be based on specific conditions, such as engagement level, conversions, location, events, and more.
- You can use dimensions, metrics, and events to define the audience criteria, and set the scope for the conditions to apply.
- Audiences can include or exclude users based on various conditions.
- It's possible to set a membership duration for the audience to automatically add or remove users over time.
- Audiences are constantly updated based on the defined conditions, and they can be applied to the dashboard to see specific data for that audience.
- Audiences are useful for targeted analysis, better understanding user behavior, and for remarketing campaigns in the Google Ads ecosystem, which can lead to higher ROI.

## Chapter 6 - Lifecycle Reports

### Analysing how to get customers

- Understand how users are acquired and their behavior on the website or app is crucial for effective analysis.
- Start by exploring the Acquisition reports to answer fundamental questions about user acquisition.
- Analyze high-level metrics such as overall users, new users, and recent sessions.
- Drill down into specific dimensions like medium, channels, and campaigns to understand how users arrived.
- Utilize customizations like secondary dimensions to gain deeper insights, such as finding out which sites are referring traffic to your site.
- Sort the data by conversions or revenue to identify the most valuable sources of traffic.
- Spend time analyzing these reports as they provide valuable data for optimizing marketing efforts and building affiliate relationships.

### Engagement Reports: Overview, Pages, Screens, Events

- Engagement reports help answer the question of how users engaged with the content on the website or app.
- Access the Engagement section under Reports to find an overview dashboard with metrics like average engagement time and event count.
- Dive into specific sections like pages and screens to analyze user interactions with individual pages or screens.
- Pages and screens are events and can be sorted and grouped by title and page location for more specific analysis.
- The chart at the top can display both quantity and quality metrics to understand how users engage with specific pages or screens.
- These reports are particularly valuable for sites with heavy content investment, providing insights into user engagement and behavior.

Events:
- Google Analytics 4 uses an event-driven model where everything is part of an event.
- Page views, session starts, and custom events are all examples of events in Google Analytics 4.
- Events contain parameters with values, such as page title, location, resolution, etc.
- Custom events can be coded to track specific actions or interactions on the website or app.
- In the Flood-It app example, events like "level fail" are recorded, providing insights into user behavior and potential issues with specific levels in the game.
- Events in Google Analytics 4 are powerful and versatile tools for understanding user interactions and behavior.

### Analysing how to convert customers

- Analyzing how to convert customers focuses on ecommerce and conversion strategies.
- To track ecommerce data, developers need to integrate ecommerce hits via the shopping cart on the website or app.
- The chart for the Google merch store reveals that there are very few repeat buyers, with the majority being first-time purchasers.
- Understanding the average purchase revenue per user is crucial for paid traffic campaigns to determine affordability per person.
- To dive deeper into the journey and steps leading to conversions, one can explore the comparisons section to view metrics for purchasers only.
- The engagement and item views vs. item revenue chart can help identify which products drive the most traffic and revenue.
- Sorting by purchase to view rate can highlight products that have a high conversion rate despite lower visitor numbers.
- The ecommerce data enhances other reports and metrics, providing valuable insights into the effectiveness of marketing campaigns and overall website performance.

### Analysing how to keep customers

- User retention is crucial for some businesses, where the goal is to make up the initial acquisition costs over time through repeat purchases or usage.
- Cohort analysis is a valuable method to understand user behavior in batches or groups, such as different generations or seasonal segments.
- The Flood-It! game shows more returning users than new users, indicating strong user retention.
- The user retention and lifetime value chart indicates a long tail of users who don't return for a second visit, but those who do tend to keep coming back.
- Cohort reporting allows for detailed analysis of user behavior over time, and the template gallery in the analysis hub offers pre-built reports for cohort analysis.
- In cohort analysis, various configurations can be adjusted, such as segments, return criteria, granularity (weekly, daily, monthly), and the metrics to measure (e.g., active users, user engagement, ad revenue, or in-app purchases).
- Cohort analysis provides valuable insights into how user engagement and behavior change over time, allowing businesses to optimize campaigns, promotions, and content accordingly.

## Chapter 7 - User Reports and Events

### Demographics and Interest Reports

- Demographics and interests reports in Google Analytics provide valuable information about users' characteristics and preferences.
- Google Analytics uses anonymized and aggregated data from its own internal analytics to supplement the reports, offering insights into user demographics and interests.
- The demographics overview includes information about users' geographic location (by country and city), gender, age cohorts, language preference, and real-time user data.
- The demographic details report allows for a deeper examination of user demographics, such as gender, language, and age breakdowns for different countries.
- By using secondary dimensions and sorting by different metrics, one can gain insights into user engagement and behavior based on demographics. For example, the average engagement time can reveal which age groups or interest categories are most engaged with the site or app.
- The interests report shows user segments based on their browsing and content interaction behavior. Marketers can use this data to identify profitable user segments and target their marketing efforts accordingly.
- Lookalike modeling can be employed to find subsets of users who share common interests and traits with the best users, which can inform marketing strategies to reach high-potential users.
- By leveraging Google's user graph and combining it with account data, businesses can gain a deeper understanding of their visitors and make informed decisions to better serve their customers and prospects.

### Tech, Devices and Platforms

- The tech reports offer information about the type of devices, operating systems, and platforms that users are using to access the website or app.
- The users by platform report shows the volume of users on different platforms and also reveals the overlap of users who access the content through multiple devices (cross-device tracking).
- Cross-device tracking is possible when a user ID is supplied to Google Analytics, enabling tracking of the same user across different devices.
- The demographics of users accessing the website or app can be analyzed based on operating systems, browsers, and screen resolutions.
- Cross-device usage may vary based on the nature of the website or app. For example, a mobile app-based game might see little to no overlap between Android and iOS users.
- Screen resolution data is crucial for understanding how users consume content, and it can be helpful in designing the site or app to cater to different devices.
- The technology and device data can be used to gain insights into user behavior and preferences and can inform decisions related to website or app design and optimization.


## Chapter 8 - Analysis Hub

The Analysis Hub, now known as the Explore tool, is a powerful feature in Google Analytics that allows users to create custom reports and analyze data in a flexible and versatile manner. Here are the key points from this section:

- The Explore tool is highly customizable and allows users to build reports tailored to their specific analysis needs.
- Users can start with a blank canvas or use pre-built templates to create reports.
- The tool provides access to a wide range of segments, dimensions, and metrics that can be used to filter and analyze data.
- Users can add metrics and dimensions to the report canvas and apply filters to focus on specific data subsets.
- The power of the Explore tool lies in its ability to create custom segments and apply complex filters to extract meaningful insights.
- The tool allows users to compare different segments, conduct cohort analysis, and visualize data in various formats.
- By utilizing the Explore tool, users can gain deeper insights into their website or app's performance and make data-driven decisions to optimize their digital strategies.

Overall, the Explore tool is an essential resource for analysts and marketers who want to harness the full potential of Google Analytics and extract valuable insights from their data.

### Pathing Analysis

Pathing analysis in Google Analytics 4 (GA4) allows users to analyze the sequential flow of events or pages that users take on a website or app. Here are the key points from this section:

- Pathing analysis in GA4 is similar to the behavior flow reports in the previous version of Google Analytics, but with improved functionality and performance.
- The previous version of pathing reports often suffered from slow loading times and data sampling, leading to inaccuracies in the displayed data. GA4's pathing reports address these issues and provide more accurate insights.
- The pathing reports in GA4 can be segmented, allowing users to analyze the flow of specific user groups, which is essential for more detailed analysis.
- To access the pathing analysis, users can start with a blank canvas in the Explore tool and select the "Path Exploration" technique.
- The pathing diagram displays the sequential progression of events or pages, allowing users to understand how users navigate through the website or app.
- Users can choose to display page titles or screen names instead of event names to better understand the flow of users through specific screens or pages.
- Additionally, users can break down the pathing analysis by dimensions such as device category to understand how different user segments progress through the path.
- Users can apply filters to focus on specific device categories or other criteria to refine the pathing analysis further.
- The pathing analysis also allows for reverse pathing, starting from an ending point and analyzing the paths users took to reach that endpoint.
- Users can choose to display the number of events or the number of active users moving through the pathing analysis, providing a more meaningful understanding of user behavior.

Overall, pathing analysis in GA4 is a powerful tool for understanding user behavior and identifying opportunities for improving website or app navigation and user experience.

### Funnel Visualisation Analysis

Funnel visualization analysis in Google Analytics 4 (GA4) allows users to track and analyze the sequential steps that users take towards completing a specific goal or conversion on a website or app. 

- Traditional funnel analysis in GA4 has been drastically improved compared to previous versions of Google Analytics. It is now more flexible and allows users to build custom funnels from page views, events, or conversions.
- The new funnel analysis in GA4 is retroactive, meaning it collects data for the funnel steps even after you create it, so you don't have to guess the path in advance.
- Funnel analysis can be done in standard or trended format. Standard funnel analysis shows the flow of users through the steps, while trended funnel analysis shows how each step is trending over time.
- Users can choose to create either an open or closed funnel. An open funnel allows users to enter at any step, while a closed funnel requires users to start from the beginning.
- Funnel analysis can be segmented to understand how different user groups progress through the funnel.
- To create a funnel analysis, users can start with a blank canvas in the Explore tool and select the "Funnel Exploration" technique.
- Users can add steps to the funnel by specifying page views or events. Each step can be directly or indirectly followed by the next step, depending on the user flow.
- Funnel analysis provides valuable insights into user behavior, completion rates, abandon rates, and more at each step of the funnel.
- Users can break down the funnel analysis by dimensions such as device category to understand how different device users move through the funnel.
- Additional features, such as elapsed time and next action analysis, provide further insights into the consumer journey and help identify areas of improvement in the funnel.

Overall, funnel visualization analysis in GA4 is a powerful tool for tracking and optimizing conversion funnels on websites and apps, providing valuable insights into user behavior and conversion rates at each step of the process.

## Chapter 9 - Config Basics

### Enchanced Measurement

- Enhanced Measurement is now enabled by default for new data streams in GA4.

- To check if it's enabled or to enable it for older data streams, navigate to the admin section, select the data stream for your property, and click into the data stream settings. You should see an option for Enhanced Measurement.

- Enhanced Measurement automatically tracks the following user interactions:

1. Page Views: This is already a standard event tracked by Google Analytics, but Enhanced Measurement ensures it is captured.
2. Scrolls: Enhanced Measurement can track user scroll behavior on your website.
3. Outbound Clicks: It automatically tracks clicks on links that lead users outside of your website.
4. Site Search: If your website has a search functionality, Enhanced Measurement will capture the search queries and related data.
5. Video Engagement: For embedded videos on your website, it tracks video play, pause, progress, and other engagement metrics.
6. File Downloads: Enhanced Measurement can track when users download files, such as PDFs, from your website.

- Enabling Enhanced Measurement is recommended as it saves time and effort in manually setting up event tracking for these interactions.

- By enabling Enhanced Measurement, you can get a more comprehensive view of user engagement and behavior on your website or app, making it easier to optimize and improve the user experience.

Overall, Enhanced Measurement is a valuable feature in GA4 that simplifies event tracking and provides richer data insights without the need for extensive custom coding.

### Setting Up Goals

- Goals in Google Analytics 4 are crucial for tracking the quality of traffic and measuring desired outcomes.
- Goals can include e-commerce transactions, ad revenue, form submissions, whitepaper downloads, or any valuable actions on the website.
- Google Analytics 4 allows making almost anything a goal conversion, providing flexibility in tracking various actions.
- If the desired conversion event doesn't exist, custom events can be created with specific conditions to trigger them.
- For example, a custom event named "FormSubmitComplete" can be created to track completed form submissions.
- To create the custom event, the "page_location" is checked for the value "formcomplete."
- Once the custom event is set up, it can be used as a conversion event in the "Conversions" section.
- Google Analytics 4 may take up to 24 hours to display the new conversion event in the Events section.
- Using goals and conversion events, website owners can track valuable user actions and evaluate the effectiveness of their campaigns and website performance.

### Manageing User Accounts

- To manage user accounts in Google Analytics, go to the "User Management" section in the admin area.
- User management can be done at the account level and the property level, with changes at the account level inheriting down to properties.
- To add a user, click "Add users" and provide their email address and desired permissions.
- There are four levels of permissions: Edit (allows managing the account and properties), Collaborate (can collaborate on shared assets), Read and - - - Analyze (can view and filter reports), and User Management (can add or delete users and their permissions).
- Give careful consideration to the permissions you assign to each user based on their role and responsibilities.
- Collaborate is common for users who need access to view and collaborate on shared assets without configuring settings.
- Edit includes Collaborate automatically, and it is required for creating audiences.
- User Management is a powerful permission but doesn't automatically include Edit or Collaborate permissions.
- User permissions can be set at both the account and property levels, and you can override inheriting permissions by editing a property directly.
- Make sure to assign appropriate permissions to users to ensure data security and access to the necessary information for their roles.

