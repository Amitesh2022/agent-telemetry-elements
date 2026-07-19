# Agent Telemetry Elements

A portable Web Components observatory for monitoring autonomous workflow pressure, tool reliability, and intervention actions.

[Watch the running product demo](docs/demo.webm)

## Why this product matters

Agentic workflows can span tools, models, and product surfaces. Teams need reusable observability components that can be embedded wherever an operational decision is made.

## Intended users

- AI platform and reliability teams
- Frontend platform and design-system engineers
- Operations leaders supervising autonomous workflows

## Core workflows

- Review active agents and trace pulse
- Compare workload pressure across agent workflows
- Intervene in a pressured workflow
- Observe metrics update through reactive components

## Current capabilities

- Agent workflow telemetry and state labels
- Reusable Shadow DOM status cards
- Interactive intervention behavior
- Lifecycle-aware trace pulse
- Responsive standards-native component layout

## Lit technical highlights

- Lit 3 reactive elements
- Custom-element APIs compatible with any framework
- Reactive controller for trace pulse state
- Keyed repeat rendering
- Strict TypeScript and component tests

## Architecture and data flow

A top-level observatory element owns workflow state and renders reusable status elements. The pulse controller participates in the host lifecycle, while interaction events update workload pressure immutably.

## Accessibility and responsive behavior

The interface uses semantic headings, labelled regions, native interactive controls, visible status text in addition to color, keyboard-operable actions, and layouts that adapt to narrower screens. Automated tests cover the central state behavior; a production release should add continuous WCAG audits with assistive-technology review.

## Project structure

- src/my-element.ts — agent observatory element
- src/status-card.ts — portable metric card
- src/pulse-controller.ts — trace pulse behavior
- src/status-card.test.ts — custom-element tests
- docs/demo.webm — verified running UI

## Run locally

```bash
npm ci
npm test
npm run build
npm run dev
```

For Angular projects, `npm start` is also available for the development server.

## Verification

- Strict TypeScript compilation
- Automated component or state tests
- Production build
- Real-browser interaction check
- Demo-video playback and frame inspection

## Tradeoffs

The demo intentionally avoids external agent credentials and uses deterministic telemetry. Production implementation would add trace ingestion, tool-call correlation, cost and latency distributions, policy alerts, retention controls, and incident workflows.

## Roadmap

- OpenTelemetry-compatible trace ingestion
- Tool reliability and latency drill-downs
- Human-intervention event contracts
- Embeddable React, Vue, and Angular examples
