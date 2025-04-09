# Deployment Guide for ng-v19-mat-select-infinite-scroll

This document outlines the steps to deploy updates to this package on npm.

## Prerequisites

- Node.js and npm installed
- npm account (required for publishing)
- Access rights to the npm package

## Deployment Steps

### 1. Apply Your Changes

Make all necessary code changes to the library. Ensure that all tests pass:

```bash
npm run test
```

### 2. Update Package Version

Update the version number in both package.json files:

- `/package.json`
- `/projects/ng-mat-select-infinite-scroll/package.json`

Follow semantic versioning:
- MAJOR version for incompatible API changes
- MINOR version for added functionality in a backwards compatible manner
- PATCH version for backwards compatible bug fixes

### 3. Build the Package

Build the package for production:

```bash
npm run build
```

Or use the prepare script which runs the build:

```bash
npm run prepare
```

### 4. Navigate to the Distribution Directory

```bash
cd dist/ng-mat-select-infinite-scroll
```

### 5. Authenticate with npm

Check if you're already logged in:

```bash
npm whoami
```

If not logged in, authenticate with your npm account:

```bash
npm login
```

If you don't have an npm account, create one:

```bash
npm adduser
```

### 6. Publish to npm

```bash
npm publish
```

For a dry run (to test without actually publishing):

```bash
npm publish --dry-run
```

### 7. Verify Publication

After publishing, verify that the new version is available:

```bash
npm view ng-v19-mat-select-infinite-scroll versions
```

Visit the npm package page to confirm: https://www.npmjs.com/package/ng-v19-mat-select-infinite-scroll

## Troubleshooting

- If you get authentication errors, try `npm login` again
- If there's a version conflict, ensure you've incremented the version number correctly
- If the package fails to publish due to name conflicts, check that the package name is available

## Notes

- Make sure to push all changes and version updates to the GitHub repository
- Consider adding release notes or changelogs for significant updates
