# 🚀🚀 Shopify App Template | Next.js | Typescript

This is an opinionated starter template for embedded Shopify apps. The biggest opinion is, that Typescript should be used everywhere and it's the only right opinion.

This Template utilizes Middleware and Next.js APIs for OAuth, so no custom server is needed.

Found a bug? Please create an issue! ❤️

Apps built with this template:

| <img src="https://cdn.shopify.com/app-store/listing_images/17bb7072fce41022eb1d956025f805d2/icon/CLCT5M3R9vgCEAE=.png?height=72&width=72" /> | [Manufactory](https://apps.shopify.com/manufactory-production) |
|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|

Want your app listed? Create a PR!

## Table of Contents

- 🤩 Features
- 👀 Requirements
- 🤓 Getting Started
- 🎣 Fetching Data
- 🧰 Built with
- ☕️ Buy me a coffee

## 🤩 Features

- 📝 TypeScript
- ⚡ Next.js - React Framework for static rendering
- ✨ Serverless Architecture
- 💳 App Subscriptions
- 💾 Session Storage with Redis
- 🚇 Ngrok for development
- 🪝 Webhook registration and persistance after server restart
- 🔑 Ready to use online and offline accesstokens simultaneously
- 🌐 App context set up. Can be used to store data, that only needs to be fetched once, but is needed in multiple places
- Request verification set up
- Link component to convert `<a>` tags to Next Links for relative paths
- Routepropagation set up
- Examples for creating and displaying of app subscriptions
- Loading screen while the app context is initializing


### 🦺 Typesafety

- [GraphQl Code Generator](https://www.graphql-code-generator.com) for the Shopify Admin API
- [tRPC](https://trpc.io) for end-to-end typesafe APIs

## 👀 Requirements

- Shopify Partner Account
- Shopify Dev Store
- Ngrok account
- Upstash Redis Database

## 🤓 Getting Started

- Click `Use this template` or [this link](https://github.com/carstenlebek/next-shopify-app/generate)
- Create an App in your Shopify Partner Account
  - Set https://localhost as the App Url for now
- Fill out your `.env` file
  - `SHOPIFY_API_KEY`: The Shopify Api key of the app, you have just created
  - `SHOPIFY_API_SECRET_KEY`: The Shopify Api secret key of the app, you have just created
  - `SCOPES`: The [access scopes](https://shopify.dev/api/usage/access-scopes) your app needs
  - `USE_OFFLINE_ACCESS_TOKEN`: Set to true, if you want to use offline accesstokens
  - `SHOP`: Your dev stores url
  - `NGROK_AUTH_TOKEN`: Your [Ngrok auth token](https://dashboard.ngrok.com/get-started/your-authtoken)
  - `UPSTASH_REDIS_REST_URL`: Your Upstash Redis REST url.
  - `UPSTASH_REDIS_REST_TOKEN`: Your Upstash Redis REST token.
- Run `pnpm install` or `npm install --force` (There is a peer dependency issue between React 18 and Polaris, but it works.)
- Run `npm run dev`
- Your apps ngrok url will be printed to the terminal
- Install the app to your dev store
- After you have completed auth, you can run `npm run get-schema` to generate the gql schema for the admin API, if you want to use a different version than `2022-07z`
- Run `npm run generate` in a seperate terminal to start the GraphQL code generator

## 🎣 Fetching Data

### Shopify Admin API

1. Start the GraphQL code generator with `npm run generate`
2. Create your Query/Mutation (examples in `src/graphql`)
3. Use the generated react-query hook to get your data (example in `src/pages/get-data.tsx` and `src/pages/subscriptions.tsx`)

### tRPC

1. Read the [tRPC docs](https://trpc.io/docs)
2. Hook up your DB ([Prisma](https://www.prisma.io) is a great addition to tRPC)
3. Define your tRPC router
4. Use the `trpc.useQuery()` hook to access your data

## 🧰 Built with

- [TypeScript](https://www.typescriptlang.org)
- [Next.js](https://nextjs.org/)
- [@shopify/shopify-api](https://github.com/Shopify/shopify-node-api)
- [tRPC](https://trpc.io)
- [React Query](https://react-query.tanstack.com)
- [GraphQL Code Generator](https://www.graphql-code-generator.com)

## ☕️ Buy me a coffee

Found this repo useful? Buy me a coffee to keep me awake 🤩

  [![BuyMeACoffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/carstenlebek) 

Made by [Carsten Lebek](https://clebek.dev)
