# Camtree Digital Library — AI and Machine Access

This repository contains guidance for AI agents, language models, developers, and other automated systems accessing the [Camtree Digital Library](https://library.camtree.org/).

The Camtree Digital Library is an open-access repository of teacher-led research, practitioner inquiry, research reports, educational resources, and related publications maintained by the Cambridge Teacher Research Exchange (Camtree).

## Contents

- [llms.txt](llms.txt) — primary entry point for AI and machine access
- [api-guide.md](api-guide.md) — guidance on using the DSpace REST API and OAI-PMH interfaces
- [collections.md](collections.md) — overview of major repository collections and their scope

## Purpose

These files are intended to help automated systems:

- understand the purpose and scope of the repository
- discover appropriate machine-readable interfaces
- search the repository efficiently
- preserve collection and research context
- cite canonical repository records
- distinguish repository metadata from publication content and generated interpretation
- avoid unsupported generalisation from teacher-led research

The guidance supplements, rather than replaces, the repository's existing machine interfaces.

## Repository access

Main repository:

https://library.camtree.org/

DSpace REST API:

https://library.camtree.org/server/api

OAI-PMH endpoint:

https://library.camtree.org/server/oai/request

For targeted search and retrieval, use the REST API.

For bulk metadata harvesting and synchronisation, use OAI-PMH.

## llms.txt

The primary machine-oriented entry point is:

[llms.txt](llms.txt)

It follows the 'llms.txt' approach for providing a concise description of a resource and links to further machine-readable guidance.

The file may be linked directly from the Camtree Digital Library interface so that users and automated systems can discover these resources even though the files are maintained separately from the DSpace server.

## Evidence and responsible use

The Camtree Digital Library contains research conducted in specific educational contexts.

Automated systems should:

- preserve the context in which research was conducted
- avoid attributing claims that are not supported by the source
- avoid treating repository search results as automatically exhaustive
- distinguish clearly between source material and generated interpretation
- check rights and licensing information before reusing content

Where full text is unavailable, findings should not be inferred from metadata alone.

## Maintenance

These files are maintained separately from the DSpace application so that guidance for machine access can be updated without requiring access to the repository server.

Changes are version-controlled through GitHub.

## About Camtree

[Camtree: the Cambridge Teacher Research Exchange](https://camtree.org/) supports close-to-practice research by educators, practitioner inquiry, professional learning, and open-access publication.

The [Camtree Digital Library](https://library.camtree.org/) provides open access to the outcomes of close-to-practice research by educators and related educational resources.