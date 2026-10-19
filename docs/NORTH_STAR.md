# Launchpad — North Star

## Mission

**Make evidence-driven software validation approachable and reproducible through working examples, installation guidance, and integration documentation.**

Launchpad helps a developer move from discovering Forge or its companion tools to successfully running them against a realistic example and adapting that example to an existing project.

Launchpad is **not a fifth application, shared runtime, dashboard, or mandatory wrapper**. The products remain **Forge, Tun, Atticus, and Shipweard**, each responsible for its own functionality and experience.

## What Launchpad owns

- **Getting started:** prerequisites, installation, configuration, first successful run, and troubleshooting.
- **Runnable examples:** small, realistic projects with source code, tests, documented commands, expected behavior, and a repeatable baseline.
- **Integration recipes:** how to adopt the tools in existing applications and CI systems, with enough context to adapt examples rather than blindly copying them.
- **Cross-product examples:** optional demonstrations of how Forge, Tun, Atticus, and Shipweard complement one another. No individual tool should depend on Launchpad to operate.
- **Developer-oriented documentation:** clear product boundaries, practical workflows, limitations, and links to each project's authoritative technical documentation.

## A useful example must be executable

Each published example should let a developer:

1. Check out the example and install documented prerequisites.
2. Execute its existing tests or validation baseline.
3. Make or inspect a deliberate source change and reproduce its impact.
4. Run the relevant product/tooling and observe the actual output.
5. Understand what the result demonstrates, **why** a validation was selected, and what remains uncertain or unvalidated, when supported by the product.
6. Reproduce the documented behavior without assistance from the example's author.

Examples must be verified in CI where practical. Documented output must agree with the software's actual capabilities; planned behavior must be labeled as planned.

## Language and ecosystem coverage

Start with a **TypeScript + Vitest** Forge example when Forge has enough test-selection functionality to demonstrate a meaningful end-to-end flow.

Expand through focused, runnable examples as integrations become available: Python/pytest, .NET, Java/JUnit, Rust/Cargo, C++/CMake/CTest, and eventually cross-language cases such as Rust or C++ compiled to WebAssembly and consumed by a TypeScript application.

These are **future example targets**, not claims of existing support or release commitments. Example-specific build and validation scripts are welcome; a general-purpose build platform is not a Launchpad requirement.

## Boundaries

- **Forge** owns change analysis, validation planning and selection, and explainable validation evidence.
- **Atticus** owns controlled dependency/API behavior and mocking.
- **Tun** owns its supporting test resources and tooling.
- **Shipweard** owns production/operational signals and their relationship to validation evidence.
- **Launchpad** teaches developers how to adopt these capabilities. Product code, core adapters, and product-specific authoritative documentation remain in their respective repositories.

Do not create a Launchpad CLI, unified dashboard, execution coordinator, or shared product state without a separately demonstrated need. The existence of a portfolio does not justify another application.

## Success criterion

**Done when a developer unfamiliar with the project can follow the documentation, run a maintained example locally (and in CI where applicable), observe the promised behavior, and understand both the evidence and its limitations.**

Launchpad succeeds by reducing the effort required to adopt the existing products—not by accumulating its own features.
