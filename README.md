# Docusaurus 3.6.1 Peer Dependency Warnings Repro

This is a minimal reproducible example for the peer dependency warnings in Docusaurus 3.6.1.

## Steps to reproduce

- Clone this repository
- Ensure [yarn is available](https://yarnpkg.com/getting-started/install) (`corepack enable`)
- Run `yarn install`

See warnings:

```
➤ YN0002: │ @docusaurus/bundler@npm:3.6.1 [fb9bc] doesn't provide react (p61e2d), requested by @docusaurus/types
➤ YN0002: │ @docusaurus/bundler@npm:3.6.1 [fb9bc] doesn't provide react-dom (p19f9f), requested by @docusaurus/types
➤ YN0002: │ @docusaurus/plugin-content-blog@npm:3.6.1 [38fed] doesn't provide @mdx-js/react (p7dbc9), requested by @docusaurus/core
➤ YN0002: │ @docusaurus/plugin-content-docs@npm:3.6.1 [38fed] doesn't provide @mdx-js/react (p9f38b), requested by @docusaurus/core
➤ YN0002: │ @docusaurus/plugin-content-pages@npm:3.6.1 [38fed] doesn't provide @mdx-js/react (p77e7e), requested by @docusaurus/core
➤ YN0002: │ @docusaurus/plugin-debug@npm:3.6.1 [38fed] doesn't provide @mdx-js/react (p6f0af), requested by @docusaurus/core
➤ YN0002: │ @docusaurus/plugin-google-analytics@npm:3.6.1 [38fed] doesn't provide @mdx-js/react (p9f6c6), requested by @docusaurus/core
➤ YN0002: │ @docusaurus/plugin-google-gtag@npm:3.6.1 [38fed] doesn't provide @mdx-js/react (p7a09c), requested by @docusaurus/core
➤ YN0002: │ @docusaurus/plugin-google-tag-manager@npm:3.6.1 [38fed] doesn't provide @mdx-js/react (p0011e), requested by @docusaurus/core
➤ YN0002: │ @docusaurus/plugin-sitemap@npm:3.6.1 [38fed] doesn't provide @mdx-js/react (p93365), requested by @docusaurus/core
➤ YN0002: │ @docusaurus/preset-classic@npm:3.6.1 [e1d64] doesn't provide @mdx-js/react (p45d1a), requested by @docusaurus/core
➤ YN0002: │ @docusaurus/theme-search-algolia@npm:3.6.1 [38fed] doesn't provide @mdx-js/react (p4a912), requested by @docusaurus/core
➤ YN0002: │ @docusaurus/utils-common@npm:3.6.1 doesn't provide react (pc078f), requested by @docusaurus/types
➤ YN0002: │ @docusaurus/utils-common@npm:3.6.1 doesn't provide react-dom (p5bd66), requested by @docusaurus/types
➤ YN0002: │ @docusaurus/utils@npm:3.6.1 doesn't provide react (p8d75d), requested by @docusaurus/types
➤ YN0002: │ @docusaurus/utils@npm:3.6.1 doesn't provide react-dom (pb357f), requested by @docusaurus/types
```

Note: if you run a newer version of Yarn, it may not report all warnings on install. You can run 
`yarn explain peer-requirements` to see them manually.