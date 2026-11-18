# openGym MERN Stack Migration Plan

This plan documents the migration path from openGym's current flat-file JSON and vanilla `node:http` stack to the **MERN Stack** (MongoDB, Express.js, React / React Native, Node.js).

The full technical specification and phased implementation roadmap is available in:
👉 **[docs/dev/MERN_MIGRATION_PLAN.md](docs/dev/MERN_MIGRATION_PLAN.md)**

---

## Quick Summary

* **Database**: MongoDB 7.x + Mongoose (replacing flat-file `./data/*.json`).
* **API Server**: Express.js 5.x (replacing vanilla `node:http` router map).
* **Mobile App**: React Native / Expo (replacing Capacitor WebView wrapper).
* **Domain Logic**: Extracted to shared monorepo package `@opengym/core` (retaining 100% of pure progression/1RM algorithms and unit tests).
* **Deployment**: Updated `docker-compose.yml` including MongoDB container and volume persistence.

For detailed schemas, Express router mappings, data migration scripts, and phase-by-phase implementation timelines, please refer to [docs/dev/MERN_MIGRATION_PLAN.md](docs/dev/MERN_MIGRATION_PLAN.md).
