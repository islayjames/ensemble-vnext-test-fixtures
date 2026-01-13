# Ensemble vNext Test Fixtures

Test fixtures and user stories for Ensemble vNext integration testing.

## Purpose

This repository provides standardized test fixtures and user stories for testing the Ensemble vNext workflow framework. It supports:

1. **Integration Testing** - Consistent project scenarios for testing hooks, skills, and agents
2. **A/B Testing** - Comparative testing of skill-assisted vs non-assisted workflows
3. **Regression Testing** - Stable fixtures to detect behavioral changes

## Directory Structure

```
ensemble-vnext-test-fixtures/
├── README.md
├── user-stories/           # Sample user stories for different tech stacks
│   ├── python-cli/         # Python CLI application scenarios
│   ├── flutter-widget/     # Flutter widget development scenarios
│   ├── typescript-validation/  # TypeScript validation scenarios
│   ├── fastapi-endpoint/   # FastAPI endpoint scenarios
│   └── pytest-tests/       # Pytest test scenarios
├── fixtures/               # Pre-configured project states
│   ├── empty-project/      # Bare project for initialization testing
│   └── pre-initialized/    # Project with .claude/ already configured
└── ab-tests/               # A/B test configurations
    ├── with-skill/         # Test cases using skill assistance
    └── without-skill/      # Baseline test cases without skills
```

## Usage

### User Stories

Each user story directory contains:
- `story.md` - The user story description
- `expected-output/` - Expected artifacts from successful execution
- `test-config.json` - Test configuration and success criteria

### Fixtures

Fixtures are complete project snapshots used to initialize test environments:
- `empty-project/` - Starting point for `/init-project` testing
- `pre-initialized/` - Starting point for `/create-prd`, `/create-trd` testing

### A/B Tests

A/B test directories enable comparative analysis:
- `with-skill/` - Test cases leveraging Ensemble skills
- `without-skill/` - Baseline cases for comparison

## Integration with Ensemble vNext

This repository is used by the Ensemble vNext test suite located at:
```
packages/core/hooks/*.test.js
packages/router/tests/
packages/permitter/tests/
```

## Contributing

When adding new fixtures or user stories:
1. Follow the existing directory structure
2. Include clear documentation in each scenario
3. Ensure fixtures are deterministic and reproducible

## License

MIT - See Ensemble vNext main repository for details.
