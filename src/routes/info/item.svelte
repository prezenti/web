<script>
	import { slide } from "svelte/transition";
	export let entry
	let isOpen = false 
	const toggle = () => isOpen = !isOpen
</script>
<style>
	div {border: none; background: none;display:block; color: inherit;  cursor: pointer; margin: 0; padding-bottom: 0.5em; padding-top: 0.5em}
    li {        
        font-family: 'Roboto', sans-serif;
    }
	span {
		text-align: center !important;
        align-items: center !important;
		justify-content: center !important;
		font-family: 'Roboto', sans-serif;
	}

	svg { transition: transform 0.2s ease-in;
	}
	
	[aria-expanded=true] svg { transform: rotate(0.25turn); }
</style>
<div on:click={toggle} aria-expanded={isOpen}><span><svg style="tran"  width="20" height="20" fill="none" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" stroke="currentColor"><path d="M9 5l7 7-7 7"></path></svg> </span><span>{entry[0]}</span> </div>
{#if isOpen}
<ul transition:slide={{ duration: 300 }}>
	{#each entry[1] as item}
    {#if item == "\n"}
    <br/>
    {:else}
	<li>{item}</li>
    {/if}
	{/each}
</ul>
{/if}