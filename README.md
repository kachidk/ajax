# Pocketbase, Nextjs, and Capacitor Starter App

Create cross-platform Web, iOS, and Android apps from a single codebase.

Styled with [Shadcn](https://ui.shadcn.com/).

Can be deployed as a JAMstack using Pocketbase to serve static files.

## Guides

- [Live reload in simulator](https://capacitorjs.com/docs/guides/live-reload#using-with-framework-clis)

## Tips

- [Don't leak your keys](https://ionicframework.com/docs/troubleshooting/cors#dont-leak-your-keys):

  If you are trying to connect to a 3rd-party API, first check in its documentation that is safe to use it directly from the app (client-side) and that it won't leak any secret/private keys or credentials, as it's easy to see them in clear text in Javascript code. Many APIs don't support CORS on purpose, in order to force developers to use them in the server and protect important information or keys.

- To solve CORS errors for Native-only apps (iOS/Android):

  For Capacitor applications, use the [Capacitor HTTP API](https://capacitorjs.com/docs/apis/http). This API patches fetch and XMLHttpRequest to use native libraries. Please note that if you also deploy the application to a web-based context such as PWA or the local development server (via ionic serve for example) you still need to implement CORS for those scenarios.

- To solve CORS errors for Web apps:

  You need a server that adds the necessary [CORS headers](https://ionicframework.com/docs/troubleshooting/cors#a-enabling-cors-in-a-server-you-control) to the responses.
