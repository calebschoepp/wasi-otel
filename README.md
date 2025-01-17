# [Example WASI proposal]

This template can be used to start a new proposal, which can then be proposed in the WASI Subgroup meetings.

The sections below are recommended. However, every proposal is different, and the community can help you flesh out the proposal, so don't block on having something filled in for each one of them.

Thank you to the W3C Privacy CG for the [inspiration](https://github.com/privacycg/template)!

# WASI OTel

A proposed [WebAssembly System Interface](https://github.com/WebAssembly/WASI) API.

### Current Phase

Phase 0

### Champions

- [Caleb Schoepp](https://github.com/calebschoepp)

### Portability Criteria

TODO before entering Phase 2.

## Table of Contents

- [Introduction](#introduction)
- [Goals](#goals-or-motivating-use-cases-or-scenarios)
- [Non-goals](#non-goals)
- [API walk-through](#api-walk-through)
  - [Use case 1](#use-case-1)
  - [Use case 2](#use-case-2)
- [Detailed design discussion](#detailed-design-discussion)
  - [[Tricky design choice 1]](#tricky-design-choice-1)
  - [[Tricky design choice 2]](#tricky-design-choice-2)
- [Considered alternatives](#considered-alternatives)
  - [[Alternative 1]](#alternative-1)
  - [[Alternative 2]](#alternative-2)
- [Stakeholder Interest & Feedback](#stakeholder-interest--feedback)

### Introduction

WASI Otel exposes an [OpenTelemetry](https://opentelemetry.io/) interface to Wasm components to allow them to collect traces, metrics, and logs [signals](https://opentelemetry.io/docs/concepts/signals/). The primary motivation of the interface is to enable Wasm components to use standard [OTel SDKs](https://opentelemetry.io/docs/languages/). A secondary goal is to enable Wasm components to directly consume this interface. WASI OTel seeks to closely mirror the upstream OTel APIs.

#### An aside about the origin of the proposal

This work was originally being pursued under the banner of [WASI Observe](https://github.com/WebAssembly/wasi-observe). Throughout that process the contributors felt that it was best to pursue creating an interface that was tightly bound to the upstream OpenTelemetry APIs. Both because that is what most developers actually required and because it was more easily achievable than creating a generic interface. Hence WASI OTel was created to make a space for this work leaving WASI Observe as a space for more generic observability interface in the future.

### Goals

[What is the end-user need which this project aims to address?]

### Non-goals

[If there are "adjacent" goals which may appear to be in scope but aren't, enumerate them here. This section may be fleshed out as your design progresses and you encounter necessary technical and other trade-offs.]

### API walk-through

The full API documentation can be found [here](wasi-proposal-template.md).

[Walk through of how someone would use this API.]

#### [Use case 1]

[Provide example code snippets and diagrams explaining how the API would be used to solve the given problem]

#### [Use case 2]

[etc.]

### Detailed design discussion

[This section should mostly refer to the .wit.md file that specifies the API. This section is for any discussion of the choices made in the API which don't make sense to document in the spec file itself.]

#### [Tricky design choice #1]

[Talk through the tradeoffs in coming to the specific design point you want to make.]

```
// Illustrated with example code.
```

[This may be an open question, in which case you should link to any active discussion threads.]

#### [Tricky design choice 2]

[etc.]

### Considered alternatives

[This section is not required if you already covered considered alternatives in the design discussion above.]

#### Enabling observability through WASI Observe

TODO

#### Enabling observability through canon builtins

TODO

### Stakeholder Interest & Feedback

TODO before entering Phase 3.

[This should include a list of implementers who have expressed interest in implementing the proposal]
