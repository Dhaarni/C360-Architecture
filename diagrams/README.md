# TOYOTA C360 - ARCHITECTURE DIAGRAMS

This folder contains Mermaid diagram source code for the C360 custom build architecture.

## Available Diagrams

1. **01-HIGH-LEVEL-SYSTEM-ARCHITECTURE.mmd** - Complete system overview
2. **02-DATA-FLOW-ARCHITECTURE.mmd** - Data pipeline flows
3. **03-MICROSERVICES-ARCHITECTURE.mmd** - 6 core services + infrastructure
4. **04-DATA-LAYER-STORAGE.mmd** - Multi-tiered storage strategy
5. **05-DEPLOYMENT-INFRASTRUCTURE.mmd** - AWS cloud setup
6. **06-HA-DR-TOPOLOGY.mmd** - Multi-region failover

## How to Convert to PNG

### Option 1: Online (Easiest)
1. Go to: https://mermaid.live
2. Copy diagram source from .mmd file
3. Paste into left panel
4. Click Download → PNG
5. Select desired resolution

### Option 2: Using Mermaid CLI
```bash
# Install
npm install -g @mermaid-js/mermaid-cli

# Convert to PNG
mmdc -i 01-HIGH-LEVEL-SYSTEM-ARCHITECTURE.mmd -o 01-HIGH-LEVEL-SYSTEM-ARCHITECTURE.png --width 1920 --height 1080

# Convert to SVG
mmdc -i 01-HIGH-LEVEL-SYSTEM-ARCHITECTURE.mmd -o 01-HIGH-LEVEL-SYSTEM-ARCHITECTURE.svg
```

### Option 3: Batch Conversion
```bash
# Convert all diagrams
for file in *.mmd; do
  mmdc -i "$file" -o "${file%.mmd}.png" --width 1920 --height 1080
done
```

## Diagram Specifications

- **Format:** Mermaid syntax
- **Resolution:** 1920x1080+ recommended
- **Colors:** Pre-configured for clarity
- **Export:** PNG, SVG, PDF supported

## View Online

Paste any diagram code into: https://mermaid.live

## In GitHub

GitHub renders .md files with Mermaid blocks automatically if you name them with .mmd extension and use proper syntax.
