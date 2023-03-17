# WasmEdge Proposal for GSoD 2023

## About our project

WasmEdge is a lightweight, high-performance, extensible, and OCI-compatible WebAssembly runtime. WasmEdge is hosted by CNCF and Linux Foundation.

There are two ways to run Wasm apps in WasmEdge. One is to embed WasmEdge into a host application. To that end, WasmEdge provides embedding SDKs in C/C++, Rust, Go, Java, and Python. The other way is to use WasmEdge as a standalone container (sandbox). The WasmEdge container could seamlessly integrate into existing container ecosystems like Kubernetes and Docker.

WasmEdge powers serverless apps, embedded functions, microservices, smart contracts, and IoT devices.

Doc site: https://wasmedge.org/book/en/

## Project idea: Reorganzie the contributor guide

### Problem

WasmEdge plugins allow developers to add functionalities and features to the runtime. A plugin could package and register native host functions in the WasmEdge runtime. The Wasm bytecode program could then call those native host functions. 

WasmEdge supports writing plugins in C, C++, and Rust. Each of the language SDKs for plugin development has code examples. However, the lack of official tutorials and reference documentation makes it difficult for community members to contribute new plugins.

### Project scope

The scope of this project is to create a clear and comprehensive contributor guide for WasmEdge that will help new contributors develop plugins. This will involve reviewing the existing contributor documentation and creating new guides and references for the C, C++, and Rust plugin SDKs.

This WasmEdge project will 

* Review the existing contributor documentation and develop a new outline for the contributor guide. Here are required content (some of them already exist but need improvements)
    * Architectural overview
    * Getting started with contributing
    * Building WasmEdge
    * Testing WasmEdge
    * Fuzzing
    * Building a plugin
    * Reporting an issue
    * Proposing a feature request
* Create new WasmEdge plugin contributor guides in C, C++, and Rust.
* Update the docs on the new Docusarus-based site wasmedge.org/docs/.

#### What is out-of-scope for this project

*  This project doesn't need to cover open-source governance and a code of conduct
*  This project doesn't need to cover creating and compiling  Wasm applications from source code.

We have two committer candidates for mentoring our GSoD project, and we estimate that this work will take three months to complete.

* @yiying, can help answer questions about the design system of plugin.
* @juntao, can help review docs pull requests
* @alabulei1, can help walk through the WasmEdge contributing steps

### How would we measure success?

Currently, WasmEdge receives about 80 pull requests each quarter to fix bugs or to add new features. However, only two current contributors are creating plugins. They both are experienced WasmEdge developers. This improved contributor guide will help new contributors create plugins, and add features to WasmEdge.

Our goal is to increase the number of new contributors by 10%, the number of new plugin contributors by 50%, and to have at least one new contributor to the WasmEdge runtime itself.

* increase the number of new contributors.
* increase the number of new plugin contributors.
* at least one contributor for the WasmEdge runtime.

### What skills would a technical writer need to work on this project?

* Must have: Good understanding of Docusaurus and markdown
* Must have: Good understanding of WasmEdge's plugin system (Or willingness and ability to learn).
* Must have: Good understanding of how GitHub works
* Nice to have: programming skills in C, C++, and Rust
* Nice to have: Familiarity with our GitHub CI in order to automatically update the documentation

### Timeline

This project is estimated to take three months to complete. We will spend one month onboarding the technical writer and getting familiar with the existing contribution and plugin work process. Then we will spend 1.5 months on creating the documentation, followed by 0.5 months to review the docs.

| Dates | Action items |
| -------- | -------- | 
|  May | Onboarding the technical writers    | 
|  June - July | documentation development    | 
|  August | documentation Review    | 

## Project budget
| Budget items | Amount | Running Total | Notes |
| -------- | -------- | -------- |-------- |
| Technical writer to review, update, test, and publish new documentation of the WasmEdge Plugin | 4000     | 4000    |
| Technical writer to review, update, test, and publish documentation of the WasmEdge contribution guide, excluding the plugin part     | 3000     | 7000    |
| Volunteer stipends    | 1200    | 8200    |3 volunteer stipends x $400 each|
| Project SWAG including T-shirts, stickers and shipping fee | 300    | 8500    |10 T-shirts x $30 each|
| Total  | 8500  |


### Additional information

WasmEdge once participated in GSoC 2022. The project was to implement WASI and wasmedge_process host functions on Windows, and completed successfully.

## Contact us

If you are a Technical Writer and you are interested in contributing to WasmEdge community for Google Season of Docs 2023, Please send your proposal (by following the template of writing the statement of interest from Google) to our mail at: vivian@secondstate.io
