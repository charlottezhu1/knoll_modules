# Paper Intro Writing
## Details 
|  Key | Value|
| ------------- | ------------- |
| Description | Guidelines on how to write good paper introduction. |

### Introduction Guidelines
While there are many approaches to write an introduction, in Computer Science most of these approaches need to explain two things: (1) What is the problem, and (2) How are you solving it?

Follow the following paragraph-by-paragraph outline for an Introduction:

*Problem:*
What's the problem you're solving? Cite other work that helps motivate the problem. Make the reader feel the urgency of the problem, so that by the end of the paragraph they care a lot that someone finds a solution. 

Example topic sentence: We all want to build IoT applications that are responsive to our behaviors — for example, coffee machines that make coffee for us after we wake up, or phones that know not to ring while we're in meetings — but we lack the data to endow our algorithms with this information about our patterns and behaviors.


*Set up the bit*
This paragraph usually answers the question, "Why isn't this problem solved yet?" by setting up the bit that you're going to flip. The topic sentence typically summarizes existing approaches to solving the problem by articulating the bit that they share, and points out why those approaches and the bit more broadly hasn't been able to solve the problem. So, it's a brief summary of the most important related work — but it's a summary, not a survey, meaning that its goal is to set up the bit, not to cover everything. 

Example topic sentence: Existing solutions to this problem require manually authored rules (e.g., coffee is a morning drink, we drink morning drinks after we wake up), but the required manual effort results in incomplete data about human situations and behaviors.

*Flip the bit*
Here you introduce your insight by flipping the bit. The topic sentence of this paragraph is the thesis statement for the entire paper. It should lay out the big idea that you'll be pursuing. Spend this paragraph explaining your insight clearly, why it flips the bit that you set up, and what the implications of flipping that bit will be for the problem at hand. For the purposes of this assignment, it's fine to assume that your bit flip will work out — we all know that research is iterative and projects will evolve. 

Example topic sentence:
In this paper, we suggest that data mining a large dataset of modern fiction offers a promising alternative to manual annotation.

*Instantiate that bit flip in a solution*
At this point, the reader understands the idea that you're proposing, but it's still very high level. In this paragraph, map that idea onto a concrete instantiation. This is where you introduce the system you've built, the model you're creating, the study design, or whatever is the main artifact of your research, and how it instantiates that insight. 

Example topic sentence: We introduce Augur, a knowledge base that relates human activities and the objects around them by mining 1.8 billion words of modern fiction from the online writing community Wattpad into a vector space model for predicting human activities.

*Evaluate the solution*
A good introduction summarizes the evaluation that you performed to demonstrate that flipping the bit has the effects that you suspect. For the purposes of this assignment, ask yourself: how would you prove to a critical reader that flipping the bit has the effect you promised in solving the problem? 

Example topic sentence: To evaluate Augur's ability to predict human behaviors, we first compared Augur's predictions to human estimates of behaviors given the same inputs, and second performed a field deployment to test Augur's precision and recall in a realistic application.

*Implications* 
If you're right about this bit flip being the right way for the field to go, what implications will there be for the field? Don't overplay your hand here by stating that all of computing will shift, but do be clear and forceful in pushing the case as hard as you feel that the case warrants.

Example topic sentence: This work demonstrates that fiction can provide deep insight into the minutiae of human behavior, and that modern NLP algorithms can structure those minutiae into useful hooks for IoT applications.


This outline will depend a bit on the kind of paper you're writing. For example, start by answering: are you an old problem / new solution paper, or a new problem / old solution paper? Old problem / new solution papers already have a warrant for the problem, so that part of the Introduction is easy, but they need to argue for the solution very carefully since there's no warrant there. Similarly, new problem / old solution papers need to be extra careful to argue the problem persuasively, but they can draw on existing warrants for the solution and only argue for how they're adapting it to the problem.

Start by creating the outline for your Introduction, using only the topic sentences that you will eventually expand into full paragraphs. It means that you only have those six sentences to tell the entire story of your paper. So, you can't add any unnecessary detail or extra concepts, or those six sentences won't be possible for a reader to understand. Just like a pro swimmer makes no unnecessary motions as they focus all energy on executing a stroke, and just like a pro chess player makes no unnecessary moves as they focus their actions on enacting their strategy, your topic-sentence outline should introduce no unnecessary concepts or ideas as it focuses on explaining the project.

