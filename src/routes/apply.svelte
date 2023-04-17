<script  lang="ts">
	export const prerender = true;
    import Icon from '@iconify/svelte';

</script>

<svelte:head>
	<title>Apply For a Grant</title>
	<meta name="Prezenti Apply" content="Create a grants application" />
</svelte:head>

<section>

<div class="corner">
    <a sveltekit:prefetch aria-label="Link to go back" href="/links">
        <Icon icon="mdi:arrow-left" />
    </a>
</div>

<h1 aria-label="Apply page" ></h1>

<div class="apply">
    <!-- <p>Applications are currently closed</p>
    <p>Look out for a Celo Forum post soon!</p> -->
    <!-- <p>We look forward to a prosperous 2023 with you all!</p> -->
    <!-- <iframe tabindex="-1" aria-label="Google sheet with transaction details" role="presentation" width="100%" height="100%" title="Prezenti transactions" src="https://docs.google.com/forms/d/e/1FAIpQLSf7h-hYDZsgJ6ikmzAsGUSp438zGnDKx363ryUsZ-mWNTqwdQ/viewform?usp=sf_link">Loading....</iframe> -->
    <div id="ff-compose"></div>
<script async defer src="https://formfacade.com/include/100113532735355078880/form/1FAIpQLSf7h-hYDZsgJ6ikmzAsGUSp438zGnDKx363ryUsZ-mWNTqwdQ/classic.js?div=ff-compose"></script>
</div>

</section>

<style>

	.apply {
		justify-content: center;
		align-items: center;
		height:80vh;
        color: var(--text-color);
        padding-bottom: 100px	
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

    p a:hover {
        color:black;
        background-color:#3bfa98 ;
        opacity: 0.5;
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
            font-size: 3rem;
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