# Goal

* develop W3C standard proposal for EPA.
* create reference implementation
* create polyfills for legacy browsers
* promote into CMS and browser

# EPA goal

Standardize Web 3.0 concepts: embedding 3rd party web applications into web page. Serve the
1. Embedding into page convention via WebComponent interface
2. Content insulation including JS scope( document, window, local storage, cookies,etc), CSS scope
3. CMS component concept
   1. embedding and identifying the component on page via API and URL
   2. preserving the state
   3. configuration for app, page, instance.
   4. API for preserving state and config
   5. implementation of API above on client side, server-side reference implementation
   6. API for ACL, reference implementation for client side

# The need

Web 3.0 made the 3rd party apps dominant over embedded into back-end apps for portals and CMS. 
Due to independent life cycle the 3rd party apps (comparing to embedded components) able to bring more 
business value as user base, revenue sources, extended marketing tools, etc. That made CMS less 
attractive as 3rd party apps embedding became more significant factor than CMS advantages. 
As from business as from development effort side.

CMS have tried to cover the need by utilizing 3rd party via web services or code sniplets. 
Unfortunately it still requires individual per-app effort of coding and maintenance on host site.
Creation of unified EPA standards for embedding and interaction with host page will significantly 
ease or completely eliminate the need for per-app tuning.

The EPA also will unify the many aspects of CMS components like vendor and service resolving, configuration 
and state on host and per-instance level, administration, ACL, etc. Those have been a native part of CMS but 
not formalized for Web 3.0 apps.

# Glossary

**Web 3.0** concept assumes the web page content served by multiple vendors from different hosts simultaneously.

**EPA** - Embeddable Progressive Web Application, a WebComponent acting as IFRAME with interaction with host 
page layer. The "web" is skipped in acronim as same convention is applicable to device native apps.
