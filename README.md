# Animal Rescue CRUD API with Rust on Cloudflare Workers w/ Cloudflare KV

See [this blog post](https://blog.damianesteban.dev/blog/building-a-yoga-graphql-server-with-cloudflare-workers/) for more details.

This is a CRUD API. It is built with [Cloudflare Workers](https://workers.cloudflare.com/) and [Cloudflare KV](https://www.cloudflare.com/products/workers-kv/).

# Template: worker-rust

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/cloudflare/templates/tree/main/worker-rust)

A template for kick starting a Cloudflare worker project using [`workers-rs`](https://github.com/cloudflare/workers-rs).

This template is designed for compiling Rust to WebAssembly and publishing the resulting worker to Cloudflare's [edge infrastructure](https://www.cloudflare.com/network/).

## Setup

To create a `my-project` directory using this template, run:

```sh
$ npm init cloudflare my-project worker-rust
# or
$ yarn create cloudflare my-project worker-rust
# or
$ pnpm create cloudflare my-project worker-rust
```

> **Note:** Each command invokes [`create-cloudflare`](https://www.npmjs.com/package/create-cloudflare) for project creation.

## Usage

This template starts you off with a `src/lib.rs` file, acting as an entrypoint for requests hitting your Worker. Feel free to add more code in this file, or create Rust modules anywhere else for this project to use.

With `wrangler`, you can build, test, and deploy your Worker with the following commands:

```sh
# run your Worker in an ideal development workflow (with a local server, file watcher & more)
$ npm run dev

# deploy your Worker globally to the Cloudflare network (update your wrangler.toml file for configuration)
$ npm run deploy
```

Read the latest `worker` crate documentation here: https://docs.rs/worker

## WebAssembly

`workers-rs` (the Rust SDK for Cloudflare Workers used in this template) is meant to be executed as compiled WebAssembly, and as such so **must** all the code you write and depend upon. All crates and modules used in Rust-based Workers projects have to compile to the `wasm32-unknown-unknown` triple.

Read more about this on the [`workers-rs`](https://github.com/cloudflare/workers-rs) project README.

## Issues

If you have any problems with the `worker` crate, please open an issue on the upstream project issue tracker on the [`workers-rs` repository](https://github.com/cloudflare/workers-rs).
