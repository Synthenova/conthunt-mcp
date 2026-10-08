# ContHunt MCP capability map

The SQL update has thirteen tools. Advertised schemas establish what your connection actually supports.

| Tool | Action |
| --- | --- |
| whoami | Account, plan and remaining credits. |
| query_saved_data | Read-only, authenticated saved SQL; read [the SQL reference](query-saved-data.md) first. |
| search | Start keyword discovery; SQL reads persisted results. |
| deep_search | Start, inspect, steer or follow up in a persistent specialist conversation. |
| analyze_video | Start short-video full/fine-grained analysis; SQL reads evidence. |
| analyze_long_video | Start one long-video objective or get the exact native run. |
| creator | Live profile or paginated creator videos. |
| video | Save platform URLs. |
| boards | Create/delete/add/remove; SQL reads saved details/membership. |
| insights | Explicit board refresh; SQL reads saved cache/freshness. |
| files | List/read/download real report files in an owned chat. |
| download | Obtain authorized media access. |
| trending | Platform/niche trends. |

No separate SearchAgent, schema, saved getter or SQL write tool is required.

`deep_search(prompt=objective)` starts work and returns the owning chat plus a separate native thread/execution. `deep_search(thread_id=returned_thread)` inspects; adding a prompt steers active work or follows up after completion. An execution selector reads a particular attempt. Do not treat acceptance as consumed/completed or start again because the observation timed out.

Long-video `start` takes a supported video URL or saved asset plus objective/questions. `get` takes only the existing asset and native run ID, with no URL or start-only inputs. Pending, failed and unavailable are not completed answers. Use the returned owning chat to link the exact saved video in your answer.

For retry keys, search uses a UUID request_id; specialist keys use 1–200 safe letters/digits/underscores/hyphens. Preserve the original key/input. Read-only calls and file reads need no new admission.
