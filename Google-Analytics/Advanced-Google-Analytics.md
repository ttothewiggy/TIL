# Advanced Google Analystics 4

## Leveraging GA4 for Greater Insight

### Surveying advanced GA4 property settings

- Property settings in GA4 offer various features and options to customize your data collection and reporting.
- Key sections in data settings include data collection, data retention, data importing, attribution settings, and data deletion.
- Google signals enable cross-device reporting for signed-in Google users, but privacy considerations should be taken into account.
- Data retention default is set to two months, but it's recommended to increase it to 14 months for deeper exploration.
- BigQuery integration allows you to retain data beyond the 14-month limit.
- Attribution settings are still under development, offering limited options for reporting attribution models.
- Reviewing the lookback window is essential to align it with your sales cycle.
- Data deletion in GA4 is more straightforward and offers more options compared to Universal Analytics.
- Product linking options provide a way to connect GA4 with other Google products for better insights.
- Understanding and reviewing property settings is crucial before setting up data in GA4 to ensure optimal data collection and reporting.

### Building data streams in GA4


- GA4 data streams are how data gets into GA4 and offer more features and flexibility compared to Universal Analytics property IDs.
- There are three types of data streams: iOS app, Android app, and web. We'll focus on web streams due to their versatility.
- Web streams offer various configuration options, such as enhanced measurement settings, connected site tags, measurement protocol secrets, event settings, cross-domain tracking, internal traffic definitions, referral exclusions, and session timeout adjustments.
- Experimenting with session timeout and engaged session timer settings can help optimize data collection based on user behavior.
- Using multiple data streams is possible, but Google recommends using a single stream for most cases. Filtering by stream ID is an option, but it might not be an official feature yet.
- GA4 is designed to handle multiple streams for different platforms like web, iOS, and Android, allowing you to track and analyze data from various sources in one property.

### Implementing data filters in GA4

- In GA4, views are replaced by data filters, which are currently not as flexible as filters in GA Universal but serve a similar purpose.
- By default, GA4 properties have one data filter for internal traffic, but you can add up to 10 filters per property.
- There are two types of filters available: internal traffic and developer traffic.
- You cannot delete filters once created, only set them to inactive, so be cautious when setting them up.
- Data filters can be set to include or exclude specific traffic types based on parameters like IP addresses or query variables.
- Testing filters before setting them to active is crucial, as once data is filtered out, it cannot be recovered.
- GA4 offers a simple method to append the traffic type parameter for web streams using Google Tag Manager and URL query variables.
- For app data streams, the traffic type parameter must be appended manually using the SDK.
- Using Google Tag Manager to add the traffic type parameter is more convenient for cases where IP addresses change regularly.
- Properly configuring data filters will help ensure your GA4 data is accurately filtered and provide meaningful insights.










# Advanced-Google-Analytics

## Chapter 1 - Measuring Data

### How data collection works

- Google Analytics collects data through a snippet of JavaScript code installed on every tracked page of a website. This code monitors user interactions on the site.
- The tracking code can be customized to trigger and pass specific information, allowing for tracking of more than just page views, such as pages, events, eCommerce transactions, and social interactions.
- Each recorded activity is called a "hit," and all hits are packaged into a payload, which is sent to Google Analytics. Each payload must contain a hit type and its required fields, carrying all the insights for analysis.
- The payload includes common parameters like document location (DL), document referrer (DR), and document title, as well as additional insights like screen resolution, viewport size, and tracking ID.
- For specific events, custom dimensions and metrics can be assigned, and the payload includes event category, event action, and optional custom dimensions and metrics.
- Google's Measurement Protocol Parameter Reference provides a comprehensive list of available parameters, and the Hit Builder tool allows testing and validation of hits.
- To introduce more data into Google Analytics, programming may be required, and understanding the possibilities enables collaboration with developers to implement desired insights.
- Knowing how data collection works allows you to think creatively and capture valuable insights beyond the basic page views.


### How new vs. returning users work

