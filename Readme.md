<!DOCTYPE html>
<html>
<head>
<title>markdown_cheat_sheet.md</title>
<meta http-equiv="Content-type" content="text/html;charset=UTF-8">

<style>
/* https://github.com/microsoft/vscode/blob/master/extensions/markdown-language-features/media/markdown.css */
/*---------------------------------------------------------------------------------------------
 *  Copyright (c) Microsoft Corporation. All rights reserved.
 *  Licensed under the MIT License. See License.txt in the project root for license information.
 *--------------------------------------------------------------------------------------------*/

body {
	font-family: var(--vscode-markdown-font-family, -apple-system, BlinkMacSystemFont, "Segoe WPC", "Segoe UI", "Ubuntu", "Droid Sans", sans-serif);
	font-size: var(--vscode-markdown-font-size, 14px);
	padding: 0 26px;
	line-height: var(--vscode-markdown-line-height, 22px);
	word-wrap: break-word;
}

#code-csp-warning {
	position: fixed;
	top: 0;
	right: 0;
	color: white;
	margin: 16px;
	text-align: center;
	font-size: 12px;
	font-family: sans-serif;
	background-color:#444444;
	cursor: pointer;
	padding: 6px;
	box-shadow: 1px 1px 1px rgba(0,0,0,.25);
}

#code-csp-warning:hover {
	text-decoration: none;
	background-color:#007acc;
	box-shadow: 2px 2px 2px rgba(0,0,0,.25);
}

body.scrollBeyondLastLine {
	margin-bottom: calc(100vh - 22px);
}

body.showEditorSelection .code-line {
	position: relative;
}

body.showEditorSelection .code-active-line:before,
body.showEditorSelection .code-line:hover:before {
	content: "";
	display: block;
	position: absolute;
	top: 0;
	left: -12px;
	height: 100%;
}

body.showEditorSelection li.code-active-line:before,
body.showEditorSelection li.code-line:hover:before {
	left: -30px;
}

.vscode-light.showEditorSelection .code-active-line:before {
	border-left: 3px solid rgba(0, 0, 0, 0.15);
}

.vscode-light.showEditorSelection .code-line:hover:before {
	border-left: 3px solid rgba(0, 0, 0, 0.40);
}

.vscode-light.showEditorSelection .code-line .code-line:hover:before {
	border-left: none;
}

.vscode-dark.showEditorSelection .code-active-line:before {
	border-left: 3px solid rgba(255, 255, 255, 0.4);
}

.vscode-dark.showEditorSelection .code-line:hover:before {
	border-left: 3px solid rgba(255, 255, 255, 0.60);
}

.vscode-dark.showEditorSelection .code-line .code-line:hover:before {
	border-left: none;
}

.vscode-high-contrast.showEditorSelection .code-active-line:before {
	border-left: 3px solid rgba(255, 160, 0, 0.7);
}

.vscode-high-contrast.showEditorSelection .code-line:hover:before {
	border-left: 3px solid rgba(255, 160, 0, 1);
}

.vscode-high-contrast.showEditorSelection .code-line .code-line:hover:before {
	border-left: none;
}

img {
	max-width: 100%;
	max-height: 100%;
}

a {
	text-decoration: none;
}

a:hover {
	text-decoration: underline;
}

a:focus,
input:focus,
select:focus,
textarea:focus {
	outline: 1px solid -webkit-focus-ring-color;
	outline-offset: -1px;
}

hr {
	border: 0;
	height: 2px;
	border-bottom: 2px solid;
}

h1 {
	padding-bottom: 0.3em;
	line-height: 1.2;
	border-bottom-width: 1px;
	border-bottom-style: solid;
}

h1, h2, h3 {
	font-weight: normal;
}

table {
	border-collapse: collapse;
}

table > thead > tr > th {
	text-align: left;
	border-bottom: 1px solid;
}

table > thead > tr > th,
table > thead > tr > td,
table > tbody > tr > th,
table > tbody > tr > td {
	padding: 5px 10px;
}

table > tbody > tr + tr > td {
	border-top: 1px solid;
}

blockquote {
	margin: 0 7px 0 5px;
	padding: 0 16px 0 10px;
	border-left-width: 5px;
	border-left-style: solid;
}

code {
	font-family: Menlo, Monaco, Consolas, "Droid Sans Mono", "Courier New", monospace, "Droid Sans Fallback";
	font-size: 1em;
	line-height: 1.357em;
}

body.wordWrap pre {
	white-space: pre-wrap;
}

