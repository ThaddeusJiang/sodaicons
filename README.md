# sodaicons

[![npm (scoped)](https://img.shields.io/npm/v/@sodaicons/react?style=for-the-badge)](https://www.npmjs.com/package/@sodaicons/react)

- [sodaicons](#sodaicons)
  - [React](#react)
  - [Double Color (aka Highlight Icons)](#double-color-aka-highlight-icons)
  - [How To Contribute](#how-to-contribute)
  - [Vue](#vue)
  - [License](#license)

## React

First, install `@sodaicons/react` from npm:

```sh
npm install @sodaicons/react
```

Now each icon can be imported individually as a React component:

```js
import { BeakerIcon } from '@sodaicons/react/solid'

function MyComponent() {
  return (
    <div>
      <BeakerIcon className="h-5 w-5 text-blue-500"/>
      <p>...</p>
    </div>
  )
}
```

The 24x24 outline icons can be imported from `@sodaicons/react/outline`, and the 20x20 solid icons can be imported from `@sodaicons/react/solid`.

Icons use an upper camel case naming convention and are always suffixed with the word `Icon`.

[Browse the full list of icon names on UNPKG &rarr;](https://unpkg.com/browse/@sodaicons/react/outline/)

## Double Color (aka Highlight Icons)

1. add `class="highlight"` to SVG

```diff
<svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" xmlns="http://www.w3.org/2000/svg">
  <path
+    class="highlight"
    fill-rule="evenodd" clip-rule="evenodd" d="..." />
  <path d="..." stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
</svg>
```

2. defined `.highlight`

```css
.highlight {
  stroke: #fc6d26;
}
```

Result:

![double-colors-sodaicons](./.github/double-colors-sodaicons.png)

## How To Contribute

1. copy your svg file to outline or solid folder.


2. build

```
yarn
yarn build
```

3. confirm

```
cd react/
yarn link

cd example/nextjs
yarn link "@sodaicons/react"
// confirm the icons
```

## Vue

<details>

*Note that this library currently only supports Vue 3.*

First, install `@sodaicons/vue` from npm:

```sh
npm install @sodaicons/vue
```

Now each icon can be imported individually as a Vue component:

```vue
<template>
  <div>
    <BeakerIcon class="h-5 w-5 text-blue-500"/>
    <p>...</p>
  </div>
</template>

<script>
import { BeakerIcon } from '@sodaicons/vue/solid'

export default {
  components: { BeakerIcon }
}
</script>
```

The 24x24 outline icons can be imported from `@sodaicons/vue/outline`, and the 20x20 solid icons can be imported from `@sodaicons/vue/solid`.

Icons use an upper camel case naming convention and are always suffixed with the word `Icon`.

[Browse the full list of icon names on UNPKG &rarr;](https://unpkg.com/browse/@sodaicons/vue/outline/)

</details>

## License

This library is MIT licensed.
