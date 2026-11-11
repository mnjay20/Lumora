# Lumora

Lumora is an interactive AI-powered gaming universe combining a Godot client, real-time backend services, and Lumi AI orchestrator.

## Architecture & Project Structure

```text
lumora/
│
├── README.md
├── CONTRIBUTING.md
├── LICENSE
├── .gitignore
├── .editorconfig
├── .env.example
├── docker-compose.yml
│
├── apps/
│   │
│   └── game/                      # Godot Game Client
│       │
│       ├── project.godot
│       │
│       ├── assets/
│       │   ├── sprites/
│       │   ├── characters/
│       │   ├── environments/
│       │   ├── tilesets/
│       │   ├── animations/
│       │   ├── audio/
│       │   ├── fonts/
│       │   └── ui/
│       │
│       ├── scenes/
│       │   ├── main/
│       │   ├── intro_world/
│       │   ├── campfire/
│       │   ├── minigames/
│       │   ├── teleportation/
│       │   └── ui/
│       │
│       ├── scripts/
│       │   ├── core/
│       │   ├── player/
│       │   ├── world/
│       │   ├── interactions/
│       │   ├── minigames/
│       │   ├── dialogue/
│       │   ├── api/
│       │   ├── persistence/
│       │   └── ui/
│       │
│       ├── systems/
│       │   ├── game_state/
│       │   ├── save_system/
│       │   ├── local_storage/
│       │   ├── sync_manager/
│       │   └── audio_manager/
│       │
│       ├── shaders/
│       ├── resources/
│       └── tests/
│
│
├── services/
│   │
│   ├── backend/                   # Backend Service
│   │   │
│   │   ├── src/
│   │   │   ├── main.py
│   │   │   │
│   │   │   ├── config/
│   │   │   ├── core/
│   │   │   ├── api/
│   │   │   │   └── v1/
│   │   │   │       ├── auth/
│   │   │   │       ├── players/
│   │   │   │       ├── game_state/
│   │   │   │       ├── conversations/
│   │   │   │       └── sync/
│   │   │   │
│   │   │   ├── models/
│   │   │   ├── schemas/
│   │   │   ├── repositories/
│   │   │   ├── services/
│   │   │   ├── middleware/
│   │   │   └── utils/
│   │   │
│   │   ├── migrations/
│   │   ├── tests/
│   │   ├── requirements.txt
│   │   └── Dockerfile
│   │
│   │
│   └── ai/                        # Lumi AI Service
│       │
│       ├── src/
│       │   ├── main.py
│       │   │
│       │   ├── agent/
│       │   │   ├── lumi.py
│       │   │   ├── orchestrator.py
│       │   │   ├── prompts/
│       │   │   └── guardrails/
│       │   │
│       │   ├── conversation/
│       │   │   ├── pipeline.py
│       │   │   ├── context_builder.py
│       │   │   ├── dialogue_manager.py
│       │   │   └── response_generator.py
│       │   │
│       │   ├── memory/
│       │   │   ├── short_term/
│       │   │   ├── episodic/
│       │   │   ├── long_term/
│       │   │   ├── retrieval/
│       │   │   ├── embeddings/
│       │   │   └── memory_manager.py
│       │   │
│       │   ├── llm/
│       │   │   ├── providers/
│       │   │   ├── model_router.py
│       │   │   └── inference.py
│       │   │
│       │   ├── personalization/
│       │   ├── evaluation/
│       │   ├── schemas/
│       │   └── utils/
│       │
│       ├── prompts/
│       ├── tests/
│       ├── requirements.txt
│       └── Dockerfile
│
│
├── packages/                      # Shared Components
│   │
│   ├── contracts/
│   │   ├── api/
│   │   ├── events/
│   │   └── schemas/
│   │
│   └── shared-config/
│
│
├── infrastructure/
│   │
│   ├── docker/
│   ├── database/
│   │   ├── postgres/
│   │   └── initialization/
│   │
│   ├── deployment/
│   ├── monitoring/
│   └── scripts/
│
│
├── docs/
│   │
│   ├── architecture/
│   │   ├── high_level_architecture.md
│   │   ├── backend_architecture.md
│   │   ├── ai_architecture.md
│   │   └── game_architecture.md
│   │
│   ├── api/
│   ├── database/
│   ├── ai/
│   │   ├── memory_design.md
│   │   ├── conversation_pipeline.md
│   │   └── guardrails.md
│   │
│   ├── game_design/
│   │   ├── world_design.md
│   │   ├── game_mechanics.md
│   │   └── story.md
│   │
│   ├── decisions/                 # Architecture Decision Records
│   └── development/
│
│
└── .github/
    │
    ├── workflows/
    │   ├── backend-tests.yml
    │   ├── ai-tests.yml
    │   └── game-validation.yml
    │
    ├── ISSUE_TEMPLATE/
    └── PULL_REQUEST_TEMPLATE.md
```
