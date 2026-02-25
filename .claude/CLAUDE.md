# Presentation codebase rules

## content.yaml is the source of truth
`content.yaml` describes the structure and content of every slide. When making changes to `index.html` slides, always update `content.yaml` to reflect the current state. Read it before making changes to understand slide structure.

## CSS animation + transform conflict
Never use `transform` for positioning (e.g. `translate(-50%, -50%)`) on elements that receive CSS animations which set `transform`. The animation's `transform` overwrites the positioning transform entirely. Instead use `inset: 0` + flexbox (`justify-content: center; align-items: center`) for centering animated elements.
