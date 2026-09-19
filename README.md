# SuchMCP

**Your coding agent can write the code. It should also be able to find the file.**

SuchMCP is the MCP bridge for Such.

It gives Codex, Claude, and other MCP clients direct access to the same local search runtime used by Such, without dragging the search backend into the MCP repository.

Small server. Small surface. Fast lookup.

## Tools

SuchMCP exposes tools for things like:

- searching files
- listing search roots
- changing the search root
- adding a search root
- reindexing
- reading runtime status
- pinning and indexing state

It runs over **STDIO MCP**, so one server works cleanly with local coding agents.

## Architecture

```text
Codex / Claude
      |
   SuchMCP
      |
 RuntimeClient
      |
 stable Such ABI
```

The production search implementation is not included here.

That separation is deliberate.

## Why a separate repository?

Because the MCP protocol should be allowed to change without turning the main Such repository into a connector warehouse.

Such searches files.  
SuchMCP lets agents ask Such to search files.

Simple boundary. Less mess.

## Building

See [`BUILDING.md`](BUILDING.md).

## About

SuchMCP is developed by **Heritage Inc.** for Such.
