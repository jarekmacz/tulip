---
post_title: 'GTM tips'
layout: Default
published: false
---
#GTM Set up Tips

## #1 Structure your account
The general rule would be to create one GTM account per company and one GTM container per website. 

- The different countries can be under the same container. For example, mywebsite.de and mywebsite.fr tracking can be set up under the same container
-	Container can easily be copied to make your work easier

## #2 Use naming convention
Name your tags, variables and trigger in a meaningful way to make management of your GTM workspace easier.

We recommend using in the naming:


- Destination e.g “GA” for Google Analytics
- Track type e.g “pageview“, “event”, “CT” (conversion tracking)
- Trigger e.g “conversion”, “newletter signup”
 
One tag could look like: “AdWords – CT – newsletter signup”

## #3 Use generic event Listener
To make your GTM container lighter we recommend to use a generic event listener. All the events in the dataLayer should be named the same e.g ‘gtmEvent’. Then in GTM only one event tag needs to be set up with a trigger based on all the ‘gtmEvent’. Category, action, label and value of the events can be set up with variables.

![](pics\gtm-set-up-tips-1.png) 

with the following trigger:
![](pics\gtm-set-up-tips-2.png) 
 
## #4 Send Enhanced Ecommerce with one event
To make set up of Enhanced Ecommerce less extensive, send the Enhanced Ecommerce with a standard event and enable Enhanced Ecommerce feature from that tag. Then set up a trigger that includes all Enhanced Ecommerce events.

Don’t forget to give a name to your Enhanced Ecommerce events in the dataLayer to be able to identify them in GTM.
For example event:’eeProductImpression’

![](pics\gtm-set-up-tips-3.png) 
 
## #5 use lookup Table
Use lookup tables to limit the number of tags. For example, a lookup table can be used to send different countries environment to different Google Analytics properties.

## #6 create constant variable for you GA property
It is more convenient to have one variable storing the Property ID so that you can manage it in one place and avoid updating several tags and variables in case of change in your Google Analytics structure.

## #7 use environments and send the traffic to different views
We strongly recommend to set up different environments for staging and production. This will make it possible to send the staging environment traffic (testing) to another Google Analytics property really easily. This will make it possible to publish your container first on staging, to debug it and then to deploy on production.

## #8 use debug console before publishing anything
Always test your change with the preview mode to be sure that the tags fire properly and the dataLayer is properly populated.

## #9 write description for each new version release
Each time you do a new release of your container, make sure to add a description so that you can easily go back to a certain version if needed

