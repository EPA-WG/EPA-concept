# EPA-concept
Embeddable Progressive Application Working Group for WebComponent for embedding 3rd party web and native apps into HTML page.

What would be the proper framework for modern Web 3.0 app? The Embeddable Progressive Web Application(EPA) seems to be the answer.

Recently I have faced a new challenge of integration many 3rd party sites into OSS collaboration site. The trouble came from so many APIs and UI customization. It is just too much work, making the development time unrealistic.

More than decade ago Java Portal have solved similar problem by unifying as UI as other tiers of sub-application integration by Portlet framework. Today the same host apps integration is not sufficient anymore. Apps are served by multiple businesses from their own sites with own release schedules, etc. Usually a way better than any integrated portlet as the businesses of 3rd party apps are competing elevating the best, unlike monopoly of single governed integrated portlet. 

3rd party apps are implemented in different frameworks in most cases not compatible when served alongside with other apps on same page. Which does not fit into concept of Portlet anymore.

# Embeddable Progressive Web Application concept.
As implementation of [microapplication](./microapplication.md) concept,
EPA is a WebComponent for embedding 3rd party site content, insulation of context (js, css, dom), and API for interaction with container (page or another EPA). From insulation point of view, it is like IFRAME except it is included into container dom. From integration side, the EPA or derived component can act as within embedded app content as with own content as WebComponent.

# Client side CMS convention
Unlike Progressive Web Application its Embeddable version is not a singleton on desktop. Rather multiple instances are embedded into container (web page).
The set of portlet APIs for interaction with container has a sense in relations between container and EPA WebComponent including
* the configuration per app, page within hierarchy of container(s), and instance inside of container
* (de-) serialization of state
* Access control TBD
* Interaction with container, messaging/push notification TBD

Also, specific to web page API
* Multimedia: Camera, sound/video playback
* Geolocation, etc.

# How it could be done
While the W3C standard of this kind is not even on horizon, it is possible to create a proof of concept based on WebComponent

**CSS and DOM insulation** could be done by WebComponent.  But the page objects (like window, document, location, etc.) need to be simulated for JS from embedded page.

**JS scope, global objects** insulation could be done by the loading of SCRIPT tags could be done within closure with redefined globals.

The trouble comes with script loading via ES6 imports. Way around would be in downgrade all scripts to ES5 level by transpiler will work in via trappable SCRIPT tag injection.

Simulated _window_ and _document_ could be bound to ShadowRoot of EPA.

**Browser APIs** like location, cookies or local storage should be wrapped with scoping matching to settings and state.
 
**CMS features** to be defined based on modern CMS patterns.

# Help Needed
Join the effort for <[embed-page](/EPA-WG/embed-page)> WebComponent as POC for Embeddable Progressive Web Application and [EPA working group](./working-group.md) for W3C proposal.

The _OSS foundation_ to support the initiative TBD. 

## Ideas appreciated. 
Please create a ticket to start a thread.

# Links
* [Working Group](./working-group.md)
* [Contribution guidelines](./CONTRIBUTING.md)
* <[embed-page](https://github.com/EPA-WG/embed-page)> proof of concept as WebComponent