- When a user arrives on a page with Google Analytics tracking code, a random unique ID called "client ID" (CID) is generated and associated with the user's browser cookie.
- The client ID remains the same as the user navigates through the website, even when they visit different pages. It persists if the user closes the browser and returns later.
- Google Analytics considers each unique client ID as a unique user. If a brand new client ID is detected, it is counted as a new user, and if an existing client ID is recognized, it is counted as a returning user.
- However, there are limitations to tracking users based on client IDs. If a user clears their browser cookies or uses an incognito window, the client ID is lost, and they will be treated as a new user when they return.
- The client ID allows tracking of the same user across multiple sessions on the same browser and device. To track users across different devices or browsers, the user ID feature needs to be utilized.
- User ID enables cross-device tracking by associating a unique ID with a logged-in user, allowing them to be tracked across different devices and browsers.
- Understanding how new versus returning users are identified in Google Analytics can provide valuable insights into user behavior on the website.

### Tracking users with User ID

- Google Analytics has a limitation when it comes to tracking users across different devices. If a user switches from a desktop browser to a mobile device, Google Analytics considers them as a new user, losing the association with their previous sessions.
- To overcome this limitation, Google offers a feature called User-ID. User-ID allows you to associate multiple sessions across different devices with a single unique and persistent ID that you create.
- To use User-ID effectively, you must have the capability to generate your own unique IDs and assign them to users. This is typically done in scenarios where users log into a service or an eCommerce platform, enabling you to identify them across devices.
- Implementing User-ID requires a programmatic solution to attach the unique user ID to the Google Analytics record.
- While not delving into the detailed implementation of User-ID, it's essential to be aware of its availability and research whether it fits your tracking requirements, especially if you need to track users across multiple devices with consistent identification.

### Using GA4 with single-page applications

- Single-page applications (SPAs) are websites where each page of content doesn't require a new page load.
- Tracking SPAs in GA4 requires some adjustments, and there are three possible methods: enhanced measurement settings, history change trigger in Google Tag Manager, and data layer pushes.
- To use the enhanced measurement settings method, enable "page changes based on browser history events" under advanced settings for page views.
- Check if your website sends history change events in GTM preview mode to determine if this method will work for your SPA.
- The history change method involves turning on history built-in variables in GTM and creating a trigger for a history change.
- Then, a page view event can be created using that trigger, with variables for page location and title added based on your SPA's setup.
- The data layer method is the most precise but usually requires developer help. Your SPA will send data layer pushes when page view events should be fired.
- With this method, you'll set up custom event triggers for page views and data layer variables to capture relevant data, such as page location and title.
- Using the data layer method provides more control and accuracy, making it a preferred option even if the history change method is available.
- Implementing tracking for SPAs in GA4 requires careful consideration of your website's structure and the chosen tracking method.

## Working with Events in GA$

### Working with automatically captured events in GA4

- GA4 automatically captures events that previously required separate setup in Google Analytics Universal.
- Automatically captured events occur in apps and websites, and a list of these events can be found on Google's site.
- Enhanced measurement events are a subset of automatically captured events for websites, and they can be viewed and modified in GA4 data stream settings.
- Page view events cannot be disabled individually through enhanced measurement; if you want to add specific page view-level events, set up a separate tag in Google Tag Manager.
- Scroll depth is automatically captured, but it only records 90% depth, and additional depths require custom event setup.
- Outbound clicks are automatically captured, but be sure to configure your domains properly to avoid recording external clicks within the same GA4 property.
- Site search is automatically captured if the parameter is included; otherwise, you can manually send events using Google Tag Manager and a data layer push.
- Video engagement is automatically captured for YouTube videos embedded on your site, but you'll need to create custom tracking for other video platforms.
- File downloads are automatically captured for specific file types, but custom events are needed for tracking other types of file downloads.
- Custom events can be created to track specific actions not covered by the automatically captured events.
- Modify the automatically captured events or set up custom events as needed to meet your website analysis requirements in GA4.

### Adding new events to GA4

- GA4 automatically captures many events, but not everything. For custom events, use Google Tag Manager to send new events to GA4.
- Check Google's list of recommended events to see if your event is already listed there.
- Create a trigger in Google Tag Manager to capture the form submit event. Use data layer pushes for better control.
- Set up data layer variables in Google Tag Manager to capture form field values.
- Create a GA4 tag in Google Tag Manager with the event name and parameters.
- Add custom dimensions in GA4's custom definitions to accommodate the new parameters.
- Document your configuration thoroughly to help others understand what you've done.
- Always write event names in lowercase to avoid potential issues with GA4.
- There is no hit limit in GA4, so you can track as many custom events as needed.

