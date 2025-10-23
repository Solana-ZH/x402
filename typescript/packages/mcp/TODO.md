# @x402/mcp

## TODO

The `@x402/mcp` package implements **x402 payment flows over the Model Context Protocol (MCP)** using JSON-RPC messaging.

It wraps the `x402Client`, `x402Server`, and `x402Facilitator` classes to enable x402 payments within MCP request/response cycles — including tool calls, resource access, and initialization flows.

Payment requirements are signaled using JSON-RPC `error` responses with `code: 402`, containing a `PaymentRequirementsResponse` in `error.data`.  
Clients transmit payment payloads via the `_meta["x402/payment"]` field, and servers return settlement results in `_meta["x402/payment-response"]`.

---

**Note:** There are already several MCP-based x402 implementations in the wild.  
We are open to promoting one of these existing projects to become the **official reference SDK** implementation.
