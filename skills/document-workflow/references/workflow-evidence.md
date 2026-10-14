# Workflow evidence checklist

Use only the categories relevant to the traced flow.

| Boundary | Evidence to collect |
| --- | --- |
| Entry | Trigger, route/topic/job, owning handler, caller, authentication |
| Input | Parsing, defaults, validation, version or strategy differences |
| State | Reads, writes, transaction boundaries, cache interactions |
| Dependency | Target, call site, synchronous/asynchronous behavior, timeout and error handling |
| Continuation | Publisher, consumer, retry or duplicate handling, completion signal |
| Output | Final transport status, application result, acknowledgement, side effects |
| Failure | Origin, translation, recovery, and caller-visible or eventual outcome |

Track a source path and symbol for each material contract claim. Resolve constants where possible; label unresolved values rather than publishing synthetic routes. Keep final HTTP status separate from body status. Do not generalize one branch's behavior to every version or strategy.

Check that examples match the traced branch and that guide, contract, and diagram describe the same behavior. Record inaccessible downstream components as evidence gaps. Avoid filling absent retry, monitoring, or security configuration with assumed defaults.
