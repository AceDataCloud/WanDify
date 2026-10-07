# Wan capability mapping

Compared with [MCPs at f0eed10abf31](https://github.com/AceDataCloud/MCPs/tree/f0eed10abf310824cb4c33d4944c63d3654ac95b/wan) and the public API contract at PlatformBackend `fa94598267a82545fb1afed6ee26bafd6cbb9ca7`.

The table maps service operations to Dify tools. Different MCP helper functions may use the same action selector or structured JSON input.

| MCP function | Dify equivalent | Notes |
|---|---|---|
| `wan_list_models` |  | Model/action selectors and the API reference; informational guidance does not submit a request. |
| `wan_list_resolutions` |  | Model/action selectors and the API reference; informational guidance does not submit a request. |
| `wan_list_actions` |  | Model/action selectors and the API reference; informational guidance does not submit a request. |
| `wan_get_task` | `wan_task_retrieve` | Set action=retrieve |
| `wan_get_tasks_batch` | `wan_tasks_retrieve_batch` | Set action=retrieve_batch |
| `wan_generate_video` | `wan_generate_video`, `wan3_generate` | Set action=text2video |
| `wan_generate_video_from_image` | `wan_generate_video`, `wan3_generate` | Set action=image2video |
| `wan_generate_video_all_in_one` | `wan_generate_video`, `wan3_generate` |  |

## Parameter equivalents

- `wan_get_tasks_batch`: `task_ids` → ids.

## Verification boundary

Contract examples and regression tests cover request validation, transport and task handling. Actual Dify browser cases are recorded separately in `tests/e2e-results.json` and `tests/e2e-audit.json` when available. A schema test is not a successful paid generation. Unsupported service availability and untested advanced combinations must not be described as passed.
