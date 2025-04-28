# Max Roald Eckardt

I am Senior Software Engineer at the [Center for Hybrid Intelligence](https://mgmt.au.dk/center-for-hybrid-intelligence/). See my [CV on LinkedIn](https://www.linkedin.com/in/max-roald-eckardt-69706071/).

I use these pages as a blog for commentary on topics close to my interests. 

# Domain-Driven World Models
At NVIDIA GTC 2025 Yann LeCun excalaimed that he was "not so interested in LLMs anymore." He goes on appraising world model simulation-based AI models. What are the implications for software developers today?

## Beyond language - Symbolic Reasoning
GPT-based LLMs have effectively solved language and even offer spurious _reasoning_. However, for many developers the agentic AI experience feels like flirting with insanity. LLMs, the basic component of agentic AI tooling, heavily prioritize completion and syntactical integrity over _rigorous reasoning_ and _factual grounding_. 

Even "_Reasoning models_" are essentially improvised architectures, cobbling together small _reasoning capacities_ in meshed LLM runs to produce acceptable but poorly scalable results. The key challenge, therefore, is to manage complexity by breaking _reasoning work_ into delegatable, manageable, and validatable (controllable) tasks and steps. GPTs excel at language generation but are less suited for abstract thinking in that language. Optimally the reasoning model would be explainable.

One suitable solution for abstract thinking is _symbolic reasoning_ with a ___world model___. A ___world model___ maintains connections between knowledge and its abstractions (__reasoning symbols__), potentially aligned with __reasoning traces__ forming deduced and induced relationships:

- an __(apple)__ is a __(physical object)__ are governed by __(physical laws)__ featuring __(gravity)__
- thus __(gravity)__ applies to __{apples}__

These _traces_ represent physical, social, phenomenological, and epistemological relationships to a ___knowledge term___ in varying degrees of abstraction. The goal is to form an alignment between entries and viable chain-of-thought pathways. In contrast, LLMs neither maintain explicit references to specific ___terms___ nor provide connections readily interpretable by human minds. They learn from written language, which often includes “poisonous” patterns for reasoning: figures of speech, sarcasm, creative writing, personal accounts, and similar that do not necessarily cohere into a congruent core model of the world.

## Canonical Core
Generating and maintaining a Vulcan-like account of humanity’s world promises more efficient navigation in the abstract plane of common-sense problem solving. Such basic canonical techno-positivistic observations would form the core of our ___world model___. Here problem solving follows curved reasoning paths starting with a specific issue extrapolating into abstract ultimately _symbolic reasoning_ and arrives at potential specific solutions. This would service causal regression and heuristic approaches to problem solving. Higher temperature in the core lead to more abstract thinking allowing to evaluate increasingly abstract/symbolic reasoning for a given solution.

## Setting Life to the World Model
The Vulcan's impeccable logic does not serve wicked social issues though. Our ___world model___ needs to be lived in before we can attempt to address social issues. The challenge here is that our individually perceived realities do not align very well. To account for this, we must extend the technological positivistic (canonical) core with subjective accounts from individual users. These outer layers trace individual stakes and user experiences with deep connections to the core. Here higher temperature could extend search to multiple subjectivities aiming for better social fitness. 

## Explainability
In practice, a LLM-informed Neural Network (LLMINN) might process a set of ___knowledge terms___ (e.g., an English dictionary) across a limited set of abstractions with anchor ___terms___ for human intelligibility. Its pipeline would escalate term processing strategies based on the criteria above, prompting a reasoning model or even requesting human input for particularly challenging or ___contested terms___.

Knowledge indexing ultimately hinges on memory management. In social contexts, ground truth is neither static nor purely objective, which introduces data quality challenges and overheads. Abstract projections can mitigate some of these concerns, but evolving beyond a static snapshot requires synchronization work. Planting ___anchor terms___ to link key lemmas and symbols fosters explainability, regressible trees of thought, and testable outputs.

## Synergistic Compatibility
The notion “world model” thus describes an index of ___canonical and subjective terms___ and connections, focusing on quality rather than sheer scale. They resolve ___terms and relationships___ as intelligible annotated structures. The best thing about world models is their intuitive nature, modular extensible composition, and the affordance to be maintained, extended, and reviewed by human operators. Maximizing _intelligibility_ empowers us also to reach optimal reasoning with current LLMs with semantic retrievals. This allows us to: 

a) use current LLMs to integrate annotated knowledge graphs already today for specific use cases.
b) optimize reasoning in runs with today's LLMs 

Short of training such model with gigantic compute demands at home, we can contruct it as analog in a graph database fx. with neo4j and naturally integrate it as a RAG extension to any domain-driven LLM-based app. As a matter of fact, the requirement of online models with intelligible reasoning paths would be well supported by classically scaling hardware.

## Initial Experience 
I have conducted a series of experiments with MCP tooling to explore viable integration strategies across data types, and text document structures. I have written knowledge integrators for formal reference- and verbose texts, user-defined indexes for typed data, and custom digestion engines for highly structured data in streamed event architectures. 

Especially deeply structural data, such as Abstract Syntax Trees (AST) cross referenced with scope annotations and symbol-reference tracing, offer an extremely promising reduction in complexity by offering navigatable and selectable textures. This stabilizes reasoning with genAI models and supports sustained agentic code maintenance with a developer piloting it. The setup requires an experienced programmer / architect.



# Vibe Coding vs. Agentic Code Copilots
Vibe coding uses LLMs or reasoning models (LRMs) for code generation. With democratized access to these tools, we can create functional applications in minutes, or maybe within a few hours of chatting. So, what prevents vibe coding from scaling into production?

