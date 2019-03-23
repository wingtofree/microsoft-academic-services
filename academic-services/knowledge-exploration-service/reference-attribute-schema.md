---
title: Define KES index fields
description: 
ms.topic: reference
ms.date: 10/17/2018
---

## Paper attribute fields

Name | Type | Equals | Range | Completions | Fuzzy | Description
--- | --- | --- | --- | --- | --- | ---
id | int64 | :heavy_check_mark:| - | - | - | TBD
doi | string? | :heavy_check_mark:| - | - | :heavy_check_mark:| TBD
docType | string | :heavy_check_mark:| - | - | - | TBD
year | int32? | :heavy_check_mark:| :heavy_check_mark:| :heavy_check_mark:| :heavy_check_mark:| TBD
date | date? | :heavy_check_mark:| :heavy_check_mark:| - | - | TBD
actualCitationCount | int64? | :heavy_check_mark:| :heavy_check_mark:| - | - | TBD
estimatedCitationCount | int64? | :heavy_check_mark:| :heavy_check_mark:| - | - | TBD
title | string? | :heavy_check_mark:| - | :heavy_check_mark:| :heavy_check_mark:| TBD
originalTitle | blob | - | - | - | - | TBD
bookTitle | blob | - | - | - | - | TBD
publisher | blob  | - | - | - | - | TBD
originalVenue | blob | - | - | - | - | TBD
volume | int32? | :heavy_check_mark:| :heavy_check_mark:| - | :heavy_check_mark:| TBD
issue | int32? | :heavy_check_mark:| :heavy_check_mark:| - | :heavy_check_mark:| TBD
firstPage | int32? | :heavy_check_mark:| :heavy_check_mark:| - | :heavy_check_mark:| TBD
lastPage | int32? | :heavy_check_mark:| :heavy_check_mark:| - | :heavy_check_mark:| TBD
languages | string* | :heavy_check_mark:| - | - | - | TBD
recommendations | blob* | - | - | - | - | TBD
 | | | | | |
abstract | composite? | | | | |
abstract.word | blob | - | - | - | - | TBD
abstract.indexes | blob | - | - | - | - | TBD
 | | | | | |
authors | composite* | | | | |
authors.authorId | int64 | :heavy_check_mark:| - | - | - | TBD
authors.firstName | string? | :heavy_check_mark:| - | :heavy_check_mark:| :heavy_check_mark:| TBD
authors.lastName | string? | :heavy_check_mark:| - | :heavy_check_mark:| :heavy_check_mark:| TBD
authors.originalName | blob | - | - | - | - | TBD
authors.affiliationId | int64? | :heavy_check_mark:| - | - | - | TBD
authors.affiliationName | string? | :heavy_check_mark:| - | :heavy_check_mark:| :heavy_check_mark:| TBD
authors.originalAffiliation | blob | - | - | - | - | TBD
authors.sequence | int32 | :heavy_check_mark:| :heavy_check_mark:| - | - | TBD
 | | | | | |
conference | composite+ | | | | |
conference.id | int64 | :heavy_check_mark:| - | - | - | TBD
conference.name | string | :heavy_check_mark:| - | :heavy_check_mark:| :heavy_check_mark:| TBD
 | | | | | |
conferenceInstance | composite+ | | | | |
conferenceInstance.id | int64 | :heavy_check_mark:| - | - | - | TBD
conferenceInstance.name | string | :heavy_check_mark:| - | :heavy_check_mark:| :heavy_check_mark:| TBD
 | | | | | |
fieldsOfStudy | composite* | | | | |
fieldsOfStudy.id | int64 | :heavy_check_mark:| - | - | - | TBD
fieldsOfStudy.name | string | :heavy_check_mark:| - | :heavy_check_mark:| :heavy_check_mark:| TBD
 | | | | | |
journal | composite+ | | | | |
journal.id | int64 | :heavy_check_mark:| - | - | - | TBD
journal.name | string | :heavy_check_mark:| - | :heavy_check_mark:| :heavy_check_mark:| TBD
 | | | | | |
references | composite* | | | | |
references.id | int64 | :heavy_check_mark:| - | - | - | TBD
references.context | blob | - | - | - | - | TBD
 | | | | | |
resources | composite* | | | | |
resources.type | string | :heavy_check_mark:| - | - | - | TBD
resources.relationship | string | :heavy_check_mark:| - | - | - | TBD
resources.url | blob | - | - | - | - | TBD
resources.sourceUrl | blob | - | - | - | - | TBD
 | | | | | |
sources | composite* | | | | |
sources.type | string | :heavy_check_mark:| - | - | - | TBD
sources.url | blob | - | - | - | - | TBD