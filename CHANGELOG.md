# Changelog

## 2024-05-01

### Fixes

#### Some clients escape all forward slashes with a backslash.

Fundaments standard libraries removed those escape characters without the developer being aware of it.
But the DRC->content (inhoud) field is handled differently because its contents can be very large. The escape characters remained inn that field, resulting in errors. This has now been solved so that escape characters are also removed in the inhoud field.
