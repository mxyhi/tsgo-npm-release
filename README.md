# Unofficial NPM Package for TypeScript-Go

[中文文档](./README.zh-CN.md)

This package provides an unofficial NPM distribution of [Microsoft's TypeScript-Go](https://github.com/microsoft/typescript-go) project, which is a Go-based port of TypeScript.

## ⚠️ Important Notice

This is **NOT** an official package from the TypeScript team. It is published as a convenience for testing and evaluation purposes only. The TypeScript-Go project is still under active development and considered experimental.

Per [this discussion](https://github.com/microsoft/typescript-go/discussions/466), the official team currently has no plans to publish an NPM package as the project is still very incomplete.

## Why This Package Exists

This unofficial package allows developers to:

- Try TypeScript-Go without building from source
- Test integration with existing tooling
- Experiment with the Go-based TypeScript implementation

## Installation

```bash
npm install @mxyhi/tsgo
```

## Usage

This package provides the `tsgo` binary which functions similarly to `tsc`:

```bash
# Check a TypeScript file (similar to tsc)
npx tsgo tsc path/to/file.ts

# Use a tsconfig.json file
npx tsgo tsc --project path/to/tsconfig.json
```

For LSP (Language Server Protocol) usage, please refer to the [official repository](https://github.com/microsoft/typescript-go) for setup instructions.

## Build Schedule

The package is automatically built and published every 6 hours at 00:00, 06:00, 12:00, and 18:00 UTC. Each build includes the latest changes from the TypeScript-Go repository.

## Current Limitations

As noted in the official repository, TypeScript-Go is still a work in progress with many features incomplete. Current limitations include:

- Not all resolution modes are supported
- JavaScript-specific inference and JSDoc are not ready
- JSX support is not ready
- Declaration emit is not ready
- Emit (JS output) is in progress (only `target: esnext` is well-supported)
- Watch mode is prototype-only
- Build mode / project references are not ready
- Incremental build is not ready
- Language service (LSP) is prototype-only with minimal functionality

## Updates

This unofficial package will be updated periodically as significant progress is made in the TypeScript-Go repository. When the official team decides to publish an official package, this unofficial package will be deprecated in favor of the official one.

## Contributing

For issues related to TypeScript-Go itself, please file them in the [official repository](https://github.com/microsoft/typescript-go).

For issues specific to this NPM package distribution, please file them in <https://github.com/mxyhi/tsgo-npm-release>.

## License

The TypeScript project is licensed under the [Apache License 2.0](https://github.com/microsoft/typescript-go/blob/main/LICENSE).
