<script lang="ts">
	export const prerender = true;
    import Icon from '@iconify/svelte';
</script>

<svelte:head>
	<title>History</title>
	<meta name="history" content="How we got here" />
</svelte:head>

<section>
<div class="corner">
    <a sveltekit:prefetch href="/links">
        <Icon icon="mdi:arrow-left" />
    </a>
</div>


<div class="history-typewriter">
    
    <div class="container">
        <div  class="content">
            <img src="prezenti-logo.svg" alt="Welcome" /> 
        </div>
    </div>

        <div class="container-typewriter ">
            <div  class="content-typewriter">
                <h1>What is Prezenti</h1>
                <p>Prezenti is a grant fund for the Celo community.</p>
                <p>Prezenti is the second phase Celo community approved spend proposal from the on-chain <a href="https://docs.celo.org/celo-codebase/protocol/proof-of-stake/epoch-rewards/community-fund">Community Fund</a>[<a href="https://explorer.celo.org/address/0xD533Ca259b330c7A88f74E000a3FaEa2d63B7972/tokens">explorer</a>]. Community members seeking grant funding can apply to Prezenti which is managed by three community stewards. Alternatively there is always the option of submitting their own <a href="https://docs.celo.org/celo-codebase/protocol/governance">governance</a> spend proposal to be voted on by CELO owners.

                    Prezenti supports projects that share <a href="https://celo.org/about">Celo’s Mission</a> and broadly fits into one of these focus areas.
                    
                    It's great there are numerous avenues for grant funding: <a href="https://celo.org/experience/grants#introduction">Celo Foundation Grants</a> and the  <a href="https://climatecollective.org">Climate Collective</a>. We work closely with each granting entity to ensure we all offer the best service to the community.</p>
                <p>If you're building something on Celo then get in touch and let’s discuss how we might be able to help you.</p>    
                </div>
        </div>
        <div class="container-typewriter ">
            <div  class="content-typewriter">
                <h1>How to apply</h1>

                <p>You can apply to the Prezenti fund using the attached application form. </p>

                <p>At present applications are taken on a rolling basis.</p>

                <p>Here’s how the Prezenti process works, from application to finish line.</p>

                <h2>Step 1: Choose a category</h2>
                <p class="apply-text">If your project fits into one of these 4 grant programs and aligns with the Celo mission, you’re a candidate for a Prezenti grant. Join Discord and reach out.</p>

                <h2>Step 2: Submit your grant application</h2>
                <p class="apply-text">Make sure you thoroughly complete the application form and clearly state how your project will contribute to the Celo ecosystem. Please review the Grant Application Terms and Conditions before submitting.</p>

                <h2>Step 3: Evaluation and approval</h2>
                <p class="apply-text">The Stewards will review your application in the order it is received. If your proposal meets the program criteria, you will be invited to an interview with two committee members.</p>

                <h2>Step 4: Acceptance or denial notification</h2>
                <p class="apply-text">All applicants will be notified whether their application has been accepted or denied. If your application is accepted, at this point, you will go through the agreement formation process.</p>

                <h2>Step 5: Build and launch your project</h2>
                <p class="apply-text">Get started with the tutorials, learn about the SDK and<a href="https://github.com/celo-org">explore</a> the codebase.</p>
            </div>
        </div>

</section>


<style>

    section {
        margin-bottom: 40px;
    }

	.history-animation {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height:100vh;
        margin-top: -10%;
	}

    .history-typewriter {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
        margin-top: -10%;
	}

    .container {
        flex-wrap: wrap;
        min-height: 15vh;
        width:20%;
        display: flex;
        justify-content: center;
        align-items: center;
        color: var(--mdc-theme-on-secondary, #fff);
    }

    .container-typewriter {
        flex-wrap: wrap;
        min-height: 15vh;
        width:80%;
        margin:auto;
        display: flex;
        justify-content: center;
        align-items: center;
        color: var(--mdc-theme-on-secondary, #fff);
    }

    .content-typewriter {
        justify-content: center;
        align-items: center;
        margin: auto;
        font-size: 1rem;
        color: white;
    }

    .content-typewriter p {
        color: white;
    }

    h1 {
        margin-bottom: 5px;
        font-family: 'Cormorant Garamond', serif;
    }

    h2 {
        font-weight: bold;
        font-size: 1.5rem;
        margin-bottom:3px;
        font-family: 'Cormorant Garamond', serif
        
    }

    p {
        font-family: 'Proza Libre', sans-serif;
        text-align: center;
        align-items: center;
        margin-top:3px;
    }

    .apply-text {
        font-family: 'Proza Libre', sans-serif;
        text-align: left;
        align-items: left;
        margin-top:3px;
    }

    .content {
        justify-content: center;
        align-items: center;
        margin: auto;
        font-size: 3rem;
    }

    img {
        object-fit:fill;
        width:100%;
    }

    .corner a {
            font-size: 5rem;
         }

    a {
        text-decoration: none;
        color: var(--secondary-color)
    }

    a:hover {
        color:black;
        background-color:#3bfa98 ;
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
            font-size: 0.7rem;
        }

        .content-typewriter {
            font-size: 0.7rem;
        }

        .history-typewriter {
            margin-top: -20%;
        }

        .container {
            margin-top:10%
         }

         .corner a {
            font-size: 2.4rem;
         }
    }

    

	
</style>
