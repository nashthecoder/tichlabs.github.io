# Case Study: AI & Democracy Threat Map

**Client:** P4Dem (People for Democracy)  
**Role:** Lead Engineer / Technical Lead  
**Timeline:** 2025–2026  
**Stack:** Astro, TypeScript, React, D3.js, Tailwind CSS, Bun, Python  
**Live:** [p4dem.github.io/ai-democracy-map](https://p4dem.github.io/ai-democracy-map/)  
**Staging:** [nashthecoder.github.io/ai-democracy-map-dev](https://nashthecoder.github.io/ai-democracy-map-dev/)

## Overview

The AI & Democracy Threat Map is an interactive research visualization platform developed for [People for Democracy (P4Dem)](https://www.powerfordemocracies.org/). It maps the growing body of academic literature on AI's threats and opportunities for democratic institutions, turning a complex research taxonomy into an explorable, accessible interface for policy researchers, advocates, and the public.

## Problem

P4Dem's literature review on AI and democracy had grown into a large, structured dataset. In spreadsheet form, it was difficult to identify cross-cutting patterns between AI harms, mechanisms, and their impacts on democratic pillars. The core challenge was to make dense academic research navigable and visually intuitive without sacrificing accuracy or accessibility.

## Solution

Designed and built a performant, static-first web application with interactive data visualizations:

- **Interactive threat maps** – Custom D3.js visualizations (bubble maps, bipartite harm–mechanism views, and pathway diagrams) reveal relationships between technical mechanisms and democratic impacts.
- **Explorable data table** – Filterable, multi-faceted table enabling users to slice by democratic aspects, harms, mechanisms, domains, and more.
- **Responsive, accessible UI** – Built with Tailwind CSS v4, semantic HTML, ARIA labels, and keyboard navigation support.
- **Research-grade data pipeline** – Python preprocessing validates, normalizes, and transforms CSV research data into structured JSON with a strict schema (40 automated validation tests).
- **Static site architecture** – Astro SSG for near-instant loads, with React islands only where interactivity is needed.

## Technical Implementation

### Data Pipeline
- Python-based ingestion (`preprocessing/`) validates taxonomy consistency and prevents malformed entries
- Schema validation + pytest suite (40/40 passing) enforces data integrity before build
- CSV → normalized JSON workflow allows non-technical researchers to update content safely

### Frontend Architecture
- **Astro** for static site generation with minimal JavaScript footprint
- **TypeScript** throughout for type safety and maintainability
- **D3.js** for custom, interactive network/pathway visualizations
- **React + islands** for targeted interactivity (filters, dialogs, carousel)
- **Tailwind CSS v4** for utility-first, consistent styling aligned to P4Dem's visual identity

### Performance & Deployment
- Zero-cost hosting on GitHub Pages (staging + production environments)
- Sub-100ms client-side filtering on in-memory dataset
- Optimized builds with code-splitting and lazy-loaded visualizations
- TypeScript (`tsc --noEmit`) and Python tests run as quality gates

## Key Outcomes

- **Improved discoverability** – Users can explore relationships between AI mechanisms (e.g., disinformation, microtargeting, deepfakes) and democratic impacts (electoral integrity, deliberative trust, institutional legitimacy).
- **Research accessibility** – Translates academic taxonomy into an approachable public interface.
- **Maintainable & extensible** – CSV-driven content updates + automated validation reduce risk of data errors.
- **Production-grade quality** – Full type safety, 40 passing tests, clean builds, and dual-environment (staging/production) deployment workflow.

## Links

- [Live Site (Production)](https://p4dem.github.io/ai-democracy-map/)
- [Staging Environment](https://nashthecoder.github.io/ai-democracy-map-dev/)
- [P4Dem AI & Democracy Landscape](https://www.powerfordemocracies.org/research/our-research/ai-democracy-landscape/)
