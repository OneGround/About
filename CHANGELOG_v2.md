# Changelog

- [Changelog](#changelog)
  - [2024.06.4](#2024064)
  - [2024.06.3](#2024063)
  - [2024.06.2](#2024062)
  - [2024-05-28.5](#2024-05-285)

## 2024.06.4

Release date: *14-06-2024*

 | Component | Release item             | Implication for consumers of the Api's (english)        | Functional implication (dutch) |
 | --------- | ------------------------ | ------------------------------------------------------- | ------------------------------ |
 | All ZGW   | Redis cache optimization | ZTC should not throw an error when importing case types | Geen                           |

## 2024.06.3

 Release date: *12-06-2024*

| Component | Release item                   | Implication for consumers of the Api's (english)                                                                                                                                   | Functional implication (dutch)                                               |
| --------- | ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| DRC       | Business rule DRC-005 disabled | Status of document can be altered even if ontvangstdatum is filled (Api version 1.5 only, not previous versions)                                                                   | Status van het document kan veranderd worden ook al is ontvangstdatum gevuld |
| CSV       | Endpoint for ClientID's        | Api method for retrieving Api endpoints and credentials now supports filtering on application (rx.mission etc) and always returns information, be it for Fundament or external ZGW | Geen                                                                         |

## 2024.06.2

 Release date: *04-06-2024*

| Component               | Release item     | Implication for consumers of the Api's (english) | Functional implication (dutch)                                                     |
| ----------------------- | ---------------- | ------------------------------------------------ | ---------------------------------------------------------------------------------- |
| All ZGW (change in ZCA) | Bug fix ZSDMS UI | No impact                                        | Medewerkers van Roxit konden  geen data meer zien in ZCA -> ZSDMS. Dit is opgelost |

## 2024-05-28.5

 Release date: *30-05-2024*

| Component               | Release item                                   | Implication for consumers of the Api's (english)                                                                                                                                                                                                                                                                                                                                                                              | Functional implication (dutch) |
| ----------------------- | ---------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------ |
| All ZGW (change in CSV) | Authentication in ZCA/CSV New secrets endpoint | Authentication has been adjusted in preparation of making ZCA functions available for customers; There is a new endpoint on CSV for retrieving urls/secrets of external ZGW. In the case these are configured, it returns an array of components (DRC, ZRC etc) with ClientId, secret, and endpoint. In case Fundament is used, the same array is returned but without endpoints. The endpoint is a service to other modules. | Geen                           |
