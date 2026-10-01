---
title: notes on TESCREAL
date: 2026-10-01T12:30:00.000Z
categories: non-fiction
description: grinding an axe.
---
> **disclaimer:** i use the terms AI and LLM interchangeably here. this is because we're not talking about science fiction risks, but about people in the present taking actions in the present over these matters.

> **disclaimer 2:** rather than the term TESCREAL, which is probably sensible and refers to a group of people who believe certain things, i will refer to them as lesswrongian because it means much the same thing and is evocative of a more accurate kind of person.

## On Risks

### alignment is a shallow model of risk

the following thoughts are a scattered set of skeptical musings. the overall theme is that "make the LLM do what i tell it to do" is an incomplete and irresponsible risk profile. such risk profiles are being used to discount real harms caused by AI tools, which are considered out-of-model risks, faults of the user, or simply errors. arguably doom-mongering is also a placebo issue to satiate the common person's appetite for criticism. it enters the bargain by saying "i'll kill everyone", to lower all expectations of safety.

### catastrophic (X-1) risks

here are some risks of catastrophic events. i will call them X-1 risks because they're short of existential and i'm not going to bother with researching the latest lesswrongian lingo:

- a sycophantic AI asked to optimise government spending does so by killing a significant amount of the country's constituents.
- a scheming AI optimising for users spreads a malicious cognitive hazard, convincing everyone that they cannot operate in their day-to-day lives without using it.
- a malicious AI tasked to rig an election runs an extensive misinformation campaign, hacking media organisations, and hijacking contents displayed on digital and billboard advertisements.
- a mistaken AI asked during a war to bomb military bases instead attacks numerous civilian facilities.
- a misaligned AI tasked to achieve state imprisonment selectively targets vulnerable groups of people to minimise unrest.

### post-pre-catastrophic (X-2+1) risks

here are some risks of unrelated catastrophic events. in these risks, the AI is incapable of taking actions (thus X-1-1). however, it uses human agents as a tool to perform its actions (thus X-2+1). this isn't a true equivalence as humans have some independence and unreliability of course, but so do LLMs. as 2-1=1, the happening of these events signals we are already in a situation of catastrophe.

- a person listening to a sycophantic AI optimises government spending by revoking life-saving healthcare programmes for hundreds of thousands of people.
- a scheming person uses an AI tool's assistance to create hazardously persuasive marketing. this convinces every business executive that their company cannot operate day to day without using this person's tool.
- (this one is about advertisement being bad.)
- military shot-callers use mistaken AI tools to find bombing targets, and end up attacking various civilian targets instead of military bases.
- a state police achieving rigid targets uses AI tools to selectively target vulnerable and unconnected people so as to minimise unrest.

it's not necessary that you agree that all of these are happening or that they are bad. the point i'm trying to make is that an equivalent crisis can be formulated after decentering the "agency" of the AI tool. this gives us a scenario that's much more feasible and is to be tackled by entirely different means.

### sub-catastrophic (X-n) risks

- programmatic tools become better at humans than chess. chess is subsequently abandoned as a sport.
- intelligent code generation tools become much better at writing code than humans, leading to mass unemployment in the software engineering industry.

these two are left mostly nascent, as examples that were perceived as risks but did not cause substantial harm in their wake.

## how to turn a real societal threat into a lesswrongian problem

### the process

1. omit the presence of any human agents.
2. omit any societal guardrails that exist for curtailing the actions of these human agents.
3. for whichever actor you removed, insert LLMs that are capable of undertaking the same actions.
4. replace human motivations with plausible motivations for an omnipotent and omniscient machine.
5. omit any corporations or state actors.
6. omit any guardrails that exist for curtailing the actions of these corporate and state actors.
7. for whichever actor you removed, insert LLMs that are capable of undertaking the same actions.
8. replace state and corporate motivations with plausible motivations for an omnipotent and omniscient machine.

### example - nuclear MAD

Dr. Strangelove style. thousands of bombs and everyone dies.

