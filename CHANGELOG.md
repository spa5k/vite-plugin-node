# 0.0.14

---

Start from this patch, this plugin will use the vite http server instead of create its own.

**Breaking Changes!**

- config option `handler` renamed to `adapter`
- removed `server` config options, now you can just use vite server options, see [vite doc](https://vitejs.dev/config/#server-host)

# 0.0.13

---

fastify: use fatify.routing to handle incoming request

# 0.0.12

---

Support async app

# 0.0.11

---

- code refactor for framework adapters. move out the http server from the adapter.
- now support to customize the export name of your app
  **Breaking Changes**
  plugin config updated. Please take a look and update your config.

# 0.0.10

---

add fastify support!

# 0.0.9

---

I re-implemented how this plugin works internally. Previously, this plugin relay on vite dev server HMR signals to restart the server, which is too slow. In this new version, the app is loaded on each request and the http server is always running.

**Breaking Changes**

- the named exported required from your entry renamed from `createViteNodeApp` to `viteNodeApp`
  **Updates**
- update readme.md with new How? section
- add koa as builtin supported framework
- update usages section in readme.md
- add examples for all the supported framework
