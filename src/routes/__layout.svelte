<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
	import '@beyonk/gdpr-cookie-consent-banner/dist/style.css' // optional, you can also define your own styles
    import GdprBanner from '@beyonk/gdpr-cookie-consent-banner'
	import Icon from '@iconify/svelte'; 

	function initAnalytics () {
    // do something with segment.io or google analytics etc
  }
</script>


<main>
	<slot />
</main>



<footer>
	<p> <a href="/">Prezenti Inc. 2022</a> | <a href="https://docs.prezenti.xyz">Terms & Conditions</a> |    
	<a sveltekit:prefetch aria-label="Discord" href="https://discord.gg/bA6gzZzZAK">
        <Icon icon="mdi:discord" />
    </a>
	<a sveltekit:prefetch aria-label="Discord" href="https://twitter.com/prezenti_grants">
        <Icon icon="mdi:twitter" />
    </a>
	<a  aria-label="Blog" href="https://blog.prezenti.xyz">
		<Icon icon="mdi:file-document" />
	</a>
		<GdprBanner class="gdpr" heading="Privacy Notice" description="We use cookies to improve your browsing experience, show you personalized ads or content, and analyze our traffic. By clicking Accept Cookies you consent to our use of cookies." on:analytics={initAnalytics} />
	</p>
</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100vw;
		margin: 0 auto;
		box-sizing: border-box;
	}

	p {
        font-family: 'Roboto', sans-serif;
        text-align: center;
        align-items: center;
        margin-top:3px;
    }

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		position: fixed;
		bottom: 0;
		width:100vw;		
	}

	footer p {
		font-family: 'Roboto';
	}


</style>
