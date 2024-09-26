# About OneGround

- [What is OneGround](#what-is-oneground)
- [Changelog](./CHANGELOG.md)
- [Api Versions supported](./ApiVersions.md)
- [Use of ClientID's on Fundament](./ClientID.md)
- [Apply authorisations to ClientId's](./Authorisation.md)
- [Usage of version headers in Fundament](./VersionHeader.md)
- [Example document upload](./exampledocumentupload.md)
- [Problems in and solutions for ZTC 1.3](./ztc1_3problemsandsolutions.md)

## What is OneGround

Fundament is the implementation by Roxit of "case oriented" Api's and registrations according to the [VNG specifications](<https://vng-realisatie.github.io/gemma-zaken/standaard/>).
It contains ZTC, ZRC, DRC, BRC, NC, AC and reference lists.

Fundament comes in two ways: attended and unattended. Attended is the full Saas variant currently available. Unattended is the Open Source variant which will be released later.

## Characteristics of Fundament (attended)

- Fast onboarding
- High performance
- No limit on document size
- Support of the latest ZGW Api versions
- Follows the standard as closely as possible
- Fullfills NEN-ISO 16175
- Built to comply only to the ZGW standards
- Proven in production.

## Why are we saying this?

### Fast onboarding

In order to use Fundament you only have to contact Roxit and request a login account for the configuration tool. In the configuration tool, you can configure ClientID's and secrets, authorise them and  immediately apply them to a Client application such as Open Forms. Thereafter you can start working with documents and cases in Fundament, and share them with your other applications that run on Fundament. The only prerequisite for using Fundament is an RSIN: the KvK (chamber of commerce) identification of your organisation. Your integration with Fundament can be up and running just a few minutes after receiving your login account.

### High performance

99% of ZGW Api requests are handled by Fundament within 50 milliseconds. Most calls that do take longer are related to uploading or downloading documents or expand requests that return large data sets. Fundament runs on Docker, except for document storage which is on the Ceph file system. this set up ensures that extra nodes can be added easily when needed. The system is monitored continuously and performance degradations are noticed fast so that they can be solved timely. The performance of Fundament will contribute to a good user experience of your Client Application.

### No limit on document size

By applying the DRC 1.1 notion of <em>file parts</em> (bestandsdelen), documents of any size can be stored and retrieved. You don;t need to set limits on file size in your client application.

### Support of the latest ZGW Api versions

We are currently in the process of finishing support for the currently (july 2024) latest versions of ZGW. That means that you can run all ZGW-compliant client applications on Fundament.  

### Follows the standard as closely as possible

We intend to follow the standard as closely as possible. Only when it is not possible, for example because the requirements of the standard are contradictory, we deviate from the standard.
In all those instances we file an issues on the VNG Github repository with a request to clarify or a suggestion to fix the problem. Conformity to the standards means that you won't have long integration trajects if you run a ZGW compliant client application on Fundament.

### Fullfills NEN-ISO 16175

Fundament and Archive Management</em> (Archiefbeheer) have been assesed according to ISO-16175:2020, part 1. The assessment was succesful and a declaration of conformity was provided. The base for conformity is provided by the ZGW business rules in ZRC and ZTC. They ensure that each completed case gets a relevant result type with proper indication for the period of retention. The values for result types and retention periods are provided by the Reference list component of Fundament, that we have loaded with the municipial and provincial selection lists. Compliancy to NEN-ISO 16175 means that you don't need an Open Source DMS like Alfresco or a proprietary DMS by a software vendor.

### Built to comply only to the ZGW standards

We started building all components of Fundament with the VNG ZGW standard as a blueprint. The only way to access the data in Fundament therefore is via ZGW conformant Api's. Thus, there is no other way to stoire a case or doucment than via these Api's. This ensures that the data in Fundament always conforms to the standard. Also it helps to provide optimal performance, because there are no older Api's or components to deal with and that might hamper performance. Because of this, you can be sure that all data retrieved from Fundament by a ZGW-compliant client application is readable.

### Proven in production

The VTH application Rx.Mission uses Fundament in production for 130 organisations (july 2024). At peak hours, thousands of users are indirectly using Fundament to read and store case information, to preview documents, and much more. This can lead to about a million Api calls in peak hours. We have many teams working together to keep this system running smoothly. Up to now nine other applications other than Rx.Mission are using Fundament, which number is increasing. This means for you that you can go live fast on Fundament, and expect few problems in production.  
