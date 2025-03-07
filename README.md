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

WASI Otel exposes an [OpenTelemetry](https://opentelemetry.io/) interface to Wasm components to allow them to collect trace, metric, and log [signals](https://opentelemetry.io/docs/concepts/signals/).

#### An aside about the origin of the proposal

This work was originally being pursued under the banner of [WASI Observe](https://github.com/WebAssembly/wasi-observe). Throughout that process the contributors felt that it was best to pursue creating an interface that was tightly bound to the upstream OpenTelemetry APIs. Both because that is what most developers actually required and because it was more easily achievable than creating a generic interface in the near term. Hence WASI OTel was created to make a space for this work leaving WASI Observe as a space for more generic observability interface in the future.

### Goals

- Enable Wasm components to use standard [OTel SDKs](https://opentelemetry.io/docs/languages/)
- Closely mirror the upstream OTel APIs.

### Non-goals

- Provide an interface that is easily consumed directly by components.

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

#### Enabling observability through WASI Observe

In the future if a need for a more generic observability interface is identified, WASI Observe would be a reasonable home for it. However, for an interface that is tightly bound to the upstream OpenTelemetry APIs, WASI OTel is a better fit.

#### Enabling observability through canon builtins

It would be possible to expose observability through canon builtins. This would potentially provide for a better DX and improved performance. However, the speed of iteration would be greatly reduced and something so core to WASI should not be tied to another project like OpenTelemetry. Therefore, this is left as a potential future opportunity.

### Stakeholder Interest & Feedback

TODO before entering Phase 3.

[This should include a list of implementers who have expressed interest in implementing the proposal]
