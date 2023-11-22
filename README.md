# README

## Setup

```sh
pnpm i @yandongxu/tsconfig -D
```

## Usage

**tsconfig.app.json**

```json
{
  "extends": "@yandongxu/tsconfig/web/tsconfig.json",
  "include": ["env.d.ts", "src/**/*", "src/**/*.tsx", "src/**/*.vue"],
  "exclude": ["src/**/__tests__/*"],
  "compilerOptions": {
    "composite": true,
    "noImplicitAny": false,
    "baseUrl": ".",
    "paths": {
      "@/*": ["./src/*"]
    }
  }
}
```

**tsconfig.node.json**

```json
{
  "extends": "@yandongxu/tsconfig/node/tsconfig.json",
  "include": ["vite.config.*", "vitest.config.*", "playwright.config.*"],
  "compilerOptions": {
    "composite": true,
    "module": "ESNext",
    "moduleResolution": "Bundler",
    "types": ["node"]
  }
}
```