### Using event parameters effectively in GA4

- In GA4, you can include multiple parameters with events, providing more flexibility compared to GA Universal's limited category, action, and label event properties.
- Review the automatically collected parameters in GA4 events to get ideas for what parameters you may want to use with your own events.
- Plan your implementation and consider what data will be useful to have before adding new parameters. Avoid collecting data just for the sake of it.
- Reuse existing parameters whenever possible to keep your GA implementation tidy and avoid hitting parameter limits.
- You can use up to 25 parameters per event, and parameter names should be under 40 characters while the value should be under 100 characters.
- Make sure to add custom dimensions in the "Configure" section to view and analyze the custom parameters in your reports and explorations.
- Be aware of the limit of 50 custom dimensions in total, so plan in advance which parameters you want to have registered.
- Custom dimensions are a powerful tool and are covered in-depth in the video, "Using Custom Dimensions and Metrics in GA4."
- With GA4, you have the flexibility to track and analyze data in more detail, limited only by your imagination and the 50 custom dimension limit.

### Creating and modifying events in GA4

- GA4 includes powerful event creation and editing tools that allow you to create and modify events based on existing events or specific conditions.
- To create a new event based on an existing one, go to "Configure" > "Events" > "Create event" and select an existing event as the source. You can modify parameters and use typeahead search to ensure accuracy.
- This functionality is helpful for setting up conversions based on specific events, such as page views or form fills, by creating separate events for each form or action.
- To modify an event, go to "Configure" > "Events" > "Modify event" and select an existing modification or create a new one. You can change the event name, add or remove parameters, and reorder modifications if necessary.
- Keep in mind that modifications are applied in a specific order, and you can have up to 50 modifications and 50 created events.
- Modifications do not change historical data and may take about an hour to take effect. They are processed before created events, so you cannot modify a created event.
- Use event creation and modification to tailor your GA4 data to your specific analysis needs and improve the accuracy and organization of your events.
- Remember to use lowercase letters in your events, as GA4 considers differently-cased event names as separate events.
- Utilize these features to enhance your GA4 data and gain valuable insights into user behavior and conversions on your website or app.

### Using the debug view in GA4

- GA4 has a debug view that is very robust and useful for testing analytics implementations.
- There are three ways to access debug mode: using the Google Analytics Debugger Chrome extension, adding a debug mode parameter in your GA4 code, or enabling debug mode in Google Tag Manager.
- To use the Chrome extension method, install the Google Analytics Debugger Chrome extension, click the extension icon to enable it, and then reload the page.
- For direct GA4 code on your site, add a debug mode parameter to the configuration code to enable debug mode for all events, or add the parameter to specific events to debug only those.
- In Google Tag Manager, edit the GA4 configuration tag and add the debug mode parameter in the "Fields to Set" section, or add it to specific event parameters.
- Access the debug mode in GA4 under the "Configure" menu.
- Debug mode shows incoming events quickly, and you can pause the timeline to review events at your own pace.
- Clicking on individual events shows the parameters for that event on the right-hand side.
- Debug mode is valuable for testing custom analytics implementations and ensuring everything is set up correctly before going live.

### Configuring conversion events in GA4

- Conversions in GA4 are simplified and entirely based on events.
- To set an event as a conversion, go to Events under Configure and turn on the slider for the desired event.
- Custom Events can be created to capture conversions that don't neatly correspond with existing events.
- Turning off conversions is easy by setting the conversion slider to Off, but historical data remains unchanged.
- To set a conversion for a new event that hasn't been recorded yet, go to the Conversions option, click New Conversion Event, enter the event name, and save it.
- GA4 allows tracking ad networks for app tracking in the Network Setting section.
- Limit edit access to properties to avoid accidentally turning on every page as a conversion.







## Old GA
## Chapter 2 - Views

### About Views

