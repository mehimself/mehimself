# Max Roald Eckardt

I am Senior Software Engineer at the [Center for Hybrid Intelligence](https://mgmt.au.dk/center-for-hybrid-intelligence/). See my [CV on LinkedIn](https://www.linkedin.com/in/max-roald-eckardt-69706071/).

I will use these pages as a blog for commentary on topics close to my interests. 

## Yann leCun's World Model at Home 
At NVIDIA GTC 2025 Yann LeCun excalaimed that he was "not so interested in LLMs anymore." Here is my take on why that is and what my personal approach to a economic evolution into the next gen genAI would be.

GPT-based LLMs have effectively solved language and even offer spurious reasoning. However, for many devevlopers the agentic AI experience feels like flirting with insanity because LLMs prioritize completion and syntactical integrity over rigorous reasoning and factual grounding. Reasoning Models are essentially improvised architectures, cobbling together small reasoning capacities in meshed LLM runs to produce acceptable but poorly scalable results. The key challenge, therefore, is to manage complexity by breaking reasoning work into delegatable, manageable, and validatable (controllable) tasks and steps. GPTs excel at language generation but are less suited for abstract thinking in that language.

A more suitable solution for abstract thinking is symbolic reasoning with a world model. A world model maintains connections between knowledge and its abstractions (reasoning symbols), potentially aligned with reasoning traces:

- an apple is a physical object. 
- physical objects are governed by physical laws
- gravity is one of the physical laws
- tha apple is subject to forces such as gravitaional pull

These traces represent physical, social, phenomenological, and epistemological relationships to a knowledge term in varying degrees of abstraction. The goal is to form an alignment between entries and viable chain-of-thought pathways. In contrast, LLMs neither maintain explicit references to specific terms nor provide connections readily interpretable by human minds. They learn from written language, which often includes “poisonous” patterns for reasoning: figures of speech, sarcasm, creative writing, personal accounts, and similar that do not necessarily cohere into a unified model of the world.

Generating and maintaining a Vulcan-like account of humanity’s world promises more efficient navigation in the abstract plane of common-sense problem solving. To achieve this, we must disambiguate subjective accounts into objective (canonical) knowledge and terms that disambiguate in their abstract relationships. In the canonical representation, a higher temperature does not spark fringe perspectives but rather remains tied to abstract formalisms of the issue referenced in a prompt. Of course, this distinction is both debatable and problematic in certain domains, as evidenced by fx. Wikipedia article-editing wars.

We can still leverage the embeddings of LLMs and the (canonical-ish) synthesis achieved by reasoning models. In practice, a LLM-informed Neural Network (LLMINN) might process a set of knowledge terms (e.g., an English dictionary) across a limited set of abstractions with anchor terms for human intelligibility. Its pipeline would escalate term processing strategies based on the criteria above, prompting a reasoning model or even requesting human input for particularly challenging or contested terms.

Knowledge indexing ultimately hinges on memory management. In social contexts, ground truth is neither static nor purely objective, which introduces data quality challenges and overheads. Abstract projections can mitigate some of these concerns, but evolving beyond a static snapshot requires synchronization work. Planting anchor terms to link key lemmas and symbols fosters explainability, browseable reasoning paths, and verifiable outputs.

The term “world model” thus describes an index of canonical terms and connections—focusing on quality rather than sheer scale. They resolve terms and realtionships as  intelligible annotated structures. Processing even miniscule or narrowly focused bodies of knowledge can streamline reasoning with moderately sized models. Subjective (even conflicting) terms can still be included for personalization, allowing world models to accommodate subtle biases in individual user contexts. (This capability raises intriguing implications for the ethical use of AI going forward).

I have written knowledge integrators for formal reference- and verbose texts, typed data, highly structured data, and ephemeral events for online knowledge graph tech demos and found that custom knowledge graphs form the foundation for the next generation of AI applications. 

Especially deeply structural data, such as Abstract Syntax Trees (AST) cross referenced with scope annotations and symbol-reference tracing, offer an extremely promising reduction in complexity by offering navigatable and selectable textures. This stabilizes reasoning with genAI models and supports sustained agentic code maintenance with a developer piloting it. The setup requires an experienced programmer / architect.

## Vibe Coding vs. Agentic Code Maintenance
Vibe coding uses LLMs or reasoning models (LRMs) for code generation. With democratized access to these tools, we can create functional applications in minutes, or maybe within a few hours of chatting. So, what prevents vibe coding from scaling into production?

I’m a full-stack developer who has felt the pressure to work “quick and dirty” first, then scale apps into production later since I started learning the craft in the 90s. Software users and programming learners often judge software based on functionality alone. They aim to implement the features first, then upgrade the code later for security, scalability, and compatibility.

However, code doesn’t scale linearly. There is no set of keywords, wrappers, or patterns that can just “plug in” security or performance. If you ask a generative AI tool to refactor code with these concerns in mind, you often end up with a completely rewritten codebase, destroying your cognitive grasp of it.

If app functionality is the payload and your source code is the vehicle, why can’t security and performance be added later? Because these are __qualities__, not _features_. They must be addressed globally and persistently, not just layered on. You need to consider them in your architecture and defend them over time. A single hole undermines security; a single bottleneck undermines performance. And production code requires even many more qualities beyond these two.

The hardest part of programming is learning, formalizing, and maintaining best practices—using a language’s features and trusted libraries without compromising these qualities. You can implement the same functionality in thousands of ways, but 99.9% will undermine some code quality. The overhead of writing and deploying production-grade code is immense. On complex projects, it can take days to “tune in” to the solution space.

But does this mean all generated code is poor quality? Is production-grade code out of reach for generative models? Are humans inherently better at managing complexity? No. I can’t remember all the considerations that shaped a function I wrote two weeks ago. I still look up design patterns. I make mistakes. Generative code could, in theory, address these human lapses.

How might generative AI produce production-grade code? Consider what makes generative AI powerful for software development in the first place: it reads our natural language and outputs functioning code. If you ask it carefully, it can even incorporate best-practice design patterns for a few concerns. This still requires an experienced developer to guide it. Why not write a “book of best practices” for your production environment and create an agent that references those practices?

GPT models (LLM/LRM) are excellent at text generation—primarily retrieval with some reasoning. They reproduce and synthesize typical text well. The biggest limitation is prompt complexity. Early GPT models struggled with more than five concerns at once (e.g., a database query that filters, sorts, paginates, and counts matched documents). Today’s models handle more complexity but still degrade quickly as complexity grows. In practice, a few hundred lines of code can become expensive and unreliable to edit.

Determine Compatibility With Projected Behavior and Guidelines
Whenever you’re introducing new functionality or refactoring existing code, it’s vital to determine its compatibility with the project’s future behavior and standards. Before adding features or addressing new requirements, developers need to confirm that the underlying architecture supports them without breaking current contracts or best-practice guidelines. This means revisiting fundamental assumptions about data flow, security posture, and performance expectations. By proactively examining these aspects, teams can avoid costly rework and ensure the code remains robust as demands evolve.

Stay Predictable and Stereotypical for Best Results
Generative AI tools excel at producing “stereotypical” patterns—code structures that follow common practices. Maintaining predictable, recognizable patterns can significantly reduce confusion, both for the tools and for human developers. While creativity in development has its place, adhering to well-known conventions helps automated or semi-automated systems recognize the relevant context, prevents misunderstandings, and makes it easier to swap tools or library implementations later. By staying within these familiar patterns, you allow generative AI (and other developers) to operate with more accuracy and reliability.

Test-Driven, Piloted, Not Fully-Automated Development
When it comes to sustaining high-quality code, a test-driven and piloted approach is critical. No matter how sophisticated generative tools become, software quality isn’t fully automatable. All it takes is a single oversight or an overlooked user scenario to introduce a fatal flaw. Continuous integration, test-driven development, and diligent pilot-testing of newly generated features are essential to catch these potential failures before they reach production. Requirements can change at any time, and a human-in-the-loop process ensures ongoing alignment between evolving user needs and the codebase. By mixing automated generation with hands-on testing and piloting, developers maintain control over quality while still leveraging the speed and adaptability of generative AI.

So, how do we use these reasoning models for high-quality, scalable development? We need an agent that __thinks like a developer__ while minimizing prompt complexity. Once we upload our “book of best practices” to vector storage and set a concise system prompt, we must approach prompted work systematically. Break the work into tasks, and resolve each task into refactoring strategies. These strategies involve nine parts navigation and delimitation, and one part code replacement. When targeting a change in behavior, isolate the relevant symbols, their referencing contexts, and the behaviors they implement, refactor the code, re-index, diff files, and summarize the changes in the threat. _Commit_, _revisit_, or _revert_ changes based on user response. The delimitation of code I am most comfortable being left to human pilots, since the most advanced models undergo subtle changes and occasional disconnects and after all: Our payload is a user's experience. So with a little more tooling Vibe coding ought to be __helping a developer think__ by laying out his work and automating the tediuos navigation and scope retrieval and leaving the creative considerations to human developers.  



