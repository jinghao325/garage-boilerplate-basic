# Firestore Schema

## Overview

All collections use the typed collection pattern. Type definitions are stored in
`frontend/src/types/firestore.ts`, typed collection exports are stored in
`frontend/src/lib/firebase/firestore.ts`, and security rules are stored in
`firebase/firestore.rules`.

## Schema versioning

Every document in every collection must include a `_schemaVersion` field:

```typescript
_schemaVersion: 1