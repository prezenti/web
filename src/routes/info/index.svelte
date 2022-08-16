<script lang="ts">
	export const prerender = true;
    import Icon from '@iconify/svelte';
	import Item from './item.svelte'

    const data = {
		'Who will make grant decisions?': ["The three Prezenti stewards will make grant decisions. In some cases, if additional expertise or help is needed they may enlist help from Celo community members or subject matter experts. However, the final decision will be made by the stewards."],
		'Who is eligible?': ["Individuals and business entities that are aligned with Celo’s mission, comply with KYC/AML policies provided by TrustID, and Terms and Conditions are eligible. If your application is accepted, we will send you the grantee agreement and the KYC/AML questionnaire."],
		'What funding levels are available?': ["Prezenti will provide grants based on the amount needed to achieve the applicants objectives as well as the anticipated value added to the Celo ecosystem. We expect to fund a majority of projects in the 'Medium' range.", "\n", " Small: 10k cUSD or less" ,"Medium: between 10k-50k cUSD","Large: more than 50k cUSD","\n","Each applicant will create their own milestones and timeline based on their availability."],
        'What are the expected timelines?' : ["We expect the project and all milestones completed within 6 months."],
        'How does the Prezenti measure the success of the project?' : ["We expect the applicants to create their own milestones which will be used as evidence for payment release(s) for the duration of the grant. Stewards can request changes to milestones before acceptance of the application, and will have sole discretion to determine the completion of milestones after acceptance."],
        'How is the payment handled?' : ["All grants are paid on-chain in cUSD via the grants software Questbook. All accepted applications will receive the first milestone payment upfront, and subsequent milestone payments by submitting evidence of completion (and having that evidence approved by a steward)."],
        'How much equity will the Prezenti take?' : ["None! Prezenti is a non-profit organisation and provides grants without taking any equity. "],
        'I have a ongoing grant from CCF1 - what happens to me now?' : ["Nothing at all. Your grant will continue to be managed by the original steward that knows and understands your project. Patrick, Dee and Deepak are committed to fulfill their current obligations until your project ends."],
        'I have a ongoing grant from CCF1 - can I now apply for more/extra funds?' : ["You are always welcome to apply for more funds, but think carefully about the value add and actual need. This will need to be clearly articulated in your proposal and will be reviewed accordingly. We will discuss your ongoing grant with the CCF1 stewards who are still managing that contract application."],
        'I was turned down for funding by CCF1, can I re-apply?' : ["You are always welcome to apply for funds at any time and you have honed your project ideas. But again, but think carefully about the value add and actual need. This will need to be clearly articulated in your proposal and will be reviewed accordingly."],
        'How will the funds/projects be tracked?' : ["All active grants will be managed on Questbook. All other transactions (including steward’s payments) for Prezenti are available here on Questbook"],
        'I want to be a subject matter expert and support Prezenti.' : ["Great! Please do get in touch with us and we can go from there (admin@prezenti.xyz). We will be looking for brilliant people to join us to help advise and galvanize people working on Celo globally. Please note there are limited funds for these roles."]
	}
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
            <img src="prezenti-logo.svg" alt="Prezenti logo" /> 
        </div>
    </div>

        <div class="container-typewriter ">
            <div  class="content-typewriter">
                <h1>What is Prezenti</h1>
                <p>Prezenti is a grant fund for the Celo community.</p>
                <p>Prezenti is the second phase of the Celo Community Fund that was created with an approved spend proposal from the on-chain <a href="https://docs.celo.org/celo-codebase/protocol/proof-of-stake/epoch-rewards/community-fund">Community Fund</a>[<a href="https://explorer.celo.org/address/0xD533Ca259b330c7A88f74E000a3FaEa2d63B7972/tokens">explorer</a>]. Community members seeking grant funding can apply to Prezenti, which three community stewards manage. We provide grants of between 5000 - 50,000 $cUSD or equivalent $CELO amount. Alternatively, if you seek a higher amount, there is always the option of submitting their own <a href="https://docs.celo.org/celo-codebase/protocol/governance">governance</a> spend proposal to be voted on by CELO owners.

                    Prezenti supports projects that share <a href="https://celo.org/about">Celo’s Mission</a> and broadly fit into one of the following focus areas.</p>
                    <hr/>
                    <h1>Focus Areas</h1>
                    <ul>
                        <li><b>Education </b><i> is the why.</i></li><p> Having informative data in various forms is the initial starting point for people to gain awareness. We can picture this as seeds that are thrown in a field to grow</p>
                        <li><b>Research </b><i> is the growth.</i></li><p> Once we have the why, we can dive deeper, build upon our initial interest and build conviction to an idea. We can picture this as the water and nutrients that help the seed to grow strong and become a plant </p>
                        <li><b>Commmunity Tools </b><i> are the How</i></li><p> Once we have a belief and a conviction, we need the appropriate tools to be able to execute these ideas. We can think of this as the environment. We need this to be ideal to grow strong.</p>
                        <li><b>Other </b><i> captures serendipity</i></li><p>While the other items are part of the growth story. We leave room for flexibility. </p>
                    </ul>
                    <hr/>
                    <h1>Celo Grant Ecosystem</h1>
                  <p> We work closely with other granting entities like <a href="https://celo.org/experience/grants#introduction">Celo Foundation Grants</a> and the  <a href="https://climatecollective.org">Climate Collective</a> to ensure we capture services that may not fit with the other programs. Although closely aligned, we are independent of the Celo foundation.</p>
                <p>If you're building something on Celo then get in touch and let’s discuss how we might be able to help you.</p> 
                <hr/>   

                <h1>FAQ</h1>
                <div class="accordian">
                    {#each Object.entries(data) as entry}
                        <Item {entry} />
                    {/each}
                </div>
                <hr/>
                </div>
                
        </div>



        <div class="container-typewriter ">
            <div  class="content-typewriter">
                <h1>How to apply</h1>


                <p>The application process will be open in the coming weeks!</p>

                <p>If you would like to be notified once we open, please send a quick email to <a href="mailto:info@prezenti.xyz">info@Prezenti.xyz</a></p>

                <!-- <p>You can apply to the Prezenti fund using the attached application form. </p>

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
                <p class="apply-text">Get started with the tutorials, learn about the SDK and<a href="https://github.com/celo-org">explore</a> the codebase.</p> -->
                
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

    h2 {
        font-weight: bold;
        font-size: 1.5rem;
        margin-bottom:3px;
        font-family: 'VECTRO-bold';
        line-height: 100%;
        
    }

    p {
        font-family: 'Roboto', sans-serif;
        text-align: center;
        align-items: center;
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
        background-color:#3bfa98 ;
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
