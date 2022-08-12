<script  lang="ts">
	export const prerender = true;
    import Icon from '@iconify/svelte';

</script>

<svelte:head>
	<title>Tx tracking</title>
	<meta name="Prezenti Tx Tracking" content="What are we spending on" />
</svelte:head>

<section>

<div class="corner">
    <a sveltekit:prefetch aria-label="Link to go back" href="/links">
        <Icon icon="mdi:arrow-left" />
    </a>
</div>

<h1 aria-label="Transactions page" ></h1>

<div class="about-us">
    <iframe tabindex="-1" aria-label="Google sheet with transaction details" role="presentation" width="100%" height="100%" title="Prezenti transactions" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRU7rOrbNlBps2LweCSKL_DS-OCJb2wyVP09mzlvYmrBn74NiZkxKa0MiENsxHYCDNXaXoyuXstc8kA/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
</div>

</section>

<style>

	.about-us {
		justify-content: center;
		align-items: center;
		height:80vh;
	}

    img {
        padding:5%;
        object-fit:fill;
        width:100%;
    }

    p {
        padding:1% 5% 1% 5%;
		justify-content: center;
		align-items: center;
        text-align: center;
    }

    .container {
        position:relative;
        min-height: 20vh;
        display: flex;
        justify-content: center;
        align-items: center;

        color: var(--mdc-theme-on-secondary, #fff);
    }

    .content {
        display:relative;
        justify-content: center;
        align-items: center;
        margin: auto;
    }

    .content p {
        color:#fff;
        font-family: 'Roboto', sans-serif;
        font-size: 0.9rem;
    }

    a {
        text-decoration: none;
        font-size: 5rem;
        color: var(--secondary-color)
    }
     
    h2 {
        text-align: center;
        font-size: 2rem;
        padding-top: 10%

    }

    a:hover {
        color:black;
        opacity: 0.5;
    }

    .corner {
        padding:5%;
		width: 1rem;
		height: 1rem;
        margin-bottom:5%;
	}

    .corner a {
        color:var(--text-color);
    }
    .corner img {

    width: 3rem;
    height: 3rem;
    }

    @media (max-width: 600px) {
        a {
            font-size: 4rem;
        }
        .corner {

            margin-bottom:10%;
        }
    }

    @media (max-width: 400px) {
        a {
            font-size: 2.4rem;
        }
    }

    

	
</style>