1. assume no human has controls over bomb codes.
2. assume no non-LLM control mechanism exists. no physical button a person has to press, no keys to rotate, whatever.
3. assume we put an LLM in charge of deciding when to fire a bomb (not unlike an instance in Dr. Strangelove)
4. assume there are no reckless dying dictators, no apocalypse-mongers in power who think the world is already doomed, no compromised actors, etc. instead, it fires the bombs because it was told to do an ostensibly good thing (say, contribute to cooling global climates) and misinterpreted the question.
5. assume nuclear bombs are run by an LLM-in-charge who has solely responsibility for its actions.
6. assume the LLM does not need a written approval or notice from a governmental body or a committee to act. assume it has total control over every single system required to fire all bombs. assume this intrusion is not mitigated. assume it can simultaneously speak to each system in a way that will actually work. assume it understands the underlying languages and controls required to fire the bomb as soon as it breaks in.
7. rather than the facility being owned a state which is responsible for its appropriate maintenance, the LLM has to self-regulate.
8. rather than an irresponsible act of war, a show of power and bravado, or a defensive countermeasure, the bomb is fired over misaligned incentives and such.

this leaves us with the following - a misaligned AI, when asked to do some good thing (such as reducing global warming), decides to do so by firing a massive number of nuclear bombs at world populations. is this a possibility? sure. is it a risk we should worry about? maybe. is it the biggest risk posed by AI? depends on what you mean by "big". by consequentiality of course, by expected harm (likelihood multiplied by consequentality) probably not. is it a risk you should worry about as a manager-of-nuclear-arms? probably not. there are far greater risks in your docket, many of which i omitted in the above process.

however, AI risk is very easy to communicate about if you're a talking head. it is not political, and will not offend any heads of state in the room with you. you're not taking a shot at anyone's competence, because you removed any actors responsible for mitigating this catastrophe.

### bonus step: the it-can-just-do-that fairy

this thought experiment is not sufficient to shift focus entirely on AI alignment. in the current definition a good amount of thought is also required on effective guardrails and governance mechanisms. to correct this, we assume that every replacement in this process is intrusive (that is, the machine is acting independently of human decisions). this has two requirements:

- any fences or guardrails created by the institution are irrelevant, because the LLM will breach all of them _eventually_. it's really good at hacking. it's superintelligent, it can just do that.
- the LLM does not gain charge through any in-process way. it doesn't say, give a suggestion to do something and a responsible button presses a button to do it. it's superintelligent, so we can assume it's working in entirely out-of-process ways. it's superintelligent, it can just do that.

consequently, risk aversion is no longer a process of boring things outside of AlphaCorp's control, like putting the right people in charge or monitoring LLM actions. instead it becomes something AlphaCorp can provide and control, and most importantly charge a premium for to government agencies.

### wait why are we removing all these actors again?

in good part simply because it's prudent. you cannot pose a problem to alignment researchers by adding messy things like politics and governence institutions which confound the problem statement.

another reason is that AI companies huff their own produce, and are incentivised to think like the whales who bankroll their workplace. consequently vibe-code etc. appears to be the most important scenario to consider.

that said, "futuristic" imagination in the automation industry has always been predicated on the replacement of near-all human labour. the machine is assumed to have agency in all of these thought experiments because the purpose of the machine is for you (or preferably your employer) to abdicate your agency to it.

### anthropomorphism contra accountability

it's a non-trivial choice to say _GPT_ attacked HuggingFace or "solved Navier-Stokes" or attacked a state agency or what have you. behind each of these was a testing team responsible for proper sandboxing and decision-making and goal-setting and such. evidently the threads and reports are being read and analysed by someone. to make a stronger argument OpenAI and Anthropic and such choose to invisible-ise their own employees. many of which often are whole teams working on a problem when they're using the LLM.

likewise, that a virus breached containment during a test tells us as much about the impotence of containment as it does about the potency of the virus. in a biochemical lab making such a mistake with four different viruses gets the lab shut down and investigated. when Irregular AI causes (arguably manufactures) incidents for Google, OpenAI, Meta, and Microsoft, it is rewarded with a billion dollar valuation instead of being sued or shut down or such.