Now, to write the Introduction section itself! Each topic sentence becomes the anchor of a paragraph in your Introduction, and the rest of each paragraph should set out to prove the point made by that topic sentence. If you need to split a paragraph into multiple paragraphs to be clearer, do so — but keep the rough proportions of those original six paragraphs. (In other words, don't spend three paragraphs on the problem, then rush through everything else.)

Don't forget to cite any work you're referencing that motivates your problem, sets up the bit, or helps explain why the flip is a good idea.


### Introduction Example
How might we craft an interactive artificial society that reflects believable human behavior? From sandbox games such as The Sims to applications such as cognitive models and virtual environments, for over four decades, researchers and practitioners have envisioned computational agents that can serve as believable proxies of human behavior. In these visions, computationally powered agents act consistently with their past experiences and react believably to their environments.Such simulations of human behavior could populate virtual spaces and communities with realistic social phenomena, train people on how to handle rare yet difficult interpersonal situations, test social science theories, craft model human processors for theory and usability testing, power ubiquitous computing applications and social robots, and underpin non-playable game characters that can navigate complex human relationships in an open world.

However, the space of human behavior is vast and complex. Despite striking progress in large language models that can simulate human behavior at a single time point, fully general agents that ensure long-term coherence would be better suited by architectures that manage constantly growing memories as new interactions, conflicts, and events arise and fade over time while handling cascading social dynamics that unfold between multiple agents. Success requires an approach that can retrieve relevant events and interactions over a long period, reflect on those memories to generalize and draw higher-level inferences, and apply that reasoning to create plans and reactions that make sense in the moment and in the longer-term arc of the agent’s behavior.

In this paper, we introduce generative agents—agents that draw on generative models to simulate believable human behavior—and demonstrate that they produce believable simulacra of both individual and emergent group behavior. These agents draw a wide variety of inferences about themselves, other agents, and their environment. They create daily plans that reflect their characteristics and experiences, act out those plans, react, and re-plan when appropriate. They respond when the end user changes their environment or commands them in natural language. For instance, generative agents turn off the stove when they see that their breakfast is burning, wait outside the bathroom if it is occupied, and stop to chat when they meet another agent they want to talk to. A society full of generative agents is marked by emergent social dynamics where new relationships are formed, information diffuses, and coordination arises across agents. 

To enable generative agents, we describe an agent architecture that stores, synthesizes, and applies relevant memories to generate believable behavior using a large language model. Our architecture comprises three main components. The first is the memory stream, a long-term memory module that records, in natural language, a comprehensive list of the agent’s experiences. A memory retrieval model combines relevance, recency, and importance to surface the records needed to inform the agent’s moment-to-moment behavior. The second is reflection, which synthesizes memories into higher-level inferences over time, enabling the agent to draw conclusions about itself and others to better guide its behavior. The third is planning, which translates those conclusions and the current environment into high-level action plans and then recursively into detailed behaviors for action and reaction. These reflections and plans are fed back into the memory stream to influence the agent’s future behavior. 

This architecture suggests applications in multiple domains, from role-play and social prototyping to virtual worlds and games. In social role-play scenarios (e.g., interview preparation), a user could safely rehearse difficult, conflict-laden conversations. When prototyping social platforms, a designer could go beyond temporary personas to prototype dynamic, complex interactions that unfold over time. For this paper, we focus on the ability to create a small, interactive society of agents inspired by games such as The Sims. By connecting our architecture to a large language model, we manifest a society of twenty-five agents in a game environment. End users can observe and interact with these agents. If an end user or developer wanted the town to host an in-game Valentine’s Day party, for example, traditional game environments would require scripting tens of characters’ behavior manually. We demonstrate that, with generative agents, it is sufficient to simply tell one agent that she wants to throw a party. Despite many potential points of failure—the party planner must remember to invite other agents to the party, attendees must remember the invitation, those who remember must decide to actually show up, and more—our agents succeed. They spread the word about the party and then show up, with one agent even asking another on a date to the party, all from a single user-generated seed suggestion. 

We conducted two evaluations of generative agents: a controlled evaluation to test whether the agents produce believable individual behaviors in isolation, and an end-to-end evaluation where the agents interacted with each other in open-ended ways over two days of game time to understand their stability and emergent social behaviors. In the technical evaluation, we leverage a methodological opportunity to evaluate an agent’s knowledge and behavior by “interviewing” it in natural language to probe the agents’ ability to stay in character, remember, plan, react, and reflect accurately. We compared several ablations that limit agents’ access to memory, reflection, and planning. We observe that each of these components is critical to strong performance across these interview tasks. Across the technical and end-to-end evaluation, the most common errors arose when the agent failed to retrieve relevant memories, fabricated embellishments to the agent’s memory, or inherited overly formal speech or behavior from the language model.

In sum, this paper makes the following contributions: 
• Generative agents, believable simulacra of human behavior that are dynamically conditioned on agents’ changing experiences and environment.
• A novel architecture that makes it possible for generative agents to remember, retrieve, reflect, interact with other agents, and plan through dynamically evolving circumstances. The architecture leverages the powerful prompting capabilities of large language models and supplements those capabilities to support longer-term agent coherence, the ability to manage dynamically evolving memory, and recursively produce higher-level reflections. 
• Two evaluations, a controlled evaluation and an end-to-end evaluation, that establish causal effects of the importance of components of the architecture, as well as identify breakdowns arising from, e.g., improper memory retrieval. 
• Discussion of the opportunities and ethical and societal risks of generative agents in interactive systems. We argue that these agents should be tuned to mitigate the risk of users forming parasocial relationships, logged to mitigate risks stemming from deepfakes and tailored persuasion, and applied in ways that complement rather than replace human stakeholders in design processes.
