---
title: Resume
layout: landing
# description: 'Lorem ipsum dolor sit amet nullam consequa<br />sed veroeros. tempus adipiscing nulla.'
image: assets/images/campanile.jpg
nav-menu: true
---

<!-- Main -->
<div id="main">

<!-- One -->
<section id="one">
	<div class="inner">
		<header class="major">
			<h2>About Me</h2>
		</header>
		<p>I'm Abhi Ganesh: a Software Engineer, writer, and amateur everything else-er. This section describes some of my professional experiences! Feel free to click on each entry to see more details; reach out to me with any questions via the form in the footer!</p>
		<ul class="actions">
					<li><a href="assets/resume.pdf" class="button icon fa-download">Download my resume!</a></li>
					<li><a href="https://www.linkedin.com/in/abhiganesh" class="button icon fa-linkedin">Connect with me!</a></li>
		</ul>
	</div>
</section>

<!-- Two -->
<section id="two" class="spotlights">
	<section>
		<!-- <a href="generic.html" class="image">
			<img src="{% link assets/images/pic08.jpg %}" alt="" data-position="center center" />
		</a> -->
		<div class="content">
			<div class="inner">
				<header class="major">
					<h2>Education</h2>
				</header>
				<h3>University of California, Berkeley</h3>
					<p style="margin-left: 50px;">
					B.S. in Electrical Engineering and Computer Science <br>
					Minor in Creative Writing <br>
					Studied abroad in Rome and Copenhagen
					</p>
			</div>
		</div>
	</section>
	<!-- <section>
		<a href="generic.html" class="image">
			<img src="{% link assets/images/pic09.jpg %}" alt="" data-position="top center" />
		</a>
		<div class="content">
			<div class="inner">
				<header class="major">
					<h3>Oracle</h3>
				</header>
				<p>Nullam et orci eu lorem consequat tincidunt vivamus et sagittis magna sed nunc rhoncus condimentum sem. In efficitur ligula tate urna. Maecenas massa sed magna lacinia magna pellentesque lorem ipsum dolor. Nullam et orci eu lorem consequat tincidunt. Vivamus et sagittis tempus.</p>
				<ul class="actions">
					<li><a href="generic.html" class="button">Learn more</a></li>
				</ul>
			</div>
		</div>
	</section>
	<section>
		<a href="generic.html" class="image">
			<img src="{% link assets/images/pic10.jpg %}" alt="" data-position="25% 25%" />
		</a>
		<div class="content">
			<div class="inner">
				<header class="major">
					<h3>Sed nunc ligula</h3>
				</header>
				<p>Nullam et orci eu lorem consequat tincidunt vivamus et sagittis magna sed nunc rhoncus condimentum sem. In efficitur ligula tate urna. Maecenas massa sed magna lacinia magna pellentesque lorem ipsum dolor. Nullam et orci eu lorem consequat tincidunt. Vivamus et sagittis tempus.</p>
				<ul class="actions">
					<li><a href="generic.html" class="button">Learn more</a></li>
				</ul>
			</div>
		</div>
	</section> -->
</section>

