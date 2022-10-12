<script context="module" lang="ts">
	export const prerender = true;
	import { page } from '$app/stores';
    import Icon from '@iconify/svelte';

</script>


<svelte:head>
	<title>Links</title>
	<meta name="links" content="links to content" />
</svelte:head>
<section>

<div class="corner">
    <a class="corner-a" sveltekit:prefetch aria-label="Link to go back" href="/">
        <Icon icon="mdi:arrow-left" />
    </a>
</div>
<h1 aria-label="Links page" ></h1>

<div class="links">
    <a sveltekit:prefetch tabindex="0" aria-label="Link to information section" href="/info">Info.</a>
	<a sveltekit:prefetch tabindex="0" aria-label="Link to How-to-apply for a grant" href="/apply">Apply.</a>
    <a sveltekit:prefetch tabindex="0" aria-label="Link to grant applications" target="_blank" href="https://grants.prezenti.xyz">Grants.</a>
    <a sveltekit:prefetch tabindex="0" aria-label="Link to past Prezenti transactions" href="/tx">Transactions.</a>
    <a sveltekit:prefetch tabindex="0" aria-label="Link to about us section" href="/about-us">Who are we.</a>
    <a sveltekit:prefetch tabindex="0" aria-label="Link to the history of Prezenti" href="/history">History.</a>
</div>

</section>

<style>

    section {
            margin-bottom: 40px;
        }
	.links {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height:80vh;
	}

    a {
        text-decoration: none;
        font-size: 5rem;
        color: var(--secondary-color)
    }

    a:hover {
        color:black;
        opacity: 0.5;

    }

    .corner a {
        padding:5%;
		width: 1rem;
		height: 1rem;
        color:var(--text-color);
         }

    .corner {
        padding:5%;
		width: 1rem;
		height: 1rem;
	}

    .corner-a:hover {
        color:var(--text-color);
        opacity: 0.5;

    } 
    .corner img {
        width: 3rem;
        height: 3rem;
    }

    @media (max-width: 600px) {
        a {
            font-size: 4rem;
        }
    }

    @media (max-width: 400px) {
        a {
            font-size: 2.4rem;
        }
    }

    

	
</style>
