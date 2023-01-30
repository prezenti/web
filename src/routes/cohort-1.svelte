<script lang="ts">
	export const prerender = true;
    import Icon from '@iconify/svelte';
</script>

<svelte:head>
	<title>Info</title>
	<meta name="Prezenti - Info" content="About Prezenti" />
</svelte:head>

<section>
<div class="corner">
    <a class="corner-a" aria-label="Link to go back" sveltekit:prefetch href="/links">
        <Icon icon="mdi:arrow-left" />
    </a>
</div>


<div class="history-typewriter">
    
    <div class="container">
        <div  class="content">
            <h1>COHORT 1</h1>
        </div>
    </div>

        <div class="container-typewriter ">
            <div  class="content-typewriter">
                <h2>Alcancia</h2>

                <p>Alcancia is a native mobile application. A wallet that lets users bridge their fiat Mexican and Dominican pesos into stablecoins (USDC and cUSD).</p>
                <li><a href="https://mirror.xyz/0x86792D8d875a06ccC787096304647aA98C5FB9Bb">Mirror</a></li>
                <li><a href="https://landing.alcancia.io/">Website</a></li>
                <li><a href="https://twitter.com/Alcancia_io">Twitter</a></li>

                <hr/>

                <h2>Ostrom</h2>

                <p>Ostrom is a protocol for community-based development and environmental regeneration. Communities and individuals can deposit their land or purchase Ostrom independently to be invested in a land asset. Ostrom enables a network of Community Land Trust’s to be formed and dynamic management of land.</p>
                <li><a href="https://www.de-plan.xyz/">Website</a></li>
                <li><a href="https://twitter.com/de_planDAO">Twitter</a></li>

                <hr/>

                <h2>Ethics for a Humanized Technological Development</h2>

                <p>Ethics for a Humanized Technological Development is planning a 6 month project, where they will educate high school and college students on the foundations of blockchain technology and ethics of token engineering. Their main focus will be public schools in Salvador, Brazil, and the course will help onboard students to Celo and its Dapps, with a focus on how blockchain can improve the lives of different communities.</p>
                <li><a href="https://www.notion.so/Blockchain-na-Escola-DAO-8cacb7e784694c3695b7b13abd882bda">Notion</a></li>
                <li><a href="https://blockchainnaescola.tech/en">Website</a></li>
                <li><a href="https://twitter.com/BlckNaEscola">Twitter</a></li>

                <hr/>

                <h2>Sargo</h2>

                <p>Sargo is a decentralized protocol for swapping between stablecoins and local currencies from your phone. Over time they aim to integrate Sargo into a range of 3rd-party wallets, dapps and interfaces. Making it cheaper and easier to enter and exit the web-3 economy without the need for a token bridge, order book, fiat integration, or pooling mechanism</p>
                <li><a href="https://twitter.com/sargo_io">Twitter</a></li>

                <hr/>

                <h2>Love Crypto</h2>

                <p>Love Crypto is a Proof of Concept for interoperability on the Brazilian Real Digital Ledger into a full-fledged product to allow users to purchase Real World Assets registered in the Real Brazilian Digital Ledger.</p>
                <li><a href="http://liftlabs.lovecrypto.com.br:3000/">Proof of Concept</a></li>
                <li><a href="https://www.lovecrypto.net/#/">Website</a></li>
                <li><a href="https://twitter.com/Lovecryptobr">Twitter</a></li>

                <hr/>

                <h2>TokPay</h2>

                <p>Tokpay is an African Focused web 3 Neobank for high-yield USD savings and Fixed Deposit Accounts.</p>
                <li><a href="http://tokpayapp.com/">Website</a></li>
                <li><a href="https://twitter.com/tokpayapp">Twitter</a></li>


        </div>

                
                
        </div>

        </div>

</section>


<style>
    hr {
        margin-top: 50px;
        margin-bottom: 50px;
    }
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
        padding-bottom: 5%;
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
        padding-top: 5%;
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
        color: var(--text-color);
    }

    .content-typewriter p {
        color: var(--text-color);
    }

    h1 {
        margin-top:7%;
        margin-bottom: 2%;
        font-family: 'VECTRO-bold';
        font-size: 3rem;
        line-height: 100%;
    }

 

    .focus-area-image {
        height: 100px;
    }

    h2 {
        font-weight: bold;
        font-size: 1.5rem;
        margin-bottom:2%;
        font-family: 'VECTRO-bold';
        line-height: 100%;
        
    }

    p {
        font-family: 'Roboto', sans-serif;

        margin-top:3px;
    }

    accordian {
        font-family: 'Roboto', sans-serif;
        text-align: center;
        align-items: center;
        margin-top:3px;
    }



    .apply-text {
        font-family: 'Roboto', sans-serif;
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
            color:var(--text-color);
         }

    .corner-a:hover {
        color:var(--text-color);
        opacity: 0.5;

    } 

    a {
        text-decoration: none;
        color: var(--secondary-color)
    }

    p a:hover {
        color:black;
        background-color:#44d8f2 ;
        opacity: 0.5;
    }

    .corner {
        padding:5%;
		width: 1rem;
		height: 1rem;
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