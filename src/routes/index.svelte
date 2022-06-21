<script context="module" lang="ts">
	import { circOut } from "svelte/easing";
	import { OnMount } from 'fractils'
	export const prerender = true;
	function customTransition() {
    return {
      css: (t) => {
        return `
        transform: scale(${t});
        `;
      },
      easing: circOut,
      duration: 2000,
	  delay:100,
	  init: true
    };
  };
</script>


<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<OnMount>
	<section>

		<a  sveltekit:prefetch href="/links">
		<img in:customTransition src="prezenti-logo.svg" alt="Welcome" />

		<h1>
			Prezenti
		</h1>
	</a>

	</section>
</OnMount>

<style>

	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height:90vh;
		width:100vw;
	}

	img {
		max-width: 375px;
	}

	h1 {
		width: 100%;
		font-size:5rem ;
		margin:0;
		padding:0;
	}


	a {
		text-decoration: none;
		width:100vw;
		text-align: center;
		justify-content: center;
		object-fit: contain;
	}

	a:hover {
		cursor:pointer;
	}

</style>
