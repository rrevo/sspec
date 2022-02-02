# sspec

sspec is a project to enable authoring of technical specifications. The project will enable technical specifications to be configurable, extensible, live documents that will sync with the systems that they define.

## Rationale

Technical specifications are a blueprint or plan to solve a technical problem. Specifications are useful at various stages of a project. In early analysis, it is useful to specify the requirements and unknowns. During the building phase, it serves as a reference for what needs to be done along with verification. When the project is active, it is a useful reference as team members and requirements of the project change. For projects that are decommissioned it is useful to understand impact as well. During all these stages, specifications help communication across different teams and functions. 

Traditional technical specifications have issues-

* Drift - If not maintained, the specifications go out of sync from the systems they describe. In the worst case the system built never meets the requirements.
* Scope - Typically only very high-level information is mentioned in specifications by a small group of architects. Other important information is captured in other code artifacts or docs, although it is critical.
* Adhoc - Specifications from different teams even in the same organization do not follow similar standards.

sspec aims to address these shortcomings. The primary idea is based on specs itself being programmable. As the project progresses the *how* will become clearer.

## Goals

sspec specifications will be based on a custom [domain specific language](https://en.wikipedia.org/wiki/Domain-specific_language) (DSL). Features will be - 

* sspec will define a basic grammar for core requirements for any spec.
* The grammar will be extensible based on custom requirements.
* A library will be created with common features or extensions to the grammar. These should be available to the users of sspec.
* It must be possible to adopt sspec in an incremental fashion from minimal textual spec in the ideation phase to a spec integrated with a monitoring tool for continuous verification of the system.
* sspecs should be identifiable.
* sspecs should be version-able.
* sspecs must be composable. It should be able to cross-reference different sspecs.

Ideas for the DSL are-
* Doc generator - Given a sspec, generate a markdown file so that it can be used in external tools like wikis for reviews or sharing with others.
* Verifier - A monitoring system provides stats on the expected latency for calls to the system. A sspec connector is able to push alarms to the monitoring system based on the configured spec.

## Status

The project is currently in an ideation phase.

Version 0.0.1

## Next steps

* Learn more on the topic and research prior art including references below.
* Draft potential sspecs at various project stages.

## References

### Projects

* [TLA+](https://lamport.azurewebsites.net/tla/tla.html)
* [Clojure spec](https://clojure.org/about/spec)
* [Read the Docs - docs](https://docs.readthedocs.io/en/stable/index.html)
* [Gherkin](https://cucumber.io/docs/gherkin/reference/)
* [Literate Programming](/docs/literate_programming.md)

### Articles

* [Machine readable specifications at scale](https://alastairreid.github.io/mrs-at-scale/)
* [A practical guide to writing technical specs](https://stackoverflow.blog/2020/04/06/a-practical-guide-to-writing-technical-specs/)
