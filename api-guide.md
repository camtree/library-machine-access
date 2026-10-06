# Camtree Digital Library API Guide

This guide describes the preferred machine-access interfaces for the Camtree Digital Library.

## Preferred interfaces

Use __the DSpace REST API__ for targeted search, item retrieval, metadata inspection and collection browsing.

Base endpoint:

https://library.camtree.org/server/api

Use __OAI-PMH__ for bulk metadata harvesting and synchronisation.

OAI endpoint:

https://library.camtree.org/server/oai/request

## Searching the repository

Preferred discovery endpoint:

https://library.camtree.org/server/api/discover/search/objects

Use targeted search for:
- keywords
- titles
- authors
- dates
- subjects
- collection-scoped searches

Avoid treating search results as exhaustive evidence unless the query and scope justify this.

## Retrieving items

Items are available through:

https://library.camtree.org/server/api/core/items

Prefer canonical repository handle URLs when presenting results to users.

Example canonical identifier:

https://library.camtree.org/handle/20.500.14069/1234

Internal UUIDs may be used for API calls but should not be shown as the primary citation.

## Collections and communities

Collections:

https://library.camtree.org/server/api/core/collections

Communities:

https://library.camtree.org/server/api/core/communities

Use collection information to preserve the context of a publication.

## OAI-PMH

Use OAI-PMH for bulk harvesting.

All OAI-PMH verbs are supported:

- Identify
- ListSets
- ListIdentifiers
- ListRecords
- ListMetadataFormats
- GetRecord

Example:

https://library.camtree.org/server/oai/request?verb=ListSets

For Dublin Core records:

https://library.camtree.org/server/oai/request?verb=ListRecords&metadataPrefix=oai_dc

'Communities' and 'collections' in DSpace are both treated as 'Sets'; communities have the suffix "com", collections have the suffix 'col'.

Resumption tokens are required as items are returned in batches of 100. Using clients such as [https://pypi.org/project/oaipmh-scythe/](Scythe) (Python) or  [https://metacpan.org/pod/HTTP::OAI::Harvester](HTTP::OAI::Harvester) (Perl) is recommended.

## Agent guidance

Agents should:

- prefer structured metadata over scraping HTML
- preserve item titles and authorship exactly where possible
- cite canonical handle URLs
- retain collection context
- distinguish repository metadata from generated interpretation
- avoid inferring findings not stated in the publication
- state when repository evidence is limited or absent

## Full text

Some records include downloadable files such as PDF, DOCX or PPTX.

Check the item's files and rights metadata before reuse.

Where full text is unavailable, do not infer findings from metadata alone.