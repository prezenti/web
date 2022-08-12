<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
	import '@beyonk/gdpr-cookie-consent-banner/dist/style.css' // optional, you can also define your own styles
    import GdprBanner from '@beyonk/gdpr-cookie-consent-banner'

	function initAnalytics () {
    // do something with segment.io or google analytics etc
  }
</script>


<main>
	<slot />
</main>



<footer>
		<GdprBanner class="gdpr" heading="Privacy Notice" description="We use cookies to improve your browsing experience, show you personalized ads or content, and analyze our traffic. By clicking Accept Cookies you consent to our use of cookies." on:analytics={initAnalytics} />

</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		width: 100vw;
		margin: 0 auto;
		box-sizing: border-box;
		font-family: 'VECTRO-bold';

	}



	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		position: fixed;
		bottom: 0;
		width:100vw;
		font-family: 'Roboto' !important;
		
	}

	footer p {
		font-weight: bold;
		color:var(--tertiary-color);
	}


</style>
