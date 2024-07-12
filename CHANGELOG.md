# Changelog

- [Changelog](#changelog)
  - [2024.06.14: ZCA UI fixes](#20240614-zca-ui-fixes)
  - [2024.06.12: ZSDMS Synchronization Fix \& ZCA UI improvements](#20240612-zsdms-synchronization-fix--zca-ui-improvements)
  - [2024.06.8: Better Ceph logging and authorization on UI functions](#2024068-better-ceph-logging-and-authorization-on-ui-functions)
  - [2024.06.4](#2024064)
  - [2024.06.3](#2024063)
  - [2024.06.2](#2024062)
  - [2024-05-28.5](#2024-05-285)

## 2024.07.12: Caching bug in ZT - IOT relationship solved

Release date: *26-06-2024*

| Component | Release item                | Implication for consumers (English)                                            | Functional implication (Dutch)                                                                                  |
| --------- | --------------------------- | ------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------- |
| ZTC       | When an IOT was added to a published ZT (a so called 'correction') the cache was not updated leading to an error when a doucment with the IOT was related to a case with the ZT | Probleem opgelost bij het terugschrijven van het bewijsrapport van Validsign |

## 2024.06.14: ZCA UI fixes

Release date: *26-06-2024*

| Component | Release item                | Implication for consumers (English)                                            | Functional implication (Dutch)                                                                                  |
| --------- | --------------------------- | ------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------- |
| ZCA       | Authorize Applications page | Fixed authorization create form which was broken after the 2024.06.12 release. | Probleem opgelost met het maken van een autorisatieformulier dat niet meer werkte na de release van 2024.06.12. |
| ZCA       | Secrets page                | Minor UI/UX improvements with bug fixes.                                       | Geen                                                                                                            |

## 2024.06.12: ZSDMS Synchronization Fix & ZCA UI improvements

Release date: *25-06-2024*

| Component | Release item           | Implication for consumers (English)                                                                    | Functional implication (Dutch)                                                                                                               |
| --------- | ---------------------- | ------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| CSV       | Authorization          | Resolved synchronization issues in ZSDMS by fixing the authorization between internal Roxit services.  | In 2024.06.8 release is in ZSDMS een fout ontstaan en veroorzaakte dat GetDocumentMetaDataAsync niet meer functioneerde. Dit is nu opgelost. |
| ZCA       | Secret View/Edit panel | Introduced new panel design for secret: added authorizations form, redesigned actions buttons.         | Geen                                                                                                                                         |
| ZCA       | Secret List panel      | Added more columns to the table: authorizations column & information about last modifications columns. | Geen                                                                                                                                         |

## 2024.06.8: Better Ceph logging and authorization on UI functions

Release date: *18-06-2024*

 | Component | Release item  | Implication for consumers (English)                                                                                             | Functional implication (Dutch)                                                                                                                                     |
 | --------- | ------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
 | DRC       | Ceph library  | The library for accessing Ceph, used for document storage, is updated to the newest version. This should improve error logging. | Geen                                                                                                                                                               |
 | ZCA       | Authorization | The authorization in ZCA now is entirely based on the activated modules in RAB and user permissions from RAB.                   | Het ZSDMS-menu is nu alleen benaderbaar voor gebuikers met de permissie functioneel beheer en alleen zichtbaar als uw organisatie de ZSDMS-module heeft afgenomen. |
 | ZCA       | Home page     | There is a home page in ZCA in which the permissions and available modules in Fundament are displayed.                          | Er is nu een landingspagina waarin de gebruiker permissies en modules van Fundament ziet.                                                                          |

## 2024.06.4

Release date: *14-06-2024*

 | Component | Release item             | Implication for consumers (English)                     | Functional implication (Dutch)                                             |
 | --------- | ------------------------ | ------------------------------------------------------- | -------------------------------------------------------------------------- |
 | All ZGW   | Redis cache optimization | ZTC should not throw an error when importing case types | Bij het importeren van zaaktypes trad vaak een fout op. Dit is nu opgelost |

## 2024.06.3

 Release date: *12-06-2024*

| Component | Release item                   | Implication for consumers (English)                                                                                                                                                | Functional implication (Dutch)                                                |
| --------- | ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| DRC       | Business rule DRC-005 disabled | Status of document can be altered even if ontvangstdatum is filled (Api version 1.5 only, not previous versions)                                                                   | Status van het document kan veranderd worden ook al is ontvangstdatum gevuld. |
| CSV       | Endpoint for ClientID's        | Api method for retrieving Api endpoints and credentials now supports filtering on application (rx.mission etc) and always returns information, be it for Fundament or external ZGW | Geen                                                                          |

## 2024.06.2

 Release date: *04-06-2024*

| Component               | Release item     | Implication for consumers (English) | Functional implication (Dutch)                                                      |
| ----------------------- | ---------------- | ----------------------------------- | ----------------------------------------------------------------------------------- |
| All ZGW (change in ZCA) | Bug fix ZSDMS UI | No impact                           | Medewerkers van Roxit konden  geen data meer zien in ZCA -> ZSDMS. Dit is opgelost. |

## 2024-05-28.5

 Release date: *30-05-2024*

| Component               | Release item                                   | Implication for consumers (English)                                                                                                                                                                                                                                                                                                                                                                                           | Functional implication (Dutch) |
| ----------------------- | ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------ |
| All ZGW (change in CSV) | Authentication in ZCA/CSV New secrets endpoint | Authentication has been adjusted in preparation of making ZCA functions available for customers; There is a new endpoint on CSV for retrieving urls/secrets of external ZGW. In the case these are configured, it returns an array of components (DRC, ZRC etc) with ClientId, secret, and endpoint. In case Fundament is used, the same array is returned but without endpoints. The endpoint is a service to other modules. | Geen                           |
