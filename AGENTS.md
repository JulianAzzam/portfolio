# Project guide

This repository is a static personal portfolio. Open `index.html` in a browser to run it; there is no build step or package manager.

## Layout

- `index.html`: page content and markup for the sidebar, About, Resume, Portfolio, and Contact sections.
- `assets/css/style.css`: visual styles and responsive layout.
- `assets/js/script.js`: sidebar toggle, portfolio filtering, contact form validation, and page navigation.
- `assets/images/`: local image and icon assets.
- `index.txt`: source/reference text; the live page is `index.html`.

## Working on this project

- Keep the `data-*` hooks in `index.html` aligned with selectors in `assets/js/script.js` when changing interactive controls.
- Keep asset paths relative so the page works when opened directly and when served as a static site.
- Check the affected page section in a browser after changes, including narrow and wide viewports.
- The contact form currently uses `action="#"`; avoid describing it as a working message delivery service.
- Preserve unrelated working-tree changes, especially binary assets.

## Code Review Graph

The graph database is stored in `.code-review-graph/graph.db`. At the last build, Code Review Graph parsed `assets/js/script.js` and found 1 file, 2 function nodes, and 42 edges. HTML, CSS, images, and `AGENTS.md` are outside its parsed code graph, so inspect those files directly when relevant.

Start a graph-assisted task with `get_minimal_context_tool` for this repository. Run `build_or_update_graph_tool` after JavaScript changes, then use the graph query or review tools as needed. The graph is an aid to review, not a substitute for checking the page in a browser.
