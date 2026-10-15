# apowerb Local Tool Index

Comprehensive index of all tool modules in the apowerb repository (1,061 files total). Each module is a reusable agent tool with documented capabilities.

## Tool Modules by Category

### 1. Google Workspace
| Module | Description |
|--------|-------------|
| `google_drive` | List, search, read, download files |
| `google_gmail` | List, search, read, send emails |
| `google_calendar` | List, search, create events |
| `google_sheets` | Get spreadsheet info, read, write cells |
| `google_docs` | Create, read, append to documents |

### 2. Microsoft 365
| Module | Description |
|--------|-------------|
| `outlook_mail` | List, search, read, send emails, list folders, download attachments |
| `onedrive_read` | Read files from OneDrive |
| `onedrive_write` | List, search, read, download, upload, update files, create folders, delete, shared files |
| `teams` | List chats, get/send messages, reply, search, create group chats, list members |
| `sharepoint` | Find sites, browse and search document libraries, read files (text, CSV, Excel, Word, PDF) — read-only, `Sites.Read.All` |

### 3. GitHub
| Module | Description |
|--------|-------------|
| `github` | List repositories, read files, search code, read pull requests, index repository docs |

### 4. CRM / Business Apps
| Module | Description |
|--------|-------------|
| `hubspot` | HubSpot contacts and deals |
| `marketing` | HubSpot marketing leads |
| `pipedrive` | Create and search Pipedrive deals and people |
| `odoo` | Search, read, create and update Odoo records |
| `datadog` | Send application logs to Datadog |

### 5. Database & Data
| Module | Description |
|--------|-------------|
| `database` | Generic database queries, SQL execution |
| `database_mcp` | Generic database queries, SQL execution (MCP) |
| `oracle` | Read-only SQL on Oracle Database (single SELECT/WITH, read-only transaction), list tables |
| `mongodb` | List collections, find, count and aggregate documents — read-only (`$out`/`$merge` refused) |
| `text_to_sql` | Natural language to SQL, schema introspection |
| `db_to_rag` | Index database query results into RAG |
| `data_handler` | Data filtering, aggregation, transformation |
| `business_intelligence` | Charts, dashboards and datasets |
| `bi_datasets` | Charts, dashboards and datasets |

### 6. RAG & Knowledge
| Module | Description |
|--------|-------------|
| `rag` | Create, list, search, delete knowledge bases |
| `memory` | Save/search user memory, tool usage patterns |
| `ocr` | Extract text (markdown) from documents and images |

### 7. Communication
| Module | Description |
|--------|-------------|
| `emailing` | Send emails (SMTP) |
| `audio` | Speech-to-text, text-to-speech, audio analysis and generation |

### 8. Utilities
| Module | Description |
|--------|-------------|
| `basic` | Read files, data loader, image conversion, bearer tokens |
| `api_call` | Generic API calls, Thaink² forecast |
| `python_script` | Run Python in a confined subprocess |
| `image_generation` | Generate images (multi-provider) |
| `s3_tools` | Read S3 PDFs, search S3 files |
| `visualization` | Chart generation, CSV to chart export |
| `web_search_mcp` | Web search via MCP |
| `thaink2` | Custom Thaink² RAG tools |

### 9. Skills & Workflows
| Module | Description |
|--------|-------------|
| `skill_manager` | Skill registry management |
| `workflow_trigger_store` | Workflow trigger store |
| `workflow_store` | Workflow storage and management |
| `superagents` | Templates composing several agents |

### 10. Agent Infrastructure
| Module | Description |
|--------|-------------|
| `agent_manager` | Agent management (create, list, reload, status, template resync, run) |
| `run_store` | Agent run history storage |
| `workflow_defs` | Workflow definitions |
| `workflow_triggers` | Workflow triggers |
| `workflows` | Workflow routing |
| `tools.py` | Tool registry and per-agent tool configuration |

### 11. Integrations
| Module | Description |
|--------|-------------|
| `integration_status.py` | Integration status tracking |
| `webhook_handlers/` | Gmail webhook, Outlook webhook, Slack webhook |
| `jev_client.py` | Jev demo MCP client |

### 12. Scheduler / Orchestration
| Module | Description |
|--------|-------------|
| `scheduler/` | Scheduled runs via th2etl/mage orchestrator |
| `run_gate.py` | Admission control for runs |
| `history_compaction.py` | Conversation trimming |
| `run_main.py` | Main agent execution loop |

### 13. Core / Foundation
| Module | Description |
|--------|-------------|
| `adk_runner.py` | ADK (Agent Development Kit) execution |
| `adk_agent_builder.py` | Agent Python file generation |
| `guardrails.py` | Input/output guardrails |
| `run_gate.py` | Admission control for runs |
| `history_compaction.py` | Conversation trimming |
| `agent_main.py` | Main agent entry point |
| `agent_seeds.py` | Agent seed data |
| `agent_runtime_sync.py` | Agent runtime synchronization |
| `supervision` | Session list and session trace for audit |
| `sessions` | Session management |

### 14. Security & Auth
| Module | Description |
|--------|-------------|
| `auth/` | Email/password login, JWT dependencies, session cut-off |
| `middleware/` | Request middleware |
| `security.py` | Security helpers |
| `encryption` | Encryption for API keys, tokens, sensitive data |

### 15. Storage
| Module | Description |
|--------|-------------|
| `storage/` | Local and S3 storage abstraction |
| `s3_tools.py` | S3 read/write utilities |

### 16. Misc
| Module | Description |
|--------|-------------|
| `artifacts/` | Artifact storage and execution |
| `bi/` | BI — charts, dashboards, datasets |
| `chart_refresh_router.py` | Chart refresh routing |
| `forecast_*.py` | Forecasting modules (outlook, telemetry) |
| `data_lake/` | Data lake abstraction |
| `notification_bus.py` | Notification bus |
| `user_migration.py` | User migration |

## Summary Statistics
- **Total files:** 1,061
- **Tool modules (portfolio):** 31
- **Core modules:** ~50+ (ADK, agents, workflows, RAG, storage, security)
- **Integrations:** 6+ (Google, Microsoft, GitHub, Slack, S3, Thaink2)
- **Languages:** Python (primary), MCP (JSON configs)

## Notes
- All modules are documented in the README and source code
- The framework supports FastAPI + Google ADK + LiteLLM multi-model compatibility
- Built on Docker Compose for local deployment with PostgreSQL
- Open-source core (Apache 2.0); thaink² sells additional commercial bricks
