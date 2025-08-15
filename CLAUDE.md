# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Development Commands
- Start dev server: `pnpm dev` (runs on port 3030)
- Build slides: `pnpm build`
- Export slides: `pnpm export`

## Key Files
- `slides.md`: Main slide content (Markdown with Slidev extensions)
- `package.json`: Contains all project dependencies and scripts

## Architecture
- Slidev-based presentation system
- Supports Markdown with extended syntax (Mermaid diagrams, LaTeX, etc.)
- Uses Vite for fast hot-reloading development

## Important Notes
- All slide content is in `slides.md`
- Custom components can be added in `components/`
- Theme configurations in `styles/`