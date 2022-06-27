<script lang="ts">
	export const prerender = true;
    import { onMount } from 'svelte';
    import Typewriter from 'svelte-typewriter';
    import Icon from '@iconify/svelte';
    import celo from './celo.svg'
    import ccf from './ccf.svg'
    let show = false;
    let ready = false;


    function fade(node, {
        delay = 0,
        duration = 400
        }) {
        const o = +getComputedStyle(node).opacity;

        return {
            delay,
            duration,
            css: t => `opacity: ${t * o}`,
            init: true
        };
    }

    function toggle() {
            show = !show;
        }

    onMount(async () => {
        ready = true;
        setTimeout(toggle, 5400);
	});

</script>

<svelte:head>
	<title>History</title>
	<meta name="Prezenti - History" content="How we got here" />
</svelte:head>

<section>
<div class="corner">
    <a class="corner-a" aria-label="Link to go back" sveltekit:prefetch href="/links">
        <Icon icon="mdi:arrow-left" />
    </a>
</div>

<h1 aria-label="History page" ></h1>

{#if ready}
{#if !show}
<div class="history-animation">

            <div class="container celo">
                <div class="content">
                    <img in:fade="{{delay:100, duration:1000}}" src={celo} alt="Celo logo" />
                </div>
            </div>

            <div class="container">
                <div in:fade="{{delay:1100, duration:1000}}" class="content">
                    <Icon icon="mdi:arrow-down" />
                </div>
            </div>

            <div class="container">
                <div class="content">
                    <img in:fade="{{delay:2100, duration:1000}}" src={ccf} alt="CCF1 logo" />
                </div>
            </div>

            <div class="container">
                <div in:fade="{{delay:3100, duration:1000}}" class="content">
                    <Icon icon="mdi:arrow-down" />
                </div>
            </div>

            <div class="container">
                <div in:fade="{{delay:4100, duration:1000}}" class="content">
                    <img src="prezenti-logo.svg" alt="Prezenti logo" />
                </div>
            </div>

</div>
{/if}
{#if show}
<div class="history-typewriter">
    
    <div class="container">
        <div  class="content">
            <img src="prezenti-logo.svg" alt="Prezenti logo" />
        </div>
    </div>

    <Typewriter cascade interval={2}>
        <div class="container-typewriter ">
            <div  class="content-typewriter">
                <h1>2020: Celo Genesis and the launch of the Celo Community Fund</h1>
                <p>Celo Protocol was officially launched on Earth Day, April 22. Part of the protocol is the Celo Community Fund. The Community Fund provides for general upkeep of the Celo platform. CELO holders decide how to allocate these funds through governance proposals. Funds might be used to pay bounties for bugs or vulnerabilities, security audits, or grants for protocol development.</p>
                <p class="list">The Community Fund receives assets from three sources:</p>
                <ul>
                    <li>The Community Fund obtains a desired epoch reward defined as a fraction of the total desired epoch rewards (governable, initially planned to be 25\%25%). This amount is subject to adjustment up or down in the event of under- or over-spending against the epoch rewards target schedule. The Community Fund epoch rewards may be redirected to bolster the <a href="https://docs.celo.org/celo-codebase/protocol/proof-of-stake/epoch-rewards/community-fund#bolstering-the-reserve">Reserve</a>.</li>
                    <li>Thee Community Fund is the default destination for slashed assets.</li>
                    <li>The Community Fund also receives the 'base' portion of <a href="https://docs.celo.org/celo-codebase/protocol/transactions/gas-pricing">transaction fees</a></li>
                </ul>
            </div>
        </div>
        <div class="container-typewriter ">
            <div  class="content-typewriter">
                <h1>2021: Celo Community Fund 1(CCF1)</h1>
                <p>The first <a href="https://celocommunityfund.org/">Celo Community Fund (CCF)</a> was set up in 2021 by Patrick Baron(<a href="https://moola.market/">Moola</a>), Dee and Deepak Nuli(<a href="https://www.kresko.fi/">Kresko</a>) and was the first community approved spend proposal, from the on-chain Community Fund. It was set up for Celo community members to apply for funds in the form of a grant for work aligned to the focus areas and Celo mission. The three original stewards did an amazing job setting up the fund and in the end distributing $XX/CELO to XX grant recipients. </p>
            </div>
        </div>
        <div class="container-typewriter "> 
            <div  class="content-typewriter">
                <h1>2022: Prezenti</h1>
                <p>The CCF1 funds have now been spent and set of three new stewards (Aaron, Maya and Wade) have sought governance approval for the re-opening of the grant fund in mid 2022. Based on community feedback they have chosen to re-name the fund to avoid confusion with the Celo Community Fund and called it Prezenti - Esperanto for gift/to give.</p>
           
            </div>
        </div>
    </Typewriter>
</div>
{/if}    
{/if}   
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
		height:100vh;
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
        margin-top:7%;
        margin-bottom: 2%;
        font-family: 'Cormorant Garamond', serif;
        font-size: 3rem;
        line-height: 100%;
    }

    h2 {
        font-weight: bold;
        margin-bottom:3px;
    }

    p {
        font-family: 'Proza Libre', sans-serif;
        text-align: center;
        align-items: center;
        margin-top:3px;
    }

    .list {
        text-align:left;
    }

    .content {
        justify-content: center;
        align-items: center;
        margin: auto;
        font-size: 3rem;
    }

    .celo {
        padding:4%;
    }


    img {
        object-fit:fill;
        width:100%;
    }

    a {
        text-decoration: none;

        color: var(--secondary-color)
    }


    p a:hover {
        color:black;
        background-color:#3bfa98 ;
        opacity: 0.5;
    }

 
    .corner-a:hover {
        color:white;
        opacity: 0.5;

    } 

    li {
        margin-top:13px;
        font-family: 'Proza Libre', sans-serif;
    }


    .corner {
        padding:5%;
		width: 1rem;
		height: 1rem;
	}

    .corner a {
        color:var(--tertiary-color);
        font-size: 5rem;
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


        h1 {
            font-size: 1.5rem;
        }
        
        a {
            font-size: 0.7rem;
        }

        .content-typewriter {
            font-size: 0.7rem;
        }

        .history-typewriter {
            margin-top: 40%;
        }

        .container {
            margin-top:10%
         }

         .corner a {
            font-size: 2.4rem;
         }
    }

    

	
</style>
