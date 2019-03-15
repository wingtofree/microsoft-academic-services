---
title: Define KES index fields
description: 
ms.topic: reference
ms.date: 10/17/2018
---
# Define KES Index Fields

TODO: Summarize

## Data types

Type | Description
--- | ---
string | Text string (maximum length 4096)
int32 | Signed 32-bit integer
int64 | Signed 64-bit integer
double | Double-precision floating point value
date | Date string using the format YYYY-MM-DD
guid | Globally unique identifier string using the format "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
blob | Compressed text string (TODO: figure out maximum size)
composite | Composition of multiple sub-fields, meant to model complex data types.

### Data type quantifiers

Quantifier | Description
--- | ---
** | Indicates the field can have zero or more values
++ | Indicates the field can have one or more values
? | Indicates the field can have zero or one value

Examples:

``` JSON
{ "name": "peopleInElevator", "type": "string*" }
{ "name": "authorNames", "type": "string+" }
{ "name": "publishedIn", "type": "string?" }
```

### Composite type fields

Composite type fields are used to represent complex data types that include one or more sub-fields. Composite field definitions are composed of both the composite parent field definition, and separate sub-field child definitions.

Example:

``` JSON
{ "name": "person", "type": "composite"}
{ "name": "person.name", "type": "string"}
{ "name": "person.age", "type": "int32"}
```

## Index attributes

Attribute | Value | Supported by | Description
--- | --- | --- | ---
name | string | N/A | Required. The name of the field. If field is part of a composite type (i.e. a sub-field), the name of the composite type and a period (".") must precede the field name, e.g. "person.age".
type | string | N/A | Required. The data type of the field.
supportFuzzySearch | boolean (false) | string, int32, int64, double, date, guid | Indicates that the field can be used for fuzzy search operations. Fuzzy search enables the field to be matched using partial and/or similar words, e.g. "dog jump moon" would match "Hey Diddle Diddle, The cat and the fiddle, The cow jumped over the moon. The little dog laughed, To see such fun, And the dish ran away with the spoon."
supportEqualsFilter | boolean (false) | string, int32, int64, double, date, guid |  Indicates that the field can be used in filter equality expressions, e.g. foo='bar'.
supportRangeFilter | boolean (false) | int32, int64, double, date | Indicates that the field can be used in filter range (lt,lte,gt,gte) expressions, e.g. birthDate<='1981-01-13'.
supportCompletion | boolean (false) | string, int32, int64, double | Indicates that the field can be used query completions, e.g. suggesting "an overview of microsoft academic service mas and applications" for the partial query "an overview of microsoft academic".
synonymMap | string | string |  Optional. Associates a synonym map with the field.