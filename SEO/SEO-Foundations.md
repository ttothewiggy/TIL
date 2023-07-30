## Notes on SEO Foundations LinkdIn Leanring Course

### Search Engine Optimisation

- Search engine optimization is the process of making improvements on and off your website in order to gain more exposure in search engine results.
- Search Engine Result Pages (SERPS)

### Foundations

Similar to the tryrating job. Keyworkds: Intent, reliabilty, relevance. 

## Chapter 1 - Intro

### Uderstanding GTM

- Google Tag Manager is essential to manage the complexity of tags, scripts, and tracking pixels on websites.
- It provides speed, agility, and the ability to make changes remotely, avoiding long release cycles.
- Corporate governance is enforced through the permissions model, ensuring compliance with standards.
- Proper tag management improves data accuracy and ensures effective website and digital marketing.
- Increased automation reduces the need for hard-coding and keeps code clean and up to date.
- Google Tag Manager utilizes Google's data center infrastructure for high speed and reliability.
- Centralizing and simplifying the release process improves efficiency and reduces workload.
- Google Tag Manager is free and a valuable tool for the future of digital marketing.

### Understanding the GTM Hierachy

- The Google Tag Manager (GTM) is based on the concept of a container that holds all scripts and tags.
- The older model of running scripts on a page required manual coding for each page and script, leading to complexity.
- In the modern tag manager model, a single JavaScript snippet is placed on all pages, acting as the container for all tags.
- The container holds three types of entities: tags (collect and manipulate data), triggers (rules to fire tags), and variables (information accessible to tags and triggers).
- GTM is part of the Google marketing stack and uses Google single sign-on authentication.
- Multiple containers can be used in one GTM account, with each container corresponding to a website or domain.

### Server-Side vs Client-Side Tags Explained

- Server-side container is a new option in Google Tag Manager that works differently from the usual client-side approach.
- In the client-side model, scripts are downloaded and executed in the browser.
- In the server-side container, a server is configured to communicate with the container and send data to various destinations.
- Server-side tagging offers additional control, potential security improvements, and reduced browser load times.
- However, it doesn't support all tags, may have associated costs, and is considered an advanced implementation.
- Google recommends implementing the container in the standard client-side way first before considering a migration to server-side.

## Chapter 2 - Work with Accounts and Containers

### How to configure permissions and security in Google Tag Manager

- User permissions and security are critical considerations in Google Tag Manager (GTM).
- GTM allows controlling who can publish code to your site, ensuring authorized access.
- Permissions can be set at the account and container levels.
- Available permission levels: Administrator, User, Edit, and Approve.
- Give users the lowest permissions needed to avoid accidental deployments.
- "Publish" permission is crucial and should be limited to key individuals.
- Implement two-step log and verification for added security.
- Properly configuring user permissions is essential for a successful GTM implementation.

### Create an account and container

- Create an account and container in GTM by logging in with your Google account.
- Set up the container with the domain name and usage type.
- Copy and install the container code snippets provided on your site.
- Add users to the account and set their permissions (e.g., "edit only" user).
- You can create multiple containers for different sites, each with a unique ID.
- Enable two-factor authentication for added security.
- While waiting for the container code, configure your container in the interface.
- In the next video, learn how to put the container code on your page.

### Install your first container

- Copy the JavaScript snippet from GTM.
- Paste the first part in the head tag of each page you want to track.
- Paste the second part (no script) in the body tag of those pages.
- Verify the installation in the page source.
- Place the container code on every desired page.
- Use GTM interface to create tags and triggers.
- Ensure proper code placement for GTM to function correctly.


## Using Built-In Tags

### Efficiency bonus: Google Analytics built-in tags

- Advantages of tag managers: simplifies deploying tags with templates.
- Google Analytics (GA) is a popular tag, commonly used.
- Install the GTM container code on every desired page.
- Create a new tag in GTM to set up GA tracking.
- Choose tag type: Standard Universal Analytics.
- Set track type: Page View.
- Configure GA settings, such as tracking ID and display advertising features.
- Save the tag and add a trigger to fire on all pages.
- Publish the container to make the tag live.
- Verify the GA tag is firing using tools like WASP.
- GTM can handle more than just GA; explore other tags in the next video.


### CrazyEgg and other built-in tags

- Explore other tags in GTM for various functionalities.
- Google offers built-in tags for AdWords, DoubleClick, remarketing, and more.
- Other tags from external providers like AdRoll, Mediaplex, Marin, Crazy Egg, etc.
- Try Crazy Egg as an example of a turnkey tag template.
- Add Crazy Egg tag, set trigger for all pages, and publish it.
- Turnkey tags are quick to deploy and less prone to errors.
- Turnkey tags are maintained by Google and vendors, ensuring updates.
- GTM continues to add more integrations for easier tag management.


## Chapter 3 - Work with Variables

### Understanding basic variables