- Views are subsets of the Analytics property allowing unique configuration settings and filters.
- They help users work efficiently and gain different perspectives for valuable insights.
- All data sent to Google Analytics property is associated with all views.
- Use filters to focus on specific data subsets within each view.
- Best practices include having at least three views: raw data, test, and master.
- Raw data view is unfiltered, acting as a safeguard against incorrect filters.
- Test view is for experimentation and not used for real reporting.
- Master view has minimum filters aligned with business needs for regular reports.
- Additional views can be created for specific needs like target market or traffic sources.
- Views can be based on subdomains, folders, device types, etc.
- By default, there's one view including all website data; create additional views to optimize workflow.
- Up to 25 views can be used to understand and analyze website data.

### Create a measurement plan

- Clear measurement strategy needed for collecting data in Analytics, pulling reports, setting filters, and features.
- Define business objectives and how outcomes will be measured.
- Users take key actions on the website leading to macro and micro conversions.
- Macro conversions are broad goals like making a purchase, while micro conversions support macro conversions.
- Measurement plan includes business objectives, supporting strategies and tactics, key performance indicators (KPIs), segments, and KPI targets.
- Example measurement plan from Google's help articles for the Google Merchandise Store.
- Once you know what to measure, you can configure Google Analytics in an advanced and robust manner.

### Adding a new view

- To create a new view for an existing property, go to the Analytics dashboard and select "Admin" in the lower left-hand corner.
- In the admin view, choose the account and property you want to create the view for.
- Click on "Create View" in the right column.
- Select the type of data you are tracking, such as website data or mobile app data.
- Give the view a specific and descriptive name.
- Choose the reporting time zone for the view, which affects how data is displayed but not how it's collected.
- Click "Create View" to create the new view.
- The new view will appear in the right-hand column and in the views pane in the upper left-hand corner.
- You can toggle between views by selecting the view you want to see.

### View settings

- To edit view settings, go to the admin view by selecting the gear icon in the bottom left-hand corner.
- Confirm the account and property, then select the view you want to edit from the dropdown menu on the right-hand side.
- In the view settings, you can edit the view name and confirm the website URL with HTTP or HTTPS.
- You can change the time zone, but it only affects data moving forward, not retroactively.
- The default page setting allows you to specify if your website serves the same content for different URL variations (e.g., yoursite.com and yoursite.com/index.html). It's better to leave this blank and use filters to control such variations.
- You can exclude URL query parameters that do not change the page's content by adding them to the exclusion list.
- For monetary values, you can select the desired currency display format, such as US dollars.
- It's recommended to leave the option to exclude all hits from known bots and spiders checked.
- You can toggle on site search if you're using it and learn more about it by hovering over the question mark.
- Save the changes after configuring the view settings.
- Views in the web and app versions have similar settings with some variations.


### View Panel

- At the view level, you can set user management, deciding who can access the view.
- Configure goals specific to the view to track important conversions.
- Manage content grouping to organize your data within the view.
- Utilize powerful filters to customize the information displayed in the view's reports.
- Access features like channel settings, channel grouping, and e-commerce settings at the view level.
- Personal tools and assets are not associated with the view level but appear in the column for easy access.
- To access these view-level options, go to the admin overview by selecting the gear icon labeled Admin.


## Chatper 3 - Filters

### View Filters

- There are two types of filters in Google Analytics: predefined filters and custom filters.
- Predefined filters are already set up by Google and can include or exclude data based on traffic parameters like ISP domain, IP address, subdirectory, or host name.
- Custom filters offer more flexibility and allow you to include or exclude data based on various criteria, such as device category or specific patterns in fields.
- Custom filters can also be used to normalize data by using lowercase and uppercase filters to make reports more consistent.
- Search and replace filters let you search for a pattern in a field and replace it with different data.
- Advanced filters enable you to combine data from two fields to create a third field, and you can even use regular expressions for more advanced manipulation.
- It's important to test filters in a test view before applying them to your main views to ensure they work as intended.

### Filter ordering

- The order of filters in Google Analytics is crucial, as they are applied sequentially from top to bottom.
- Filters can include or exclude data and manipulate it in various ways.
- Incorrect filter order can lead to issues with data reporting.
- To manage filter order, go to the Filters option within your view and select Assign Filter Order.
- Review and rearrange filters to ensure they are firing in the correct order.
