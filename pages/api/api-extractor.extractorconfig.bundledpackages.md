---
layout: page
navigation_source: api_nav
improve_this_button: false
---
<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@microsoft/api-extractor](./api-extractor.md) &gt; [ExtractorConfig](./api-extractor.extractorconfig.md) &gt; [bundledPackages](./api-extractor.extractorconfig.bundledpackages.md)

## ExtractorConfig.bundledPackages property

A list of NPM package names whose exports should be treated as part of this package.

<b>Signature:</b>

```typescript
readonly bundledPackages: string[];
```

## Remarks

For example, suppose that Webpack is used to generate a distributed bundle for the project `library1`<!-- -->, and another NPM package `library2` is embedded in this bundle. Some types from `library2` may become part of the exported API for `library1`<!-- -->, but by default API Extractor would generate a .d.ts rollup that explicitly imports `library2`<!-- -->. To avoid this, we can specify:

```js
  "bundledPackages": [ "library2" ],

```
This would direct API Extractor to embed those types directly in the .d.ts rollup, as if they had been local files for `library1`<!-- -->.
