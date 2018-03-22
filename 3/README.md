---
domain: rfc.opencannabis.info
shortname: 3/OCS
name: OpenCannabis Specification
status: raw
editor: Sam Gammon <sam@bloombox.io>
contributors:
  - Tyler Porras <tyler@bloombox.io>
  - Tim Samartino <tim@bloombox.io>
  - Matt McLean <matt@gocaliva.com>
  - Scott Robinson <srobinson@abatinsacramento.com>
---

# OpenCannabis Specification ![raw](http://rfc.unprotocols.org/spec:2/COSS/raw.svg) [![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg?longCache=true&style=flat-square)](https://www.gnu.org/licenses/gpl-3.0)

### Table of Contents
1. [Introduction](#Introduction)
    - [Why write a spec?](#Why-write-a-spec?)
    - [Process and Licensing](#Process-and-licensing)
    - [Language](#Language)
3. [Vision](#Vision-and-Principles)
    - [Project Goals](#Project-Goals)
4. [Architecture](#Architecture)
5. [Conventions](#Conventions)

## Introduction

This document describes an interoperable technical data specification tailored for the **worldwide legal cannabis
market**. As legal markets to buy, sell, cultivate and manufacture cannabis products come online, a need is emerging for
a universal way of connecting data systems and components that work with cannabis or cannabis-related data.

#### Why write a spec?
Currently, the state of the art in cannabis technology is one of two options: Massive, sweeping ecosystems of
proprietary code (that frequently break), and isolated, SaaS-style startups that provide great tools but without the
ecosystem around them for maximal value.

Some business operators opt for the big players, and feel the pain when they go down. Others spread that pain out over
many smaller providers but both are still unhappy. What's the answer to fixing these problems?

An open specification, for cannabis data. For your menu, your transactions, your customers, and so on - so that when one
provider isn't enough, or it's time to switch, or you want to write your own code - your data and your business aren't
locked away.

#### Process and licensing

This specification is based on the [2/COSS](../2/README.md) (*Consensus-Oriented Specification System*) process, and
before it, the original [Digistan 1/COSS](http://www.digistan.org/spec:1/COSS), which are designed to be a lightweight
editorial process that seeks to engage the widest possible range of interested parties and move rapidly to consensus
through working code.

Extensions to the main specification should be proposed for each market stakeholder (from _seed to smoke_, as it were).
The hope is that this work can begin a conversation amongst cannabis software providers about a universal spec and
integration suite.

##### Change Process

This document is governed by the [2/COSS](../2/README.md) (*Consensus-Oriented Specification System*), and is published
via, and inspired by, the [Unprotocols RFC](https://github.com/unprotocols/rfc) structure.

##### Spec licensing as GNU GPLv3

The _OpenCannabis Specification_ itself - i.e., this document and any accompanying specification materials, including,
but not limited to, graphics, additional spec revisions or extensions, and so on, is licensed under the [GNU General
Public License](./LICENSE.md), version 3. This means additional work on this spec, or forks of this spec, must also be
kept open source and shared-alike with the community.

##### Code licensing as Apache 2.0

Software written _to comply with_ or _make use of_ this spec does not have to be open source. For this reason, the
_actual code_ for the OpenCannabis specification is licensed under the
[Apache License](https://www.apache.org/licenses/LICENSE-2.0), version 2.0.

### Language

The key words "**MUST**", "**MUST NOT**", "**REQUIRED**", "**SHALL**", "**SHALL NOT**", "**SHOULD**", "**SHOULD NOT**",
"**RECOMMENDED**",  "**MAY**", and "**OPTIONAL**" in this document are to be interpreted as described in
[RFC 2119](http://tools.ietf.org/html/rfc2119).

## Vision and Principles

The OpenCannabis Data Specification's mission statement is to **facilitate the implementation, and agreement upon, an
open information structure for legal cannabis operations**. The hope is that a point of agreement such as this one
amongst industry practitioners and stakeholders can bring about easier development of integrations between major
systems.

From [2/COSS](../2/README.md):
*A "technical specification" defines a protocol, a process, an API, a use of language, a methodology, or any other
aspect of a technical environment that can usefully be documented for the purposes of technical or social
interoperability.*

**OpenCannabis intends to apply these same principles:**
* We aim for rough consensus and running code.
* Specifications are small pieces, made by small teams.
* Specifications should have a clearly responsible editor.
* The process should be visible, objective, and accessible to anyone.
* The process should clearly separate experiments from solutions.
* The process should allow deprecation of old specifications.

Specifications should take minutes to explain, hours to design, days to write, weeks to prove, months to become mature,
and years to replace. Specifications have no special status except that accorded by the community.

### Project Goals

- **Goal:** Specify a universal information model for cannabis cultivation, manufacturing, distribution, testing, and
  retail operations.
- **Goal:** Construct and release spec implementations in every major programming language.
- **Goal:** Write and release detailed narrative documentation and API reference materials in every supported language.
- **Goal:** Encourage adoption and contribution to the spec through open, transparent, and fair process.
- **Goal:** Cross-functional structures and protocols that reflect accurate science.
- **Anti-goal:** Specific provider-coupled structures, services, or concepts.
- **Anti-goal:** Separate notions or data modelling on stakeholder-defined boundaries.
- **Anti-goal:** Isolated, central control of the cannabis industry's data.
- **Anti-goal:** Regulatory information repository or legal advice. This specification is structural, and compliance
  with the law is up to you and your lawyer.

## Architecture

In accordance with the [2/COSS](../2/README.md) architecture, OpenCannabis (the spec) makes use of modern tools such as
Git, Markdown, and Slack. Code is written in Protobuf to facilitate language agnostic adoption. Primarily, a wiki-style
model is employed for authoring, editing, and publishing specification texts. 

This specification's _domain root_ is `rfc.opencannabis.info`, and, thus, this very document can be accessed at:

```
https://rfc.opencannabis.info/spec:3/OCS
```

Quoth [2/COSS](../2/README.md):
* The *domain* is the conservancy for a set of specifications in a certain area.
* Each domain is implemented as an Internet domain, hosting a wiki and optionally other communications tools.
* Each specification is a set of wiki pages, together with comments, attached files, and other resources.
* Important specifications may also exist as subdomains, i.e. child wikis.

The goal of the OpenCannabis spec is to unify industry stakeholders around one model. It **MAY** be necessary, but
**SHOULD** be avoided, because it is an explicit anti-goal to avoid stakeholder-based coupling (and a goal to promote
cross-stakeholder integration).

Accordingly, major spec extensions to the main _OCS_ spec:

* **MUST** be assigned their own number, name, short name.
* **MUST** follow the [2/COSS](../2/README.md) lifecycle.
* **MAY** be assigned their own sub domain.
* **SHOULD** be designed around functional boundaries.
* **SHOULD NOT** be designed around functional or stakeholder boundaries.

Individuals can become members of the domain by completing the necessary legal clearance.  The copyright, patent, and 
rademark policies of the domain must be clarified in an Intellectual Property policy that applies to the domain.

Specifications exist as multiple pages, one page per version of the specification (see "_Branching and Merging_",
below), which may be assigned URIs that include an incremental number.  Thus, we refer to a specification by specifying
its domain, number, and short name.  New versions of the same specification will have new numbers.  The syntax for a
specification reference is:


    <domain>/spec:<number>/<shortname>


For example, this specification is **rfc.opencannabis.info/spec:3/OCS**.  The short form **3/OCS** may be used when
referring to the specification from other specifications in the same domain.

Every specification (including branches) carries a different number.  Lower numbers indicate more mature specifications,
higher numbers indicate more experimental specifications.

## Conventions

Where possible editors and contributors are encouraged to:

* Refer to and build on existing work when possible, especially IETF specifications.
* Contribute to existing specifications rather than reinvent their own.
* Use collaborative branching and merging as a tool for experimentation.

## License

Copyright (c) 2018, the OpenCannabis Editor and Contributors.

This Specification is free software; you can redistribute it and/or modify it under the terms of the
[GNU General Public License](LICENSE.md) as published by the Free Software Foundation; either version 3 of the License,
or (at your option) any later version.

This Specification is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied
warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program; if not, see
http://www.gnu.org/licenses.