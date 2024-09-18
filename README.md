# notion-sv

Render Notion markdown representation using svelte 5 snippets!


## Intended use:
```svelte
<h1>{page.title}</h1>
<RenderNotion ignore-unmarked {blocks}>
{#snippet heading(importance, richText)}
{#if importance == 1}
<h1>{@render richText()}</h1>
{:else if importance == 2}
<h2>{@render richText()}</h2>
{:else if importance == 3}
<h3>{@render richText()}</h3>
{/if}
{/snippet}
</RenderNotion>
```