# openapi-demo

```
npx @docusaurus/init@next init docs classic
```

```
cd docs
```

```
yarn add docusaurus-plugin-openapi
```

```
plugins: [
  ["docusaurus-plugin-openapi", {
    openapiPath: require.resolve("./openapi.json"),
    proxy: {
      "/proxy": {
        target: "http://localhost:4000",
        pathRewrite: { "^/proxy": "" },
      },
    },
  }],
]
```


```
{
  to: "api/",
  activeBasePath: "api",
  label: "API",
  position: "left",
}
```