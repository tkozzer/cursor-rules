# Cursor Rules Repository

This is my personal collection of Cursor IDE configuration rules organized by technology stack and use case. I use these rules across my projects, and you can too through the [`cursor-rules-cli`](https://github.com/tkozzer/cursor-rules-cli) tool I'm developing.

## Repository Structure

```
cursor-rules/
├── README.md                           # This documentation
├── frontend/                           # Frontend technology rules
│   ├── react/                         # React-specific rules
│   ├── vue/                           # Vue.js-specific rules
│   └── general/                       # General frontend rules
├── backend/                            # Backend technology rules
│   ├── rust/                          # Rust-specific rules
│   ├── python/                        # Python-specific rules
│   └── node/                          # Node.js-specific rules
├── devops/                             # DevOps and tooling rules
├── quick-add/                          # Manifest files for bulk operations
└── QUICK_ADD_ALL.txt                   # Special manifest for all rules
```

## Usage with cursor-rules-cli

### Quick Add Functionality

Use my [`cursor-rules-cli`](https://github.com/tkozzer/cursor-rules-cli) tool to quickly add rule collections from this repository:

```bash
# List available manifests
cursor-rules --owner tkozzer quick-add nonexistent

# Add a fullstack React setup
cursor-rules --owner tkozzer quick-add fullstack-react

# Preview changes with dry-run
cursor-rules --dry-run --owner tkozzer quick-add backend-rust

# Force add with confirmation
cursor-rules --owner tkozzer quick-add frontend-only --force
```

### Available Manifest Collections

- **fullstack-react** - Complete React + Node.js development stack
- **fullstack-vue** - Complete Vue.js + Node.js development stack  
- **backend-rust** - Rust backend development with async programming
- **frontend-only** - Frontend-focused rules (React, Vue, HTML, CSS)
- **devops-complete** - Comprehensive DevOps and infrastructure rules
- **starter-pack** - Essential rules for getting started

### Special Manifests

- **QUICK_ADD_ALL.txt** - Adds all available rules for comprehensive setup

## Rule Categories

### Frontend Rules
- **React**: Core React development, hooks, and Tailwind integration
- **Vue**: Vue.js core and composition API patterns
- **General**: HTML best practices and modern CSS techniques

### Backend Rules
- **Rust**: General Rust practices, Actix-web, and async programming
- **Python**: General Python, FastAPI, and Django development
- **Node.js**: General Node.js, Express, and TypeScript integration

### DevOps Rules
- **Docker**: Container best practices and optimization
- **Kubernetes**: Container orchestration and deployment
- **CI/CD**: Continuous integration and deployment workflows

## File Formats

This repository supports multiple manifest formats:

- **`.txt`** - Simple line-based format with comments
- **`.yaml/.yml`** - Structured YAML with metadata
- **`.json`** - JSON format with name, description, and rules array

## Testing Features

This repository includes comprehensive testing scenarios:

- **Priority Resolution**: Multiple formats for the same manifest name
- **Error Handling**: Invalid file references for testing CLI robustness
- **Validation**: Proper manifest structure and rule file validation
- **Coverage**: Small, medium, and large manifest collections

## License

MIT License - feel free to use these rules in your own projects! 