# Building SuchMCP

SuchMCP is an independent public repository. It contains only the MCP STDIO server and the stable Such runtime client ABI.

```bash
scripts/build_linux.sh --clean
```

For production use, install the Such private runtime shared library beside `SuchMCP` or set `SUCH_RUNTIME_LIBRARY`.