- Variables in GTM allow reusing values across multiple tags.
- Variables consist of key-value pairs.
- Example of a constant variable: Google Analytics ID.
- Example of a dynamic variable: Current URL.
- Dynamic variables update automatically based on page views.
- Variables are useful for sending contextual data to analytics systems.
- Example: Using a variable to capture user's local time.
- Variables offer flexibility and efficiency in tag management.
- Next videos will demonstrate how to implement examples using variables.

### Utilize built-in variables

- Variables in GTM allow reusing values across tags.
- Built-in variables are available and configurable in the workspace.
- Example of using a built-in variable, Page URL, as a custom dimension in Google Analytics.
- Custom dimensions are numbered indexes used to send additional data to GA.
- Variables can be combined with custom dimensions for dynamic data tracking.
- Browser tools like WASP or Chrome dev tools can be used to check the data being sent.

### Create custom variables

- Variables can be used to minimize errors and simplify changes in multiple tags.
- Google Analytics settings variable allows using the same account number across various tags.
- Creating variables in Google Tag Manager can be done by selecting a constant and defining its value.
- User-defined variables are shown in the variables section and are aware of their usage in tags.
- Next, the video will cover dynamic variables and JavaScript tricks for populating them.

### Dynamic Variables

- Dynamic variables are used to capture data that changes based on user interactions.
- Custom JavaScript variables can be created to fetch data from global variables, cookies, URLs, or scrape text from the page.
- Custom JavaScript variables are flexible but should be used with caution as they can be fragile and prone to breaking.
- Dynamic variables can be used to populate tags for conversion tracking and send critical data to marketing tools.
- With dynamic variables, data like shopping cart totals can be retrieved from JavaScript, loaded into GTM, and then sent to Google Ads for conversion tracking.

### Incorporating custom JavaScript into GTM variables

- Custom JavaScript can be utilized within Google Tag Manager (GTM) to extract data and perform specific actions on the page.
- Custom JavaScript variables can be created in GTM, allowing you to write and execute JavaScript code directly within the tool.
- Custom JavaScript variables are useful for extracting data from the page in real-time and storing it as variables.
- For example, you can create a custom JavaScript variable to retrieve the local time of the user's browser and store it as a variable (e.g., Local Browser Time Hour).
- These custom variables can be sent back to Google Analytics as custom dimensions or used for other purposes within GTM.
- Viewing the current variables in use can be done through the GTM workspace under the "Versions" section.
- Utilizing variables makes code more repeatable and reliable, improving the overall efficiency and effectiveness of GTM implementation.

## Chapter 4 - Create Triggers

### Understanding triggers

- Triggers in Google Tag Manager determine when and under what circumstances a tag should be fired.
- A tag remains dormant until a trigger instructs it to execute, making it crucial to configure triggers accurately to ensure tags are fired only when needed.
- When setting up triggers, it's essential to be specific and precise about when a tag should fire to avoid misfiring on irrelevant pages.
- GTM offers various trigger options, such as DOM Ready, element visibility, custom events, timers, and more, to define when a tag should fire.
- Testing and troubleshooting triggers is important to verify that tags execute as intended and don't misfire on unrelated actions or pages.
- Triggers should be flexible enough to accommodate minor page changes while avoiding being overly broad, which could lead to excessive firing of tags.
- Incorrectly configured triggers can break tag functionality when page elements change, so it's crucial to be cautious and thorough during setup.
- In the next section, more examples of different trigger types will be explored.

### Fire Google Analytics events using triggers

- Triggers in Google Tag Manager determine when and under what circumstances a tag should be fired.
- Tags remain dormant until a trigger instructs them to execute, making it essential to configure triggers accurately to ensure tags are fired only when needed.
- Google Tag Manager offers various trigger options, such as page views, element visibility, custom events, timers, and more, to define when a tag should fire.
- Triggers should be specific and precise to avoid misfiring on irrelevant pages or actions.
- Google Analytics events are a great way to track interactions with elements on the page and can be used to track outbound link clicks or other specific actions.
- To track outbound link clicks, a trigger can be created that fires the event tag when a link's URL does not contain the domain, indicating an external link.
- Utilizing variables and data layer variables allows for dynamic and flexible tracking of various events and interactions on the website.
- By combining tags, triggers, and variables, powerful tracking and analytics capabilities can be achieved with Google Tag Manager.
- In the next sections, more examples of using triggers and events will be explored to showcase the versatility of Google Tag Manager.


## Chapter 5 - Control Versioning 

### Create versions and view publishing history

- Google Tag Manager offers a versioning system that allows you to create snapshots of your workspace at different points in time.
- Versions in Google Tag Manager help you track changes, maintain a history of your edits, and facilitate rollbacks if needed.
- Creating versions in Google Tag Manager is similar to saving different versions of a document while writing a novel in Microsoft Word.
- Each version can be named descriptively, making it easy to identify changes and understand the purpose of each version.
- You can create and save versions without necessarily publishing them live to your website. This allows for testing and reviewing changes before deployment.
- When making changes to the workspace, you can set a previous version as the latest version if you need to revert back to it.
- Keeping detailed notes and descriptions for each version is essential for maintaining clarity and understanding the changes made, especially when working with a team.
- Google Tag Manager also allows you to create multiple workspaces if you work with a team, providing a more organized and collaborative environment.
- Utilizing version management effectively ensures that you can easily back out of changes or revert to previous versions, reducing the risk of errors and improving overall data accuracy and reliability.


