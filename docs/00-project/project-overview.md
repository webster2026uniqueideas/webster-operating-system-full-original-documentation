# Project Overview

**STATUS: PROPOSED.** Webster is a planned Windows-integrated operating-system environment and systems platform. This repository currently contains documentation only; Webster implementation status: **NOT YET IMPLEMENTED IN THIS REPOSITORY**.

## Definition

Webster aims to provide its own desktop experience, management tools, user-facing applications, stable APIs and native Windows integration. In the first phase it runs on Windows and relies on Windows for kernel, drivers, scheduling, memory, account logon, filesystem and networking primitives. It is not currently a standalone OS.

## Outcomes

1. A coherent, accessible desktop environment that coexists with Windows.
2. A Computer Management experience that reports platform state truthfully and invokes authorized actions through narrow interfaces.
3. A maintainable native C++ layer with testable boundaries and least privilege.
4. A documented path from Windows integration to deeper native services, with independent OS research kept optional.

## Project Knowledge and Proposal

**Known:** the repository has a GPL-3.0 license and no Webster source implementation. **Proposed:** all components and behaviors specified in this documentation. **Dependency:** Windows support, privileges and API availability must be validated before implementation. **Future:** bootable independent OS components.

See [scope](project-scope.md), [architecture](../01-architecture/master-architecture.md), and the [master specification](../../specifications/WEBSTER-MASTER-SPECIFICATION.md).