<!-- Three -->
<section id="three">
	<div class="inner">
		<header class="major">
			<h2>Experience</h2>
		</header>
		<h2 style="display: inline;">Oracle</h2>
			<div class="row">
				<!-- Break -->
				<div class="4u 12u$(medium)">
					<h3 style="display: inline;">Current </h3>
					<p style="display: inline; margin-left: 5px;">Software Engineer</p>
					<p>
						<ul>
							<li>Working on the Fusion AI team to bring Generative AI solutions to Oracle Cloud applications</li>
						</ul>
					</p>
				</div>
				<div class="4u 12u$(medium)">
					<h3 style="display: inline;">Summer 2023 </h3>
					<p style="display: inline; margin-left: 5px;">ML Engineer</p>
					<p>
						<ul>
							<li>Continued building production features for DataFox, an AI engine for Big Data acquisition on companies</li>
							<li>
								<details>
									<summary>Read more</summary>
										<li>Created three new NLP news signal parsers with Compromise to flag existing/predicted bankruptcies, regulatory issues, etc, and contributed to increasing the true positive rate of previous parsers by ~25% to achieve a historic DataFox high</li>
										<li>Designed a vector search and generative AI-based POC with Weaviate and Cohere for news signal tagging</li>
										<li>Integrated a new ML model into the current pipeline to improve DataFox’s recognition of company-centric terminology when ‘reading’ news signals</li>
								</details>
							</li>
						</ul>
					</p>
				</div>
				<div class="4u$ 12u$(medium)">
					<h3 style="display: inline;">Summer 2022 </h3>
					<p style="display: inline; margin-left: 5px;">Software Engineer</p>
					<p>
						<ul>
							<li>Built numerous full-stack production features with unit/integration tests for DataFox, a predictive intelligence software for Big Data acquisition on 10.3 million businesses in Node.js, Ember.js, TypeScript, Handlebars, etc.</li>
							<li>
								<details>
									<summary>Read more</summary>
										<li>Doubled data auditors’ workflow efficiency by adding the ‘bulk edit audit notes’ and ‘common names merge’ features, which automated the manual merging of duplicate company data and writing of audit notes describing the actions done</li>
										<li>Created a frontend feature and backend Solr process to filter companies based on creation time—sorts through all 10 million+ companies in &lt;1 second after redefining Solr schemas and reindexing production</li>
										<li>Implemented a ‘Data Integrity Problem’ detection algorithm to flag companies with flawed data</li>
										<li>Developed a script + cron job to deliver Oracle Marketing a weekly keywords export on all companies</li>
								</details>
							</li>
						</ul>
					</p>
				</div>
			</div>
		<hr>
		<h2 style="display: inline;">Teaching at UC Berkeley</h2>
			<div class="row">
				<!-- Break -->
				<div class="4u 12u$(medium)">
					<h3 style="display: inline;">CS 168 </h3>
					<p style="display: inline; margin-left: 5px;">Internet Architecture & Protocols</p>
					<p>
						<ul>
							<li>Ran sections and office hours and developed course material covering content including but not limited to: routing protocols, addressing, congestion control, SDN, datacenters, and wireless/cellular</li>
						</ul>
					</p>
				</div>
				<div class="4u 12u$(medium)">
					<h3 style="display: inline;">CS 161 </h3>
					<p style="display: inline; margin-left: 5px;">Computer Security</p>
					<p>
						<ul>
							<li>Taught 600+ students concepts such as memory safety/web vulnerabilities & prevention (buffer overflow, CSRF/XSS/SQL injections), cryptography, and the Internet (ARP, DHCP, WPA, BGP, TCP/UDP, TLS, DNS)</li>
						</ul>
					</p>
				</div>
				<div class="4u$ 12u$(medium)">
					<h3 style="display: inline;">CS 61B </h3>
					<p style="display: inline; margin-left: 5px;">Data Structures</p>
					<p>
						<ul>
							<li>Ran labs, taught discussion sections, held office hours, and lectured on Java, data structures, OOP, runtime analysis, algorithms (e.g., Dijkstra’s, A*, Prim’s/Kruskal’s MST) and sorting, graph traversals, and more</li>
						</ul>
					</p>
				</div>
			</div>
			<div class="row">
				<!-- Break -->
				<div class="4u 12u$(medium)">
				<details>
					<summary>
					<h3 style="display: inline;">CS 61A, CS 10 </h3>
					<p style="display: inline; margin-left: 5px;">Click to read more</p>
					</summary>
					<p>
						<ul>
							<li>Lab Assistant for Structure and Interpretation of Computer Programs, Data Structures, and The Beauty and Joy of Computing</li>
							<li>Guided students in understanding lab/homework/project concepts pertaining to Python/Java/Scheme/SQL/Git, OOP, runtime analysis, algorithms and sorting, graph traversals, interpreter design, and more</li>
						</ul>
					</p>
					</details>
				</div>
			</div>
		<hr>
		<h2 style="display: inline;">Federal Reserve Bank of St. Louis, </h2>
		<p style="display: inline; margin-left: 5px;">Software Engineer Intern — Summer 2021</p>
		<p>
			<ul>
				<li>Implemented Selenium test automation to serve as a smoke test for a large U.S. Treasury application</li>
				<li>
					<details>
						<summary>Read more</summary>
							<li>Created a server touch comparison program to analyze changes in quarterly usage by various Treasury applications which was used by Bank leadership to generate periodic expenditure reports and perform cost analysis</li>
							<li>Assisted with Python RPA efforts for the Bureau of the Fiscal Service’s processes</li>
							<li>Developed VBA tools for disaster recovery exercise automation and for employee leave reporting</li>
							<li>Collaborated on a Salesforce migration POC for an existing Bank application</li>
					</details>
				</li>
			</ul>
		</p>
		<hr>
		<h2 style="display: inline;">Saint Louis University, </h2>
		<p style="display: inline; margin-left: 5px;">Drone Research Intern — July 2019-July 2020</p>
		<p>
			<ul>
				<li>Developed and released an open-source package for UAV control/MIT Scratch integration</li>
				<li>
					<details>
						<summary>Read more</summary>
							<li>Established a Node.js HTTP server for minidrone communication, telemetry, and path following</li>
							<li>Implemented a virtual reality interactive drone control system via Unreal Engine</li>
					</details>
				</li>
			</ul>
		</p>
		<hr>
		<h2 style="display: inline;">University of Missouri-St. Louis, </h2>
		<p style="display: inline; margin-left: 5px;">Computational Biology Intern — Summer 2019</p>
		<p>
			<ul>
				<li>Created and released an open-source Python wrapper for the (Perl) CNS macromolecular library</li>
				<li>
					<details>
						<summary>Read more</summary>
							<li>Received the PRI Full Tuition Excellence in Research Award for ‘PyFold,’ which halved prior processual runtime</li>
							<li>Generated 3D folded proteins via my wrapper, CNS, and bash scripts—visualized proteins in UCSF Chimera</li>
					</details>
				</li>
			</ul>
		</p>
		<hr>
		<h2 style="display: inline;">St. Louis Student Robotics Organization, </h2>
		<p style="display: inline; margin-left: 5px;">Robotics Intern/Volunteer — 2015-2020</p>
		<p>
			<ul>
				<li>Collaborated on Moroccan & Malawian national teams’ robot design</li>
				<li>
					<details>
						<summary>Read more</summary>
							<li>Compiled training data and created ML models for NVIDIA Jetson Nano</li>
							<li>Presented to/for WWT, Thomson Reuters, and MADE</li>
					</details>
				</li>
			</ul>
		</p>
	</div>
</section>
</div>