## Features vs. Qualities
As full-stack developer I have felt the pressure to work “quick and dirty” first, then scale apps into production later, since I started learning the craft in the 90s. Software users and programming learners often judge software based on functionality alone. They aim to implement the features first, then upgrade the code later for security, scalability, and compatibility.

However, code doesn’t scale linearly. There is no set of keywords, wrappers, or patterns that can just “plug in” security or performance. If you ask a generative AI tool to refactor code with these concerns in mind, you often end up with a completely rewritten codebase, destroying your cognitive grasp of it.

If app functionality is the payload and your source code is the vehicle, why can’t security and performance be added later? Because these are __qualities__, not _features_. They must be addressed globally and persistently, not just layered on. You need to consider them in your architecture and defend them over time. A single hole undermines security; a single bottleneck undermines performance. And production code requires even many more qualities beyond these two.

## Considered Complexity
The hardest part of programming is learning, formalizing, and maintaining best practices—using a language’s features and trusted libraries without compromising these qualities. You can implement the same functionality in thousands of ways, but 99.9% will undermine some code quality. The overhead of writing and deploying production-grade code is immense. On complex projects, it can take days to “tune in” to the solution space.

But does this mean all generated code is poor quality? Is production-grade code out of reach for generative models? Are humans inherently better at managing complexity? No. I can’t remember all the considerations that shaped a function I wrote two weeks ago. I still look up design patterns. I make mistakes. Generative code could, in theory, address these human lapses.

How might generative AI produce production-grade code? Consider what makes generative AI powerful for software development in the first place: it reads our natural language and outputs functioning code. If you ask it carefully, it can even incorporate best-practice design patterns for a few concerns. This still requires an experienced developer to guide it. Why not write a “book of best practices” for your production environment and create an agent that references those practices?

GPT reasoning models are excellent at text generation—primarily retrieval with limited reasoning. They reproduce and synthesize typical text well. The biggest limitation is considered complexity. Early GPT models struggled with more than five concerns at once (e.g., a database query that filters, sorts, paginates, and counts matched documents). Today’s reasoning models handle more complexity but lose stability as complexity grows. In practice, a few hundred lines of code can become expensive and unreliable to edit.

## Polite Programming with Paradigms
Whenever you’re introducing new functionality or refactoring existing code, it’s vital to maintain its compatibility with the project’s future behavior and standards. Before adding features or addressing new requirements, developers need to confirm that the underlying architecture supports them without breaking current contracts or best-practice guidelines. This means revisiting fundamental assumptions about data flow, security posture, and performance expectations. By proactively examining these aspects, teams can avoid costly rework and ensure the code remains robust as demands evolve. For this purpose programmers have summarized hard-learned lessons as paradigms. Personally, I find the most universally applicable ro be:
- Separation of Concerns / Occam's Razor
- Function Extraction (avoid flow disjunctions)
- Don't Repeat Yourself
- You ain't gonna need it (YAGNI)

Uncle Bob, a great source for such condensed experience labeled this style ___"Polite Coding"___, because it produces code that does not assume implicit knowledge to make sense to casual readers. The requirement to annotate production code often indicates poor architecture or code quality. There are distinct exceptions to this if quality concerns post programming guides excluding basic language features (like NASA's C guidelines). 

## Generation Guidelines
The point of above paradigms is to remove implicit knowledge form any given scope. Well-considered naming, intuitive flow routing, and typing should produce tidy, predictable, three-dimensional code projects. Fundamentally polite code is boring to read, cut into single-concern scopes and types, and predictable flow. When you feel that you can predict next lines, module names, and function headers, you are looking at polite code. The tokenization of your architecture into predictable scopes and interfaces are like doping for LLM-based software development runs. The contextual complexity plummets for scopes and symbol retrieval and scope-stack delimitation, and implicitly forms genereation guidelines for code generation. LLMs thrive on predictable patterns, any recurring quality issues can be addressed by maintaining explicit guidelines. In web development there is the unique opportunity to implement the entire stack in a single language (EcmaScript YYYY) which greatly reduces architectural, conceptual, and functional complexity.

## Limits of Automation
When it comes to sustaining high-quality code, a test-driven and piloted approach is critical. No matter how sophisticated generative tools become, software quality is not fully automatable with LLMs. It takes only a single hallucination, or temporary omission to introduce fundamental flaws. Continuous integration, test-driven development, and diligent pilot-testing of newly generated features are essential to catch these potential failures before they reach production. Requirements can change at any time, and a human-in-the-loop process ensures ongoing alignment between evolving user needs and the codebase. My best bet is to implement rigorous test-driven-development (TDD) with an agentic copilot TDD naturally enforces above paradigms and being with generative support could leave the quality control and creative freedom to the human pilot. Human piloting is essential 

## Experience
So, how do we use these reasoning models for high-quality, scalable development? For best cognitive support we need to globally minimize complexity. Break the work into tasks, and resolve each task into refactoring strategies. These strategies involve nine parts navigation and delimitation, and one part code replacement. When targeting a change in behavior: 

- isolate the relevant symbols
- trace their referencing contexts throughout the stack
- identify the behaviors they implement and how you want to change it
- refactor the code
- re-index
- diff mutated files
- summarize the changes in the thread
- _Commit_, _revisit_, or _revert_ changes based on user response

I think human piloting is essential. Especially reasoning models undergo subtle changes over time and have occasional disconnects and after all: Our payload is ___user experience___.  