pre:not(.hljs),
pre.hljs code > div {
	padding: 16px;
	border-radius: 3px;
	overflow: auto;
}

pre code {
	color: var(--vscode-editor-foreground);
	tab-size: 4;
}

/** Theming */

.vscode-light pre {
	background-color: rgba(220, 220, 220, 0.4);
}

.vscode-dark pre {
	background-color: rgba(10, 10, 10, 0.4);
}

.vscode-high-contrast pre {
	background-color: rgb(0, 0, 0);
}

.vscode-high-contrast h1 {
	border-color: rgb(0, 0, 0);
}

.vscode-light table > thead > tr > th {
	border-color: rgba(0, 0, 0, 0.69);
}

.vscode-dark table > thead > tr > th {
	border-color: rgba(255, 255, 255, 0.69);
}

.vscode-light h1,
.vscode-light hr,
.vscode-light table > tbody > tr + tr > td {
	border-color: rgba(0, 0, 0, 0.18);
}

.vscode-dark h1,
.vscode-dark hr,
.vscode-dark table > tbody > tr + tr > td {
	border-color: rgba(255, 255, 255, 0.18);
}

</style>

<style>
/* Tomorrow Theme */
/* http://jmblog.github.com/color-themes-for-google-code-highlightjs */
/* Original theme - https://github.com/chriskempson/tomorrow-theme */

/* Tomorrow Comment */
.hljs-comment,
.hljs-quote {
	color: #8e908c;
}

/* Tomorrow Red */
.hljs-variable,
.hljs-template-variable,
.hljs-tag,
.hljs-name,
.hljs-selector-id,
.hljs-selector-class,
.hljs-regexp,
.hljs-deletion {
	color: #c82829;
}

/* Tomorrow Orange */
.hljs-number,
.hljs-built_in,
.hljs-builtin-name,
.hljs-literal,
.hljs-type,
.hljs-params,
.hljs-meta,
.hljs-link {
	color: #f5871f;
}

/* Tomorrow Yellow */
.hljs-attribute {
	color: #eab700;
}

/* Tomorrow Green */
.hljs-string,
.hljs-symbol,
.hljs-bullet,
.hljs-addition {
	color: #718c00;
}

/* Tomorrow Blue */
.hljs-title,
.hljs-section {
	color: #4271ae;
}

/* Tomorrow Purple */
.hljs-keyword,
.hljs-selector-tag {
	color: #8959a8;
}

.hljs {
	display: block;
	overflow-x: auto;
	color: #4d4d4c;
	padding: 0.5em;
}

.hljs-emphasis {
	font-style: italic;
}

.hljs-strong {
	font-weight: bold;
}
</style>

<style>
/*
 * Markdown PDF CSS
 */

 body {
	font-family: -apple-system, BlinkMacSystemFont, "Segoe WPC", "Segoe UI", "Ubuntu", "Droid Sans", sans-serif, "Meiryo";
	padding: 0 12px;
}

pre {
	background-color: #f8f8f8;
	border: 1px solid #cccccc;
	border-radius: 3px;
	overflow-x: auto;
	white-space: pre-wrap;
	overflow-wrap: break-word;
}

pre:not(.hljs) {
	padding: 23px;
	line-height: 19px;
}

blockquote {
	background: rgba(127, 127, 127, 0.1);
	border-color: rgba(0, 122, 204, 0.5);
}

.emoji {
	height: 1.4em;
}

code {
	font-size: 14px;
	line-height: 19px;
}

/* for inline code */
:not(pre):not(.hljs) > code {
	color: #C9AE75; /* Change the old color so it seems less like an error */
	font-size: inherit;
}

/* Page Break : use <div class="page"/> to insert page break
-------------------------------------------------------- */
.page {
	page-break-after: always;
}

</style>

<script src="https://unpkg.com/mermaid/dist/mermaid.min.js"></script>
</head>
<body>
  <script>
    mermaid.initialize({
      startOnLoad: true,
      theme: document.body.classList.contains('vscode-dark') || document.body.classList.contains('vscode-high-contrast')
          ? 'dark'
          : 'default'
    });
  </script>
