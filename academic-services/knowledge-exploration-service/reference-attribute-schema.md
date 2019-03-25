---
title: Define KES index fields
description: 
ms.topic: reference
ms.date: 10/17/2018
---

## Root entity attribute fields

Name | Type | Equals | Range | Completions | Fuzzy | Description
--- | --- | --- | --- | --- | --- | ---
id | int64 | :heavy_check_mark: | - | - | - | TBD
type | string | :heavy_check_mark: | - | - | - | TBD
totalEntities | int64 | - | - | - | - | TBD
totalEstimatedCitations | int64 | - | - | - | - | TBD
totalAffiliations | int64 | - | - | - | - | TBD
totalAuthors | int64 | - | - | - | - | TBD
totalConferenceInstances | int64 | - | - | - | - | TBD
totalConferenceSeries | int64 | - | - | - | - | TBD
totalFieldsOfStudy | int64 | - | - | - | - | TBD
totalJournals | int64 | - | - | - | - | TBD
totalPapers | int64 | - | - | - | - | TBD
totalBooks | int64 | - | - | - | - | TBD
totalBookChapters | int64 | - | - | - | - | TBD
totalConferencePapers | int64 | - | - | - | - | TBD
totalJournalPapers | int64 | - | - | - | - | TBD
totalPatents | int64 | - | - | - | - | TBD

## Paper attribute fields

Name | Type | Equals | Range | Completions | Fuzzy | Description
--- | --- | --- | --- | --- | --- | ---
id | int64 | :heavy_check_mark: | - | - | - | TBD
type | string | :heavy_check_mark: | - | - | - | TBD
doi | string? | :heavy_check_mark: | - | - | :heavy_check_mark: | TBD
docType | string | :heavy_check_mark: | - | - | - | TBD
year | int32? | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | TBD
date | date? | :heavy_check_mark: | :heavy_check_mark: | - | - | TBD
actualCitationCount | int64? | :heavy_check_mark: | :heavy_check_mark: | - | - | TBD
estimatedCitationCount | int64? | :heavy_check_mark: | :heavy_check_mark: | - | - | TBD
title | string? | :heavy_check_mark: | - | :heavy_check_mark: | :heavy_check_mark: | TBD
originalTitle | blob? | - | - | - | - | TBD
bookTitle | blob? | - | - | - | - | TBD
publisher | blob?  | - | - | - | - | TBD
originalVenue | blob? | - | - | - | - | TBD
volume | int32? | :heavy_check_mark: | :heavy_check_mark: | - | :heavy_check_mark: | TBD
issue | int32? | :heavy_check_mark: | :heavy_check_mark: | - | :heavy_check_mark: | TBD
firstPage | int32? | :heavy_check_mark: | :heavy_check_mark: | - | :heavy_check_mark: | TBD
lastPage | int32? | :heavy_check_mark: | :heavy_check_mark: | - | :heavy_check_mark: | TBD
languages | string* | :heavy_check_mark: | - | - | - | TBD
recommendations | blob* | - | - | - | - | TBD
bibtexType | blob? | - | - | - | - | TBD
abstract | jsonBlob* | - | - | - | - | TBD
 | | | | | |
authors | composite* | | | | |
authors.authorId | int64 | :heavy_check_mark: | - | - | - | TBD
authors.firstName | string? | :heavy_check_mark: | - | :heavy_check_mark: | :heavy_check_mark: | TBD
authors.lastName | string? | :heavy_check_mark: | - | :heavy_check_mark: | :heavy_check_mark: | TBD
authors.originalName | blob | - | - | - | - | TBD
authors.affiliationId | int64? | :heavy_check_mark: | - | - | - | TBD
authors.affiliationName | string? | :heavy_check_mark: | - | :heavy_check_mark: | :heavy_check_mark: | TBD
authors.originalAffiliation | blob | - | - | - | - | TBD
authors.sequence | int32 | :heavy_check_mark: | :heavy_check_mark: | - | - | TBD
 | | | | | |
conference | composite+ | | | | |
conference.id | int64 | :heavy_check_mark: | - | - | - | TBD
conference.name | string | :heavy_check_mark: | - | :heavy_check_mark: | :heavy_check_mark: | TBD
 | | | | | |
conferenceInstance | composite+ | | | | |
conferenceInstance.id | int64 | :heavy_check_mark: | - | - | - | TBD
conferenceInstance.name | string | :heavy_check_mark: | - | :heavy_check_mark: | :heavy_check_mark: | TBD
 | | | | | |
fieldsOfStudy | composite* | | | | |
fieldsOfStudy.id | int64 | :heavy_check_mark: | - | - | - | TBD
fieldsOfStudy.name | string | :heavy_check_mark: | - | :heavy_check_mark: | :heavy_check_mark: | TBD
 | | | | | |
journal | composite+ | | | | |
journal.id | int64 | :heavy_check_mark: | - | - | - | TBD
journal.name | string | :heavy_check_mark: | - | :heavy_check_mark: | :heavy_check_mark: | TBD
 | | | | | |
references | composite* | | | | |
references.id | int64 | :heavy_check_mark: | - | - | - | TBD
references.context | blob | - | - | - | - | TBD
 | | | | | |
resources | composite* | | | | |
resources.type | string | :heavy_check_mark: | - | - | - | TBD
resources.relationship | string | :heavy_check_mark: | - | - | - | TBD
resources.url | blob | - | - | - | - | TBD
resources.sourceUrl | blob | - | - | - | - | TBD
 | | | | | |
sources | composite* | | | | |
sources.type | string | :heavy_check_mark: | - | - | - | TBD
sources.url | blob | - | - | - | - | TBD

## Affiliation attribute fields

Name | Type | Equals | Range | Completions | Fuzzy | Description
--- | --- | --- | --- | --- | --- | ---
id | int64 | :heavy_check_mark: | - | - | - | TBD
type | string | :heavy_check_mark: | - | - | - | TBD

## Author attribute fields

Name | Type | Equals | Range | Completions | Fuzzy | Description
--- | --- | --- | --- | --- | --- | ---
id | int64 | :heavy_check_mark: | - | - | - | TBD
type | string | :heavy_check_mark: | - | - | - | TBD

## Conference series attribute fields

Name | Type | Equals | Range | Completions | Fuzzy | Description
--- | --- | --- | --- | --- | --- | ---
id | int64 | :heavy_check_mark: | - | - | - | TBD
type | string | :heavy_check_mark: | - | - | - | TBD

## Conference instance attribute fields

Name | Type | Equals | Range | Completions | Fuzzy | Description
--- | --- | --- | --- | --- | --- | ---
id | int64 | :heavy_check_mark: | - | - | - | TBD
type | string | :heavy_check_mark: | - | - | - | TBD

## Field of study attribute fields

Name | Type | Equals | Range | Completions | Fuzzy | Description
--- | --- | --- | --- | --- | --- | ---
id | int64 | :heavy_check_mark: | - | - | - | TBD
type | string | :heavy_check_mark: | - | - | - | TBD

## Journal attribute fields

Name | Type | Equals | Range | Completions | Fuzzy | Description
--- | --- | --- | --- | --- | --- | ---
id | int64 | :heavy_check_mark: | - | - | - | TBD
type | string | :heavy_check_mark: | - | - | - | TBD
