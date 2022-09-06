<script  lang="ts">
	export const prerender = true;
    import { onMount } from 'svelte';
    import Icon from '@iconify/svelte';
    import { Row, Col } from 'svelte-materialify';
    import image from './portrait-aaron-white.png'
    import image_wade from './portrait-wade-white.png';
    import image_maya from './portrait-maya-white.png';
    import subject from './subject-white.png' 
 

    let mobile = false;

    onMount(async () => {
		let height = window.innerWidth;
        console.log(height)
		mobile = (height < 600) ? true : false;
        console.log(mobile)
	});
    
</script>

<svelte:head>
	<title>About Us</title>
	<meta name="Prezenti - About Us" content="Who are we" />
</svelte:head>

<section>

<div class="corner">
    <a sveltekit:prefetch aria-label="Link to go back" href="/links">
        <Icon icon="mdi:arrow-left" />
    </a>
</div>

<h1 aria-label="About us page" ></h1>



<div class="about-us">
        <Row noGutters>
          <Col cols={12} sm={6} md={6}>
            <div class="container">
                <div class="content">
                    <img src={image} alt="Aarons profile picture" />
                </div>
            </div>
          </Col>
          <Col cols={12} sm={6} md={6}>
            <div class="container">
                <div class="content">
                    <h2><b>Aaron</b></h2>
                    <p>Founder and operator of <a href="https://vladiatorlabs.io/">VladiatorLabs.io</a>, a protocol-aligned infrastructure company validating on Celo and expanding to other proof-of-stake networks, especially in the Cosmos ecosystem. Vladiator Labs is a founding project in the Staking Defense League, an infrastructure special interests group aimed at promoting decentralization in the staking space. Freelance Solidity, blockchain, database and cloud engineer and recently has worked with <a href="https://ravespace.io/">RaveSpace</a> on metaverse NFT gallery <a href="https://musee-dezentral.com">Musee Dezentral</a>.</p>
                </div>
            </div>
          </Col>
        </Row>

        <Row noGutters>
            <Col cols={12} sm={6} md={6}>
                <div class="container">
                    <div class="content">
                        {#if !mobile}
                            <h2><b>Maya</b></h2>
                            <p><b>Background:</b> I am passionate about making a positive impact in the world we live in. I spent 5 years running a low carbon technology grant programme, disbursing over £50m. For 7 years I worked for Save the Children supporting end-to-end grant management in East Africa managing funds from a variety of donors.  For 18 months I have been the Chief Operating Officer for a UK based fintech building on Celo, helping them deliver cash transfer programs to help vulnerable users use Celo to meet their basic household needs</p>
                            <p><b>Current Work : </b>Contributing to a possible new DAO and this!</p>
                        {:else}
                        <img src={image_maya} alt="Maya's profile picture" />
                       {/if}
                    </div>
                </div>
            </Col>
            <Col cols={12} sm={6} md={6}>
                <div class="container">
                    <div class="content">
                        {#if !mobile}
                            <img src={image_maya} alt="Maya's profile picture" />
                        {:else}
                            <h2><b>Maya</b></h2>
                            <p><b>Background: </b> I am passionate about making a positive impact in the world we live in. I spent 5 years running a low carbon technology grant programme, disbursing over £50m. For 7 years I worked for Save the Children supporting end-to-end grant management in East Africa managing funds from a variety of donors.  For 18 months I have been the Chief Operating Officer for a UK based fintech building on Celo, helping them deliver cash transfer programs to help vulnerable users use Celo to meet their basic household needs</p>
                            <p><b>Current Work: </b> Contributing to a possible new DAO and this!</p>
                        {/if}
                    </div>
                </div>
            </Col>
          </Row>

          <Row noGutters>
            <Col cols={12} sm={6} md={6}>
                <div class="container">
                    <div class="content">
                        <img src={image_wade} alt="Wades profile picture" />
                    </div>
                </div>
            </Col>
            <Col cols={12} sm={6} md={6}>
                <div class="container">
                    <div class="content">
                        <h2><b>Wade</b></h2>
                        <p><b>Background: </b> I operate <a href="https://thepassivetrust.com">The Passive Trust</a>, an infrastructure provider for blockchain networks. The Passive Trust runs a validator group on Celo since Genesis. The Passive Trust has distributed a large percentage of funds received from being an operator on Celo to support projects built on Celo. This includes Moola, Ubeswap, ImpactMarket, Poof Cash and Resource Network. I was initially part of the Mentor/mentee program in The Great Celo Bake Off, my motivation for becoming a steward is to help potential entrepreneurs and engineers to be able to get funding through grants and be given an opportunity like I was.</p>
                        <p><b>Current Work: </b> Operates The Passive Trust. I also contribute to multiple DAOs and open source projects.</p>
                    </div>
                </div>
            </Col>
          </Row>

          <Row noGutters>
            <Col cols={12} sm={6} md={6}>
                <div class="container">
                    <div class="content">
                        {#if !mobile}
                            <h2><b>Subject matter experts</b></h2>
                            <p>We call on experts of particular domains or regions when needed. This is done when we need clarification on a grant that has been proposed or for outreach to get the right people connected with Prezenti and funded. If you interested to support us please reach out.</p>
                            <p>If you are in helping Prezenti by being a subject matter expert, please contact <a href="mailto:info@prezenti.xyz">info@Prezenti.xyz</a></p>
                        {:else}
                        <img src={subject} alt="SM profile picture" />
                       {/if}
                    </div>
                </div>
            </Col>
            <Col cols={12} sm={6} md={6}>
                <div class="container">
                    <div class="content">
                        {#if !mobile}
                            <img src={subject} alt="SM profile picture" />
                        {:else}
                            <h2><b>Subject matter experts</b></h2>
                            <p>We call on experts of particular domains or regions when needed. This is done when we need clarification on a grant that has been proposed or for outreach to get the right people connected with Prezenti and funded.</p>
                            <p>If you are in helping Prezenti by being a subject matter expert, please contact <a href="mailto:info@prezenti.xyz">info@Prezenti.xyz</a></p>
                        {/if}
                    </div>
                </div>
            </Col>
          </Row>

</section>

<style>


	.about-us {
		justify-content: center;
		align-items: center;
		height:80vh;
	}

    img {
        padding:5%;
        object-fit:contain;
        width:100%;
        height:100%;
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
        color:var(--text-color);
        font-family: 'Roboto', sans-serif;
        font-size: 0.9rem;
    }

    a {
        text-decoration: none;
        font-size: 1rem;
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

    p a:hover {
        color:black;
        background-color:#44d8f2 ;
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
        font-size: 5rem;
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
            font-size: 0.7rem;
        }

        .corner a {
            font-size: 2.4rem;
         }

    }

</style>
