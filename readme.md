---


---

<h1 id="project-title-and-information---template">Project title and information - template</h1>
<p>Here we give an overview in a couple of sentences on what this service or application does. Simple for the information of the developers. Below this, we add a link to the Confluence page that is linked to this project.</p>
<p><strong>Confluence:</strong> <a href="link-to-confluence">project information</a></p>
<h2 id="getting-started">Getting Started</h2>
<p>These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.</p>
<h3 id="prerequisites">Prerequisites</h3>
<p>What things you need to install the software and how to install them by listing the technologies.</p>
<ul>
<li>Virtual environment of choice (anaconda, venv, …)</li>
<li>Python 3.6</li>
<li>pip</li>
</ul>
<p>optional:</p>
<ul>
<li>gcloud</li>
<li>kubectl</li>
</ul>
<h3 id="installing">Installing</h3>
<p>A step by step series of examples that tell you how to get a development environment running.</p>
<h4 id="install-requirements">1. Install requirements</h4>
<pre><code>pip install -r requirements.txt
</code></pre>
<h4 id="set-the-environment-variables">2. Set the environment variables</h4>
<p>**<strong>required</strong></p>

<table>
<thead>
<tr>
<th>Environment Variable</th>
<th>Default</th>
<th>Explanation</th>
</tr>
</thead>
<tbody>
<tr>
<td>REDIS_IP</td>
<td>localhost</td>
<td>Connection to the redis. For the default to work use kubectl port-forwarding or run redis locally</td>
</tr>
<tr>
<td>CLIENT_ID**</td>
<td></td>
<td>Office 365 client id.</td>
</tr>
<tr>
<td>CLIENT_SECRET**</td>
<td></td>
<td>Office 365 client secret</td>
</tr>
<tr>
<td>LOG_LEVEL</td>
<td>debug</td>
<td>Can be one of the following: CRITICAL, FATAL, ERROR, WARN, WARNING, INFO, DEBUG, NOTSET</td>
</tr>
<tr>
<td>SCOPES</td>
<td>message_all</td>
<td>The scope of the mail listener. For normal mailboxes is it the default value. for shared mailboxes is this <code>SCOPES=message_all_shared</code></td>
</tr>
<tr>
<td>SHARED_MAILBOX</td>
<td>me</td>
<td>Which mailbox is used. me for normal mailboxes. The email address for shared mailboxes.</td>
</tr>
</tbody>
</table><p>All the values for the environment variables can be found at X (link).<br>
If you don’t have access please ask the Technical Lead according to the Confluence page.</p>
<h4 id="run-the-application">3. Run the application</h4>
<p>In this section we list all steps of local development.</p>
<pre><code>python -m outlook_service
</code></pre>
<h2 id="run-the-tests">Run the tests</h2>
<p>You can run the test by running pytest:</p>
<pre class=" language-bash"><code class="prism  language-bash">pytest
</code></pre>
<h2 id="deployment">Deployment</h2>
<p>This project has CI with bitbucket pipelines. When pushing to master branch (customize if needed) it will be build<br>
and deployed automatically.</p>

