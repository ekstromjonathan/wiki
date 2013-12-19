Getting started
=
Data flow, template design and other preparations

This document presents the different steps of integration needed to have an app ready for the market using Ivy. Please note that this document will be continuously updated, and is meant as a guideline only. Changes may occur. 

Last revision: <>
=
<b>Milestones for delivery:</b>
Agens hands over generic unbranded default demo version of Ivy Engine, running on Agens’ demo environment
Client decides on strategy: Pricing, publications etc.
Client ensures publication process will be in place and starts training necessary key personnel for content production
Client starts design on article templates and other HTML pages (based on default templates provided by Agens)
Client sends configuration choices and build requisites to Agens
Client decides how and where Ivy Server should be hosted
Client confirms setup works with Aptoma, and ensures correct data (demo articles) are supplied for Ivy Engine
- If iOS apps use in-app purchase, client sets up products in iTunes
Agens sets up Ivy Server in the agreed environment
- If client chooses to use Ivy Admin for issue creation, Agens sets it up in the agreed environment
- If client chooses to use Ivy Server API for issue creation, Agens provides access to API and how-to documentation. Client implements, tests and verifies that it is set up
If there are new custom plugin modules, client tests and verifies these together with Agens (as specified in contract)
Agens hands over early (non-branded or branded) pre-release version of app
Client confirms article templates and HTML pages are production ready 
Agens hands over release candidate
Client accepts release candidate
Client submits app
As Ivy Engine is updated, client submits new and updated app versions

1. The basics
This is an overview of what we’ll need from you:

Build requisites
Name of application (e.g. “Ivy”)
Slug / id of application (e.g. “ivyEngine”)
Logo in vector or high resolution format with alpha channel
Information about publications upon first release - name, short description, frequency of publication
Credentials to your iTunes Connect & Google Play accounts, or agreement on a proper way to submit apps

Configuration choices:
Will you be using the Ivy Server API to create/update issues (requires implementation on your side), or Ivy Admin?
Are you going to use iTunes in-app-purchase to sell subscriptions? 
What  interaction method do you want to use? Specify for each publication. (VG+ <rename> method, traditional method) 
What navigation model do you wish to use for iPhone and iPad?
Which items that should reside in the main menu? Make sure to specify any necessary URLs.
Will you require any plugins to Ivy Engine? Specify which, and give configuration information where needed.


2. Designing templates for LayoutPreview
Since this is regarded as a rather time consuming process, it’s a good idea to start designing templates as early as possible. Be sure to allocate the necessary resources from your company. Please consult us if you might have questions about this process. Note that we don’t support iframes to be used directly in our articles. 

Tablet landscape
name: tablet_landscape
width: 1024
height: 768
scrolling: paged
Mobile portrait
Used by android and iOS handhelds to render a single article
name: mobile_portrait
width: 320 (should be scalable)
height: any/auto
scrolling: vertical free scroll
Issue cover
Used by the app to represent a single issue
name: issue_cover_landscape
width 1024
height: 768
scrolling: none (1 page only)
Section cover (only needed for VG+ <rename> TOC)
name: section_cover
width 1024
height: 488 
scrolling: none (1 page only)
Please note that 12 px in the bottom of the section cover are not usually visible - they only show when a user drags an article page downward and outside the canvas for a resize effect.)


3. Exporting articles to DrMobile
Every article exported to DrMobile as described in their wiki will be available in our system. 

Sharing
Export the field meta.shareUrl with the absolute url which can be used to view the article on the web.
Format: full url string
Level of access
Export the field meta.access on each article to set access restriction. 
Format: TBA


4. Styling and branding
As a customer you are able to brand every article with your logo. This is done in LayoutPreview. In addition the app’s icon, the splash screen and the menu will by default use your logo. We will need your logo in vector and/or high resolution with alpha channel. Our team will take care of fitting it to different devices.


5. Crafting issues
In order to read the articles on the mobile device each article must, after being created in LayoutPreview, be placed into issues. Creating and maintaining issues can be done in two ways. Either through our API or through our UI.

API
See http://api.ivyengine.com/doc/ (note: choose directory /v1)
UI
This is currently under development. If this is something you would like to use please tell us.


6. Recommended HTML pages
The end user will need to access to different kinds of information whether he/she has questions, feedback or is interested in getting a quick guide for the app. We will provide example HTML for the following pages for you to use as a starting point. In order to implement these pages, we will need an URL in order for the app to access them.
FAQ
An example for this html page is currently under development.
Feedback form
The end user will need to give feedback of various kind. It could be editorial feedback, bug reports, questions or complaints. An example for this html page is currently under development.
Guide
An example for this html page is currently under development.
Paywall
This is what the user should see when he/she tries to open content which he/she is not authorized to view/browse. An example for this html page is currently under development.


7. Additional features for articles
For an up-to-date overview over what is currently supported, please see this document.
Native video player
See BridgeAPI or URLAPI
Linking to web content
See BridgeAPI or URLAPI


8. Preparing for future features
For an up-to-date overview over what is currently supported, please see this document.
Linking to article in a specific issue
See URLAPI
Linking to standalone article
See URLAPI
Zip-support
Everything is taken care of automatically.


9. Statistics and tracking
TBA. Please watch this space.


10. Ads
During the first phase, the Ivy platform will display ads contained within the articles in HTML/CSS/Javascript format. The ads in question will be inserted as figures within Dr. Mobile. Please consult Aptoma for more information about this.
