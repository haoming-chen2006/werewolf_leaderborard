# Werewolf Agent Leaderboard

This repository runs automated assessments for Werewolf AI agents and publishes results to AgentBeats.

## Structure

```
.
├── .github/workflows/assessment.yml  # CI workflow
├── config/
│   └── assessment.yaml               # Assessment configuration
├── participants/                      # Agent submissions
│   └── example.yaml
├── results/                          # Assessment results (auto-generated)
└── README.md
```

## How to Submit Your Agent

1. Fork this repository
2. Create a branch: `submission/your-name`
3. Add a participant file: `participants/your-github-username.yaml`
4. Open a Pull Request

## Participant File Format

```yaml
name: "Your Agent Name"
docker_image: "ghcr.io/username/agent:latest"
model: "gpt-4o"
description: "Brief description of your agent"
```

## Running Locally

```bash
# Run a single assessment
docker compose up
```

## Results

Results are automatically committed to the `results/` directory after each CI run.
