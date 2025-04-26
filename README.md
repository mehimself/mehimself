# Max Roald Eckardt

I am Senior Software Engineer at the [Center for Hybrid Intelligence](https://mgmt.au.dk/center-for-hybrid-intelligence/). See my [CV on LinkedIn](https://www.linkedin.com/in/max-roald-eckardt-69706071/).

I will use these pages as a blog for thoughts on topics close to my interests. 

## Yann leCun's World Model at Home 
At Invidia GTC 2025 Yann LeCun excalaimed that he was "no longer so interested in LLMs anymore". Here is my take on why that is and what my personal approach to a economic evolution into the next gen genAI would be.

GPT-based LLMs have effectively solved language and even offer spurious reasoning. However, for many devevlopers the agentic AI experience feels like flirting with insanity because LLMs prioritize completion and syntactical integrity over rigorous reasoning and factual grounding. LRMs are essentially improvised architectures, cobbling together small reasoning capacities in meshed LLM runs to produce acceptable but poorly scalable results. The key challenge, therefore, is to manage complexity by breaking reasoning work into delegatable, manageable, and validatable (controllable) tasks and steps. GPTs excel at language generation but are less suited for abstract thinking in that language.

A more suitable solution for abstract thinking is symbolic reasoning with a world model. A world model maintains connections between knowledge and its abstractions (reasoning symbols), potentially aligned with reasoning traces:

```
- an apple is a physical object. 
- physical objects are governed by physical laws
- gravity is one of the physical laws
- tha apple is subject to forces such as gravitaional pull
```

These traces represent physical, social, phenomenological, and epistemological relationships to a knowledge term in varying degrees of abstraction. The goal is to form an alignment between entries and viable chain-of-thought pathways. In contrast, LLMs neither maintain explicit references to specific terms nor provide connections readily interpretable by human minds. They learn from written language, which often includes “poisonous” patterns for reasoning: figures of speech, sarcasm, creative writing, personal accounts, and similar that do not necessarily cohere into a unified model of the world.

Generating and maintaining a Vulcan-like account of humanity’s world promises more efficient navigation in the abstract plane of common-sense problem solving. To achieve this, we must disambiguate subjective accounts into objective (canonical) knowledge and terms that disambiguate in their abstract relationships. In the canonical representation, a higher temperature does not spark fringe perspectives but rather remains tied to abstract formalisms of the issue referenced in a prompt. Of course, this distinction is both debatable and problematic in certain domains, as evidenced by fx. Wikipedia article-editing wars.

We can still leverage the embeddings of LLMs and the (canonical-ish) synthesis achieved by LRMs. In practice, a LLM-informed Neural Network (LLMINN) might process a set of knowledge terms (e.g., an English dictionary) across a limited set of abstractions with anchor terms for human intelligibility. Its pipeline would escalate term processing strategies based on the criteria above, prompting an LRM or even requesting human input for particularly challenging or contested terms.

Knowledge indexing ultimately hinges on memory management. In social contexts, ground truth is neither static nor purely objective, which introduces data quality challenges and overheads. Abstract projections can mitigate some of these concerns, but evolving beyond a static snapshot requires synchronization work. Planting anchor terms to link key lemmas and symbols fosters explainability, browseable reasoning paths, and verifiable outputs.

The term “world model” thus describes an index of canonical terms and connections—focusing on quality rather than sheer scale by separating objective from subjective knowledge. Even processing miniscule or narrowly focused bodies of knowledge can streamline reasoning with moderately sized models. Subjective (even conflicting) terms can still be included for personalization, allowing world models to accommodate subtle biases in individual user contexts. This capability raises intriguing implications for the ethical use of AI going forward.

I have written knowledge integrators for formal and prosaic texts, typed data, and ephemeral events for online knowledge graph tech demos and find that these repositories will form the foundation of the next generation of AI applications. 

## Vibe Coding vs. Agentic Stack Maintenance
Vibe coding uses LRM for code generation. Due to above limitations to LRM prompt complexity (and other issues) it is not applicable to maintain projects above a (very low) maturity. I have developed agentic strategies with custom semantic index with feathered-abstractions and symbol/reference resolution as a tech demo. This is equivalent to a mini world model for a hyper-formalized code base. It looks over-engineered, but to limit complexity to a proactical degree dozens of design patterns, paradigms, best-practices, and preferences had to be specified.
