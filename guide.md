# React + TypeScript + Vite

## Table of Contents

- [About](#about)
- [Features](#features)
- [Tutorial](#tutorial)
  - [Vite](#vite)
  - [Prettier](#prettier)
  - [ESLint + Prettier](#eslint--prettier)
  - [ESLint + React](#eslint--react)
  - [ESLint + TypeScript](#eslint--typescript)
  - [Check Updates](#check-updates)
- [Links](#links)
- [References](#references)

## About

This is a starter template for React + TypeScript + Vite.

> Once you have cloned this template, you can delete this file.

## Features

- Vite
- React
- TypeScript
- ESLint
- Prettier

## Tutorial

### Vite

```bash
npm create vite@latest

npm install
```

---

### Prettier

```bash
npm install --save-dev --save-exact prettier

echo {} > .prettierrc.json
```

`package.json`

```json
"scripts": {
  // ... previous scripts
  "format": "prettier --write \"src/**/*.{js,jsx}\""
}
```

---

### ESLint + Prettier

```bash
npm install -D eslint eslint-config-prettier
```

`.eslintrc.json`

```json
{
  "extends": ["eslint:recommended", "prettier"],
  "plugins": [],
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module",
    "ecmaFeatures": {
      "jsx": true
    }
  },
  "env": {
    "es6": true,
    "browser": true,
    "node": true
  }
}
```

`package.json`

```json
"scripts": {
  // ... previous scripts
  "lint": "eslint \"src/**/*.{js,jsx}\" --quiet"
}
```

---

### ESLint + React

```bash
npm install -D eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-react
```

`.eslintrc.json`

```json
{
  "extends": [
    "eslint:recommended",
    "plugin:import/errors",
    "plugin:react/recommended",
    "plugin:jsx-a11y/recommended",
    "prettier"
  ],
  "rules": {
    "react/prop-types": 0,
    "react/react-in-jsx-scope": 0
  },
  "plugins": ["react", "import", "jsx-a11y"],
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module",
    "ecmaFeatures": {
      "jsx": true
    }
  },
  "env": {
    "es6": true,
    "browser": true,
    "node": true
  },
  "settings": {
    "react": {
      "version": "detect"
    },
    "import/resolver": {
      "node": {
        "extensions": [".js", ".jsx"]
      }
    }
  }
}
```

---

### ESLint + TypeScript

```bash
npm install -D eslint-import-resolver-typescript @typescript-eslint/eslint-plugin @typescript-eslint/parser
```

`package.json`

```json
"scripts": {
  // ... previous scripts
  "format": "prettier --write \"src/**/*.{js,jsx,ts,tsx}\"",
  "lint": "eslint \"src/**/*.{js,jsx,ts,tsx}\" --quiet"
}
```

`.eslintrc.json`

```json
{
  "extends": [
    "eslint:recommended",
    "plugin:import/errors",
    "plugin:react/recommended",
    "plugin:jsx-a11y/recommended",
    "plugin:react-hooks/recommended",
    "plugin:@typescript-eslint/recommended",
    "plugin:@typescript-eslint/recommended-requiring-type-checking",
    "prettier"
  ],
  "rules": {
    "react/prop-types": 0,
    "react/react-in-jsx-scope": 0,
    "@typescript-eslint/no-empty-function": 0
  },
  "plugins": ["react", "import", "jsx-a11y", "@typescript-eslint"],
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module",
    "project": "./tsconfig.json",
    "ecmaFeatures": {
      "jsx": true
    }
  },
  "env": {
    "es6": true,
    "browser": true,
    "node": true
  },
  "settings": {
    "react": {
      "version": "detect"
    },
    "import/parsers": {
      "@typescript-eslint/parser": [".ts", ".tsx"]
    },
    "import/resolver": {
      "typescript": {
        "alwaysTryTypes": true
      }
    }
  }
}
```

### Check Updates

`npm-check-updates` upgrades your package.json dependencies to the latest versions, ignoring specified versions.

```bash
npm install -g npm-check-updates

ncu -u

npm install
```

## Links

- [Vite](https://vitejs.dev/)
- [Prettier](https://prettier.io/)
- [ESLint](https://eslint.org/)
- [TypeScript](https://www.typescriptlang.org/)
- [React](https://react.dev/)
- [npm-check-updates](https://www.npmjs.com/package/npm-check-updates)

## References

- [Complete Intro to React v8 and Intermediate React v5](https://react-v8.holt.courses/)