## Debug Your Tags

### Using Preview and Debug modes

- In a corporate environment, it's essential to use Preview and Debug mode for testing changes before publishing them live.
- Preview mode sets a special cookie in your browser that enables you to see changes made to tags, triggers, and variables in your current container version as if they were live.
- Only the user with the Preview and Debug cookie will see the changes, while everyone else will see the previously published version.
- The Preview pane provides a summary of tags that have fired on the page, tags available but not fired, and more detailed information about tag firing at different states (e.g., page view loaded, DOM ready, window loaded).
- Utilize Preview and Debug mode to confirm that tags are firing correctly and transmitting the desired data before publishing changes.
- Debugging in Preview mode helps troubleshoot configuration issues and ensures data quality and accuracy.
- Try creating false positives and testing different user scenarios to ensure the configuration handles various use cases.
- Spend most of your editing time in Preview mode to thoroughly test and verify changes before publishing, following your organization's release process.

### Using WASP to debug

- WASP is a general tool used to visualize what's happening with your site, tags, and the data layer. It provides deeper integration with tags and does not require enabling the Preview Debug mode in the console.
- To install WASP, search for "WASP Chrome Store" and install it from the Chrome Web Store.
- To access the WASP Developer Console, use the shortcut Ctrl+Shift+I (or F12) on Windows, or Command+Option+I on Mac, then click on WASP.
- WASP displays the tags that are currently firing and shows the sequence of scripts that lead to their execution. It helps trace back where tags are loaded and which tags are firing other tags.
- WASP retains information about tag firing even when navigating to a new page, making it useful for analyzing events that happen after a link click or form submission.
- While GTM's Preview Debug mode is a fantastic tool, WASP can showcase tags that execute outside of GTM, providing valuable insights into tags not managed by GTM.
- WASP and GTM's Preview Debug mode complement each other, providing a full visualization of what's happening on your site.
- Using both WASP and GTM's Preview Debug mode can help ease anxiety and provide a clearer understanding of tag behavior and data transmission on your site.

## Chapter 7 - Use Customer HTML Tags

### Understanding and using custom HTML tags

- While Google includes many commonly used tags as built-in options, there are numerous other tags a site owner may need to manage.
- To create a custom tag, select "Custom HTML" or "Custom Image" when adding a new tag.
- For Custom HTML, you have a box where you can write any HTML code you want. This code can interact with the variables you have set up in Tag Manager.
- Custom HTML tags can be used for various purposes, such as logging data to the console, creating alert boxes, or inserting third-party tags that are not available as built-in options.
- You can utilize the variables you've set up by using curly braces and selecting the desired variable from the list, which helps avoid typos.
- After creating a custom tag, you need to set up a trigger to specify when the tag should fire. Triggers can be configured based on various conditions, such as firing on all pages, specific page views, clicks, or other events.
- To test the custom tag, you can use the Preview mode in Tag Manager, which allows you to see the tag's behavior in your browser without publishing it live for all users to see.
- Custom HTML tags can handle complex scenarios where you need to manage third-party or specialized tags that are not part of the built-in options.

### Understanding and using custom Image tags


- Custom image tags allow you to fire specific image pixels on your website by specifying the image URL.
- To create a custom image tag, select "Custom Image" when adding a new tag and provide the image URL in the provided field.
- You can use either a relative URL (starting with "//") or an absolute URL (e.g., "https://example.com/image.gif") for the image.
- The custom image tag can be triggered based on various conditions, such as firing on all pages, specific page views, clicks, or other events, depending on your tracking requirements.
- When using custom image tags, it's essential to consider the potential impact on website performance and user experience. Loading additional images can add to the page's size and affect loading times.
- Best practices for using custom image tags include using them sparingly and only when necessary, optimizing the image size, and considering the overall performance impact on the website.
- Be cautious with custom JavaScript and image tags, as they can introduce vulnerabilities and security risks if not implemented carefully.
- Use custom tags only when built-in options or other tools are not available for your specific tracking needs.

Remember that while custom tags provide flexibility and functionality, it's essential to use them thoughtfully and responsibly to ensure they enhance your website's tracking and analytics capabilities without negatively impacting its performance and security.

### Best Practices

- JS can be malicious - enable secondary authentification. 
- JS can eb accidentally malicious. 
- Use the included tags when possible.
- You could (and should) use GTM variables in customer HTML. 
- Do not use for site structure. 
- Check for doc.write. 
- Can reference JS libraries, but must pre-load. 
- Tst, test, test!