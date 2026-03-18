<style>
	@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;700&family=IBM+Plex+Mono:wght@400;500&display=swap');

	:root {
		--bg: #090d12;
		--bg-soft: #111822;
		--panel: #0f1721;
		--panel-border: #273446;
		--text: #e6edf6;
		--muted: #8f9fb3;
		--accent: #54c7ff;
		--accent-soft: rgba(84, 199, 255, 0.15);
		--success: #66e3a4;
	}

	html {
		scroll-behavior: smooth;
	}

	body {
		margin: 0;
		font-family: 'Space Grotesk', sans-serif;
		background:
			radial-gradient(circle at 12% 8%, rgba(84, 199, 255, 0.16), transparent 35%),
			radial-gradient(circle at 88% 20%, rgba(102, 227, 164, 0.1), transparent 30%),
			linear-gradient(180deg, #090d12 0%, #0a0f15 100%);
		color: var(--text);
		line-height: 1.65;
	}

	.page {
		max-width: 1100px;
		margin: 0 auto;
		padding: 1.25rem;
	}

	.top-nav {
		position: sticky;
		top: 0;
		z-index: 20;
		margin: 0.5rem 0 1.25rem;
		background: rgba(9, 13, 18, 0.85);
		border: 1px solid rgba(84, 199, 255, 0.2);
		border-radius: 14px;
		backdrop-filter: blur(10px);
	}

	.top-nav ul {
		list-style: none;
		margin: 0;
		padding: 0.85rem 1rem;
		display: flex;
		gap: 1rem;
		overflow-x: auto;
	}

	.top-nav a {
		color: var(--muted);
		text-decoration: none;
		font-size: 0.92rem;
		white-space: nowrap;
		transition: color 0.2s ease;
	}

	.top-nav a:hover {
		color: var(--accent);
	}

	.hero {
		position: relative;
		overflow: hidden;
		padding: 5rem 2rem;
		border: 1px solid var(--panel-border);
		border-radius: 22px;
		background: linear-gradient(135deg, rgba(15, 23, 33, 0.95), rgba(13, 19, 29, 0.9));
		box-shadow: 0 18px 60px rgba(0, 0, 0, 0.35);
		animation: floatIn 0.85s ease;
	}

	.hero::before {
		content: '';
		position: absolute;
		inset: 0;
		pointer-events: none;
		background: linear-gradient(120deg, transparent 0%, rgba(84, 199, 255, 0.08) 50%, transparent 100%);
	}

	.eyebrow {
		display: inline-flex;
		align-items: center;
		gap: 0.55rem;
		margin-bottom: 1rem;
		color: var(--accent);
		font-size: 0.85rem;
		letter-spacing: 0.06em;
		text-transform: uppercase;
	}

	.eyebrow::before {
		content: '';
		width: 30px;
		height: 1px;
		background: var(--accent);
	}

	h1 {
		margin: 0;
		font-size: clamp(2rem, 6vw, 3.4rem);
		line-height: 1.2;
		letter-spacing: -0.02em;
	}

	.subtitle {
		margin-top: 1rem;
		color: var(--muted);
		font-size: clamp(1rem, 2.7vw, 1.3rem);
	}

	.hero-links {
		margin-top: 2rem;
		display: flex;
		flex-wrap: wrap;
		gap: 0.85rem;
	}

	.btn {
		display: inline-flex;
		align-items: center;
		gap: 0.45rem;
		text-decoration: none;
		font-weight: 500;
		padding: 0.7rem 1.1rem;
		border-radius: 10px;
		border: 1px solid transparent;
		transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease;
	}

	.btn-primary {
		color: #061019;
		background: linear-gradient(90deg, #54c7ff, #72f1bb);
	}

	.btn-secondary {
		color: var(--text);
		border-color: var(--panel-border);
		background: rgba(17, 24, 34, 0.65);
	}

	.btn:hover {
		transform: translateY(-2px);
		box-shadow: 0 8px 18px rgba(84, 199, 255, 0.18);
		border-color: var(--accent);
	}

	.section {
		margin-top: 1.4rem;
		padding: 2rem;
		border-radius: 18px;
		border: 1px solid rgba(143, 159, 179, 0.2);
		background: rgba(15, 23, 33, 0.75);
		animation: fadeUp 0.9s ease both;
	}

	.section h2 {
		margin-top: 0;
		font-size: 1.5rem;
		color: #f2f7ff;
	}

	.section h3 {
		margin-top: 1.5rem;
		margin-bottom: 0.45rem;
		font-size: 1.08rem;
		color: #dce7f5;
	}

	.section p {
		margin: 0.65rem 0;
		color: var(--muted);
	}

	.section ul {
		margin: 0.6rem 0;
		color: var(--muted);
	}

	code {
		font-family: 'IBM Plex Mono', monospace;
		font-size: 0.88rem;
		background: rgba(84, 199, 255, 0.1);
		color: #a8e5ff;
		padding: 0.18rem 0.4rem;
		border-radius: 6px;
	}

	pre {
		margin: 1rem 0;
		border: 1px solid rgba(84, 199, 255, 0.2);
		border-radius: 12px;
		padding: 1rem;
		overflow-x: auto;
		background: #0a1119;
		box-shadow: inset 0 0 0 1px rgba(84, 199, 255, 0.05);
	}

	pre code {
		background: transparent;
		color: #cce8ff;
		padding: 0;
	}

	.grid {
		display: grid;
		gap: 1rem;
	}

	.grid-3 {
		grid-template-columns: repeat(3, minmax(0, 1fr));
	}

	.card {
		border: 1px solid rgba(84, 199, 255, 0.18);
		border-radius: 14px;
		padding: 1rem;
		background: linear-gradient(170deg, rgba(17, 24, 34, 0.95), rgba(12, 18, 26, 0.85));
	}

	.card h4 {
		margin: 0;
		font-size: 1.04rem;
		color: #e9f4ff;
	}

	.card p {
		margin: 0.55rem 0 0;
		font-size: 0.95rem;
	}

	.highlight {
		position: relative;
		overflow: hidden;
	}

	.highlight::after {
		content: '';
		position: absolute;
		width: 140px;
		height: 140px;
		right: -40px;
		bottom: -55px;
		background: radial-gradient(circle, rgba(84, 199, 255, 0.23), transparent 70%);
	}

	.screenshot {
		min-height: 170px;
		display: flex;
		align-items: center;
		justify-content: center;
		border: 1px dashed rgba(143, 159, 179, 0.45);
		border-radius: 12px;
		color: #99adc4;
		background: rgba(9, 13, 18, 0.75);
		font-family: 'IBM Plex Mono', monospace;
		font-size: 0.85rem;
	}

	table {
		width: 100%;
		border-collapse: collapse;
		margin-top: 0.9rem;
		font-size: 0.95rem;
	}

	th,
	td {
		text-align: left;
		padding: 0.85rem 0.7rem;
		border-bottom: 1px solid rgba(143, 159, 179, 0.2);
	}

	th {
		color: #d5e6fa;
		font-weight: 600;
	}

	td {
		color: var(--muted);
	}

	.status {
		display: inline-flex;
		align-items: center;
		gap: 0.35rem;
		font-size: 0.85rem;
		padding: 0.2rem 0.5rem;
		border-radius: 999px;
		border: 1px solid rgba(102, 227, 164, 0.4);
		color: #bff6dc;
		background: rgba(102, 227, 164, 0.08);
	}

	.status::before {
		content: '';
		width: 8px;
		height: 8px;
		border-radius: 999px;
		background: var(--success);
	}

	.footer {
		text-align: center;
		color: #7f90a8;
		margin: 2rem 0 0.7rem;
		font-size: 0.92rem;
	}

	@keyframes floatIn {
		from {
			opacity: 0;
			transform: translateY(24px);
		}

		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	@keyframes fadeUp {
		from {
			opacity: 0;
			transform: translateY(20px);
		}

		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	@media (max-width: 900px) {
		.grid-3 {
			grid-template-columns: 1fr 1fr;
		}

		.section {
			padding: 1.35rem;
		}

		.hero {
			padding: 2.8rem 1.25rem;
		}
	}

	@media (max-width: 640px) {
		.page {
			padding: 0.9rem;
		}

		.grid-3 {
			grid-template-columns: 1fr;
		}

		h1 {
			font-size: 1.9rem;
		}

		.top-nav ul {
			padding: 0.8rem;
			gap: 0.8rem;
		}

		th,
		td {
			padding: 0.7rem 0.45rem;
		}
	}
</style>

<div class="page">
	<nav class="top-nav" aria-label="Section navigation">
		<ul>
			<li><a href="#introduction">Introduction</a></li>
			<li><a href="#getting-started">Getting Started</a></li>
			<li><a href="#first-contribution">First Contribution</a></li>
			<li><a href="#technical-deep-dive">Technical Deep Dive</a></li>
			<li><a href="#challenges">Challenges</a></li>
			<li><a href="#solution-approach">Solution</a></li>
			<li><a href="#highlights">Highlights</a></li>
			<li><a href="#screenshots">Screenshots</a></li>
			<li><a href="#reflections">Reflections</a></li>
			<li><a href="#timeline">Timeline</a></li>
		</ul>
	</nav>

	<header class="hero">
		<span class="eyebrow">GSoC Progress Log</span>
		<h1>My Journey Contributing to LLM4S</h1>
		<p class="subtitle">Open Source | GSoC Aspirant | Backend Engineering</p>
		<div class="hero-links">
			<a class="btn btn-primary" href="https://github.com/deepak2k03" target="_blank" rel="noreferrer noopener">GitHub</a>
			<a class="btn btn-secondary" href="https://www.linkedin.com/in/deepak-singh-1b8590257/" target="_blank" rel="noreferrer noopener">LinkedIn</a>
		</div>
	</header>

	<section id="introduction" class="section">
		<h2>1. Introduction</h2>
		<p>
			LLM4S is an open source initiative focused on building practical, reliable systems powered by large language models.
			The project combines software engineering principles with applied AI to create tools that are maintainable,
			testable, and production-ready.
		</p>
		<p>
			This work is important because it bridges the gap between research-grade LLM experiments and real-world software,
			where performance, observability, and clean architecture matter as much as model outputs.
		</p>
	</section>

	<section id="getting-started" class="section">
		<h2>2. Getting Started</h2>
		<p>
			My first week focused on setup and orientation. I forked the repository, cloned it locally, configured the development environment,
			scanned the folder structure, and ran the first working example to validate the setup.
		</p>
		<pre><code>git clone https://github.com/your-username/llm4s.git
cd llm4s
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python examples/first_run.py</code></pre>
		<p>
			This process helped me understand core entry points, dependency management, and where to begin contributing confidently.
		</p>
	</section>

	<section id="first-contribution" class="section">
		<h2>3. First Contribution</h2>
		<h3>Problem</h3>
		<p>
			The README had useful information but the onboarding path was hard to follow for first-time contributors.
			Key setup instructions were spread out and some steps lacked context.
		</p>
		<h3>Approach</h3>
		<p>
			I restructured the README flow with clearer section ordering, improved wording, and concise setup guidance to reduce friction for newcomers.
		</p>
		<h3>PR Link</h3>
		<p><a href="#" aria-label="First contribution PR">Add PR link here</a></p>
		<h3>Key Learnings</h3>
		<ul>
			<li>Documentation quality directly impacts contributor velocity.</li>
			<li>Small, high-signal PRs are the best way to build trust early.</li>
			<li>Clear commit messages and context reduce review cycles.</li>
		</ul>
	</section>

	<section id="technical-deep-dive" class="section">
		<h2>4. Technical Deep Dive</h2>
		<h3>Module Overview</h3>
		<p>
			I mapped modules by responsibility: API/entry layer, orchestration layer, service integrations, and shared utilities.
			This made it easier to reason about where each fix belongs.
		</p>
		<h3>Data Flow</h3>
		<p>
			A typical request flows from controller to processing pipeline, through validation and model-service coordination,
			and then back through formatting and response handlers.
		</p>
		<h3>Important Services</h3>
		<p>
			The most critical services include inference orchestration, configuration loading, logging/telemetry,
			and storage adapters that preserve context between operations.
		</p>
	</section>

	<section id="challenges" class="section">
		<h2>5. Challenges Faced</h2>
		<ul>
			<li>Debugging dependency conflicts across local and project-specific environments.</li>
			<li>Understanding the control flow in unfamiliar modules.</li>
			<li>Fixing environment-specific setup issues during initial runs.</li>
			<li>Interpreting error traces when failures propagated across multiple services.</li>
		</ul>
	</section>

	<section id="solution-approach" class="section">
		<h2>6. Solution Approach</h2>
		<p>
			I used a disciplined feedback loop: read docs first, inspect existing issues and PR discussions,
			ask focused questions to maintainers, and iterate in small patches with quick validation.
			This reduced uncertainty and improved the quality of each revision.
		</p>
	</section>

	<section id="highlights" class="section">
		<h2>7. Highlights</h2>
		<div class="grid grid-3">
			<article class="card highlight">
				<h4>First Merged PR</h4>
				<p>Delivered a documentation-focused contribution that improved onboarding clarity for new developers.</p>
			</article>
			<article class="card highlight">
				<h4>Codebase Understanding</h4>
				<p>Developed a strong mental model of project architecture, data flow, and service boundaries.</p>
			</article>
			<article class="card highlight">
				<h4>Open Source Collaboration</h4>
				<p>Learned to communicate changes effectively through issue context, PR notes, and review iteration.</p>
			</article>
		</div>
	</section>

	<section id="screenshots" class="section">
		<h2>8. Screenshots</h2>
		<div class="grid grid-3">
			<div class="card">
				<h4>Setup Snapshot</h4>
				<div class="screenshot">Add setup screenshot</div>
			</div>
			<div class="card">
				<h4>Code/PR View</h4>
				<div class="screenshot">Add PR/code screenshot</div>
			</div>
			<div class="card">
				<h4>Feature Output</h4>
				<div class="screenshot">Add output screenshot</div>
			</div>
		</div>
	</section>

	<section id="reflections" class="section">
		<h2>9. Reflections</h2>
		<p>
			This journey has strengthened how I break down ambiguous problems, communicate technical intent,
			and build solutions incrementally with feedback. Beyond coding, I have grown in engineering mindset:
			thinking in terms of maintainability, user impact, and collaboration quality.
		</p>
	</section>

	<section id="timeline" class="section">
		<h2>10. Timeline / Milestones</h2>
		<table>
			<thead>
				<tr>
					<th>Task</th>
					<th>Status</th>
					<th>Link</th>
				</tr>
			</thead>
			<tbody>
				<tr>
					<td>Repository setup and first run</td>
					<td><span class="status">Completed</span></td>
					<td><a href="#getting-started">View section</a></td>
				</tr>
				<tr>
					<td>README improvement PR</td>
					<td><span class="status">Completed</span></td>
					<td><a href="#">Add PR link</a></td>
				</tr>
				<tr>
					<td>Architecture deep dive notes</td>
					<td><span class="status">In Progress</span></td>
					<td><a href="#technical-deep-dive">View section</a></td>
				</tr>
			</tbody>
		</table>
	</section>

	<p class="footer">Built for my GSoC journey log on GitHub Pages.</p>
</div>
