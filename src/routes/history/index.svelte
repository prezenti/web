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
	<meta name="history" content="How we got here" />
</svelte:head>

<section>
<div class="corner">
    <a sveltekit:prefetch href="/links">
        <Icon icon="mdi:arrow-left" />
    </a>
</div>
{#if ready}
{#if !show}
<div class="history-animation">

            <div class="container celo">
                <div class="content">
                    <img in:fade="{{delay:100, duration:1000}}" src={celo} alt="Welcome" />
                </div>
            </div>

            <div class="container">
                <div in:fade="{{delay:1100, duration:1000}}" class="content">
                    <Icon icon="mdi:arrow-down" />
                </div>
            </div>

            <div class="container">
                <div class="content">
                    <img in:fade="{{delay:2100, duration:1000}}" src={ccf} alt="Welcome" />
                </div>
            </div>

            <div class="container">
                <div in:fade="{{delay:3100, duration:1000}}" class="content">
                    <Icon icon="mdi:arrow-down" />
                </div>
            </div>

            <div class="container">
                <div in:fade="{{delay:4100, duration:1000}}" class="content">
                    <img src="prezenti-logo.svg" alt="Welcome" />
                </div>
            </div>

</div>
{/if}
{#if show}
<div class="history-typewriter">
    
    <div class="container">
        <div  class="content">
            <img src="prezenti-logo.svg" alt="Welcome" />
        </div>
    </div>

    <Typewriter cascade interval={2}>
        <div class="container-typewriter ">
            <div  class="content-typewriter">
                <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
            </div>
        </div>
        <div class="container-typewriter ">
            <div  class="content-typewriter">
                <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
            </div>
        </div>
        <div class="container-typewriter ">
            <div  class="content-typewriter">
                <p>Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book. It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.</p>
            </div>
        </div>
    </Typewriter>
</div>
{/if}    
{/if}   
</section>


<style>

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

    p {
        font-family: 'Proza Libre', sans-serif;
        text-align: center;
        align-items: center;
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

        .content-typewriter {
            font-size: 0.7rem;
        }

        .history-typewriter {
            margin-top: -20%;
        }
    }

    

	
</style>
