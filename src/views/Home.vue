<template>
  <div class="home">
    <header class="profile-header">
      <h1>Max Roald Eckardt</h1>
      <p class="subtitle">Senior Software Engineer at the <a href="https://mgmt.au.dk/center-for-hybrid-intelligence/" target="_blank">Center for Hybrid Intelligence</a></p>
      <p>See my <a href="https://www.linkedin.com/in/max-roald-eckardt-69706071/" target="_blank">CV on LinkedIn</a></p>
      <p class="intro">I use this page as a blog for commentary on topics close to my interests.</p>
    </header>

    <nav class="blog-nav">
      <h2>Recent Posts</h2>
      <ul>
        <li><a href="#domain-driven" @click="scrollTo('domain-driven')">Domain-Driven World Models</a></li>
        <li><a href="#ai-memory" @click="scrollTo('ai-memory')">AI and Memory</a></li>
      </ul>
    </nav>

    <main class="blog-content">
      <article id="domain-driven" class="blog-post">
        <h2>Domain-Driven World Models</h2>
        <p class="post-intro">At NVIDIA GTC 2025 Yann LeCun exclaimed that he was "not so interested in LLMs anymore." He goes on appraising world model simulation-based AI models. What are the implications for software developers today?</p>
        
        <section class="post-section">
          <h3>Beyond language - Symbolic Reasoning</h3>
          <p>GPT-based LLMs have effectively solved language and even offer spurious <em>reasoning</em>. However, for many developers the agentic AI experience feels like flirting with insanity. LLMs, the basic component of agentic AI tooling, heavily prioritize completion and syntactical integrity over <em>rigorous reasoning</em> and <em>factual grounding</em>.</p>
          
          <p>Even "<em>Reasoning models</em>" are essentially improvised architectures, cobbling together small <em>reasoning capacities</em> in meshed LLM runs to produce acceptable but poorly scalable results. The key challenge, therefore, is to manage complexity by breaking <em>reasoning work</em> into delegatable, manageable, and validatable (controllable) tasks and steps. GPTs excel at language generation but are less suited for abstract thinking in that language. Optimally the reasoning model would be explainable.</p>
          
          <p>One suitable solution for abstract thinking is <em>symbolic reasoning</em> with a <strong><em>world model</em></strong>. A <strong><em>world model</em></strong> maintains connections between knowledge and its abstractions (<strong>reasoning symbols</strong>), potentially aligned with <strong>reasoning traces</strong> forming deduced and induced relationships:</p>
          
          <ul>
            <li>an <strong>(apple)</strong> is a <strong>(physical object)</strong> are governed by <strong>(physical laws)</strong> featuring <strong>(gravity)</strong></li>
            <li>thus <strong>(gravity)</strong> applies to <strong>{apples}</strong></li>
          </ul>
          
          <p>These <em>traces</em> represent physical, social, phenomenological, and epistemological relationships to a <strong><em>knowledge term</em></strong> in varying degrees of abstraction. The goal is to form an alignment between entries and viable chain-of-thought pathways. In contrast, LLMs neither maintain explicit references to specific <strong><em>terms</em></strong> nor provide connections readily interpretable by human minds.</p>
        </section>

        <section class="post-section">
          <h3>Canonical Core</h3>
          <p>Generating and maintaining a Vulcan-like account of humanity's world promises more efficient navigation in the abstract plane of common-sense problem solving. Such basic canonical techno-positivistic observations would form the core of our <strong><em>world model</em></strong>. Here problem solving follows curved reasoning paths starting with a specific issue extrapolating into abstract ultimately <em>symbolic reasoning</em> and arrives at potential specific solutions.</p>
        </section>

        <section class="post-section">
          <h3>Setting Life to the World Model</h3>
          <p>The Vulcan's impeccable logic does not serve wicked social issues though. Our <strong><em>world model</em></strong> needs to be lived in before we can attempt to address social issues. The challenge here is that our individually perceived realities do not align very well. To account for this, we must extend the technological positivistic (canonical) core with subjective accounts from individual users.</p>
        </section>

        <section class="post-section">
          <h3>Explainability</h3>
          <p>In practice, a LLM-informed Neural Network (LLMINN) might process a set of <strong><em>knowledge terms</em></strong> (e.g., an English dictionary) across a limited set of abstractions with anchor <strong><em>terms</em></strong> for human intelligibility. Its pipeline would escalate term processing strategies based on the criteria above, prompting a reasoning model or even requesting human input for particularly challenging or <strong><em>contested terms</em></strong>.</p>
        </section>

        <section class="post-section">
          <h3>Synergistic Compatibility</h3>
          <p>The notion "world model" thus describes an index of <strong><em>canonical and subjective terms</em></strong> and connections, focusing on quality rather than sheer scale. They resolve <strong><em>terms and relationships</em></strong> as intelligible annotated structures. The best thing about world models is their intuitive nature, modular extensible composition, and the affordance to be maintained, extended, and reviewed by human operators.</p>
        </section>

        <section class="post-section">
          <h3>Initial Experience</h3>
          <p>I have conducted a series of experiments with MCP tooling to explore viable integration strategies across data types, and text document structures. I have written knowledge integrators for formal reference- and verbose texts, user-defined indexes for typed data, and custom digestion engines for highly structured data in streamed event architectures.</p>
          
          <p>Especially deeply structural data, such as Abstract Syntax Trees (AST) cross referenced with scope annotations and symbol-reference tracing, offer an extremely promising reduction in complexity by offering navigatable and selectable textures. This stabilizes reasoning with genAI models and supports sustained agentic code maintenance with a developer piloting it.</p>
        </section>
      </article>

      <article id="ai-memory" class="blog-post">
        <h2>AI and Memory</h2>
        <p>LLMs and reasoning will not in the foreseeable future achieve human-level productivity in knowledge work. This why the easiest pickings for end-user value lie in integrations. Frameworks incorporating genAI in their production logic rely on privileged curated knowledge.</p>
        
        <p>Moats are evaporating with decreased cost of production (software) systems, so your value lies increasingly in niche intelligence. Curation helps narrow foci for efficient reliable LLM prompts and action calling. How do you curate knowledge? What does that mean technically? What does it encompass to acquire knowledge? Are snapshots ok, or do you need to keep it updated? In real-time?</p>
      </article>
    </main>
  </div>
