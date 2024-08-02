# Authorisations

## How it works
The ZGW standard has a function to create an <em>application</em> with multiple Client ID's. 
The application has associated authorisations. 
When a client application calls a ZGW Api, it's bearer token is checked and the ClientID is extracted. If the token and ClientID are valid, the ZGW component looks up the associated authorisations in the AC   

## How to create applications/authorisations
Authorisations vcan be added using the configuration tool of Fundament. 
We advice to use only one ClientID per Application so that you can adjust authorisations per application if needed.
We also advice to restrict authorisations as much as possible to prevent unwanted effects. For example, if an aplication has permission for deletion of cases, it can delete all cases in your Fundament.

## Limitations of the Fundament configuration tool
Our tool only supports only one ClientID per application (whereas the api's allow multiple ClientID's) so that configuraton is as easy and clear as possible.  
Also it does not provide the possibility (supported by the Api's) to add an authorisation per casetype. The reason is that this feature has shown many problems in previous versions of our tooling: applications could not access cases with newer (versions of) casetypes than configured, but also not of older versions.
