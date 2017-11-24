# Krux (Salesforce DMP)

## Primary Location
United States (San Francisco) [Crunchbase, 01](https://www.crunchbase.com/organization/krux-digital)

## Website
[https://www.salesforce.com/products/marketing-cloud/data-management](https://www.salesforce.com/products/marketing-cloud/data-management)

## About
Salesforce DMP is a data management platform that manages data, identifies end users, and cetnralizes user-level data for advertising and content personalization [Salesforce, 24](https://konsole.zendesk.com/hc/en-us/articles/115012398067-What-if-I-just-want-to-import-data-instead-of-using-the-Control-Tag-SDK-or-other-DMP-tracking-)

## Ownership
Salesforce

## Detection Rules
krxd\.net

## Documentation
[https://konsole.zendesk.com/hc/en-us/articles/226031268-Android-SDK-Implementation-Guide](https://konsole.zendesk.com/hc/en-us/articles/226031268-Android-SDK-Implementation-Guide)

## Products and Services

### TECHNOLOGY
**AMP for Mobile Tracking**  
"What is AMP?
AMP stands for ‘Accelerated Mobile Pages’ and is designed to facilitate mobile-optimized content. A notable aspect of the design is that it keeps 3rd party JavaScript out as much as possible to improve performance, however, there are AMP libraries available to provide additional rich content."  

How does AMP serve ads?
Ads are served through an <amp-ad> element on the page.  It loads the ad through an Iframe of a different origin and executes our JavaScript into the Iframe.  The origin point is up to the client, but it will eventually load a remote.html file provided by Salesforce.

See AMP FAQ for more: [Salesforce, 56](https://konsole.zendesk.com/hc/en-us/articles/115000428507-AMP-FAQ)

**Data Layer**  
"What is a data layer?
A data layer is a Javascript object that’s used to house information about the page and user. It is implemented to store contextual data you would like to pass from the page to other applications.

What are the benefits of a data layer?
The utilization of a data layer affords an efficient, agile approach to pass data from your website to other devices. It’s more stable and secure than individual ‘scraper’ commands, and is less susceptible to modifications rendered to the html markup. When using a DMP, the data layer grants a streamlined framework to send data about your site pages, users, and content into the data management platform.

How can I tell if we have a data layer implemented on our website?
Site developers will often, though not always, denote the universal data object with an intuitive name, such as “dataLayer”. If that’s not the case, however, you can determine if one is set up by searching the page source for an organized set of page- and user- commands under a single object, such as the following:" see website: [Salesforce, 57](https://konsole.zendesk.com/hc/en-us/articles/115000428427-Data-Layer-FAQ)

**DMP Control Tags**  
"a snippet of code associated to a confid that gets generated to include in Websites, Media and uniqueids (confid) for mobile SDKs".  "Similar to Google Analytics for websites," Control Tag "gets placed in the </head> section of a website to enable tracking, targeting and more".  It performs, among other things, Data Capture for User Matching, Attributes, URLs, and JavaScript Events; Tag Management & SuperTag delivery of tags; Real-time segments and site Personalization; and Owned & Operated Targeting.  A good link: [Salesforce, 25](https://konsole.zendesk.com/hc/en-us/articles/115012555408-What-does-the-Control-Tag-do-).  

"The Control Tag is typically loaded via a JavaScript snippet which in turn loads the the configuration and the application components asynchronously leaving the browser free to continue parsing the rest of the page, only executing the code when it is available" [Salesforce, 26](https://konsole.zendesk.com/hc/en-us/articles/115012367627-Will-the-DMP-Control-Tag-Impact-Page-Load-Performance-)

**Cross Device Identity Mangement (Declarative and Predictive)**  
Predictive DCIM costs an extra fee.  "The Predictive CDIM report describes all of the devices associated with people already in a given segment.  It allows you to identify and map consumers and behavior patterns consistently across all devices, screens, and platforms."

_Key features include_: "Connects known and unknown devices (declared and predictive) / Create a CDIM segment directly from the report / Aggregate audiences and their data across devices / A choice of similarity levels allows you to consider the trade off between accuracy and scale".  _Key benefits include_: "Improves reach, relevance, and inventory monetization / Increases your opportunity to sequence ads, at optimal frequency, for consistent messaging and experience across channels, throughout the journey / Delivers accurate analytics for segment profiles and campaign conversions?

_Probablistic Matching:_  
"How does the probabilistic matching algorithm work?

The core of the model is designed to uncover the devices that stay together in various places over long periods of time. To do this effectively there are three important considerations - scale, training, and validation.

    Scale - Because the success of the model is predicated on seeing lots of devices and how they move over time, it is essential to have massive reach into the device world. With one of the largest device footprints on the planet, Salesforce DMP has an advantageous position from which to deliver accurate results.
    Training - Salesforce DMP uses deterministic data coming from authenticated events (logins, purchases, etc) to provide a truth set for training the algorithm.
    Validation - From the deterministic data set, Salesforce DMP reserves some data to validate the efficacy of the model.

Between these three items we are able to continuously improve the accuracy of the predictions and deliver a better product.

To better understand the view of devices over time, consider a user's work and home movement. During the work day, all of the user's devices are likely to be tied to the same IP from work. However, colleagues are also tied to the same IP and in that single snapshot of time, it may be assumed the user and their colleagues are the same person.

Looking at that same IP address at night, there is likely no activity, as everyone has left the office. When looking at the user's home IP at night, all of the devices that belong to that user and their family are tied to the same IP. That single snapshot might imply that the usr and their family are one "person".

...

How are shared devices handled in relation to the CDIM algorithm?

Salesforce DMP applies logic to ensure that we credit the most rational ONE deterministic ID to each KUID. We take into account multiple factors when making this determination, but frequency and recency are highly weighted aspects.

For example, if you and your significant other have both logged into a major news site on the same device (KUID1), but you have done so 10x more times and you were the most recently logged event in association with that device, the credit would be applied to you, and not your significant other.
Is household identity part of CDIM?

The CDIM solution in the Salesforce DMP does not currently have a household component at this time.
Does Salesforce DMP use 3rd party data or software to enhance its CDIM?

No, Salesforce DMP does not use 3rd party data to deliver CDIM.
Can I provide external matches to help improve device matching for my business?

Yes, If a match table is provided, it can be incorporated and the matches will be only available to that account.
Can the device graph be exported?

No, the device graph itself is not exportable. However, the Extended CDIM Data Feed is available and includes the deterministic ID for the device where applicable.

...

Is global data or US data used for the CDIM algorithm?

Currently, all data is used for the CDIM algorithm. Region-specific versions are not available. The Salesforce DMP is currently and will continue to be compliant with all global and regional privacy policies.
What percent of all devices are mapped on the CDIM graph?

Salesforce DMP can map ALL devices. However, this is a question of accuracy and scale. The higher the accuracy, the fewer matches expected.
How are Safari users being captured?

Salesforce DMP is not able to capture Safari in CDIM, as we do not have the ability to drop 3rd party cookies. We are working hard to identify a solution that will address the limitations of Safari in CDIM.
Does CDIM include app or only web/cookies?

CDIM includes app and web. Salesforce DMP supports IDFA, AAID, and Cookies. We will soon be adding additional device categories to CDIM.
If the majority of app users do not log in, how meaningful is the data collected for probabilistic matching?

The quality of the probabilistic matching algorithm is improved by deterministic data coming from all clients. If a customer does not have deterministic data, it does not mean that CDIM is not a valuable feature. It simply means the entire set of devices in the account must be probabilistically matched. Several factors will determine the validity of this approach for any given client. These factors are related to the level of uniqueness of the audience relative to the general device pool." [Salesforce, 27](https://konsole.zendesk.com/hc/en-us/articles/115009397188-Cross-Device-Identity-Management-CDIM-FAQ-)

"What population considerations are made when a segment is pushed from Salesforce DMP to DFP?
When a segment is pushed to DFP, Safari IDs are removed from the total population since Safari does not allow third party cookies.

Salesforce DMP then identifies all KUIDs that match to a Google user ID. The users that match are pushed to DFP, while remaining KUIDs are eliminated from the population sent to DFP." [Salesforce, 36](https://konsole.zendesk.com/hc/en-us/articles/115010886887-DFP-FAQ)

Difference between predictive and declarative modeling [Salesforce, 29](https://konsole.zendesk.com/hc/en-us/articles/226951307-How-to-Build-Segments-with-CDIM)  

Predicting with device composition: "Device Composition: Salesforce DMP uses predictive cookie matching to fill in the gaps where cookies may not be present, such as mobile apps, Safari browser, ad blocking software, etc. However, because Google is looking for active audience cookies, the two systems use different logic around device composition. If your segment includes a high volume of non-stable cookies (mobile/Safari/cookie-less devices), that can impact the match rate." [Salesforce, 37](https://konsole.zendesk.com/hc/en-us/articles/115010886887-DFP-FAQ)

"Each user creates multiple Krux User IDs (KUIDS) - cookies in browsers as well as IDFAs or AdIDs for mobile apps. Once our cross devices algorithm identifies that two of these KUIDs belong to the same person, we increase the count of "people" by one and select one of the KUIDs to be the "leading" KUID. We call this the one the "Uber ID". 

There are some rules in place to determine which of the KUIDs is elected the Uber ID. This evaluation can change from day to day. If the Uber ID KUID is not active for a couple of days, it loses it's status as Uber ID. In this special case, the Uber ID is removed from the segment population list and shown accordingly as "deleted". 

It is mainly Safari users to contribute to these Uber ID changes, as on Safari each page impression created a unique new KUID." [Salesforce, 54](https://konsole.zendesk.com/hc/en-us/articles/115006652948-Segment-Processing-FAQ)

**Hadoop**  
"Salesforce DMP uses Hadoop for big data processing" [Salesforce, 32](https://konsole.zendesk.com/hc/en-us/articles/214918988-First-Party-Data-Import)

**Browsers supported**  
Browser support listed as Chrome, Firefox, IE, Edge, Safari (Opera without patching compatability issues). [Salesforce, 33](https://konsole.zendesk.com/hc/en-us/articles/115012221127-Browser-Support)

**Salesforce DMP Einstein**   
"Salesforce DMP Einstein Segmentation, which allows marketers to use machine learning to discover the multiple distinct personas that exist within their audience.

Using Einstein AI, on top of unified consumer data from both first and third-party sources, enables us to algorithmically determine the “personas” that best define a brand’s audience. Now, companies can personalize marketing and reach each key persona with a message that is going to resonate, rather than blasting a one-size-fits-all retargeting message to everyone that happened to land on a particular webpage. For example, Conagra Brands has seen dramatic results by customizing the messages to different consumer personas for its Hunt’s brand.

This is a great example of how our data management layer consisting of first, second, and third-party data can feed our growing AI layer to create tangible value for marketers." [Salesforce, 1](https://www.salesforce.com/blog/2017/05/krux-is-now-salesforce-dmp.html)

**Backend**   
Salesforce DMP SDK is not mandatory: "we can also ingest the data via http calls initiated by the App or via log files. Both solutions can only be used for data collections though, but not return the segments of a user to the App." [Salesforce, 2](https://konsole.zendesk.com/hc/en-us/articles/115000451248-Salesforce-DMP-SDK-FAQ)

_Google integration:_ "How do I send segments made up of mobile app users to DFP for targeting?

Like the Interchange onsite code which passes Salesforce DMP segment IDs of the users, apps using the DFP SDK allows for custom targeting.

Developers should refer to these articles:

* iOS - https://developers.google.com/mobile-ads-sdk/docs/dfp/ios/targeting
* Android - https://developers.google.com/admob/android/targeting

We recommend testing before publishing by adding a segment to a device to ensure it is passed to in the DFP ad request.

Why is Google Play services required for the Salesforce DMP SDK integration on Android?

Following Google's privacy policy, Salesforce DMP uses the Advertising ID as the user ID. This requires Google Play Services to be implemented with your app.

For more information, see:
https://support.google.com/googleplay/android-developer/answer/6048248?hl=en" [Salesforce, 2](https://konsole.zendesk.com/hc/en-us/articles/115000451248-Salesforce-DMP-SDK-FAQ)

**Tracking**    
_Device strategies & KUIDs:_ "We differentiate between Mobile Web and Mobile App. Mobile work works just like Desktop Web with KUIDs stored as 3rd Party cookies. This has all the benefits and limitations (e.g. Safari) Desktop Web has.

Mobile Apps cannot access cookies. They provide their device IDs IDFA (iOS) or AdID (Android) which are used by Salesforce DMP as unique identifiers instead of a Salesforce DMP cookie." [Salesforce, 3](https://konsole.zendesk.com/hc/en-us/articles/115000428127-Mobile-IDs-FAQ)

_Reidentification:_ "Can I reidentify users in Apps?
Yes, the IDFA or AdID stays constant. Users can be reidentified and targeted in Apps with these device IDs. User can reset this ID and receive a new one though. This is comparable to deleting cookies but not widely used." [Salesforce, 3](https://konsole.zendesk.com/hc/en-us/articles/115000428127-Mobile-IDs-FAQ)

_Mobile Web & Mobile IDs:_ "Can I connect Mobile Web and Mobile App users?
Natively this is not possible. If the user logs in on Mobile Web and Mobile App using the same credentials, Salesforce DMP can store this login ID to both the Mobile Web cookie and the Mobile App device ID and such create a connection of the profiles. This is treated just like cross-device identification." [Salesforce, 3](https://konsole.zendesk.com/hc/en-us/articles/115000428127-Mobile-IDs-FAQ)

_Tracking in Safari and 3rd party cookie subversion:_ Uses Hashed Device Management and 1st Party cookies (set by clients) to target Safari users, as well as a proprietary Hashed Device Identification; fingerprinting.  **Salesforce can use Google PPID** if in conjunction with client and client shares Google cloud storage location.  

Can you user-match with 3rd-party data providers when utilizing a first-party cookie?

Clients will issue a 1st-party cookie to the Salesforce DMP, which we then take as our ID. Since it's not a 3rd party cookie – even though we are acting as an agent of our clients – it means that we are unable to sync those users with a 3rd party data provider unless the 3rd party fires a match pixel.
 [Salesforce, 4](https://konsole.zendesk.com/hc/en-us/articles/115000428307-Safari-FAQ)

_CDIM & Hashing:_ "What makes Salesforce's Hashed ID different from competitive offerings?
There are a few vendors outside of Salesforce who provide Hashed Device IDs, however, they do not couple it with a CDIM solution. This enables Salesforce to associate Safari activity within a larger, holistic set of that individual’s data and utilize Safari activity within a larger conversion path.

How can you tell if other providers offering Hashed Device Management solutions are accurate or employing CDIM?
If or when you hear really high numbers of unique users (UUs) reported against Safari, it often means that they are not resolving the browser down to a single user; each page view counts as a UU in Safari if you don't have a CDIM solution." [Salesforce, 4](https://konsole.zendesk.com/hc/en-us/articles/115000428307-Safari-FAQ)

_Viewing IDs (Safari FAQ):_ "Where can I see the IDs once they’ve been enabled?
You can view the hashed device ID in the pixel.gif call from beacon.krxd.net under kfuid, which serves as the user’s KUID on Safari. The kxfp value is also a corresponding hashed ID that comes from the user data service.

Are Hashed IDs written to LocalStorage?
Yes, you can view your browser’s ID, as noted above, in localStorage corresponding to “kxfp_id” and “kxfp”" [Salesforce, 4](https://konsole.zendesk.com/hc/en-us/articles/115000428307-Safari-FAQ)

"Do users have a KUID in Mobile Devices?
We differentiate between Mobile Web and Mobile App. Mobile work works just like Desktop Web with KUIDs stored as 3rd Party cookies. This has all the benefits and limitations (e.g. Safari) Desktop Web has.

Mobile Apps cannot access cookies. They provide their device IDs IDFA (iOS) or AdID (Android) which are used by Salesforce DMP as unique identifiers instead of a Salesforce DMP cookie.

Can I reidentify users in Apps?
Yes, the IDFA or AdID stays constant. Users can be reidentified and targeted in Apps with these device IDs. User can reset this ID and receive a new one though. This is comparable to deleting cookies but not widely used.

Can I connect Mobile Web and Mobile App users?
Natively this is not possible. If the user logs in on Mobile Web and Mobile App using the same credentials, Salesforce DMP can store this login ID to both the Mobile Web cookie and the Mobile App device ID and such create a connection of the profiles. This is treated just like cross-device identification." [Salesforce, 58](https://konsole.zendesk.com/hc/en-us/articles/115000428127-Mobile-IDs-FAQ)

**More Tracking**  
_Event pixels:_ "Event pixels are used to capture any user-based interaction. Examples include clicks, downloads, and form data. These interactions can be used to understand how people respond to prompts on a page, content, advertising messages, or as a means for additional first party data capture."  They can be used in real-time segments, which are evaluated in-browser.  The "JavaScript version of the pixel must be used, and your unique Control Tag must also be firing on the page(s). This is not available for events captured outside of the client's environment (i.e. where the Control Tag is not deployed)."  They can be used within an iFrame, and "the HTML version of the event pixel can be used. The JavaScript version will not function properly, as the Krux Control Tag is in the parent window."

The JavaScript event pixel and image event pixel differ as follows:

"The JavaScript event from a particular publisher account should only be deployed on pages where that publisher's Control Tag is present. Javascript pixel use cases include:

    Passing page variables as event attributes. 

    Deploying the pixel in a form, specifically on onSubmit functions, where data is captured on user action after the page has loaded. 

    Collecting additional attributes without writing custom macros


If the page does not have the relevant Control Tag deployed, the image pixel version should be used. Image pixel use cases include:

    Deploying an image pixel on a customer’s web page to retarget that traffic via a campaign.

    Deploying an image pixel on conversion pages that are on another company’s web site that does not have the Krux Control Tag deployed.

    Capturing email newsletter opens and interactions." [Salesforce, 35](https://konsole.zendesk.com/hc/en-us/articles/115010887187-Events-FAQ)

**Data Sentry Iris**  
Video: Data Sentry Iris is the UI for Data Sentry.  It is an always-on monitoring solution for data collection "on your sites or campaign", and aims to help a client monitor and protect against malicious activity, unwanted collection of their sites' data from competitors, data skimming, etc., including to monitor latency.  You can monitor "Requests and Chains" (eg, page views, sorted by company; collector-to-usher ratios; view trends; inspect tags to provide details of data collection to 3rd parties that may be in violation of your data collection terms, ie, ushering in data collectors) [Salesforce, 13](https://konsole.zendesk.com/hc/en-us/articles/115012227268-Data-Sentry-Iris-Video-Tutorial).  A "collector" is "A company whose media or snippet of code sets a cookie"; an "usher" is "A company whose media or snippet of code ushers in additional collectors"; and a "chain" is "A unique usher to collector pair".  For more explanations, see [Salesforce, 14](https://konsole.zendesk.com/hc/en-us/articles/115010652267-Data-Sentry-IRIS-FAQ) and [Salesforce, 15](https://konsole.zendesk.com/hc/en-us/articles/115010652267-Data-Sentry-IRIS-FAQ)

**Hashed Device Management (to get around Safari)**  
Used for Safari because Safari has 3rd party blocking [Salesforce, 16](https://konsole.zendesk.com/hc/en-us/articles/115012183888-Hashed-Device-Management)

"The Salesforce DMP Hashed Device Management solution allows for targeting users on Safari browsers that block 3rd party cookies.  Please open a ticket in the Help Portal if you would like to request Hashed Device Management."  Details here: [Salesforce, 35](https://konsole.zendesk.com/hc/en-us/articles/115011230687-How-to-verify-Hashed-Device-Management)

**Media Tag Generator**  
Impression trackers, click trackers, non-script (image pixel) trackers (where JavaScript is not supported, such as video environments and mobile apps).  Different macros are used to collect different media elements.  [Salesforce, 17](https://konsole.zendesk.com/hc/en-us/articles/115010825168-Media-Tag-Generator-Video-Overview).  See also, [Salesforce, 21](https://konsole.zendesk.com/hc/en-us/articles/225407808-How-to-set-up-the-Salesforce-DMP-ControlTag-Helper)

**Super Tag**  
"What is SuperTag?  

SuperTag is Salesforce DMP’s integrated tag management system, allowing full control over how your tags fire. SuperTag also offers extensive tag firing capabilities, including conditional, throttle, data and frequency-based targeting.  

What are they key use cases for SuperTag?  

* _Optimized Campaign Targeting:_ Limit tag fires to specific audiences and activate that tailored audience in your campaigns
* _Control Event and Tag-based Activities:_ Fire Salesforce DMP event pixels or custom tags to specified URLs, segments, attributes, geo-locations and frequency
* _Define the Timing and Frequency of Tag Fires:_ Specify the order, timing and frequency of tag fires for an improved site experience
* _Partner Tag Management:_ Fire Partner User Match tags, Brand Study pixels, and Programmatic partner pixels via SuperTag. Any tag you need deployed for optimized marketing or superior site experience can be deployed through SuperTag.  
* _Explore A/B Testing:_ Utilize conditional tag firing for test initiatives

What types of tag targeting are available in SuperTag?  

* _Attribute:_ Fire a tag to specific attribute(s)
* _Tag ordering:_ Fire a tag before or after another tag
* _Frequency:_ Specify how many times a tag should fire in 24 hours
* _Segment:_ Fire a tag to a specific segment(s) of users
* _Throttle:_ Fire a tag to a specific percentage of users
* _URL:_ Fire a tag to a specific URL(s)" [Salesforce, 61](https://konsole.zendesk.com/hc/en-us/articles/228024867-SuperTag-FAQ)

**Bulk Segments**  
Only accepts 1st party data -- no 3rd party data for bulk segment uploads.  Segments in video: Age Range / Category / Content Type / Context Terms / Device / Gender / HHI / Kids in Household / Location / Referrer / Reg User ID.

Example: users in the Boston area looking for a 2-3 bedroom home.  First rule might target users searching Boston Real Estate on this publisher's site.  Second rule could target users in the Boston area using the publisher's existing geo-data.  Third rule is number bedrooms user is looking for (2-3 in this example). [Salesforce, 18](https://konsole.zendesk.com/hc/en-us/articles/115008240047-How-to-Create-Bulk-Segments)

**Events Overview**  
Events are user actions, like clicks on buttons or values entered into a form; collecting data where JavaScript cannot be used (emails are partner websites that do not allow a Krux JavaScript to be placed); reports can be generated on event traffic.  Step 1: Event types (eg, "click", "email open", etc) are used to sort even pixels, all have the same features except one feature, the Krux Click Tracker, the only event type that can redirect users to a forwarding URL. Step 2: Reporting and segmentation with even pixels (report shows daily impressions and unique users) [Salesforce, 19](https://konsole.zendesk.com/hc/en-us/articles/115007996507-Events-Overview)

**Platform Segments**  
Use to make segments out of KUIDs, such as users identified by your data science team to have a high propensity to buy your products.  Krux will not know why they have that high propensity, but will put the users in the segment that you (the client) tell them to.

You create a platform segment using an API, and then populate the segment by uploading a list of KUIDs. [Salesforce, 20](https://konsole.zendesk.com/hc/en-us/articles/115005914227-How-to-Create-Platform-Segments-in-Salesforce-DMP)

**Real-time Segments**  
"_What are Real-time segments?_

Real-time segments allow you to immediately add users to a segment once segment rules are met and then target those users on the next page view. For example, you can deliver an ad on the next page view after users perform a search. 

Real-time segments are calculated at the browser level so only on-site targeting is supported. Historical activity data is not used in Real-time segments.

_How do Real-time segments work?_

Real-time segments allow a browser user to qualify for the segment and become immediately targetable; the segment ID is written to the browser's localStorage and available for targeting on the very next pageview. 

Users will remain in the Real-time segment for 72 hours without having to repeat the action that qualified them for the segment. A user must have a KUID already assigned in order for the user to qualify for a segment." [Salesforce, 53](https://konsole.zendesk.com/hc/en-us/articles/115006780068-Real-time-Segment-FAQ)

**Video Suite Inspector**  
VAST Tag (XML-based Ad Response which directs information to your video ad player, and is incompatible with JavaScript, so much implement Krug image pixel instead of JavaScript impression tag).  There is a clicktracker. See [Salesforce, 22](https://konsole.zendesk.com/hc/en-us/articles/218941948-How-to-validate-a-Video-Ad-Unit-on-Video-Suite-Inspector-using-HTTP-Fox)

**User matching**  
_For a great guide on user matching, see:_ [Salesforce, 32](https://konsole.zendesk.com/hc/en-us/articles/214918988-First-Party-Data-Import)

Salesforce and 3rd parties each use their own IDs, and match users by firing the _other_ party's pixel when their own pixel fires on a site.  Match rate is the percentage of users of party A known by party B.  SF DMP match rates exclude Safari and app IDs.  Increased match rates create greater scale, and "Greater audience scale creates more options for managing and optimizing campaign tactics such as segmentation, personalized messaging, frequency, omni channel journey, etc."  Because of 3rd party blocking, **Safari users can typicaly not be matched to partners at all.** 

"By default, we run user match pixels on client’s websites through the Control Tag for all partners a client is working with. We fire it on all pages with a frequency cap of 3 times over a 24-hour period for a given user. This will ensure return users are matched, but will not overwhelm client’s sites with unnecessary tag fires. We set the tag to fire "immediately" to make sure users are matched before leaving the page. 

It will take up to 30 days for the match rate to reach its peak after a new user match pixel has been activated.

Unlike first party data that is exclusively available to the client who owns it, user match tables are shared across all Salesforce DMP clients. This way, each client can benefit from the user match pixels being fired on other client’s websites.

Salesforce has one of the largest footprints in the industry, thus providing exceptionally high match rates. Match rates can vary from country to country though, depending on both Salesforce's and the partner’s footprint in that market.

It is also possible for partners to fire the Salesforce DMP user match pixel across all their inventory to improve the match rate upon request." [Salesforce, 23](https://konsole.zendesk.com/hc/en-us/articles/115006072448-User-Matching-and-Match-Rates-FAQ)

Critically, "The Client User ID will have a one-to-many relationship with the Krux User ID in the User Match table. Note that in general, there may be multiple Krux User IDs mapped to a given Client User ID because the Krux User ID is browser specific whereas the Client User ID will be the same across multiple browsers (assuming that it is indeed a persistent user ID as opposed to a first-party cookie)."

"For example, if there are 3 columns called Age Group, Gender, and Interest in the client’s registration database that need to be imported into Salesforce DMP, then the following represents a valid data file that can be ingested by Salesforce DMP:

User1234^gender:male;age:18-24;interest:fishing
User2345^gender:female
User3456^age:35-44
User4567^gender:male;interest:fishing,boating

When Salesforce DMP processes this file, we will create 3 attributes called Gender, Age, and Interest in the client’s Salesforce DMP account. We will also automatically create the corresponding attribute values: male and female under gender and 18-24, 35-44 under age, and fishing and boating under interest.

Salesforce DMP supports full-refresh." [Salesforce, 32](https://konsole.zendesk.com/hc/en-us/articles/214918988-First-Party-Data-Import)

Evaluating matched users:

"Segment Population is the device population of this segment from the Manage Segments screen. This is a count of all devices that are part of the segment based on the segment's rules.

Matchable population is the Segment Population minus those devices that cannot be matched to a partner. This includes Safari cookies, as per default Safari deleted all cookies after each page impression. A DSP Safari cookie will never show up again and thus can't be served ads to. Many DSPs also don't accept mobile identifiers (IDFA and AdID). So in those cases we also deduct them.

Segment Match Rate is the percentage of users from the matchable population that we have matched the DSPs cookie against within the last 30 days. We only send these users as older users are not accepted by the DSPs.

More info on user matching can be found here:
https://konsole.zendesk.com/hc/en-us/articles/115006072448-User-Matching-and-Match-Rates-FAQ

Cumulative population is the population we expect to see in DSP after all the previous considerations. In reality this can differ due to circumstances outside our control. E.g. Google only counts users that have been active in Google's universe on at least two different days for its population/forecasting. For full refresh connections the cumulative population is the population we send every day." [Salesforce, 48](https://konsole.zendesk.com/hc/en-us/articles/115009920168-Partner-Management-Additional-Account-Details-FAQ)

**Data Transfer 2.0**  
"DT 2.0 files enables supplemental data ingestion for those brands that are buying inventory through GDN [Google Display Network]. In all cases, tagging is the best practice to ensure proper user matching across channels. If your organization has limited to no Ad Ops or Agency support, DT 2.0 file ingestion may be used to feed your campaign and impression data into the platform."  Moreover, "Google Data Transfer is at cost. Please contact your Google Account Manager for pricing specifics", and "DT 2.0 is only available for DCM. DCM – includes: DBM - advertisers buying for marketers not using DCM, Display Campaign Report (includes AdWords (not search), YouTube, GDN/Adsense)" [Salesforce, 31](https://konsole.zendesk.com/hc/en-us/articles/115002783508-Data-Transfer-File-2-0-Import)

"How are users matched between Salesforce DMP and Google?
KUIDs are matched against Google’s user IDs to determine if a user fits the criteria of a segment. This is done via a combination of the Interchange Snippet and Google user match pixel firing on a site(s)." [Salesforce, 36](https://konsole.zendesk.com/hc/en-us/articles/115010886887-DFP-FAQ)

**OTT (Over-the-Top) Collection**  
"Data can be activated in OTT platforms with several execution partners, such as DFP and Freewheel.  

Ad targeting in these app environments will be supported by our S2S integration with DFP audience and other execution partners. This will work for any execution partner where we have in place a S2S integration and the partner accepts IDs for that platform. No user-matching is required, because OTT devices leverage the same persistent device ID.

Can Salesforce DMP collect data from OTT devices?
Yes, if you have an App available on the OTT device, Salesforce DMP can collect data from OTT devices through the following methods:

    API
    1st Party Import from App Logs
    1st Party Import from 3rd Party Source

Each of the methods are described below:

API: The Salesforce DMP SDK applies only to iOS and Android devices. OTT devices, like AppleTV, Roku, X-Box, PlayStation and others, leverage our HTTP API for data collection. We provide a technical spec for the app developers using those platforms and code is written to call Salesforce DMP’s API and User Data Service (like our SDK does). The main difference here is that, in these apps, the code-base/structure is not as pre-defined as it is for iOS and Android SDK’s, so we have to walk dev teams through the process for calling our API with the appropriate inbound/outbound requests. (This is the only approach where the Salesforce DMP code is “live” in the app and interacting with the DMP in real-time.) Today, we are using this approach on the following platforms: AppleTV, Roku & XBox One.

1st Party Import from App Logs: If the logs from these apps contain the required data (unique ID’s for user identification and behavioral/engagement data), we can ingest the raw logs and make it available for segment building. Please note that if the format of the logs differs significantly from our standard 1st Party import format and we’re required to write a lot of code to transform the format, then there may be an implementation fee associated with this method.

1st Party Import from 3rd Party Source: If there is another analytics partner live on the app such as Adobe Analytics, we can import from Adobe with the required user and page attributes. We are then transforming that data to adhere to our 1P import format.

Can Salesforce DMP support both ad-based and subscriber-based OTT models?
Yes, Salesforce DMP can support data collection off either of the above OTT app models. Salesforce DMP has extensive experience with clients opting for a subscriber based OTT model, as well as experience with clients opting for an ad-supported model with OTT inventory." [Salesforce, 49](https://konsole.zendesk.com/hc/en-us/articles/115009293927-Over-the-top-OTT-FAQ)

**Media Tagging**  
"When a Site is created, a unique Configuration ID (ConfID) is generated. This ConfID is included in the Salesforce DMP Control Tag used to collect data from webpages. It is also included in the media tracking tags used to collect data from media campaigns.

It’s through this mechanism that users can filter the Marketing Performance report to a specific marketing channel, such as Paid Search campaigns." [Salesforce, 50](https://konsole.zendesk.com/hc/en-us/articles/115009151507-Media-Tagging-FAQ)

**Code Snippet Versions**  
What is the difference between the code snippet versions when looking at site codes?

    Javascript: for web-based deployments
    Actionscript: for video deployments
    Ajax: used on pages with infinite scroll
    Interchange: snippet of code that allows segments to be targeted onsite" [Salesforce, 51](https://konsole.zendesk.com/hc/en-us/articles/115007393368-Data-Collection-FAQ)

**Ad Server analytics**  
"Salesforce DMP's Yield Analytics reports allow you to understand and analyze audience segment delivery and yield across all ad impressions, irrespective of whether an ad was targeted to an audience segment or not. The "raw" ad impression delivery information is combined with the user audience segment map managed in the Salesforce DMP platform to produce these audience segment delivery and yield reports... The ad impression log file contains a record of every impression delivered, and each impression delivery record must contain the Krux User ID of the user who saw the ad. Note that it is not required for every delivery record to contain the Krux User ID; Salesforce DMP simply ignores the records that don't contain the Krux User ID, but the accuracy of the reports is directly proportional to the number of records that contain the Krux User ID."

For Custom Ads:

The raw delivery log file contains the following columns:

    Timestamp: the time at which the ad was served (Salesforce DMP can accommodate many date/time formats; 2 common formats are: YYYY-MM-DD hh:mm:ss or the Unix timestamp – the number of seconds since January 1, 1970)
    User ID: the Krux User ID of the User who saw the ad
    Campaign ID (or Order ID): the ID of the Campaign that contains the ad
    Ad ID (or Line Item ID): the ID of the Ad that contains the creative for the ad.
    Ad Size: the size of the creative (728x90, 300x250, etc.)
    TargetedKruxSegments: a comma separated list of Salesforce DMP Segment IDs that were used to target this ad impression (this field must be populated if the Ad is targeted to one or more Salesforce DMP segments)


Salesforce DMP recommends that the Client also provide "clicks" and "conversions" (or "actions") log files that contain a record of every click (and respectively, conversion or action) generated by users that see the ads in the ad impression delivery log file. This will help you understand audience segment yield for CPC and CPA as well as CPM campaigns. The format for the "clicks" and "conversions" log files is the same as the "impressions" log file.

The aggregate delivery log file contains the following columns:

    Day: in YYYY-MM-DD format (e.g., 2013-01-05)
    User ID: the ID of the User in the partner's system that saw the ad
    Campaign ID (or Order ID): the ID of the Campaign that contains the ad
    Ad ID (or Line Item ID): the ID of the Ad that contains the creative for the ad.
    Ad Size: the size of the creative (728x90, 300x250, etc.)
    TargetedKruxSegments: a comma separated list of Salesforce DMP Segment IDs that were used to target the ad impressions (this field must be populated if the Ad is targeted to one or more Salesforce DMPsegments)
    Impressions: the total number of impressions aggregated over columns 1-5.
    Clicks: the total number of clicks aggregated over columns 1-5.
    Conversions: the total number of conversions (or actions) aggregated over columns 1-5." [Salesforce, 30](https://konsole.zendesk.com/hc/en-us/articles/218445237-Ad-Server-Integration-for-Yield-Analytics)

**Content Engagement Reports**  
Reports allow site metrics like:

-- pageviews and unique visits for both segments and unique users; 
-- Loyalty report cards (" records the number of return visits per unique over a selected time period"; will "Monitor website engagement over time"; and "Highlights your total users (unique devices) per site, as well as return users to that site and the percentage of your total uniques that those return users represent"); 

-- Social Activity reports ("describes all social sharing you have enabled through direct integration* with Facebook or Twitter"; allows you to "Build social influencer segments. These segments can be used to target users who are likely to share on social media: Capture Facebook Shares, Facebook Likes, Facebook Unlikes and Twitter Tweets"; with features like "Flexible date ranges" and "See the URLs of the top Facebook Likes and Twitter tweets; click-through to the original content". (NOTE: " third-party implementations, such as AddThis or ShareThis are not included.")
-- Search keywords report: "gives a list and population of referral keywords associated with inbound web traffic from top search engines including Google, Bing, and Yahoo" so you can "Build segments around search keywords; Identify valuable words to use for search campaigns to increase traffic to your site. This can help to identify good keywords for paid search campaigns; Capture site search terms and link them to your site as a data source".  This "Lists the source, keyword, and population of referrals over the last thirty days, and is filterable by site and section" and "Site results are processed weekly, and all recorded keywords are available in the Segment Builder [Salesforce, 38](https://konsole.zendesk.com/hc/en-us/articles/115010860288-Content-Engagement-Report-FAQ)

**Frequency Reports**  
"Frequency Reports describe how many times what percentage of your audience has seen your ad. This  allows you to assess how to improve conversion. Very high frequency is typically a sign of waste, and as such, a source of cost-saving. Very low frequency can suggest the audience isn’t seeing the campaign enough to spur conversion, in which case it too is wasteful."  The goal is to have the right amount of exposure for efficient conversions. [Salesforce, 39](https://konsole.zendesk.com/hc/en-us/articles/115010860128-Frequency-Report-FAQ)

**Funnels Report**  
"The Funnels report tracks the sequence of events on customers’ paths to conversion and allows you to optimize accordingly. Use Funnels to understand at what stage in the conversion process users drop off, then target those users to encourage them to finish their purchase, registration, etc.

Benefits:

    Allows you to track individual user actions in a purchase process (or other conversion)
    Monitor conversion success, perform A/B testing, and learn more about converted users with funnel reports based on events and event attributes" [Salesforce, 40](https://konsole.zendesk.com/hc/en-us/articles/115010690407-Funnels-FAQ)

**Lookalike Modeling**  
"Lookalike Modeling applies an algorithm to a base audience segment and finds new people with features and characteristics similar to those in the base audience. Similarity and reach metrics will allow you to find the most useful lookalike with the highest similarity at the reach level required.

Benefits:

    Find prospects for acquisition campaigns
    Expand reach by finding lookalikes among known users"

"Uses 1st and 3rd party data for modelling" [Salesforce, 41](https://konsole.zendesk.com/hc/en-us/articles/115010859928-Lookalike-Modeling-FAQ)

**Site Distribution Report**  
"The Site Distribution report is useful for those with multiple sites. It reveals how a particular segment indexes across all of your sites, and where you would see the highest unique reach if you were to target across all the portfolio." [Salesforce, 42](https://konsole.zendesk.com/hc/en-us/articles/115010859228-Site-Distribution-Report-FAQ)

**Segment Overlap Report**  
"The Segment Overlaps report shows which other segments you have created have the greatest similarity to a given segment.  

Benefits:

    Identify both similar profile or attributes (high overlaps) as well as additional reach opportunities (low overlaps)
    Can expand a segment by adding site visitors who fall into diﬀerent segments but are similar across thousands of attributes" [Salesforce, 43](https://konsole.zendesk.com/hc/en-us/articles/115010859208-Segment-Overlap-Report-FAQ)

**Audience Profile Report**  
"The Audience Profile report shows demographic information about a specific campaign or segment and the segments with the greatest number of unique impressions."

Benefits:

    Learn which demographics your segments or campaigns fall into and export to share with clients or colleagues
    Top overlapping segments will show how similar or unique your segments are

Features:

    The gender, age, and household income profile of your users is determined using information from third-party data providers" [Salesforce, 44](https://konsole.zendesk.com/hc/en-us/articles/115010859168-Audience-Profile-Report-FAQ)

"Does the Loyalty report use devices or people?

Devices; People are only displayed in the Segment dashboard." Safari users are not included because Safari doesn't allow 3rd party cookies. [Salesforce, 52](https://konsole.zendesk.com/hc/en-us/articles/115007354408-Salesforce-DMP-Reporting-FAQ)

**Segment Summary**  
"The Segment Summary provides a view into how a given segment is composed. It shows the number of devices included and two views of people: those we know we can surely identify as tied to a device (determined from your own login information), and those we predict are tied to a device (determined by probabilistic matching from people seen elsewhere in the DMP ecosystem)."

Benefits:

* Grow your population directly from this report using lookalikes, segment overlaps, and the Cross-Device Identity Management capabilities
* Inform your reach forecasting and omnichannel marketing opportunities

Features:

* The People & Devices chart breaks down the number of people and devices in each of three main categories: desktop and mobile web, mobile apps, and Safari
* The Device Population Trend chart shows the number of devices that have moved into and out of the segment during the prior 12 weeks" [Salesforce, 45](https://konsole.zendesk.com/hc/en-us/articles/115010689407-Segment-Summary-FAQ)

Segments are de-duplicated [Salesforce, 47](https://konsole.zendesk.com/hc/en-us/articles/115010365788-Why-are-top-segments-different-in-Audience-Profile-Reports-)

**Index Calculation & Chart Operations**  
The index in DMP Opportunities report provides clients with data about their users in comparison to the DMP universe.  It may be, for example, that you have twice the amount of Ice Cream Lovers than the DMP universe, and your ad sales team could use that as a pitch to potential advertisers looking for Ice Cream fans.

For Chart Operations, see link, though it's not interesting. [Salesforce, 59](https://konsole.zendesk.com/hc/en-us/articles/236268468-Reach-Opportunities-Index-Calculation-Chart-Operations)

**Visual representations**  
Examples: See Klever UI [Salesforce, 60](https://konsole.zendesk.com/hc/en-us/articles/227951188-Klever-UI-People-and-Devices)

## Privacy Policy
**Opting out**   
_DMP Opt-Out_ "DMP Opt-Out
https://apiservices.krxd.net/consumer/optout is the standard DMP opt-out URL. When called directly, this URL will execute the Opt-out action for a user and it will return the following JSON response:

{"code":"success"}

A user must allow cookies from Salesforce DMP in order to opt-out. Calling the DMP opt-out code (by clicking on an opt-out button placed on the client's page) will result in a persistent 'cookie' placed in the user’s web browser by Salesforce, identifying that user as being on the Salesforce DMP 'do not target' list. Taking this opt-out step won't prevent all tracking and targeting online, but it will ensure the user’s wishes are honored by all Salesforce DMP clients.

Note: If the user uses more than one computer, the process must be repeated for each one as this information is associated with a cookie unique to each machine." [Salesforce, 7](https://konsole.zendesk.com/hc/en-us/articles/217039187-Privacy-Policy-and-Opt-Out-Guide)

_DMP Cookie Status:_ "DMP Cookie Status

To determine the tracking state of a user (opted-out vs. opted-in), a publisher should call https://apiservices.krxd.net/consumer/cookie_status. This will return one of the following JSON responses:

{"code": "optedout"}

if the user has opted out of tracking by Salesforce DMP

{"code": "optedin"}

if the user is opted-in to tracking by Salesforce DMP" [Salesforce, 7](https://konsole.zendesk.com/hc/en-us/articles/217039187-Privacy-Policy-and-Opt-Out-Guide)


_On Mobile:_ "Users can reset their IDFA or AdID to receive a new one. This is comparable to deleting cookies.

They can also block these completely by opting-out of Ad Track or Ads Personalization. In that case, Salesforce DMP cannot track or target these users." [Salesforce, 3](https://konsole.zendesk.com/hc/en-us/articles/115000428127-Mobile-IDs-FAQ)

_In Safari FAQ:_ "Is there any difference in the how 1st-party cookies and Hashed Device IDs treat opt-outs?
Yes, if the client is utilizing a first-party cookie and has multiple domains, a dedicated opt-out will need to be configured and maintained for each site. Alternatively, if hashed device management is employed a single opt-out link will be applicable for a given client.

Can users opt-out of Hashed ID tracking?
Absolutely – unlike other providers of so-called Fingerprinting techniques, the Salesforce DMP actually can manage fingerprinting users through an opt-out. 

Does Fingerprinting adhere to PII rules?
Yes, our hashed device management solution is fully compliant with PII protocols.

Do both approaches lose uses when they clear their cookies?
No, first-party cookies can be cleared, while the hashed ID will persist even if cookies are emptied. [Salesforce, 4](https://konsole.zendesk.com/hc/en-us/articles/115000428307-Safari-FAQ)

"Can users opt-out of tracking in Mobile Apps?
Users can reset their IDFA or AdID to receive a new one. This is comparable to deleting cookies.

They can also block these completely by opting-out of Ad Track or Ads Personalization. In that case, Salesforce DMP cannot track or target these users." [Salesforce, 58](https://konsole.zendesk.com/hc/en-us/articles/115000428127-Mobile-IDs-FAQ)

**Amazon role: a cloud service provider?**  
"Salesforce DMP will create a bucket for the client in Krux’s Amazon S3 account and the client can upload the data files to S3 as per a mutually agreed upon schedule...Amazon S3 Bucket Information

Here is a general website regarding connecting to the Amazon S3 bucket via Cyberduck (though, Terminal can also be used): https://trac.cyberduck.io/wiki/help/en/howto/s3#ConnectingtoAmazonS3" [Salesforce, 32](https://konsole.zendesk.com/hc/en-us/articles/214918988-First-Party-Data-Import)  

**Personally Identifiable Information**  
"Personally Identifiable Information (PII) includes any data that could potentially identify a specific individual and can be used for de-anonymizing data. Salesforce does not collect or store PII."

Some examples of PII include: Full name; Email address; Phone numbers; Credit card numbers; Date of birth; Login/screen name; IP address is considered PII in some countries outside of the US; Home address; etc" [Salesforce, 8](https://konsole.zendesk.com/hc/en-us/articles/115007222048-PII)

"Data Privacy and Security Considerations

Salesforce DMP does not accept PII data and it is a breach of the MSA to send to us. Onboarding might be a better option if you have data connected to email addresses and are concerned with offline data import user matching. Usage and set up fees apply." [Salesforce, 32](https://konsole.zendesk.com/hc/en-us/articles/214918988-First-Party-Data-Import)  

**Data Retention**  
"Data Expiry

Salesforce DMP stores any data collected through online mechanisms (including user matching data) for a variable period as defined in the contractual agreement between Salesforce and the client. First-party imports remove any data not included in subsequent imports (full refresh). For best user match results, files should be uploaded frequently, or daily, even if the data output has no change." [Salesforce, 32](https://konsole.zendesk.com/hc/en-us/articles/214918988-First-Party-Data-Import)  

## Relationships
_Data Onboarding:_
comScore / LiveRamp / Neustar [Salesforce, 9](https://konsole.zendesk.com/hc/en-us/articles/115010458727-Data-Onboarding-Partners)

_Data Collection Partners:_

* Off-Site Ad Servers:_ Conversant / DoubleClick Campaign Manager (DCM) / Flashtalking / Innovid / Medialets / Sizmek
* On-Site Ad Servers:_ DoubleClick for Pulishers - DFP (Data Transfer Files)
* Email Service Providers:_ SalesforceExactTarget
* Data Management Platforms:_ Adobe Audience Manager / Oracle BlueKai DMP
* Analytics & Measurement:_ Adobe Analytics (fkaOminture SiteCatalyst) / Brightcove / comScore Validated Campaign Essentials (vCE) / Google Analytics Standard / Kochava / MOAT / Tune [Salesforce, 10](https://konsole.zendesk.com/hc/en-us/articles/227144948-Data-Collection-Partners)

**Data Activation Partners**  

_On-Site Ad Servers:_ Adition / Adswizz / AdTech / DoubleClick for Publishers - DFPAudience / DoubleClick for Publishers - DFP Key/Value Pairs / Freewheel / IPONWeb / LKQD / Nativo / OAS / OpenX / SAS/AIMatch / Smart Ad Server

_On-Site SSP's:_ DoubleClick AdExchange - AdX (via DFP) / Index Exchange (Casale) / OpenX / Pubmatic / Rubicon / Sonobi / Sticky Ads / Tremor

_Off-Site Ad Servers:_ Flashtalking / Flite / Innovid / Sizmek

_Off-Site Data Activation:_ ActiveAgent AG / Adara / AdColony / AdForm / AdRoll / AdSquare / A.ki / Amazon Advertising / AOL ONE / AppNexus / Beeswax / Comscore / Criteo / DataXu / DoubleClick Bid Manager - DBM / Dstillery / Exponential / Facebook Custom Audiences / Google AdWords / Google RLSA / IgnitionOne / Infectious Media / InMobi / Instagram (via Facebook Custom Audiences) / Jivox / Lotame / Maxpoint / MediaMath / [m]Platform | GroupM / Netmining / Next Performance / OwnerIQ / Platform161 / Quantcast / RadiumOne / RocketFuel / Run / Simpli.fi / Specific Media (Viant) / SpotXchange / Teads / The Trade Desk / TimeOne / Tradelab / Termore Video / TubeMogul / Turn / Twitter - Tailored Audience / Undertone / VideoAmp / Videology / Yahoo! DataX (replaced RMX pipeline) / Yieldlab / Zebestof

_Experience Management Systems & A/B Testing Platforms:_ AB Tasty / Acquia / Adobe Target / Maxymiser / Optimizely / Oracle Real-Time Decisions / Teradata Real - Time Interactions Manager / VWO

_Assorted Data Outputs:_ Adobe Audience Manager / Moat / Oracle BlueKai DMP / Survata / YieldEx [Salesforce, 11](https://konsole.zendesk.com/hc/en-us/articles/226620988-Data-Activation-Partners)

_Third-Party Data Marketplace:_ Acxiom / AffinityAnswers / ALC / Alliant / AnalyticsIQ / ASL / Audience Partners / AuDIGENT / B2B Targets / Bombora / Cardlytics / comScore / Connexity / Crossix / Cuebiq, Inc / Dataium / Dataline / Datamyx / DataLogix / Datonics / Digital Elements / Dun & Bradstreet / Epsilon / Ethnic Technologies / eXelate / Experian / Eyeota / Factual / Forbes / i360 / InfoGroup / IRI Worldwide / IXI Services/Equifax / Kantar Shopcom / L2 / LiveRamp Data Store / Mastercard Advisors / Maxpoint / MeritDirect / Mobiquity / GfK MRI / Gravy Analytics / #HOME by Vendigi / Navegg / NetWise Data / Neustar AdAdvisor / Nielsen / Nielsen Catalina Solutions (NCS) / NinthDecimal / PlaceIQ / PushSpring / Quantcast / SambaTV / ShareThis / Skydeo - Mobile AppAudiences / Skyhook / Specialists Marketing Services / Stirista / Tivo / TruSignal / Twine / Vertical Mass / Visual DNA / V12 / Webbula / Windfall [Salesforce, 12](https://konsole.zendesk.com/hc/en-us/articles/217592967-Third-Party-Data-Marketplace)

## Details

_Origins:_ Krux began as "a platform for brands to collect all data from digital interactions across devices and use it to better understand their customers" for better marketing.  However, they "knew that first-party data (customers’ email addresses and purchase histories) was where the puck was headed, so we doubled down on it."  They are driven by the concept "people data" because people, not browsers and mobile devices, are what buy things. [Salesforce, 1](https://www.salesforce.com/blog/2017/05/krux-is-now-salesforce-dmp.html)

_Philosophy and approach:_ "...when I am asked, what is the future of DMPs, I say that DMPs will become completely integrated into larger technology stacks offering a layer of data management (for both known and unknown data) for the “right person.” This orchestration layer consists of connected execution systems that seek to answer the “right message, right time” quandary. It also includes an artificial intelligence (AI) layer, which is the “brains” of the operation trying determine how to stitch billions of individual data points together in real time."  "...marketing is much more than ad campaigns. It is every experience a customer has with the brand, and we empower marketers to use data to impact every touchpoint along that journey, all powered by AI." [Salesforce, 1](https://www.salesforce.com/blog/2017/05/krux-is-now-salesforce-dmp.html)

"Some of the core reasons to use a DMP are to manage Identity and centralize user-level data for advertising and content personalization. Additionally, the DMP includes insights that help inform targeting and personalization use cases as well as campaign and personalization optimization." [Salesforce, 24](https://konsole.zendesk.com/hc/en-us/articles/115012398067-What-if-I-just-want-to-import-data-instead-of-using-the-Control-Tag-SDK-or-other-DMP-tracking-)

_Scope:_ "Every month, Salesforce DMP interacts with more than 3 billion browsers and devices, supports more than 200 billion data collection events, processes more than 5 billion CRM records, and orchestrates more than 200 billion personalized consumer experiences." [Salesforce, 1](https://www.salesforce.com/blog/2017/05/krux-is-now-salesforce-dmp.html)

"The Salesforce Data Management Platform (DMP) allows publishers and marketers to collect and organize all of their consumer web data in one central "big-data" warehouse. Using Salesforce DMP, organizations can consolidate and reconcile their first-party "web-behavior" data that is generated by consumers as they engage with media and/or content with data from various third-party data providers like eXelate, DataLogix, Targus etc. Organizations can also integrate data from their user registration and subscription databases (hereon referred to as “first-party data”) into Salesforce DMP and join that data with web behavior and third-party data. 

User data stored in Salesforce DMP is keyed off a global Krux User ID. The Krux User ID is a third-party cookie and as such is specific to a browser (and corresponding device too). All data that is collected by Salesforce DMP from online environments is automatically keyed off the Krux User ID.

Salesforce DMP supports the ingestion of first-party data available in client systems like registration or subscription databases and other CRM systems. This data is keyed off the client’s first-party User ID. A User Matching process that maps the client first-party User ID to the corresponding Krux User ID for every applicable user facilitates the onboarding and ingestion of this data. 

After the user matching process has been setup clients can send first-party data corresponding to the matched users. Salesforce DMP has a strict data format for the first-party data outlined below." [Salesforce, 32](https://konsole.zendesk.com/hc/en-us/articles/214918988-First-Party-Data-Import)

_Billing Clients:_ Clients are charged for impressions, and a maximum amount for a single impression is calculate: [Salesforce, 34](https://konsole.zendesk.com/hc/en-us/articles/115011719688-How-Data-Costs-are-Billed)





## BIBLIOGRAPHY
_Crunchbase, 01_ [https://www.crunchbase.com/organization/krux-digital](https://www.crunchbase.com/organization/krux-digital)


[Salesforce, 1](https://www.salesforce.com/blog/2017/05/krux-is-now-salesforce-dmp.html)
[Salesforce, 2](https://konsole.zendesk.com/hc/en-us/articles/115000451248-Salesforce-DMP-SDK-FAQ)
[Salesforce, 3](https://konsole.zendesk.com/hc/en-us/articles/115000428127-Mobile-IDs-FAQ)
[Salesforce, 4](https://konsole.zendesk.com/hc/en-us/articles/115000428307-Safari-FAQ)
[Salesforce, 5](https://secure.sfdcstatic.com/assets/pdf/misc/BCRPublicFAQ.pdf)
[Salesforce, 6](https://www.salesforce.com/company/privacy/full_privacy.jsp)
[Salesforce, 7](https://konsole.zendesk.com/hc/en-us/articles/217039187-Privacy-Policy-and-Opt-Out-Guide)
[Salesforce, 8](https://konsole.zendesk.com/hc/en-us/articles/115007222048-PII)
[Salesforce, 9](https://konsole.zendesk.com/hc/en-us/articles/115010458727-Data-Onboarding-Partners)
[Salesforce, 10](https://konsole.zendesk.com/hc/en-us/articles/227144948-Data-Collection-Partners)
[Salesforce, 11](https://konsole.zendesk.com/hc/en-us/articles/226620988-Data-Activation-Partners)
[Salesforce, 12](https://konsole.zendesk.com/hc/en-us/articles/217592967-Third-Party-Data-Marketplace)
[Salesforce, 13](https://konsole.zendesk.com/hc/en-us/articles/115012227268-Data-Sentry-Iris-Video-Tutorial)
[Salesforce, 14](https://konsole.zendesk.com/hc/en-us/articles/115010652267-Data-Sentry-IRIS-FAQ)
[Salesforce, 15](https://konsole.zendesk.com/hc/en-us/articles/115010652267-Data-Sentry-IRIS-FAQ)
[Salesforce, 16](https://konsole.zendesk.com/hc/en-us/articles/115012183888-Hashed-Device-Management)
[Salesforce, 17](https://konsole.zendesk.com/hc/en-us/articles/115010825168-Media-Tag-Generator-Video-Overview)
[Salesforce, 18](https://konsole.zendesk.com/hc/en-us/articles/115008240047-How-to-Create-Bulk-Segments)
[Salesforce, 19](https://konsole.zendesk.com/hc/en-us/articles/115007996507-Events-Overview)
[Salesforce, 20](https://konsole.zendesk.com/hc/en-us/articles/115005914227-How-to-Create-Platform-Segments-in-Salesforce-DMP)
[Salesforce, 21](https://konsole.zendesk.com/hc/en-us/articles/225407808-How-to-set-up-the-Salesforce-DMP-ControlTag-Helper)
[Salesforce, 22](https://konsole.zendesk.com/hc/en-us/articles/218941948-How-to-validate-a-Video-Ad-Unit-on-Video-Suite-Inspector-using-HTTP-Fox)
[Salesforce, 23](https://konsole.zendesk.com/hc/en-us/articles/115006072448-User-Matching-and-Match-Rates-FAQ)
[Salesforce, 24](https://konsole.zendesk.com/hc/en-us/articles/115012398067-What-if-I-just-want-to-import-data-instead-of-using-the-Control-Tag-SDK-or-other-DMP-tracking-)
[Salesforce, 25](https://konsole.zendesk.com/hc/en-us/articles/115012555408-What-does-the-Control-Tag-do-)
[Salesforce, 26](https://konsole.zendesk.com/hc/en-us/articles/115012367627-Will-the-DMP-Control-Tag-Impact-Page-Load-Performance-)
[Salesforce, 27](https://konsole.zendesk.com/hc/en-us/articles/115009397188-Cross-Device-Identity-Management-CDIM-FAQ-)
[Salesforce, 28](https://konsole.zendesk.com/hc/en-us/articles/226951307-How-to-Build-Segments-with-CDIM)
[Salesforce, 29](https://konsole.zendesk.com/hc/en-us/articles/226951307-How-to-Build-Segments-with-CDIM)
[Salesforce, 30](https://konsole.zendesk.com/hc/en-us/articles/218445237-Ad-Server-Integration-for-Yield-Analytics)
[Salesforce, 31](https://konsole.zendesk.com/hc/en-us/articles/115002783508-Data-Transfer-File-2-0-Import)
[Salesforce, 32](https://konsole.zendesk.com/hc/en-us/articles/214918988-First-Party-Data-Import)
[Salesforce, 33](https://konsole.zendesk.com/hc/en-us/articles/115012221127-Browser-Support)
[Salesforce, 34](https://konsole.zendesk.com/hc/en-us/articles/115011719688-How-Data-Costs-are-Billed)
[Salesforce, 35](https://konsole.zendesk.com/hc/en-us/articles/115011230687-How-to-verify-Hashed-Device-Management)
[Salesforce, 36](https://konsole.zendesk.com/hc/en-us/articles/115010886887-DFP-FAQ)
[Salesforce, 37](https://konsole.zendesk.com/hc/en-us/articles/115010886887-DFP-FAQ)
[Salesforce, 38](https://konsole.zendesk.com/hc/en-us/articles/115010860288-Content-Engagement-Report-FAQ)
[Salesforce, 39](https://konsole.zendesk.com/hc/en-us/articles/115010860128-Frequency-Report-FAQ)
[Salesforce, 40](https://konsole.zendesk.com/hc/en-us/articles/115010690407-Funnels-FAQ)
[Salesforce, 41](https://konsole.zendesk.com/hc/en-us/articles/115010859928-Lookalike-Modeling-FAQ)
[Salesforce, 42](https://konsole.zendesk.com/hc/en-us/articles/115010859228-Site-Distribution-Report-FAQ)
[Salesforce, 43](https://konsole.zendesk.com/hc/en-us/articles/115010859208-Segment-Overlap-Report-FAQ)
[Salesforce, 44](https://konsole.zendesk.com/hc/en-us/articles/115010859168-Audience-Profile-Report-FAQ)
[Salesforce, 45](https://konsole.zendesk.com/hc/en-us/articles/115010689407-Segment-Summary-FAQ)
[Salesforce, 46](https://konsole.zendesk.com/hc/en-us/articles/115010518787--Data-Studio-FAQ)
[Salesforce, 47](https://konsole.zendesk.com/hc/en-us/articles/115010365788-Why-are-top-segments-different-in-Audience-Profile-Reports-)
[Salesforce, 48](https://konsole.zendesk.com/hc/en-us/articles/115009920168-Partner-Management-Additional-Account-Details-FAQ)
[Salesforce, 49](https://konsole.zendesk.com/hc/en-us/articles/115009293927-Over-the-top-OTT-FAQ)
[Salesforce, 50](https://konsole.zendesk.com/hc/en-us/articles/115009151507-Media-Tagging-FAQ)
[Salesforce, 51](https://konsole.zendesk.com/hc/en-us/articles/115007393368-Data-Collection-FAQ)
[Salesforce, 52](https://konsole.zendesk.com/hc/en-us/articles/115007354408-Salesforce-DMP-Reporting-FAQ)
[Salesforce, 53](https://konsole.zendesk.com/hc/en-us/articles/115006780068-Real-time-Segment-FAQ)
[Salesforce, 54](https://konsole.zendesk.com/hc/en-us/articles/115006652948-Segment-Processing-FAQ)
[Salesforce, 55](https://konsole.zendesk.com/hc/en-us/articles/115002018607-UTM-Parameters-FAQ) <-- in FP glossary only
[Salesforce, 56](https://konsole.zendesk.com/hc/en-us/articles/115000428507-AMP-FAQ)
[Salesforce, 57](https://konsole.zendesk.com/hc/en-us/articles/115000428427-Data-Layer-FAQ)
[Salesforce, 58](https://konsole.zendesk.com/hc/en-us/articles/115000428127-Mobile-IDs-FAQ)
[Salesforce, 59](https://konsole.zendesk.com/hc/en-us/articles/236268468-Reach-Opportunities-Index-Calculation-Chart-Operations)
[Salesforce, 60](https://konsole.zendesk.com/hc/en-us/articles/227951188-Klever-UI-People-and-Devices)
[Salesforce, 61](https://konsole.zendesk.com/hc/en-us/articles/228024867-SuperTag-FAQ)