</template>

<script>
export default {
  name: 'Home',
  methods: {
    scrollTo(elementId) {
      const element = document.getElementById(elementId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    }
  }
}
</script>

<style scoped>
.home {
  max-width: 900px;
  margin: 0 auto;
  padding: 20px;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  line-height: 1.6;
  color: #333;
}

.profile-header {
  text-align: center;
  margin-bottom: 40px;
  padding: 30px 0;
  border-bottom: 2px solid #eee;
}

.profile-header h1 {
  font-size: 2.5em;
  margin-bottom: 10px;
  color: #2c3e50;
}

.subtitle {
  font-size: 1.2em;
  color: #7f8c8d;
  margin-bottom: 10px;
}

.intro {
  font-style: italic;
  color: #666;
  margin-top: 20px;
}

.blog-nav {
  background: #f8f9fa;
  padding: 20px;
  border-radius: 8px;
  margin-bottom: 30px;
}

.blog-nav h2 {
  margin-top: 0;
  color: #2c3e50;
}

.blog-nav ul {
  list-style: none;
  padding: 0;
}

.blog-nav li {
  margin: 10px 0;
}

.blog-nav a {
  color: #3498db;
  text-decoration: none;
  font-weight: 500;
  cursor: pointer;
}

.blog-nav a:hover {
  text-decoration: underline;
}

.blog-content {
  margin-top: 30px;
}

.blog-post {
  margin-bottom: 50px;
  padding-bottom: 30px;
  border-bottom: 1px solid #eee;
}

.blog-post:last-child {
  border-bottom: none;
}

.blog-post h2 {
  color: #2c3e50;
  font-size: 2em;
  margin-bottom: 15px;
  border-left: 4px solid #3498db;
  padding-left: 15px;
}

.post-intro {
  font-size: 1.1em;
  font-style: italic;
  color: #555;
  margin-bottom: 25px;
  padding: 15px;
  background: #f8f9fa;
  border-left: 4px solid #3498db;
}

.post-section {
  margin: 25px 0;
}

.post-section h3 {
  color: #34495e;
  font-size: 1.3em;
  margin-bottom: 15px;
  margin-top: 25px;
}

.post-section p {
  margin-bottom: 15px;
  text-align: justify;
}

.post-section ul {
  margin: 15px 0;
  padding-left: 25px;
}

.post-section li {
  margin: 8px 0;
}

a {
  color: #3498db;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

em {
  font-style: italic;
  color: #555;
}

strong {
  font-weight: bold;
  color: #2c3e50;
}

/* Responsive design */
@media (max-width: 768px) {
  .home {
    padding: 15px;
  }
  
  .profile-header h1 {
    font-size: 2em;
  }
  
  .blog-post h2 {
    font-size: 1.6em;
  }
  
  .post-section p {
    text-align: left;
  }
}
</style>