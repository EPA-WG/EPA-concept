# Microapplication as extension of microservice concept

In Web 3.0 world the application comprize multiple services originated from different vendors. 
It is needed as for application vendor to help monetizing the application 
as for customers to consume various helpful or simply fun features like sharing, keeping notes, and zillion others.

The 3rd party (for application) feature vendors are giving an API to retrieve and post back the data. 
Some, in addition, provide the UI to be embedded into host application UI. 
This 3rd party UI presenting a **microapplication** which unlike full application meant **to be used in context of host application,
configured, and customized by host application** (web page or native app UI). 

## Pagelet
`Pagelet` is a 1-page HTML micro front-end application capable of running as standalone web page or as embedded 
( on front-end or back-end ) into another page. 

Unlike `microapplication` the `pagelet` does not interact with external world say for keeping the data state. Container could provide the 
persistence layer enabling the use of pagelet as `microapplication` in context of container.