<h1 id="topic-1-headings">Topic-1 Headings</h1>
<p>How to give headings in markdown files?</p>
<h1 id="heading-1">Heading 1</h1>
<h2 id="heading-2">Heading 2</h2>
<h3 id="heading-3">Heading 3</h3>
<h4 id="heading-4">Heading 4</h4>
<h5 id="heading-5">Heading 5</h5>
<h6 id="heading">Heading</h6>
<p>Instructions :(Control+k)+v used to open side view</p>
<h1 id="topic-2-block-of-words">Topic-2 Block of words</h1>
<p>This is normal text in markdown</p>
<blockquote>
<p>This is block of special text</p>
<p>This is second line</p>
</blockquote>
<blockquote>
<p>This is block of special text</p>
</blockquote>
<blockquote>
<p>This is second line</p>
</blockquote>
<h1 id="topic-3-line-break">Topic-3 Line break</h1>
<p>Press ENTER twice to seprate lines or reverse slash &quot;&quot;<br>
This is 1st line</p>
<p>This is second line</p>
<h1 id="topic-4-face-of-text">Topic-4 Face of text</h1>
<p>For bold use  <strong>bold</strong></p>
<p>For italic use  <em>italic</em></p>
<p>For bold  and italic  use  <em><strong>bold and italic</strong></em></p>
<p>One can also use undersore fr bold and italic</p>
<p>use double underscore to bold <strong>bold</strong>
use single underscore fo <em>italic</em></p>
<h1 id="topic-5-bullet-pontslists">Topic-5 Bullet ponts/lists</h1>
<ul>
<li>Day 1</li>
<li>Day 2</li>
<li>Day 3</li>
<li>Day 4</li>
<li>Day 5 use tab to forward
<ul>
<li>Day 5a
<ul>
<li>Day 5a-1</li>
</ul>
</li>
<li>Day 5b</li>
</ul>
</li>
<li>Day 6 use shift+Tab to go backward</li>
<li>Day 7</li>
</ul>
<blockquote>
<p>Numbering of lists</p>
</blockquote>
<ol>
<li>Day1</li>
<li>Day2</li>
<li>Day3</li>
<li>day4</li>
<li>Day5
<ol>
<li>Day5a</li>
<li>Day5b</li>
</ol>
</li>
<li>Day6</li>
<li>Day7</li>
</ol>
<blockquote>
<p><strong>Listing using * or +</strong></p>
</blockquote>
<ul>
<li>one</li>
</ul>
<ul>
<li>One</li>
</ul>
<h1 id="topic-6-line-breaks-or-page-breaks">Topic-6 Line breaks or page breaks</h1>
<p>This is page 1</p>
<hr>
<hr>
<hr>
<p>This is page 2</p>
<h1 id="topic-7-links-and-hyperlinks">Topic-7 Links and Hyperlinks</h1>
<blockquote>
<p>Hyperlink</p>
</blockquote>
<p><a href="https://www.youtube.com/watch?v=qJqAXjz-Rh4&amp;list=PL9XvIvvVL50HVsu-Ao8NBr0UJSO8O6lBI&amp;index=21">https://www.youtube.com/watch?v=qJqAXjz-Rh4&amp;list=PL9XvIvvVL50HVsu-Ao8NBr0UJSO8O6lBI&amp;index=21</a></p>
<blockquote>
<p>Link</p>
</blockquote>
<p>The link of chlla is <a href="https://www.youtube.com/watch?v=qJqAXjz-Rh4&amp;list=PL9XvIvvVL50HVsu-Ao8NBr0UJSO8O6lBI&amp;index=21">here</a></p>
<p>The key of playlist is <a href="https://www.youtube.com/watch?v=qJqAXjz-Rh4&amp;list=PL9XvIvvVL50HVsu-Ao8NBr0UJSO8O6lBI&amp;index=21">Here</a></p>
<!---comment out--->
<h1 id="topic-8-attaching-picture-in-markdown-file">Topic-8 Attaching picture in markdown file</h1>
<blockquote>
<p>From the same folder in which markdown file is present</p>
</blockquote>
<p><img src="11.jpg" alt="Pic"></p>
<blockquote>
<p>from internet paste url</p>
</blockquote>
<p><img src="https://www.google.com/search?q=codanics+aammar&amp;tbm=isch&amp;ved=2ahUKEwie5OeI_qz1AhWq34UKHeVOBT8Q2-cCegQIABAA&amp;oq=codanics+aammar&amp;gs_lcp=CgNpbWcQAzoGCAAQChAYUJMzWJJJYMJKaAFwAHgAgAHLAYgBzAqSAQUwLjYuMZgBAKABAaoBC2d3cy13aXotaW1nwAEB&amp;sclient=img&amp;ei=-jDfYZ7_HKq_lwTlnZX4Aw&amp;bih=568&amp;biw=1349&amp;rlz=1C1CHBD_enPK961PK961&amp;hl=en#imgrc=jSNIAJI341a1QM" alt="Codanics"></p>
<h1 id="topic-9-adding-code-and-block-of-code">Topic-9 Adding code and block of code</h1>
<p>To print a string use <code>print(&quot;Codanics&quot;)</code></p>
<blockquote>
<p>to print block of code</p>
</blockquote>
<pre class="hljs"><code><div>print(&quot;Hello baba g&quot;)
</div></code></pre>
<blockquote>
<p>This line will show color accrding to python language syntax</p>
</blockquote>
<pre class="hljs"><code><div>x= <span class="hljs-number">1</span>
y= <span class="hljs-number">2</span>
z= x+y
print(z) 
</div></code></pre>
<blockquote>
<p>This line will show color accrding to R language syntax</p>
</blockquote>
<pre class="hljs"><code><div>x= <span class="hljs-number">1</span>
y= <span class="hljs-number">2</span>
z= x+y
print(z) 
</div></code></pre>
<h1 id="topic-10-adding-tables">Topic-10 Adding tables</h1>
<table>
<thead>
<tr>
<th>species</th>
<th>petal_length</th>
<th>Sepal_length</th>
</tr>
</thead>
<tbody>
<tr>
<td>virginica</td>
<td>18.2</td>
<td>10</td>
</tr>
<tr>
<td>setosa</td>
<td>45</td>
<td>78</td>
</tr>
<tr>
<td>hello</td>
<td>78</td>
<td>78</td>
</tr>
</tbody>
</table>
<blockquote>
<p>For centre align</p>
</blockquote>
<table>
<thead>
<tr>
<th style="text-align:center">species</th>
<th style="text-align:center">petal_length</th>
<th style="text-align:center">Sepal_length</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:center">virginica</td>
<td style="text-align:center">18.2</td>
<td style="text-align:center">10</td>
</tr>
<tr>
<td style="text-align:center">setosa</td>
<td style="text-align:center">45</td>
<td style="text-align:center">78</td>
</tr>
<tr>
<td style="text-align:center">hello</td>
<td style="text-align:center">78</td>
<td style="text-align:center">78</td>
</tr>
</tbody>
</table>
<blockquote>
<p>For left align</p>
</blockquote>
<table>
<thead>
<tr>
<th style="text-align:left">species</th>
<th style="text-align:left">petal_length</th>
<th style="text-align:left">Sepal_length</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:left">virginica</td>
<td style="text-align:left">18.2</td>
<td style="text-align:left">10</td>
</tr>
<tr>
<td style="text-align:left">setosa</td>
<td style="text-align:left">45</td>
<td style="text-align:left">78</td>
</tr>
<tr>
<td style="text-align:left">hello</td>
<td style="text-align:left">78</td>
<td style="text-align:left">78</td>
</tr>
</tbody>
</table>
<blockquote>
<p>For right Align</p>
</blockquote>
<table>
<thead>
<tr>
<th style="text-align:right">species</th>
<th style="text-align:right">petal_length</th>
<th style="text-align:right">Sepal_length</th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align:right">virginica</td>
<td style="text-align:right">18.2</td>
<td style="text-align:right">10</td>
</tr>
<tr>
<td style="text-align:right">setosa</td>
<td style="text-align:right">45</td>
<td style="text-align:right">78</td>
</tr>
<tr>
<td style="text-align:right">hello</td>
<td style="text-align:right">78</td>
<td style="text-align:right">78</td>
</tr>
</tbody>
</table>
<h1 id="adding-contents">Adding contents</h1>
<p><a href="#topic-1-headings">topic-1 Headings</a><br>
<a href="#topic-2-block-of-words">topic-2-block-of-words</a><br>
<a href="#topic-3-line-break">topic-3-line-break</a><br>
<a href="#topic-4-face-of-text">topic-4-face-of-text</a><br>
<a href="#topic-5-bullet-pontslists">topic-5-bullet-pontslists</a><br>
<a href="#topic-6-line-breaks-or-page-breaks">topic-6-line-breaks-or-page-breaks</a><br>
<a href="#topic-7-links-and-hyperlinks">topic-7-links-and-hyperlinks</a><br>
<a href="#topic-8-attaching-picture-in-markdown-file">topic-8-attaching-picture-in-markdown-file</a><br>
<a href="#topic-9-adding-code-and-block-of-code">topic-9-adding-code-and-block-of-code</a><br>
<a href="#topic-10-adding-tables">topic-10-adding-tables</a></p>

</body>
</html>
