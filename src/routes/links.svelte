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
    <a sveltekit:prefetch href="/">
        <Icon icon="mdi:arrow-left" />
    </a>
</div>

<div class="links">
    <a sveltekit:prefetch href="/info">Info.</a>
	<a sveltekit:prefetch href="/">Apply.</a>
    <a sveltekit:prefetch href="/">Applications.</a>
    <a sveltekit:prefetch href="/tx">Tx's.</a>
    <a sveltekit:prefetch href="/about-us">Who are we.</a>
    <a sveltekit:prefetch href="/history">History.</a>
</div>

</section>

<style>
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

    .corner {
        padding:5%;
		width: 1rem;
		height: 1rem;
	}

    .corner a {
        color:var(--tertiary-color);
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
