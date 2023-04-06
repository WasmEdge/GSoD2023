
# WasmEdge Proposal for GSoD 2023

## Project idea: Reorganize the contributor guide

### About our project

WasmEdge is a lightweight, high-performance, extensible, and OCI-compatible WebAssembly runtime. WasmEdge is hosted by CNCF and Linux Foundation.

WasmEdge is licensed under Apache License 2.0 and was started in 2019. WasmEdge has a large and healthy community with more than 132 contributors from [51 organizations](https://wasmedge.devstats.cncf.io/d/5/companies-table?orgId=1&var-period_name=Since%20joining%20CNCF&var-metric=contributions) and [27 countries and regions](https://wasmedge.devstats.cncf.io/d/18/overall-project-statistics-table?orgId=1&viewPanel=1) around the globe. Our community uses WasmEdge to power serverless apps, embedded functions like UDF and data flow functions, microservices, smart contracts, and IoT devices to have a lightweight (The size is just several MBs), fast (It could be started in milliseconds), and security runtime/container running untrusted code.

There are two ways to run Wasm apps in WasmEdge. One is to embed WasmEdge into a host application. To that end, WasmEdge provides embedding SDKs in C/C++, Rust, Go, Java, and Python. The other way is to use WasmEdge as a standalone container (sandbox). The WasmEdge container could seamlessly integrate into existing container ecosystems like Kubernetes and Docker.

Our documentation is located at https://github.com/WasmEdge/docs

### Problem

WasmEdge provides a flexible plug-in architecture that allows developers to add more functionalities to it and take advantage of its many integrations and distribution channels through extensive open source partnerships. A plug-in could package and register native host functions in the WasmEdge runtime. The Wasm bytecode program could then call those native host functions. 

WasmEdge supports writing plug-ins in C, C++, and Rust. Now each language SDK for plug-in development includes code examples. However, the absence of comprehensive tutorials and reference documentation can be challenging for community members who want to contribute new plug-ins. By providing well-structured documentation, the process of developing plug-ins becomes more straightforward and accessible. This will result in an increase in the number of WasmEdge plug-ins, ultimately benefiting every WasmEdge user through community contributions.

### Project scope

This project's scope is to create a clear and comprehensive contributor guide for WasmEdge that will help new contributors develop plug-ins. This will involve reviewing the existing contributor documentation and creating new guides and references for the C, C++, and Rust plug-in SDKs.

This WasmEdge project will 

* Review the existing contributor documentation and develop a new outline for the contributor guide. Here are required content (some of them already exist but need improvements)
    * Architectural overview
    * Getting started with contributing
    * Building WasmEdge
    * Testing WasmEdge
    * Fuzzing
    * Building a plug-in
    * Reporting an issue
    * Proposing a feature request
* Create new WasmEdge plug-in contributor guides in C, C++, and Rust.
* Update the docs on the new Docusarus-based site wasmedge.org/docs/.

#### What is out-of-scope for this project

*  This project doesn't need to cover open-source governance and a code of conduct
*  This project doesn't need to cover creating and compiling  Wasm applications from source code.

We have two committer candidates for mentoring our GSoD project, and we estimate that this work will take three months to complete.

* @yiying, can help answer questions about the design system of the plug-in.
* @juntao, can help review docs pull requests
* @alabulei1, can help walk through the WasmEdge contributing steps

### How would we measure success?

Currently, WasmEdge receives about 80 pull requests each quarter to fix bugs or to add new features. However, only two current contributors are creating plug-ins. They both are experienced WasmEdge developers. This improved contributor guide will help new contributors create plug-ins, and add features to WasmEdge.

Our goal is to increase the number of new contributors by 10%, the number of new plug-in contributors by 50%, and to have at least one new contributor to the WasmEdge runtime itself.

* increase the number of new contributors.
* increase the number of new plug-in contributors.
* at least one contributor for the WasmEdge runtime.

### What skills would a technical writer need to work on this project?

* Must have: Good understanding of Docusaurus and markdown
* Must have: Good understanding of WasmEdge's plug-in system (Or willingness and ability to learn).
* Must have: Good understanding of how GitHub works
* Nice to have: programming skills in C, C++, and Rust
* Nice to have: Familiarity with our GitHub CI in order to automatically update the documentation

### Timeline

This project is estimated to take three months to complete. First, we will spend one month onboarding the technical writer and getting familiar with the existing contribution and plug-in work process. Then we will spend 1.5 months creating the documentation, followed by 0.5 months to review the docs.

| Dates | Action items |
| -------- | -------- | 
|  May | Onboarding the technical writers    | 
|  June - July | documentation development    | 
|  August | documentation Review    | 

## Project budget
| Budget items | Amount | Running Total | Notes |
| -------- | -------- | -------- |-------- |
| Technical writer to review, update, test, and publish new documentation of the WasmEdge Plug-in | USD $4000     | USD $4000   |
| Technical writer to review, update, test, and publish documentation of the WasmEdge contribution guide, excluding the plug-in part     | USD $3000     | USD $7000    |
| Volunteer stipends    | USD $1200    | USD $8200    |3 volunteer stipends x $400 each|
| Project SWAG including T-shirts, stickers and shipping fee | USD $300    | USD $8500    |10 T-shirts x $30 each|
| Total  | USD $8500  |


### Additional information

WasmEdge once participated in GSoC 2022. The project was to implement WASI and wasmedge_process host functions on Windows, and completed successfully.

## Contact us

If you are a Technical Writer and you are interested in contributing to the WasmEdge community for Google Season of Docs 2023, Please send your proposal (by [following the template of writing the statement of interest from Google](https://developers.google.com/season-of-docs/docs/tech-writer-statement)) to our mail at: vivian at secondstate.io.
