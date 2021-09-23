# Inertia.js Svelte Adapter

Visit [inertiajs.com](https://inertiajs.com/) to learn more.

## We need more documentation, don't know where to post this

In the docs they show a great example of how to use a Layout and using the
`<script context="module">` it's possible to assing there not only the layout
but define other parts that can be presented in the main Layout, recently
we had a requirement that we needed to present a component at the top the layout
but we could not present it and I could not find a way in the documentation so I've read
the code and found about the store and have done this in the layout
```
<script>
...
import store from "@node_modules/@inertiajs/inertia-svelte/src/store"

...
</script>

{#if $store.component.banner}
  <svelte:component this={$store.component.banner} {...$$props} />
{/if}
```

and this fixed the problem, thanks for inertia it's a great tool