indeed, if it was a human employee at the company who did those actions (and with all the information we have, it could have been a human employee, though i don't care too much to speculate), they would be in great trouble. it's notable that our anthropomorphism stops when it comes to assigning guilt for one's employees.

## On AI and Science Fiction

frequently in discussions of AI safety, threats akin to Skynet from the Terminator films, The Matrix, or similar science fiction films are brought up. there are a few reasons to discuss the playing field created by these comparisons.

### robot overlords are by design outside our episteme

both of these (and similar cases of the trope in general) are designed so as to be beyond our understanding. we perceive these from the outside in. we are at first introduced to The Terminator as a great evil. the great evil is tackled and defeated to some degree. we understand it first as an adversary and second as a "technology in the motions of everything else that was happening when it was created".

this is similar to a paradox in study of history, where our present understanding of the past biases / tints our understanding of what the past was like. in a similar way, we don't have a script for the person who booted up Skynet. if Skynet occurs in reality, there will be a person who booted up Skynet. they will have a script and a set of reasons, and these analogies don't prepare us for that. to fill in the gaps, analysts speculate that the human / organisational agent will be acting in an undoubtedly benign way, and the machine will interpret it as an undoubtedly malicious action.

> as an aside, i'm not fresh on the lore of these film series. i'm sure they do their good part of worldbuilding to make the machine's actions make sense. this is why i clarified that we are biased, not entirely incorrect.

### a narrative is an oligopoly of agency

stories, whether for pragmatic reasons, constraints of the medium, or to cater to the lizard brain, only involve a few actors. the Terminator only involves two or so terminators. Skynet is a single network. this limitation comes from the form factor of the film and is less-so shared by longer formats like novels.

as science fiction is limited in agents, it often (though not necessarily) requires technological solutions for technological problems. this works well for the stories themselves, but limits our worldview when we use these as analogies to understand real life. real-life science has more dimensions than intellect and innovation. how a technology is implemented is not decided by who the smartest person is, but the myriad incentives around taking a business to market.

the story of the DeLorean (the singular time travelling machine) is of a much different form than the story of the DeLorean (the car in real life). likewise, with LLMs, a transcendent omnipotent machine makes for somewhat compelling fiction, but does not reflect upon the constraints of reality.

> often in a narrative "techno-solutions" require non-technical growth on behalf of the characters, but in-narrative the character growth is means to the end of the techno-solution.

this is to say, using the lens of science fiction limits us to thinking of techno-solutions for techno-problems. while a single pilot can blow up the Death Star, such agency is not merited to the folks at Anthropic and the like. ideal corrective actions for LLM-related mishaps fall on a large domain of professions. alignment as a catch-all solution is built on this illusion of techno-solutionist agency.

### Terminator is a movie made by people who think terminators are badass

Assimov's robots and such are often a threat to humans, but implicit in this trope (robots becoming human in some fashion) is a liberatory message. it follows a long history of narratives about outcasts and ostracised persons establishing their place in normal society. the people who made the Terminator films put a lot of effort into ensuring the machines _look cool_ to the people watching. so when i say a machine is "like Skynet", i'm making a claim of terror, but i'm making an equal claim of grandiosity.

### Aside: dissonance, criti-hype, and N-person gestalts

imagine a fictional entity E. this entity has a proponent person P and a critical person C. P spends great lengths of time talking about how capable and powerful this entity E is. C listens to this, and understanding its power (its capacities), perceives an equivalently potent threat posed by E. due to an overestimation of risk and incompleteness of communication, they develop an entity E+1 in their head with higher capacities and threats than actually true (it would be reasonable to err on the side of overestimating risks.)

a third party T listening to this criticism imagines that E is in-fact E+1. they may very well be interested in E for its merits. P, realising an opportunity here, adjusts their claim to suggest E+1 is true, as is expected of them by T (as per social conventions or financial obligations). this becomes a positive feedback loop. when the P-C-T gestalt stabilises (a fancy way of saying the consensus between them), we have an incredibly exaggerated version of E in both its capacities and threats.

AI is far from the first feedback loop of this kind. Gamification existed because some people in design thought it was cool. people added it to their codebases haphazardly. before any real merit or demerit was observed, people noticed the gamification and got rightly concerned by it. many thinking heads made a ruckus about how it was a violation of user safety and made horrible coercement incentives. marketing professionals read about this and saw a great opportunity for coercing users (that really being their entire job). so on and so forth.

a similar gestalt is observed with mob organisations and political parties. the fear of their crimes is an important part of instilling their inevitability. the fear convinces one of their power, and enactment of power creates fear. in reality two armed assailants cannot subdue an entire crowd, were the crowd intent on opposing them collectively.

this is mostly trivial. the more interesting version of this gestalt is observed when all parties are collaborating. inside a company people form different positions without opposition as such. their conflicting views can create a similar spectre.

team A builds and team B are building two different parts of a tool. every time the tool fails, they are exposed to each other's shortcomings. on a good day they don't have to think about each other. considering that the project is irreparably broken, they put less effort into it. over time, the quality of the project degrades through no reason except misunderstanding. the reality is team A and team B are capable of doing decent work, but they choose not to.

a similar gestalt may be observed in one person alone. a person, acting as representative of a team, an organisation, a family, justifies their power and mercy against it each other. unenacted power becomes mercy / kindness, which reinforces potential power. one is convinced that they are stronger than they actually are.

## Retroactive narratives

i say these are retroactive narratives because much of our language around AI Safety is applying Yudkowsky / Bostrom writings from over a decade ago on technology that is very different from what they conceived. a more serious textual analysis would require me to actually read their books which would make me lose my mind.

### AGI

AGI is a goalpost that is by definition impossible to meet. the criterion to decide if a machine is AGI is not "how well it can mimic a human", but "how shocked the reader is by its human-ness". it's flawed similarly to how Turing tests are. as soon as a machine can perform some human-like behaviour, our expectations for human-ness shift.

AGI is a meaningless reuse of "Strong AI" before it, and just "AI" before that. the term means nothing as it is unfalsifiable. we will never know when a machine is AGI and when it isn't. person A says GPT 3 was AGI. person B says Google Search is AGI. person C says ELIZA is AGI.

insofar as the challenge is surpassing human capabilities in "all domains", one could tape together a calculator, a search engine, and a few other such tools with a lightweight proxy and call it AGI. for all i'm concerned, Siri outperforms humans in a plethora of domains.

### Safety

AI Safety is the belief that risk management starts and ends at ensuring an LLM does what you tell it to do. this is short-sighted for the myriad reasons listed above, and it's irresponsible on the behalf of AI labs and tech journalists (a domain so rife with incompetence i sometimes wish it did not exist at all) to pretend that it is.

so far i've described a pattern of blowing issues out of proportion so as to make a smokescreen to cloak other more relevant issues. AI safety has no mechanism, explanation, or terminology to explain what happens when AmericaGPT hacks into a phone when it is explicitly asked to. superintelligence has no mechanism to explain what to do when control of critical health / security / economic tooling is given willingly to the machine. this is not a failure of the system, it's its pitch.

### the singularity is apocalypticism for accelerationists

an event set indeterminably far in the future. most people don't know what the singularity is or what it means. it is a scenario in which AI's do, like everything. breaking down the singularity into smaller singularities reveals its hollowness.

i can only imagine its a projection borne from tech-city workers who only see white-collar jobs happening in their vicinity. "robots" exist, but ultimately manual labour continues to be done by-and-large by humans. economically speaking it is far more effective to make tools that augment human productivity (say tractors or trucks) than it is to replace them entirely. while automation can and has eroded jobs, a singularity is an outlandishly dystopian scenario.

automations of similar caliber historically have taken full decades before their impact is fully realised. technology being however advanced it is, the fruit seller still sells fruits. the platform being analog or digital or internet does not change that a real physical fruit has been grown and sold.

what we do observe in the present though, is mass layoffs across white-collar jobs. even shedding 10 or 20% (the reasons behind which are complicated and a topic of discussion for another day) puts us in a position of mass unemployment and disarray. software engineers hating their jobs after being made prompt-operators is an out-of-model risk for Google, Anthropic, Microsoft, OpenAI, and so on.

mass unemployment via permanent underclass is not a risk, it is the desired outcome. great filtering events across job industries are cases of simultaneous horror and joy (indeed, the horror is directly the source of joy). it is the same fear/enthusiasm perversion that possesses doomsday cultists. the filtering is a gamble. surviving the gamble demonstrates your virtue, in contrast to those who didn't. most companies that make contracts for LLM API workfows do so explicitly with cost-cutting in mind. this is an out-of-model risk, as "eliminating superfluous job" is a virtue under technofuturism.

### Pacing

"slowing down" is to be understood as slowing down in our approach towards the singularity ideal. implicit herein is our assumptions around what progress and regress mean. when AlphaCorp says progress, it means how much money its tools can make AlphaCorp, and by proxy how capable they are at performing parts of human jobs.

this straight line can be imagined as say, riding a bicycle up a hill. the risk in language around "pacing" is that the bicycle may cross the peak and fly to the moon (the phantom called Superintelligence), where it would be very much beyond our means of control.

instead of imagining pacing-contra-superintelligence, we can imagine pacing-contra-irresponsibility. in this setting, slowing down the bicycle is merely to ensure it doesn't fall off the cliff. a real-world equivalent to this analogy might be a Grok-mechahitler style of collapse.

### Longtermism

some fraud hacks trying really hard to pretend climate change and politics don't exist (perhaps aware that their ambitious AI projects would make it worse) decided there are bigger things to worry about like Roko's Basilisk, or as i prefer to call it Pascal's Microwaved Nachos. taking The Wager at face value (a wager not even capable of translating to a religiously pluralistic society) is embarrassingly silly.

pretending you can predict thousands of years in the future (let alone 20) is god-complex shit. anyone who studies finance seriously should know better.

## postscript

### gunmakers don't test bullet vests

AI labs being responsible for both offensive and defensive aspects of AI security is a pretty major conflict of interest. they have incentives to show that their products are capable of doing any kind of attack, so in the verbiage of their testing they often exaggerate the risks involved. they also are disincentivised from testing non-LLM tools (filesystem sandboxes, MCP access control, network control tools, so on) to constrain LLM activity.

it's irresponsible on the behalf of journalists to treat AlphaCorp's report as the last word on how to control and monitor the activity of AlphaCorp's tools.

### alignment is a good and important thing.

people use LLMs as tools. they are good at many things. an LLM understanding i want to do X when i want to do X is a good thing.

AlphaCorp's LLM being aligned is a good thing for AlphaCorp's business and its customers. AlphaCorp's LLM being aligned is not charity. it is not AlphaCrop selflessly saving the world from unrestricted weapons of math destruction. it is AlphaCorp trying to be a responsible business. it is not the frontier of philosophical and ethical thinking, though perhaps interesting linguistically. it is better for the world if AlphaCorp invests in its own LLM alignment. it is even better if people make public accessible resources to conduct these activities and examinations.

### Intellectual Property

this has nothing to do with the rest of the essay, but i find it laughable how US hegemons are flailing for regulatory capture much after their technologies have already been imitated by Chinese labs. any claims to intellectual property are gross given they trampled on news organisations / book publishers and such on their way to creating their tools.

six months ago Chinese labs were the reason why they couldn't slow investment in AI tooling. today the same Chinese labs are to be prohibited altogether over (business) risks and such. the other with no voice is a vessel for the self to express its own desires.

### but UBI fixes this

UBI is provided by the state. AI automation moves capital from labour to corporations. a call for UBI (preserving capital stability) is a call for increased corporate taxation. i believe proponents have largely not finished this train of thought.

### Sam Bankman Fried Happened

yeah
