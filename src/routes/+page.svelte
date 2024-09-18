<h1>Welcome to your library project</h1>
<p>Create your package using @sveltejs/package and preview/showcase your work with SvelteKit</p>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>


<h1>{page.title}</h1>
<RenderNotion ignore-unmarked {blocks} getChildren={id => fetchBlockFromYourAPI(id)}>
{#snippet heading(importance, richText)}
    {#if importance == 1}
        <h1>{@render richText()}</h1>
    {:else if importance == 2}
        <h2>{@render richText()}</h2>
    {:else if importance == 3}
        <h3>{@render richText()}</h3>
    {/if}
{/snippet}
{#snippet divider()}
<hr/>
{/snippet}
</RenderNotion>