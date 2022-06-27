<script  lang="ts">
	export const prerender = true;
    import { onMount } from 'svelte';
    import Icon from '@iconify/svelte';
    import { Row, Col } from 'svelte-materialify';
    import image from './fake-portrait.jpeg'
    import image_wade from './portrait-wade.png'
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
                    <p><b>Background:</b> Software engineer for nearly 20 years, worked the better part of 15 years in the financial services industry in Australia (banking, insurance, superannuation). Active in the blockchain space since 2013 and advocate for economic self-determination.</p>
                    <p><b>Current Work:</b> Founder and operator of VladiatorLabs.io, a protocol-aligned infrastructure company currently in the process of incorporating in Switzerland and expanding to other proof-of-stake networks, especially in the Cosmos ecosystem. Vladiator Labs is a founding project in the Staking Defense League, an infrastructure special interests group aimed at promoting decentralization in the staking space. Additionally has worked briefly as a contractor within cLabs on some minor projects. Involved in the Celo ecosystem since the incentivised testnet and have been supported by the Celo Foundation as an elected validator since genesis (over two different validator groups). Freelance Solidity, blockchain, database and cloud engineer and recently has worked with RaveSpace on metaverse NFT gallery https://musee-dezentral.com.</p>
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
                            <p><b>Background:</b> I am passionate about making a positive impact in the world we live in. As a project manager, I spent 5 years running a low carbon technology grant programme, disbursing over £50m GBP. For 7 years I worked for Save the Children supporting end-to-end grant management in East Africa, identifying, securing, applying and managing funds from a huge variety of donors. Because of these roles I have the unique experience and knowledge of being both the donor and recipient. Since Feb 2021 I have been Chief Operating Officer for TrustWorks Ltd, a UK based fintech building on Celo, helping them deliver cash transfer programs in Latin America to help refugees/vulnerable users use Celo to meet their basic household needs. I have the skills to enable a slick, simple and transparent granting system and process, whilst helping to expand the fund’s impact and further Celo's reach.</p>
                            <p><b>Current Work : </b>My role as COO with Trustworks Ltd is coming to an end in July 2022. I am now a part-time founding contributor for Kakuza.</p>
                        {:else}
                        <img src={image} alt="Maya's profile picture" />
                       {/if}
                    </div>
                </div>
            </Col>
            <Col cols={12} sm={6} md={6}>
                <div class="container">
                    <div class="content">
                        {#if !mobile}
                            <img src={image} alt="Maya's profile picture" />
                        {:else}
                            <h2><b>Maya</b></h2>
                            <p><b>Background: </b> I am passionate about making a positive impact in the world we live in. As a project manager, I spent 5 years running a low carbon technology grant programme, disbursing over £50m GBP. For 7 years I worked for Save the Children supporting end-to-end grant management in East Africa, identifying, securing, applying and managing funds from a huge variety of donors. Because of these roles I have the unique experience and knowledge of being both the donor and recipient. Since Feb 2021 I have been Chief Operating Officer for TrustWorks Ltd, a UK based fintech building on Celo, helping them deliver cash transfer programs in Latin America to help refugees/vulnerable users use Celo to meet their basic household needs. I have the skills to enable a slick, simple and transparent granting system and process, whilst helping to expand the fund’s impact and further Celo's reach.</p>
                            <p><b>Current Work: </b> My role as COO with Trustworks Ltd is coming to an end in July 2022. I am now a part-time founding contributor for Kakuza.</p>
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
                        <p><b>Background: </b> Operates The Passive Trust, an infrastructure provider for blockchain networks. The Passive Trust runs a validator group that has been running on Celo since Genesis. The Passive Trust has distributed a lot of the funds received from operating the Group and Validator to fund and support projects built on Celo. This includes Moola, Ubeswap, ImpactMarket, Poof Cash and Resource Network. Wade was initially part of the Mentor/mentee program in The Great Celo Bake Off, his motivation for becoming a steward is to help potential entrepreneurs and engineers to be able to get funding through grants and be given an opportunity like he was.</p>
                        <p><b>Current Work: </b> Operates The Passive Trust. I also contribute to multiple DAOs and open source projects.</p>
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
        color:#fff;
        font-family: 'Proza Libre', sans-serif;
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
