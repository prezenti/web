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
	<title>Prezenti</title>
	<meta name="Prezenti" content="Get a grant to help the Celo ecosytem" />
</svelte:head>

<OnMount>
	<section>

		<a  sveltekit:prefetch href="/links">
		<img in:customTransition src="prezenti-logo.svg" alt="Welcome to Prezenti - click to enter" />

		<h1>
			PREZENTI
		</h1>
		<p>Where thinkers, trailblazers and workers come for grants to make their dreams a reality on the Celo network</p>
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
		max-width: 230px;
	}

	h1 {
		width: 100%;
		font-size:5rem ;
		margin:0;
		padding:0;
		font-family: 'VECTRO-bold';
	}


	a {
		text-decoration: none;
		width:100vw;
		text-align: center;
		justify-content: center;
		object-fit: contain;
	}

	p {
		margin:0 20% 0 20%;
		color:white;
		font-size:1.5rem;
		font-family: 'Roboto'
	}

	a:hover {
		cursor:pointer;
	}

</style>
