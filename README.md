[![Build](https://github.com/Retsumdk/feature-flag-service/workflows/CI/badge.svg)](https://github.com/Retsumdk/feature-flag-service/actions)
[![TypeScript](https://img.shields.io/badge/typescript-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/node.js-20-green?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org/)
[![MIT License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)

# Feature Flag Service

[![CI](https://github.com/Retsumdk/feature-flag-service/workflows/CI/badge.svg)](https://github.com/Retsumdk/feature-flag-service/actions)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.3-blue.svg)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-20.x-brightgreen.svg)](https://nodejs.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Feature flag toggle system with percentage rollouts. Control feature releases with gradual rollouts, A/B testing, and real-time toggles.

## Features

- **Gradual Rollouts** — Release features to a percentage of users
- **A/B Testing** — Test multiple variants with different user segments
- **Real-time Toggles** — Enable/disable features without redeployment
- **User Targeting** — Target specific users, roles, or regions
- **Audit Trail** — Track all flag changes with timestamps and actors

## Installation

```bash
git clone https://github.com/Retsumdk/feature-flag-service.git
cd feature-flag-service
npm install
npm run build
```

## Quick Start

```typescript
import { FeatureFlagService } from './src';

const flags = new FeatureFlagService();

// Define a feature flag
flags.define('new-checkout', {
  enabled: true,
  rolloutPercentage: 25,  // 25% of users
});

// Check if feature is enabled for user
const isEnabled = await flags.isEnabled('new-checkout', { userId: 'user123' });
```

## Related Repos

- [audit-logger](https://github.com/Retsumdk/audit-logger) — Immutable audit trail for flag changes
- [api-key-manager](https://github.com/Retsumdk/api-key-manager) — API key management
- [rate-limiter-middleware](https://github.com/Retsumdk/rate-limiter-middleware) — Rate limiting

## License

MIT License — see [LICENSE](LICENSE)
