# Case Study: AI & Democracy Threat Map

**Client:** P4Dem (People for Democracy)  
**Role:** Lead Engineer / Technical Lead  
**Timeline:** 2025–2026  
**Stack:** Astro, TypeScript, React, D3.js, Tailwind CSS, Bun, Python

## Overview

The AI & Democracy Threat Map is an interactive visualization platform that maps academic literature on AI threats and opportunities to democratic institutions. It transforms structured research data into an explorable, filterable interface designed for policy researchers, advocates, and the public.

## Problem

P4Dem needed to make a growing literature review accessible and navigable. Static spreadsheets and documents made it difficult for users to discover patterns across harms, mechanisms, and democratic aspects. The challenge was to visualize complex relationships while keeping the interface fast, accessible, and maintainable.

## Solution

Built an Astro-based single-page application with:

- **Interactive map visualizations** (bubble maps, bipartite views, pathway diagrams) using D3.js
- **Filterable data table** with multi-select facets for aspects, harms, mechanisms, and domains
- **Responsive design** with Tailwind CSS v4 and accessible UI components
- **Data pipeline** (Python + CSV → JSON) to preprocess and validate research taxonomy
- **Static site deployment** to GitHub Pages for simple, reliable hosting

## Technical Highlights

- **Performance:** Static generation via Astro, lazy-loaded components, optimized bundles
- **Data integrity:** Python preprocessing with validation and tests (40 tests passing)
- **Type safety:** Full TypeScript coverage with strict checking
- **Accessibility & UX:** ARIA labels, keyboard navigation, responsive layouts
- **DevOps:** Bun for fast installs/builds, automated builds, GitHub Pages staging/production

## Results

- Clean, searchable interface for exploring 100s of literature entries
- Improved discoverability of cross-cutting patterns (harms ↔ democratic mechanisms)
- Maintainable data pipeline enabling non-technical updates via CSV
- Deployed to production at p4dem.github.io/ai-democracy-map

## Links

- Production: https://p4dem.github.io/ai-democracy-map/
- Staging: https://nashthecoder.github.io/ai-democracy-map-dev/
