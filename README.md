# amplify-rust-arm64-function-runtime-provider

[![npm version](https://img.shields.io/npm/v/amplify-rust-arm64-function-runtime-provider.svg?style=flat-square)](https://www.npmjs.org/package/amplify-rust-arm64-function-runtime-provider)

This [AWS Amplify plugin](https://docs.amplify.aws/cli/plugins/plugins/) provides the ability to develop ARM64 Lambda functions in Rust.

## Installation

To use this plugin, follow the instructions provided by AWS Amplify: https://docs.amplify.aws/cli/plugins/plugins/#plugin-installation

In particular,

```shell
npm install --global amplify-rust-arm64-function-runtime-provider
amplify plugin scan
```

## Usage

After installing this plugin, you will be able to create Lambda functions in Rust. An option for using the `Rust` runtime will be available when using commands like `amplify function add` or `amplidy api add` to create Lambda functions.

NOTE that to actually use the Rust runtime, you will need to install a Rust template provider, such as `amplify-rust-function-template-provider`.

Don't forget to add the following code below "Runtime" in CloudFormation JSON to deploy the Rust code to ARM64 environment.

```json
    "Architectures": [
        "arm64"
    ]
```
