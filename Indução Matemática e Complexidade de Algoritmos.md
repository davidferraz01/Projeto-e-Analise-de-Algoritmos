<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"/><title>Indução Matemática e Complexidade de Algoritmos</title><style>
/* cspell:disable-file */
/* webkit printing magic: print all background colors */
html {
	-webkit-print-color-adjust: exact;
}
* {
	box-sizing: border-box;
	-webkit-print-color-adjust: exact;
}

html,
body {
	margin: 0;
	padding: 0;
}
@media only screen {
	body {
		margin: 2em auto;
		max-width: 900px;
		color: rgb(55, 53, 47);
	}
}

body {
	line-height: 1.5;
	white-space: pre-wrap;
}

a,
a.visited {
	color: inherit;
	text-decoration: underline;
}

.pdf-relative-link-path {
	font-size: 80%;
	color: #444;
}

h1,
h2,
h3 {
	letter-spacing: -0.01em;
	line-height: 1.2;
	font-weight: 600;
	margin-bottom: 0;
}

.page-title {
	font-size: 2.5rem;
	font-weight: 700;
	margin-top: 0;
	margin-bottom: 0.75em;
}

h1 {
	font-size: 1.875rem;
	margin-top: 1.875rem;
}

h2 {
	font-size: 1.5rem;
	margin-top: 1.5rem;
}

h3 {
	font-size: 1.25rem;
	margin-top: 1.25rem;
}

.source {
	border: 1px solid #ddd;
	border-radius: 3px;
	padding: 1.5em;
	word-break: break-all;
}

.callout {
	border-radius: 3px;
	padding: 1rem;
}

figure {
	margin: 1.25em 0;
	page-break-inside: avoid;
}

figcaption {
	opacity: 0.5;
	font-size: 85%;
	margin-top: 0.5em;
}

mark {
	background-color: transparent;
}

.indented {
	padding-left: 1.5em;
}

hr {
	background: transparent;
	display: block;
	width: 100%;
	height: 1px;
	visibility: visible;
	border: none;
	border-bottom: 1px solid rgba(55, 53, 47, 0.09);
}

img {
	max-width: 100%;
}

@media only print {
	img {
		max-height: 100vh;
		object-fit: contain;
	}
}

@page {
	margin: 1in;
}

.collection-content {
	font-size: 0.875rem;
}

.column-list {
	display: flex;
	justify-content: space-between;
}

.column {
	padding: 0 1em;
}

.column:first-child {
	padding-left: 0;
}

.column:last-child {
	padding-right: 0;
}

.table_of_contents-item {
	display: block;
	font-size: 0.875rem;
	line-height: 1.3;
	padding: 0.125rem;
}

.table_of_contents-indent-1 {
	margin-left: 1.5rem;
}

.table_of_contents-indent-2 {
	margin-left: 3rem;
}

.table_of_contents-indent-3 {
	margin-left: 4.5rem;
}

.table_of_contents-link {
	text-decoration: none;
	opacity: 0.7;
	border-bottom: 1px solid rgba(55, 53, 47, 0.18);
}

table,
th,
td {
	border: 1px solid rgba(55, 53, 47, 0.09);
	border-collapse: collapse;
}

table {
	border-left: none;
	border-right: none;
}

th,
td {
	font-weight: normal;
	padding: 0.25em 0.5em;
	line-height: 1.5;
	min-height: 1.5em;
	text-align: left;
}

th {
	color: rgba(55, 53, 47, 0.6);
}

ol,
ul {
	margin: 0;
	margin-block-start: 0.6em;
	margin-block-end: 0.6em;
}

li > ol:first-child,
li > ul:first-child {
	margin-block-start: 0.6em;
}

ul > li {
	list-style: disc;
}

ul.to-do-list {
	padding-inline-start: 0;
}

ul.to-do-list > li {
	list-style: none;
}

.to-do-children-checked {
	text-decoration: line-through;
	opacity: 0.375;
}

ul.toggle > li {
	list-style: none;
}

ul {
	padding-inline-start: 1.7em;
}

ul > li {
	padding-left: 0.1em;
}

ol {
	padding-inline-start: 1.6em;
}

ol > li {
	padding-left: 0.2em;
}

.mono ol {
	padding-inline-start: 2em;
}

.mono ol > li {
	text-indent: -0.4em;
}

.toggle {
	padding-inline-start: 0em;
	list-style-type: none;
}

/* Indent toggle children */
.toggle > li > details {
	padding-left: 1.7em;
}

.toggle > li > details > summary {
	margin-left: -1.1em;
}

.selected-value {
	display: inline-block;
	padding: 0 0.5em;
	background: rgba(206, 205, 202, 0.5);
	border-radius: 3px;
	margin-right: 0.5em;
	margin-top: 0.3em;
	margin-bottom: 0.3em;
	white-space: nowrap;
}

.collection-title {
	display: inline-block;
	margin-right: 1em;
}

.page-description {
    margin-bottom: 2em;
}

.simple-table {
	margin-top: 1em;
	font-size: 0.875rem;
	empty-cells: show;
}
.simple-table td {
	height: 29px;
	min-width: 120px;
}

.simple-table th {
	height: 29px;
	min-width: 120px;
}

.simple-table-header-color {
	background: rgb(247, 246, 243);
	color: black;
}
.simple-table-header {
	font-weight: 500;
}

time {
	opacity: 0.5;
}

.icon {
	display: inline-block;
	max-width: 1.2em;
	max-height: 1.2em;
	text-decoration: none;
	vertical-align: text-bottom;
	margin-right: 0.5em;
}

img.icon {
	border-radius: 3px;
}

.user-icon {
	width: 1.5em;
	height: 1.5em;
	border-radius: 100%;
	margin-right: 0.5rem;
}

.user-icon-inner {
	font-size: 0.8em;
}

.text-icon {
	border: 1px solid #000;
	text-align: center;
}

.page-cover-image {
	display: block;
	object-fit: cover;
	width: 100%;
	max-height: 30vh;
}

.page-header-icon {
	font-size: 3rem;
	margin-bottom: 1rem;
}

.page-header-icon-with-cover {
	margin-top: -0.72em;
	margin-left: 0.07em;
}

.page-header-icon img {
	border-radius: 3px;
}

.link-to-page {
	margin: 1em 0;
	padding: 0;
	border: none;
	font-weight: 500;
}

p > .user {
	opacity: 0.5;
}

td > .user,
td > time {
	white-space: nowrap;
}

input[type="checkbox"] {
	transform: scale(1.5);
	margin-right: 0.6em;
	vertical-align: middle;
}

p {
	margin-top: 0.5em;
	margin-bottom: 0.5em;
}

.image {
	border: none;
	margin: 1.5em 0;
	padding: 0;
	border-radius: 0;
	text-align: center;
}

.code,
code {
	background: rgba(135, 131, 120, 0.15);
	border-radius: 3px;
	padding: 0.2em 0.4em;
	border-radius: 3px;
	font-size: 85%;
	tab-size: 2;
}

code {
	color: #eb5757;
}

.code {
	padding: 1.5em 1em;
}

.code-wrap {
	white-space: pre-wrap;
	word-break: break-all;
}

.code > code {
	background: none;
	padding: 0;
	font-size: 100%;
	color: inherit;
}

blockquote {
	font-size: 1.25em;
	margin: 1em 0;
	padding-left: 1em;
	border-left: 3px solid rgb(55, 53, 47);
}

.bookmark {
	text-decoration: none;
	max-height: 8em;
	padding: 0;
	display: flex;
	width: 100%;
	align-items: stretch;
}

.bookmark-title {
	font-size: 0.85em;
	overflow: hidden;
	text-overflow: ellipsis;
	height: 1.75em;
	white-space: nowrap;
}

.bookmark-text {
	display: flex;
	flex-direction: column;
}

.bookmark-info {
	flex: 4 1 180px;
	padding: 12px 14px 14px;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.bookmark-image {
	width: 33%;
	flex: 1 1 180px;
	display: block;
	position: relative;
	object-fit: cover;
	border-radius: 1px;
}

.bookmark-description {
	color: rgba(55, 53, 47, 0.6);
	font-size: 0.75em;
	overflow: hidden;
	max-height: 4.5em;
	word-break: break-word;
}

.bookmark-href {
	font-size: 0.75em;
	margin-top: 0.25em;
}

.sans { font-family: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol"; }
.code { font-family: "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace; }
.serif { font-family: Lyon-Text, Georgia, ui-serif, serif; }
.mono { font-family: iawriter-mono, Nitti, Menlo, Courier, monospace; }
.pdf .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK JP'; }
.pdf:lang(zh-CN) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC'; }
.pdf:lang(zh-TW) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK TC'; }
.pdf:lang(ko-KR) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK KR'; }
.pdf .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.pdf .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK JP'; }
.pdf:lang(zh-CN) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK SC'; }
.pdf:lang(zh-TW) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK TC'; }
.pdf:lang(ko-KR) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK KR'; }
.pdf .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.highlight-default {
	color: rgba(55, 53, 47, 1);
}
.highlight-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(120, 119, 116, 1);
}
.highlight-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(159, 107, 83, 1);
}
.highlight-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(217, 115, 13, 1);
}
.highlight-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 145, 47, 1);
}
.highlight-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(68, 131, 97, 1);
}
.highlight-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(51, 126, 169, 1);
}
.highlight-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(144, 101, 176, 1);
}
.highlight-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(193, 76, 138, 1);
}
.highlight-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(212, 76, 71, 1);
}
.highlight-gray_background {
	background: rgba(241, 241, 239, 1);
}
.highlight-brown_background {
	background: rgba(244, 238, 238, 1);
}
.highlight-orange_background {
	background: rgba(251, 236, 221, 1);
}
.highlight-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.highlight-teal_background {
	background: rgba(237, 243, 236, 1);
}
.highlight-blue_background {
	background: rgba(231, 243, 248, 1);
}
.highlight-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.highlight-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.highlight-red_background {
	background: rgba(253, 235, 236, 1);
}
.block-color-default {
	color: inherit;
	fill: inherit;
}
.block-color-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(120, 119, 116, 1);
}
.block-color-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(159, 107, 83, 1);
}
.block-color-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(217, 115, 13, 1);
}
.block-color-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 145, 47, 1);
}
.block-color-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(68, 131, 97, 1);
}
.block-color-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(51, 126, 169, 1);
}
.block-color-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(144, 101, 176, 1);
}
.block-color-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(193, 76, 138, 1);
}
.block-color-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(212, 76, 71, 1);
}
.block-color-gray_background {
	background: rgba(241, 241, 239, 1);
}
.block-color-brown_background {
	background: rgba(244, 238, 238, 1);
}
.block-color-orange_background {
	background: rgba(251, 236, 221, 1);
}
.block-color-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.block-color-teal_background {
	background: rgba(237, 243, 236, 1);
}
.block-color-blue_background {
	background: rgba(231, 243, 248, 1);
}
.block-color-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.block-color-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.block-color-red_background {
	background: rgba(253, 235, 236, 1);
}
.select-value-color-interactiveBlue { background-color: rgba(35, 131, 226, .07); }
.select-value-color-pink { background-color: rgba(245, 224, 233, 1); }
.select-value-color-purple { background-color: rgba(232, 222, 238, 1); }
.select-value-color-green { background-color: rgba(219, 237, 219, 1); }
.select-value-color-gray { background-color: rgba(227, 226, 224, 1); }
.select-value-color-translucentGray { background-color: rgba(255, 255, 255, 0.0375); }
.select-value-color-orange { background-color: rgba(250, 222, 201, 1); }
.select-value-color-brown { background-color: rgba(238, 224, 218, 1); }
.select-value-color-red { background-color: rgba(255, 226, 221, 1); }
.select-value-color-yellow { background-color: rgba(253, 236, 200, 1); }
.select-value-color-blue { background-color: rgba(211, 229, 239, 1); }
.select-value-color-pageGlass { background-color: undefined; }
.select-value-color-washGlass { background-color: undefined; }

.checkbox {
	display: inline-flex;
	vertical-align: text-bottom;
	width: 16;
	height: 16;
	background-size: 16px;
	margin-left: 2px;
	margin-right: 5px;
}

.checkbox-on {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20width%3D%2216%22%20height%3D%2216%22%20fill%3D%22%2358A9D7%22%2F%3E%0A%3Cpath%20d%3D%22M6.71429%2012.2852L14%204.9995L12.7143%203.71436L6.71429%209.71378L3.28571%206.2831L2%207.57092L6.71429%2012.2852Z%22%20fill%3D%22white%22%2F%3E%0A%3C%2Fsvg%3E");
}

.checkbox-off {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20x%3D%220.75%22%20y%3D%220.75%22%20width%3D%2214.5%22%20height%3D%2214.5%22%20fill%3D%22white%22%20stroke%3D%22%2336352F%22%20stroke-width%3D%221.5%22%2F%3E%0A%3C%2Fsvg%3E");
}
	
</style></head><body><article id="2c069821-1569-4f85-a85e-9a96a2ea2cde" class="page sans"><header><h1 class="page-title">Indução Matemática e Complexidade de Algoritmos</h1><p class="page-description"></p></header><div class="page-body"><hr id="54018391-26df-4a31-8c84-616aeb06c112"/><p id="3d3bff27-9266-4f37-ad56-5c5acc00ba49" class=""><strong>1°  Prove por indução matemática que a soma dos cubos dos n primeiros números inteiros positivos, n ≥ 1, é igual ao quadrado da soma destes números.</strong><div class="indented"><p id="5e0e5007-0d2e-4cd5-8c92-e3562ef7990b" class="">Variável de Indução:<div class="indented"><p id="dc891281-5590-4cdf-a5cc-0c7a4cd0dc8e" class="">Inteiros positivos, <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>n</mi><mo>≥</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">n \geq 1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.7719400000000001em;vertical-align:-0.13597em;"></span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">≥</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span></span></span></span></span><span>﻿</span></span>.</p></div></p><p id="d11fa0af-a2a1-4c8a-b934-e62b87515341" class="">Caso Base: <div class="indented"><p id="e25cdc52-7f86-456b-9793-2d091447dae8" class=""><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>n</mi><mo>=</mo><mn>0</mn><mo>→</mo><msup><mn>0</mn><mn>3</mn></msup><mo>=</mo><mo stretchy="false">(</mo><mn>0</mn><msup><mo stretchy="false">)</mo><mn>2</mn></msup></mrow><annotation encoding="application/x-tex">n = 0  \rightarrow 0^3 = (0)^2</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.43056em;vertical-align:0em;"></span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">0</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">→</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.8141079999999999em;vertical-align:0em;"></span><span class="mord"><span class="mord">0</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141079999999999em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">3</span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1.064108em;vertical-align:-0.25em;"></span><span class="mopen">(</span><span class="mord">0</span><span class="mclose"><span class="mclose">)</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141079999999999em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">2</span></span></span></span></span></span></span></span></span></span></span></span><span>﻿</span></span></p></div></p><p id="e3923596-7951-4ab4-a5da-95cbd249894c" class="">Hipótese de Indução: <div class="indented"><p id="774bfaf3-7334-4bc5-b3b3-8e0201fb8ffc" class="">A propriedade é válida para <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>n</mi><mo>=</mo><mi>k</mi><mo>→</mo><mn>1</mn><mtext>³</mtext><mo>+</mo><mn>2</mn><mtext>³</mtext><mo>+</mo><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mo>+</mo><mi>k</mi><mtext>³</mtext><mo>=</mo><mo stretchy="false">(</mo><mn>1</mn><mo>+</mo><mn>2</mn><mo>+</mo><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mo>+</mo><mi>k</mi><mo stretchy="false">)</mo><mtext>²</mtext></mrow><annotation encoding="application/x-tex">n = k \rightarrow 1³ + 2³ + ... + k ³ = (1 + 2 + ... + k)²</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.43056em;vertical-align:0em;"></span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.69444em;vertical-align:0em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">→</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">1³</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">2³</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord">...</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.69444em;vertical-align:0em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mord">³</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mopen">(</span><span class="mord">1</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">2</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord">...</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mclose">)</span><span class="mord">²</span></span></span></span></span><span>﻿</span></span></p></div></p><p id="12bd3470-8b50-45ec-85e5-341f15e49fdd" class="">Passo indutivo, para <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>n</mi><mo>=</mo><mi>k</mi><mo>+</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">n = k + 1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.43056em;vertical-align:0em;"></span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.77777em;vertical-align:-0.08333em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span></span></span></span></span><span>﻿</span></span>:<div class="indented"><figure id="5daaa896-13c7-4cd5-988c-72f473077a1d" class="equation"><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><div class="equation-container"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><msub><mi>S</mi><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow></msub><mo>=</mo><mn>1</mn><mtext>³</mtext><mo>+</mo><mn>2</mn><mtext>³</mtext><mo>+</mo><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mo>+</mo><msup><mi>k</mi><mn>3</mn></msup><mo>+</mo><mo stretchy="false">(</mo><mi>k</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo><mtext>³</mtext></mrow><annotation encoding="application/x-tex">S_{k+1} = 1³ + 2³ + ... + k ^3 + (k + 1)³</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.891661em;vertical-align:-0.208331em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.3361079999999999em;"><span style="top:-2.5500000000000003em;margin-left:-0.05764em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.208331em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">1³</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">2³</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord">...</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.9474379999999999em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8641079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">3</span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mopen">(</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">1</span><span class="mclose">)</span><span class="mord">³</span></span></span></span></span></div></figure><p id="e0c9d2ff-0f64-4f5a-982d-2664c6f88cca" class="">Note que o termo <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mn>1</mn><mtext>³</mtext><mo>+</mo><mn>2</mn><mtext>³</mtext><mo>+</mo><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mo>+</mo><msup><mi>k</mi><mn>3</mn></msup></mrow><annotation encoding="application/x-tex">1³ + 2³ + ... + k ^3</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">1³</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">2³</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord">...</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.8141079999999999em;vertical-align:0em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141079999999999em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">3</span></span></span></span></span></span></span></span></span></span></span></span><span>﻿</span></span> é nossa Hipótese Indutiva. Logo, podemos substituir seu valor na expressão acima. Assim:</p><figure id="659f51e0-7a0e-4a28-8256-336073e47008" class="equation"><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><div class="equation-container"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><msub><mi>S</mi><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow></msub><mo>=</mo><mo stretchy="false">(</mo><mn>1</mn><mo>+</mo><mn>2</mn><mo>+</mo><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mo>+</mo><mi>k</mi><mo stretchy="false">)</mo><mtext>²</mtext><mo>+</mo><mo stretchy="false">(</mo><mi>k</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo><mtext>³</mtext></mrow><annotation encoding="application/x-tex">S_{k + 1} = (1 + 2 + ... + k)² + (k+1)³</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.891661em;vertical-align:-0.208331em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.3361079999999999em;"><span style="top:-2.5500000000000003em;margin-left:-0.05764em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.208331em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mopen">(</span><span class="mord">1</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">2</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord">...</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mclose">)</span><span class="mord">²</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mopen">(</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">1</span><span class="mclose">)</span><span class="mord">³</span></span></span></span></span></div></figure><p id="c80f3cd3-47a5-493e-bad9-b3441005c6d8" class="">Podemos perceber que o valor da Hipótese Indutiva representa uma Progressão Aritmética. Portando, podemos substituir seu valor pela fórmula de uma PA de 1 à k:</p><figure id="da1750b5-fa24-42e7-a4d0-bbe1cd420420" class="equation"><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><div class="equation-container"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><msub><mi>S</mi><mi>k</mi></msub><mo>=</mo><mo stretchy="false">(</mo><mn>1</mn><mo>+</mo><mn>2</mn><mo>+</mo><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mo>+</mo><mi>k</mi><mo stretchy="false">)</mo><mtext>²</mtext><mo>=</mo><mo fence="false" stretchy="true" minsize="3em" maxsize="3em">(</mo><mfrac><mrow><mo stretchy="false">(</mo><mn>1</mn><mo>+</mo><mi>k</mi><mo stretchy="false">)</mo><mi>k</mi></mrow><mn>2</mn></mfrac><mo fence="false" stretchy="true" minsize="3em" maxsize="3em">)</mo><mpadded voffset="1.25em"><mstyle scriptlevel="0" displaystyle="false"><mstyle scriptlevel="0" displaystyle="false"><mn>2</mn></mstyle></mstyle></mpadded><mo>=</mo><mo fence="false" stretchy="true" minsize="3em" maxsize="3em">(</mo><mfrac><mrow><mi>k</mi><mo>+</mo><mi>k</mi><mtext>²</mtext></mrow><mn>2</mn></mfrac><mo fence="false" stretchy="true" minsize="3em" maxsize="3em">)</mo><mpadded voffset="1.25em"><mstyle scriptlevel="0" displaystyle="false"><mstyle scriptlevel="0" displaystyle="false"><mn>2</mn></mstyle></mstyle></mpadded></mrow><annotation encoding="application/x-tex">S_k = (1 + 2 + ... + k)² = \Bigg (\frac {(1 + k)k} {2} \Bigg )\raisebox{1.25em}{$2$} = \Bigg (\frac {k + k²} {2} \Bigg )\raisebox{1.25em}{$2$}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.83333em;vertical-align:-0.15em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.33610799999999996em;"><span style="top:-2.5500000000000003em;margin-left:-0.05764em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.15em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mopen">(</span><span class="mord">1</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">2</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord">...</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mclose">)</span><span class="mord">²</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:3.14447em;vertical-align:-1.25003em;"></span><span class="mord"><span class="delimsizing size4">(</span></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:1.427em;"><span style="top:-2.314em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">2</span></span></span><span style="top:-3.23em;"><span class="pstrut" style="height:3em;"></span><span class="frac-line" style="border-bottom-width:0.04em;"></span></span><span style="top:-3.677em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mopen">(</span><span class="mord">1</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mclose">)</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.686em;"><span></span></span></span></span></span><span class="mclose nulldelimiter"></span></span><span class="mord"><span class="delimsizing size4">)</span></span><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:1.89444em;"><span style="top:-4.25em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">2</span></span></span></span></span></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:3.14447em;vertical-align:-1.25003em;"></span><span class="mord"><span class="delimsizing size4">(</span></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:1.37144em;"><span style="top:-2.314em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">2</span></span></span><span style="top:-3.23em;"><span class="pstrut" style="height:3em;"></span><span class="frac-line" style="border-bottom-width:0.04em;"></span></span><span style="top:-3.677em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mord">²</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.686em;"><span></span></span></span></span></span><span class="mclose nulldelimiter"></span></span><span class="mord"><span class="delimsizing size4">)</span></span><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:1.89444em;"><span style="top:-4.25em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">2</span></span></span></span></span></span></span></span></span></span></div></figure><p id="b8d7c626-163e-4f96-bd4b-338cf5c5a3e9" class="">Assim:</p><figure id="5e3042ff-1f5f-4668-acf9-1106a94aac0b" class="equation"><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><div class="equation-container"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><msub><mi>S</mi><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow></msub><mo>=</mo><mo fence="false" stretchy="true" minsize="3em" maxsize="3em">(</mo><mfrac><mrow><mi>k</mi><mo>+</mo><mi>k</mi><mtext>²</mtext></mrow><mn>2</mn></mfrac><mo fence="false" stretchy="true" minsize="3em" maxsize="3em">)</mo><mpadded voffset="1.25em"><mstyle scriptlevel="0" displaystyle="false"><mstyle scriptlevel="0" displaystyle="false"><mn>2</mn></mstyle></mstyle></mpadded><mo>+</mo><mo stretchy="false">(</mo><mi>k</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo><mtext>³</mtext><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><mtext>⠀⠀⠀⠀⠀</mtext><mo>=</mo><mfrac><mrow><mi>k</mi><mtext>²</mtext><mo>+</mo><mn>2</mn><mi>k</mi><mtext>³</mtext><mo>+</mo><mi>k</mi><mtext>⁴</mtext></mrow><mn>4</mn></mfrac><mo>+</mo><mfrac><mrow><mn>4</mn><mo stretchy="false">(</mo><mi>k</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo><mtext>³</mtext></mrow><mn>4</mn></mfrac><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><mtext>⠀⠀⠀⠀⠀</mtext><mo>=</mo><mfrac><mrow><mi>k</mi><mtext>⁴</mtext><mo>+</mo><mn>6</mn><mi>k</mi><mtext>³</mtext><mo>+</mo><mn>13</mn><mi>k</mi><mtext>²</mtext><mo>+</mo><mn>12</mn><mi>k</mi><mo>+</mo><mn>4</mn></mrow><mn>4</mn></mfrac><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><mtext>⠀⠀⠀⠀⠀</mtext><mo>=</mo><mfrac><mrow><mo stretchy="false">(</mo><mi>k</mi><mtext>²</mtext><mo>+</mo><mn>4</mn><mi>k</mi><mo>+</mo><mn>4</mn><mo stretchy="false">)</mo><mo stretchy="false">(</mo><mi>k</mi><mtext>²</mtext><mo>+</mo><mn>2</mn><mi>k</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo></mrow><mn>4</mn></mfrac><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><mtext>⠀⠀⠀⠀⠀</mtext><mo>=</mo><mo fence="false" stretchy="true" minsize="3em" maxsize="3em">(</mo><mfrac><mrow><mo stretchy="false">(</mo><mn>1</mn><mo>+</mo><mo stretchy="false">(</mo><mi>k</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo><mo stretchy="false">)</mo><mo stretchy="false">(</mo><mi>k</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo></mrow><mn>2</mn></mfrac><mo fence="false" stretchy="true" minsize="3em" maxsize="3em">)</mo><mpadded voffset="1.25em"><mstyle scriptlevel="0" displaystyle="false"><mstyle scriptlevel="0" displaystyle="false"><mn>2</mn></mstyle></mstyle></mpadded></mrow><annotation encoding="application/x-tex">S_{k+1} = \Bigg ( \frac {k + k²} {2} \Bigg )\raisebox{1.25em}{$2$} + (k+1)³
\\
⠀
\\
⠀⠀⠀⠀⠀ = \frac {k² + 2 k³ + k⁴} {4} + \frac {4(k+1)³} {4}
\\
⠀
\\
⠀⠀⠀⠀⠀= \frac {k⁴ + 6k³ + 13k² + 12k + 4} {4}
\\
⠀
\\

⠀⠀⠀⠀⠀= \frac {(k² + 4k + 4)(k² + 2k + 1)} {4}
\\
⠀
\\
⠀⠀⠀⠀⠀= \Bigg (\frac {(1 + (k+1))(k+1)} {2} \Bigg )\raisebox{1.25em}{$2$}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.891661em;vertical-align:-0.208331em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.3361079999999999em;"><span style="top:-2.5500000000000003em;margin-left:-0.05764em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.208331em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:3.14447em;vertical-align:-1.25003em;"></span><span class="mord"><span class="delimsizing size4">(</span></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:1.37144em;"><span style="top:-2.314em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">2</span></span></span><span style="top:-3.23em;"><span class="pstrut" style="height:3em;"></span><span class="frac-line" style="border-bottom-width:0.04em;"></span></span><span style="top:-3.677em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mord">²</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.686em;"><span></span></span></span></span></span><span class="mclose nulldelimiter"></span></span><span class="mord"><span class="delimsizing size4">)</span></span><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:1.89444em;"><span style="top:-4.25em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">2</span></span></span></span></span></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mopen">(</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">1</span><span class="mclose">)</span><span class="mord">³</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.36687em;vertical-align:0em;"></span><span class="mord">⠀⠀⠀⠀⠀</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:2.05744em;vertical-align:-0.686em;"></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:1.37144em;"><span style="top:-2.314em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">4</span></span></span><span style="top:-3.23em;"><span class="pstrut" style="height:3em;"></span><span class="frac-line" style="border-bottom-width:0.04em;"></span></span><span style="top:-3.677em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mord">²</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">2</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mord">³</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mord">⁴</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.686em;"><span></span></span></span></span></span><span class="mclose nulldelimiter"></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:2.113em;vertical-align:-0.686em;"></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:1.427em;"><span style="top:-2.314em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">4</span></span></span><span style="top:-3.23em;"><span class="pstrut" style="height:3em;"></span><span class="frac-line" style="border-bottom-width:0.04em;"></span></span><span style="top:-3.677em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">4</span><span class="mopen">(</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">1</span><span class="mclose">)</span><span class="mord">³</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.686em;"><span></span></span></span></span></span><span class="mclose nulldelimiter"></span></span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.36687em;vertical-align:0em;"></span><span class="mord">⠀⠀⠀⠀⠀</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:2.05744em;vertical-align:-0.686em;"></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:1.37144em;"><span style="top:-2.314em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">4</span></span></span><span style="top:-3.23em;"><span class="pstrut" style="height:3em;"></span><span class="frac-line" style="border-bottom-width:0.04em;"></span></span><span style="top:-3.677em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mord">⁴</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">6</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mord">³</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">13</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mord">²</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">12</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">4</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.686em;"><span></span></span></span></span></span><span class="mclose nulldelimiter"></span></span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.36687em;vertical-align:0em;"></span><span class="mord">⠀⠀⠀⠀⠀</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:2.113em;vertical-align:-0.686em;"></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:1.427em;"><span style="top:-2.314em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">4</span></span></span><span style="top:-3.23em;"><span class="pstrut" style="height:3em;"></span><span class="frac-line" style="border-bottom-width:0.04em;"></span></span><span style="top:-3.677em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mopen">(</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mord">²</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">4</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">4</span><span class="mclose">)</span><span class="mopen">(</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mord">²</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">2</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">1</span><span class="mclose">)</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.686em;"><span></span></span></span></span></span><span class="mclose nulldelimiter"></span></span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.36687em;vertical-align:0em;"></span><span class="mord">⠀⠀⠀⠀⠀</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:3.14447em;vertical-align:-1.25003em;"></span><span class="mord"><span class="delimsizing size4">(</span></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:1.427em;"><span style="top:-2.314em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">2</span></span></span><span style="top:-3.23em;"><span class="pstrut" style="height:3em;"></span><span class="frac-line" style="border-bottom-width:0.04em;"></span></span><span style="top:-3.677em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mopen">(</span><span class="mord">1</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mopen">(</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">1</span><span class="mclose">))</span><span class="mopen">(</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">1</span><span class="mclose">)</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.686em;"><span></span></span></span></span></span><span class="mclose nulldelimiter"></span></span><span class="mord"><span class="delimsizing size4">)</span></span><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:1.89444em;"><span style="top:-4.25em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">2</span></span></span></span></span></span></span></span></span></span></div></figure><p id="aa674285-000e-4440-9e90-6cf1cc938434" class="">Perceba que chegamos numa fórmula de PA de <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">k+ 1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.77777em;vertical-align:-0.08333em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span></span></span></span></span><span>﻿</span></span> elementos, portando:</p><figure id="ab585952-6e8b-46b6-acda-613c5338a2b6" class="equation"><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><div class="equation-container"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><msub><mi>S</mi><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow></msub><mo>=</mo><mo fence="false" stretchy="true" minsize="3em" maxsize="3em">(</mo><mfrac><mrow><mo stretchy="false">(</mo><mn>1</mn><mo>+</mo><mo stretchy="false">(</mo><mi>k</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo><mo stretchy="false">)</mo><mo stretchy="false">(</mo><mi>k</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo></mrow><mn>2</mn></mfrac><mo fence="false" stretchy="true" minsize="3em" maxsize="3em">)</mo><mpadded voffset="1.25em"><mstyle scriptlevel="0" displaystyle="false"><mstyle scriptlevel="0" displaystyle="false"><mn>2</mn></mstyle></mstyle></mpadded><mo>=</mo><mo stretchy="false">(</mo><mn>1</mn><mo>+</mo><mn>2</mn><mo>+</mo><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mo>+</mo><mi>k</mi><mo>+</mo><mo stretchy="false">(</mo><mi>k</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo><mo stretchy="false">)</mo><mtext>²</mtext></mrow><annotation encoding="application/x-tex">S_{k+1} = \Bigg (\frac {(1 + (k+1))(k+1)} {2} \Bigg )\raisebox{1.25em}{$2$} = (1 + 2 + ... + k + (k+1))²</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.891661em;vertical-align:-0.208331em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.3361079999999999em;"><span style="top:-2.5500000000000003em;margin-left:-0.05764em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.208331em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:3.14447em;vertical-align:-1.25003em;"></span><span class="mord"><span class="delimsizing size4">(</span></span><span class="mord"><span class="mopen nulldelimiter"></span><span class="mfrac"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:1.427em;"><span style="top:-2.314em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">2</span></span></span><span style="top:-3.23em;"><span class="pstrut" style="height:3em;"></span><span class="frac-line" style="border-bottom-width:0.04em;"></span></span><span style="top:-3.677em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mopen">(</span><span class="mord">1</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mopen">(</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">1</span><span class="mclose">))</span><span class="mopen">(</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mord">1</span><span class="mclose">)</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.686em;"><span></span></span></span></span></span><span class="mclose nulldelimiter"></span></span><span class="mord"><span class="delimsizing size4">)</span></span><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:1.89444em;"><span style="top:-4.25em;"><span class="pstrut" style="height:3em;"></span><span class="mord"><span class="mord">2</span></span></span></span></span></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mopen">(</span><span class="mord">1</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">2</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord">...</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.77777em;vertical-align:-0.08333em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mopen">(</span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">1</span><span class="mclose">))</span><span class="mord">²</span></span></span></span></span></div></figure><p id="dc5c0da6-5f5d-4541-a243-c4f54f38a9cf" class="">Assim, chegamos ao resultado esperado e, supondo que a propriedade do enunciado é válida para <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>k</mi></mrow><annotation encoding="application/x-tex">k</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.69444em;vertical-align:0em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span></span></span></span></span><span>﻿</span></span>, então será verdadeira para o próximo elemento <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">k + 1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.77777em;vertical-align:-0.08333em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span></span></span></span></span><span>﻿</span></span>.</p></div></p></div></p><p id="c6f65ca1-b297-4b8c-9c52-91f7a3c35a0f" class="">
</p><p id="41d83c00-ca89-4a7c-aa04-9841728c55db" class=""><strong>2° Seja T uma árvore binária cheia de altura h, h ≥ 0. Prove por indução matemática que T tem </strong><strong><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>n</mi><mo>=</mo><msup><mn>2</mn><mrow><mi>h</mi><mo>+</mo><mn>1</mn></mrow></msup><mo>−</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">n = 2^{h+1} - 1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.43056em;vertical-align:0em;"></span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.9324379999999999em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8491079999999999em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight">h</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span></span></span></span></span><span>﻿</span></span></strong><strong> nós. Uma árvore binária é dita cheia quando todos os nós de um nível ou são folhas ou possuem exatamente dois filhos.</strong><div class="indented"><p id="46939ae1-2714-494c-9036-e37bd98a97d9" class="">Variável de Indução:<div class="indented"><p id="902cecdd-a37e-4a77-9ad6-0097c7a3a2d9" class="">Altura da Árvore, <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>h</mi></mrow><annotation encoding="application/x-tex">h</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.69444em;vertical-align:0em;"></span><span class="mord mathnormal">h</span></span></span></span></span><span>﻿</span></span>.</p></div></p><p id="e240e698-5935-4bad-913e-09e4d5dfcd87" class="">Caso Base:<div class="indented"><p id="7cb1b44c-c718-4b2f-9d86-3d2f9f24ac07" class="">Sabemos que numa árvore cheia o número de nós da respectiva altura, <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>h</mi></mrow><annotation encoding="application/x-tex">h</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.69444em;vertical-align:0em;"></span><span class="mord mathnormal">h</span></span></span></span></span><span>﻿</span></span>, é dada por: <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mn>2</mn><mi>h</mi></msup></mrow><annotation encoding="application/x-tex">2^h</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.849108em;vertical-align:0em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.849108em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight">h</span></span></span></span></span></span></span></span></span></span></span></span><span>﻿</span></span>. Então, a soma dessa propriedade aplicada em cada nível até a altura <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>h</mi></mrow><annotation encoding="application/x-tex">h</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.69444em;vertical-align:0em;"></span><span class="mord mathnormal">h</span></span></span></span></span><span>﻿</span></span> será igual à  <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mn>2</mn><mrow><mi>h</mi><mo>+</mo><mn>1</mn></mrow></msup><mo>−</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">2^{h + 1} -1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.9324379999999999em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8491079999999999em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight">h</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span></span></span></span></span><span>﻿</span></span>. </p><p id="2e008af6-4032-4630-bfd1-8250460051b6" class="">Para <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>h</mi><mo>=</mo><mn>0</mn><mo>→</mo><mi>n</mi><mo>=</mo><msup><mn>2</mn><mrow><mn>0</mn><mo>+</mo><mn>1</mn></mrow></msup><mo>−</mo><mn>1</mn><mo>=</mo><msup><mn>2</mn><mn>0</mn></msup><mo>=</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">h = 0 \rightarrow n = 2^{0+1} -1 = 2^0 = 1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.69444em;vertical-align:0em;"></span><span class="mord mathnormal">h</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">0</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">→</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.43056em;vertical-align:0em;"></span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.897438em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141079999999999em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mtight">0</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.8141079999999999em;vertical-align:0em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8141079999999999em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">0</span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span></span></span></span></span><span>﻿</span></span></p><p id="1fa663f3-3a27-44aa-98a1-dc0df70619d5" class="">Assim, a propriedade é válida para o Caso Base.</p></div></p><p id="30aac435-e405-4458-9b9d-c1ee06504ca4" class="">Hipótese de Indução:<div class="indented"><p id="c1c851c0-1903-492a-acc3-51c5b582612c" class="">Supomos que tal propriedade é válida para uma árvore de altura <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>h</mi><mo>=</mo><mi>k</mi></mrow><annotation encoding="application/x-tex">h = k</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.69444em;vertical-align:0em;"></span><span class="mord mathnormal">h</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.69444em;vertical-align:0em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span></span></span></span></span><span>﻿</span></span>, logo:</p><figure id="d748b86d-42c4-49c7-9734-3dfa166f310e" class="equation"><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><div class="equation-container"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><msup><mn>2</mn><mn>0</mn></msup><mo>+</mo><msup><mn>2</mn><mn>1</mn></msup><mo>+</mo><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mo>+</mo><msup><mn>2</mn><mi>k</mi></msup><mo>=</mo><msup><mn>2</mn><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow></msup><mo>−</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">2^0 + 2^1 + ... + 2^k = 2^{k+1} - 1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.9474379999999999em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8641079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">0</span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.9474379999999999em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8641079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">1</span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord">...</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.8991079999999999em;vertical-align:0em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8991079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.9824379999999999em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8991079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span></span></span></span></span></div></figure></div></p><p id="d94ba4f4-7682-4f27-9232-32be24d13c56" class="">Caso Geral:<div class="indented"><p id="14c40326-5905-43fc-9794-2c823e519533" class="">Assim, vamos tentar provar a propriedade para uma altura <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">k+1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.77777em;vertical-align:-0.08333em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span></span></span></span></span><span>﻿</span></span>. Dessa forma, esperamos chegar no resultado <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><msup><mn>2</mn><mrow><mi>k</mi><mo>+</mo><mn>2</mn></mrow></msup><mo>−</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">2^{k + 2} -1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.9324379999999999em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8491079999999999em;"><span style="top:-3.063em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">2</span></span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span></span></span></span></span><span>﻿</span></span>:</p><figure id="ac2da05e-387d-49d5-aa18-2343cd652f4b" class="equation"><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><div class="equation-container"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><msub><mi>S</mi><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow></msub><mo>=</mo><msup><mn>2</mn><mn>0</mn></msup><mo>+</mo><msup><mn>2</mn><mn>1</mn></msup><mo>+</mo><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mi mathvariant="normal">.</mi><mo>+</mo><msup><mn>2</mn><mi>k</mi></msup><mo>+</mo><msup><mn>2</mn><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow></msup></mrow><annotation encoding="application/x-tex">S_{k+1} = 2^0 + 2^1 + ... + 2^k + 2^{k+1}</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.891661em;vertical-align:-0.208331em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.3361079999999999em;"><span style="top:-2.5500000000000003em;margin-left:-0.05764em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.208331em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.9474379999999999em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8641079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">0</span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.9474379999999999em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8641079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight">1</span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord">...</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.9824379999999999em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8991079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.8991079999999999em;vertical-align:0em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8991079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span></span></span></span></span></span></span></span></span></div></figure><p id="fca757b7-198f-464e-a6ef-03b821df6bc5" class="">Aplicando a Hipótese de Indução:</p><figure id="592f9c94-68cb-4360-beeb-51e6706ba4b4" class="equation"><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><div class="equation-container"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><msub><mi>S</mi><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow></msub><mo>=</mo><msup><mn>2</mn><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow></msup><mo>−</mo><mn>1</mn><mo>+</mo><msup><mn>2</mn><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow></msup><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><msub><mi>S</mi><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow></msub><mo>=</mo><mn>2</mn><mo stretchy="false">(</mo><msup><mn>2</mn><mrow><mi>k</mi><mo>+</mo><mn>1</mn></mrow></msup><mo stretchy="false">)</mo><mo>−</mo><mn>1</mn><mo>=</mo><msup><mn>2</mn><mrow><mi>k</mi><mo>+</mo><mn>2</mn></mrow></msup><mo>−</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">S_{k+1} = 2^{k+1} - 1 + 2^{k + 1}
\\
⠀
\\
S_{k+1}= 2(2^{k+1}) - 1 = 2^{k+2} - 1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.891661em;vertical-align:-0.208331em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.3361079999999999em;"><span style="top:-2.5500000000000003em;margin-left:-0.05764em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.208331em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.9824379999999999em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8991079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">1</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.8991079999999999em;vertical-align:0em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8991079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span></span></span></span></span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.891661em;vertical-align:-0.208331em;"></span><span class="mord"><span class="mord mathnormal" style="margin-right:0.05764em;">S</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.3361079999999999em;"><span style="top:-2.5500000000000003em;margin-left:-0.05764em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.208331em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1.149108em;vertical-align:-0.25em;"></span><span class="mord">2</span><span class="mopen">(</span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8991079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">1</span></span></span></span></span></span></span></span></span><span class="mclose">)</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.9824379999999999em;vertical-align:-0.08333em;"></span><span class="mord"><span class="mord">2</span><span class="msupsub"><span class="vlist-t"><span class="vlist-r"><span class="vlist" style="height:0.8991079999999999em;"><span style="top:-3.113em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight" style="margin-right:0.03148em;">k</span><span class="mbin mtight">+</span><span class="mord mtight">2</span></span></span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span></span></span></span></span></div></figure><p id="c90f1ff5-f3eb-4c3a-9299-e2cb127a7e47" class="">Logo, chegamos ao resultado esperado e a propriedade provou-se verdadeira.</p></div></p></div></p><p id="0d9a5506-f306-4555-8aaf-566809c678f3" class="">
</p><p id="8f2554d0-94f8-4994-943e-acab35ebb9ec" class=""><strong>3° Dado um vetor de inteiros de n elementos, elabore um algoritmo para determinar quantos destes números são negativos.</strong><div class="indented"><p id="6027e364-f44c-47bb-9018-993a430a8e61" class="">Variável de Indução:<div class="indented"><p id="dcfc0dff-bf5b-49e3-ba12-0f442fe6d5d2" class="">Quantidade de elementos, <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>n</mi></mrow><annotation encoding="application/x-tex">n</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.43056em;vertical-align:0em;"></span><span class="mord mathnormal">n</span></span></span></span></span><span>﻿</span></span>.</p></div></p><p id="def11e24-fb68-431a-9ecb-d42e223a708a" class="">Caso Base:<div class="indented"><p id="ac5cb246-dcce-4bde-9f45-5710bee0253e" class="">Lista vazia, <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>n</mi><mo>=</mo><mn>0</mn><mo>→</mo></mrow><annotation encoding="application/x-tex">n = 0 \rightarrow</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.43056em;vertical-align:0em;"></span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">0</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">→</span></span></span></span></span><span>﻿</span></span> retorna <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mn>0</mn></mrow><annotation encoding="application/x-tex">0</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">0</span></span></span></span></span><span>﻿</span></span>.</p></div></p><p id="1aad6297-1e21-4e9b-89e4-578b23ec9517" class="">Hipótese de Indução:<div class="indented"><p id="1f59b67a-da63-4bfb-8501-3d96766dd38d" class="">Sabemos resolver o problema para <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>k</mi><mo>=</mo><mi>n</mi><mo>−</mo><mn>1</mn></mrow><annotation encoding="application/x-tex">k = n - 1</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.69444em;vertical-align:0em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">−</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">1</span></span></span></span></span><span>﻿</span></span> elementos.</p></div></p><p id="8368d144-0923-4e4f-a6d0-facbbf164ed8" class="">Caso geral:<div class="indented"><p id="c875a96b-32ff-4d98-aeaa-92d5d2e6594b" class="">Reservamos o primeiro elemento, comparamos se o mesmo é negativo e aplicamos a Hipótese de Indução no restante da lista.</p></div></p><p id="8414e213-77a9-4e75-ac4a-5788317e5a41" class="">Pseudo-código:<div class="indented"><pre id="b841c2e8-3383-489b-9490-3cad848657be" class="code"><code>algoritmo neg_lista(l): Inteiro
{-
Entrada: Lista com números inteiros.
Saída: Inteiro representando a quantidade de números negativos que existem na lista.
-}
	início
		Se L = nulo, então -- Caso Base
			retorne 0
		Senão -- Caso Geral
			retorne eh_neg(l.first) + neg_lista(l.prox)
	fim
	
função eh_neg(elem): Inteiro
{-
	Entrada: Inteiro a ser analizado.
	Saída: 0, se o número for positivo, e 1 se o número for negativo.
-}
	inicio
		Se elem &lt; 0, então
			retorne 1
		Senão
			retorne 0
	fim</code></pre></div></p><p id="3d6f775e-ff52-4fc1-8559-6ef8a13a3db5" class="">Código:<div class="indented"><pre id="e7498fc8-0cf4-4b13-a29b-a776f41dae58" class="code"><code>def neg_lista(lista):
  if lista == []:
    return 0
  else:
    return eh_neg(lista[0]) + neg_lista(lista[1:])

def eh_neg(elem):
  if elem &lt; 0:
    return 1
  else:
    return 0

l = [1,2,-5,-8,23,-9,0,3,1,-1,-5,-7]
print(neg_lista(l), end=&#x27;\n\n&#x27;)</code></pre></div></p></div></p><p id="21157ba9-6c98-48b8-a286-30ede2ca7e10" class="">
</p><p id="f5cbb465-22ac-4a13-be75-694ce9bcb86c" class="">4<strong>°  Dada uma árvore binária de inteiros e dois limites de intervalo, inferior e superior, determine a soma dos elementos da árvore que estão neste intervalo de valores (intervalo fechado).</strong><div class="indented"><p id="a2f6659b-e676-4452-9b87-cb1703ab1973" class="">Variável de Indução:<div class="indented"><p id="0d99c5ef-8a12-4011-bbea-e285f358c1e9" class="">Número de nós da Árvore, <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>n</mi></mrow><annotation encoding="application/x-tex">n</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.43056em;vertical-align:0em;"></span><span class="mord mathnormal">n</span></span></span></span></span><span>﻿</span></span>.</p></div></p><p id="a18e8dc4-8a68-4db5-95b1-b5d7a45e7280" class="">Caso Base:<div class="indented"><p id="4fe660f5-6b4f-490f-b3ad-d0d5f4760b0c" class="">Árvore vazia, <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mi>n</mi><mo>=</mo><mn>0</mn><mo>→</mo></mrow><annotation encoding="application/x-tex">n = 0 \rightarrow </annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.43056em;vertical-align:0em;"></span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">0</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">→</span></span></span></span></span><span>﻿</span></span> retorne <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mn>0</mn></mrow><annotation encoding="application/x-tex">0</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">0</span></span></span></span></span><span>﻿</span></span>.</p><p id="771e0ed2-d751-4f1b-8449-45b28be92764" class="">Altura atual é maior que o intervalo desejado <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mo>→</mo></mrow><annotation encoding="application/x-tex">\rightarrow</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.36687em;vertical-align:0em;"></span><span class="mrel">→</span></span></span></span></span><span>﻿</span></span> retorne <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mn>0</mn></mrow><annotation encoding="application/x-tex">0</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">0</span></span></span></span></span><span>﻿</span></span>.</p></div></p><p id="9c4ddd0a-d12b-43ad-9c27-a1904e422efb" class="">Hipótese de Indução: <div class="indented"><p id="56d43a99-3b2f-4a33-88a6-7f2a196b3642" class="">Sei resolver para uma árvore com <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mn>1</mn><mo>≤</mo><mi>k</mi><mo>&lt;</mo><mi>n</mi></mrow><annotation encoding="application/x-tex">1 \leq k &lt; n</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.78041em;vertical-align:-0.13597em;"></span><span class="mord">1</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">≤</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.73354em;vertical-align:-0.0391em;"></span><span class="mord mathnormal" style="margin-right:0.03148em;">k</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">&lt;</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.43056em;vertical-align:0em;"></span><span class="mord mathnormal">n</span></span></span></span></span><span>﻿</span></span>.</p></div></p><p id="b384f3d1-f3ed-4cad-945f-a1864e60ccbe" class="">Caso geral:<div class="indented"><p id="a1c87f20-0a33-42b8-85ad-dd9951a7f7f1" class="">Dividiremos a árvore em subárvores cada vez menores, aplicaremos uma função auxiliar no Nó raiz da Árvore atual para verificar se o mesmo encontra-se no intervalo desejado, se sim retornamos o mesmo, caso não, retornamos <style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><span data-token-index="0" contenteditable="false" class="notion-text-equation-token" style="user-select:all;-webkit-user-select:all;-moz-user-select:all"><span></span><span><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML"><semantics><mrow><mn>0</mn></mrow><annotation encoding="application/x-tex">0</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">0</span></span></span></span></span><span>﻿</span></span>. Assim, aplicamos a Hipótese Indutiva.</p></div></p><p id="671e52e6-e652-482c-89bd-723d7f5c67d1" class="">Pseudo-código:<div class="indented"><pre id="b3edc314-c6e1-4e48-8015-e3fe90ab539e" class="code"><code>algoritmo sum_tree(root, altura, limite_inf, limite_sup): Inteiro
{-
	Entrada: Árvore Binária, sua Altura inicial (geralmente 0) 
					 e o limite inferior e superior desejado.  
	Saída: Número inteiro representado a soma dos 
				 elementos da Árvore no intervalo desejado.
-}
	inicio
	  Se root = Vazio || altura &gt; lim_sup, então -- Caso Base
	    retorne 0
	  
	  Senão -- Caso Geral
	    retorne sum_n(root.key, altura, limite_inf, limite_sup) + 
							sum_tree(root.left, altura + 1, limite_inf, limite_sup) + 
							sum_tree(root.right, altura + 1, limite_inf, limite_sup)
	fim

função sum_n(key, altura, lim_inf, lim_sup): Inteiro
{-
	Entrada: Valor do Nó que deseja-se analisar, Altura atual 
					 e os limites inferior e superior desejado.
	Saída: 0, se o valor não estiver no intervalo correto, 
				 caso contrário retorna-se o valor do nó.
-}
	inicio
	  Se altura &gt;= lim_inf &amp;&amp; altura &lt;= lim_sup, então
	    retorne key
	  Senão
	    retorne 0
	fim</code></pre></div></p><p id="d152b381-29bd-4b9c-b681-81dc22208b79" class="">Código:<div class="indented"><pre id="e783571f-ed7d-4150-94a4-790238007c8a" class="code"><code>from binarytree import BinaryTree

tree = BinaryTree()

&quot;&quot;&quot;
       10
    5      13
  3  6   12  14
&quot;&quot;&quot;

tree.add(10)
tree.add(5)
tree.add(13)
tree.add(3)
tree.add(6)
tree.add(12)
tree.add(14)

def sum_tree(root, altura, lim_inf, lim_sup):
  if root == None or altura &gt; lim_sup:
    return 0
  
  else:
    return sum_n(root.key, altura, lim_inf, lim_sup) + sum_tree(root.left, altura + 1, lim_inf, lim_sup) + sum_tree(root.right, altura + 1, lim_inf, lim_sup)

def sum_n(key, altura, lim_inf, lim_sup):
  if altura &gt;= lim_inf and altura &lt;= lim_sup:
    return key
  else:
    return 0

print(sum_tree(tree.r, 0, 0, 0), end=&#x27;\n\n&#x27;)</code></pre></div></p></div></p><p id="ad6b544f-d863-435b-9f1a-405dd30a8335" class="">
</p><p id="c1c480e2-4d1f-4000-bbf1-23f7b15efb3b" class="">5<strong>° Dados dois vetores de inteiros ordenados em ordem crescente, gere um terceiro vetor com os dados dos vetores de entrada também ordenados em ordem crescente, mas sem elementos repetidos.</strong><div class="indented"><p id="236734ff-7dc2-4b43-aecc-b496eb3f96af" class="">Ideia para solução:<div class="indented"><p id="057d030c-43db-407c-baf3-f852a143f323" class="">Vamos passar os dois vetores como argumentos .</p><p id="4cb05045-6def-49b9-8ed6-d202ad58a05f" class="">Primeiramente vemos qual dos vetores tem o menor último número, assim podemos criar um laço de repetição com esse vetor. Pois, ao terminar o laço irá sobrar elementos no segundo vetor e basta concatená-lo com o resultado. </p><p id="aba94fee-f4d0-4b96-bfc3-18f297a5b879" class="">No laço de repetição criamos duas variáveis de posição. Inciamos comparando os elementos das posições dos vetores desejadas e dependendo do resultado aumentamos a variável de posição do vetor que acabamos de pegar o elemento. Caso o elemento exista nos dois vetores aumentamos a variável de posição de ambos os vetores. Assim, percorremos todo o menor vetor definido no começo do programa, restando apenas concatenar o restante do maior vetor ao resultado.</p><p id="0c334209-6d58-43da-8de9-7ab12704c565" class="">
</p></div></p><p id="9efc6f53-3809-45dc-89ee-81cfce9f2c5f" class="">Pseudocódigo<div class="indented"><pre id="7eccaf54-bd25-45f1-a077-2364a4f8d94a" class="code"><code>algoritmo ord_vetor(vetor_a, vetor_b, tam_a, tam_b): Vetor de Inteiros
{-
	Entrada: Dois vetores de inteiros e seus respectivos tamanhos.
	Saída: Vetor contendo os elementos dos dois vetores ordenados. 
-}
	inicio
	  Se vetor_a = Vazio, então
	    retorne vetor_b
	  Se vetor_b = Vazio, então
	    retorne vetor_a
	  Se vetor_a[tam_a] &lt; vetor_b[tam_b], então
	    menor := vetor_a
			len_menor := tam_a
			maior := vetor_b
			len_maior := tam_b
	  Senão
	    menor := vetor_b
			len_menor := tam_b
			maior := vetor_a
			len_maior := tam_a
	  
	  vetor_c := []
	  pos1 := 1
		pos2 := 1
	  Enquanto pos1 &lt;= len_menor, faça
	    Se menor[pos1] &lt; maior[pos2], então
	      vetor_c.append(menor[pos1])
	      pos1 := pos1 + 1
	    Se menor[pos1] &gt; maior[pos2], então
	      vetor_c.append(maior[pos2])
	      pos2 := pos2 + 1
	    Senão
	      vetor_c.append(menor[pos1])
	      pos1 := pos1 + 1
	      pos2 := pos2 + 1
	  
	  retorne vetor_c + maior[pos2:]
	fim</code></pre></div></p><p id="b2c3d116-4a6a-401b-96c6-5d0eadadaeaf" class="">
</p><p id="a702280e-bad8-4afe-a50c-621ac7310b1a" class="">Análise de Complexidade</p><figure id="4ae1e882-0949-4f0a-a468-6365800bad72" class="equation"><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><div class="equation-container"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><mstyle scriptlevel="0" displaystyle="false"><msubsup><mo>∑</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><mi mathvariant="normal">.</mi><mn>2</mn><mo>+</mo><mn>6</mn><mi>n</mi><mo>+</mo><mstyle scriptlevel="0" displaystyle="false"><msubsup><mo>∑</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>m</mi></msubsup><mo>=</mo><mn>2</mn><mo stretchy="false">(</mo><mi>n</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo><mo>+</mo><mn>6</mn><mi>n</mi><mo>+</mo><mi>m</mi><mo>=</mo><mn>8</mn><mi>n</mi><mo>+</mo><mi>m</mi><mo>+</mo><mn>2</mn><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><mi>C</mi><mi>o</mi><mi>m</mi><mi>p</mi><mi>l</mi><mi>e</mi><mi>x</mi><mi>i</mi><mi>d</mi><mi>a</mi><mi>d</mi><mi>e</mi><mo>:</mo><mi>O</mi><mo stretchy="false">(</mo><mi>n</mi><mo>+</mo><mi>m</mi><mo stretchy="false">)</mo><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><mi>E</mi><mi>s</mi><mi>p</mi><mi>a</mi><mi>ç</mi><mi>o</mi><mtext>⠀</mtext><mi>g</mi><mi>a</mi><mi>s</mi><mi>t</mi><mi>o</mi><mo>:</mo><mi>O</mi><mo stretchy="false">(</mo><mi>n</mi><mo>+</mo><mi>m</mi><mo stretchy="false">)</mo></mstyle></mstyle></mrow><annotation encoding="application/x-tex">\textstyle\sum_{i=1}^n . 2 + 6n + \textstyle\sum_{i=1}^m = 2(n+1) + 6n + m = 8n + m + 2
\\
⠀
\\
Complexidade: O(n + m)
\\
⠀
\\
Espaço⠀gasto: O(n + m)</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1.104002em;vertical-align:-0.29971000000000003em;"></span><span class="mop"><span class="mop op-symbol small-op" style="position:relative;top:-0.0000050000000000050004em;">∑</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.804292em;"><span style="top:-2.40029em;margin-left:0em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight">i</span><span class="mrel mtight">=</span><span class="mord mtight">1</span></span></span></span><span style="top:-3.2029em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight">n</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.29971000000000003em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.16666666666666666em;"></span><span class="mord">.2</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">6</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1.104002em;vertical-align:-0.29971000000000003em;"></span><span class="mop"><span class="mop op-symbol small-op" style="position:relative;top:-0.0000050000000000050004em;">∑</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.804292em;"><span style="top:-2.40029em;margin-left:0em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight">i</span><span class="mrel mtight">=</span><span class="mord mtight">1</span></span></span></span><span style="top:-3.2029em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight">m</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.29971000000000003em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">2</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">1</span><span class="mclose">)</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">6</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.43056em;vertical-align:0em;"></span><span class="mord mathnormal">m</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">8</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord mathnormal">m</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">2</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.8888799999999999em;vertical-align:-0.19444em;"></span><span class="mord mathnormal" style="margin-right:0.07153em;">C</span><span class="mord mathnormal">o</span><span class="mord mathnormal">m</span><span class="mord mathnormal" style="margin-right:0.01968em;">pl</span><span class="mord mathnormal">e</span><span class="mord mathnormal">x</span><span class="mord mathnormal">i</span><span class="mord mathnormal">d</span><span class="mord mathnormal">a</span><span class="mord mathnormal">d</span><span class="mord mathnormal">e</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">:</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.02778em;">O</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal">m</span><span class="mclose">)</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.8777699999999999em;vertical-align:-0.19444em;"></span><span class="mord mathnormal" style="margin-right:0.05764em;">E</span><span class="mord mathnormal">s</span><span class="mord mathnormal">p</span><span class="mord mathnormal">a</span><span class="mord mathnormal">ço</span><span class="mord">⠀</span><span class="mord mathnormal" style="margin-right:0.03588em;">g</span><span class="mord mathnormal">a</span><span class="mord mathnormal">s</span><span class="mord mathnormal">t</span><span class="mord mathnormal">o</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">:</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.02778em;">O</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal">m</span><span class="mclose">)</span></span></span></span></span></div></figure><p id="0036a159-aeca-47bd-97a7-2d8fafde594c" class="">
</p><p id="29b6b7c4-c4d5-43ba-bb5a-280971a4d492" class="">Código:</p><pre id="905254ad-67ae-45ff-8b67-ed83962a0233" class="code"><code>a = [1,2,4,5,10]
b = [4,5,6,9,11]

def ord_vetor(vetor_a, vetor_b):
  
  if vetor_a == []:
    return vetor_b
  elif vetor_b == []:
    return vetor_a
  elif vetor_a[-1]  &lt; vetor_b[-1]:
    menor, maior = vetor_a, vetor_b
  else:
    menor, maior = vetor_b, vetor_a
  
  vetor_c = []
  pos1, pos2 = 0, 0
  while pos1 &lt; len(menor):
    if menor[pos1] &lt; maior[pos2]:
      vetor_c.append(menor[pos1])
      pos1 += 1
    elif menor[pos1] &gt; maior[pos2]:
      vetor_c.append(maior[pos2])
      pos2 += 1 
    else:
      vetor_c.append(menor[pos1])
      pos1 += 1
      pos2 += 1
  
  return vetor_c + maior[pos2:]

print(ord_vetor(a,b), end=&#x27;\n\n&#x27;)</code></pre></div></p><p id="2be8bb4d-afec-4cf7-957d-c835167cc40d" class="">
</p><p id="bf81c981-55c8-4d01-ba7b-f65b50e3ab03" class="">6<strong>° Dados dois vetores de inteiros A e B, gere um terceiro vetor representando o vetor interseção dos vetores originais, nas duas situações abaixo. A solução para cada situação deve ser distinta, ou seja, você não pode reutilizar parte da solução de um item em outro item. O vetor de interseção não pode ter elementos duplicados.</strong><div class="indented"><p id="4ee0f47f-2bc1-43a9-a184-063e507bed6a" class=""><strong>a. A e B estão ordenados, em ordem decrescente</strong><div class="indented"><p id="9814f05d-c972-46cb-b292-839c56a2f1b7" class="">Ideia para solução:<div class="indented"><p id="1fbd7a41-4404-4b9e-bc55-9835b4bc8c09" class="">Nessa questão, adotamos uma estratégia similar a feita na questão anterior. Porém, dessa vez selecionamos o vetor que possui o maior último número. Assim, criaremos um laço de repetição com esse vetor. </p><p id="5ec04408-1c28-4145-b236-ff3f809a3873" class="">No laço de repetição comparamos os elementos e iremos aumentar as variáveis de posição dependendo do resultado da comparação, e só adicionaremos ao resultado se os elementos forem iguais.</p><p id="8b3f9b6a-725f-4c8e-9546-29f14e287fe6" class="">
</p></div></p><p id="c6115c4d-1157-4771-873c-2049102a4663" class="">Pseudocódigo:</p><pre id="ee5905c1-adb4-4688-9078-1154c9cec97d" class="code"><code>algoritmo ord_intersec(vetor_a, vetor_b, tam_a, tam_b): Vetor de Inteiros
{-
	Entrada: Vetores de Inteiros e seus respectivos tamanhos
	Saída: Interseção ordenadas dos vetores
-}
	início
	  Se vetor_a = Vazio || vetor_b = Vazio, então
	    retorne Vazio
	  Se vetor_a[tam_a]  &gt; vetor_b[tam_b], então
	    maior := vetor_a
			len_maior := tam_a
			menor := vetor_b
			len_menor := tam_b
	  else:
	    maior := vetor_b
			len_maior := tam_b
			menor := vetor_a
			len_menor := tam_a
	  
	  vetor_c := []
	  pos1 = 1
		pos2 = 1
	  Enquanto pos1 &lt; len_maior, faça
	    Se maior[pos1] &gt; menor[pos2], então
	      pos1 := pos1 + 1
	    Se maior[pos1] &lt; menor[pos2], então
	      pos2 := pos2 + 1
	    else:
	      vetor_c.append(maior[pos1])
	      pos1 := pos1 + 1
	      pos2 := pos2 + 1
	  
	  retorne vetor_c
	fim</code></pre><p id="46c218a2-1605-4db7-87b3-5554daf11b89" class="">
</p><p id="8c9c30ef-eafa-407e-ba19-0096cfe99120" class="">Análise de Complexidade:</p><figure id="9d3d035c-45a3-43da-99e1-b43aa8b5feac" class="equation"><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><div class="equation-container"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><mstyle scriptlevel="0" displaystyle="false"><msubsup><mo>∑</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><mi mathvariant="normal">.</mi><mn>2</mn><mo>+</mo><mn>5</mn><mi>n</mi><mo>=</mo><mn>2</mn><mo stretchy="false">(</mo><mi>n</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo><mo>+</mo><mn>5</mn><mi>n</mi><mo>=</mo><mn>7</mn><mi>n</mi><mo>+</mo><mn>2</mn><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><mi>C</mi><mi>o</mi><mi>m</mi><mi>p</mi><mi>l</mi><mi>e</mi><mi>x</mi><mi>i</mi><mi>d</mi><mi>a</mi><mi>d</mi><mi>e</mi><mo>:</mo><mi>O</mi><mo stretchy="false">(</mo><mi>n</mi><mo stretchy="false">)</mo><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><mi>E</mi><mi>s</mi><mi>p</mi><mi>a</mi><mi>ç</mi><mi>o</mi><mtext>⠀</mtext><mi>g</mi><mi>a</mi><mi>s</mi><mi>t</mi><mi>o</mi><mo>:</mo><mi>O</mi><mo stretchy="false">(</mo><mi>n</mi><mo stretchy="false">)</mo></mstyle></mrow><annotation encoding="application/x-tex">\textstyle\sum_{i=1}^n . 2 + 5n = 2(n+1) + 5n = 7n+2

\\
⠀
\\
Complexidade: O(n)

\\
⠀
\\
Espaço⠀gasto: O(n)</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1.104002em;vertical-align:-0.29971000000000003em;"></span><span class="mop"><span class="mop op-symbol small-op" style="position:relative;top:-0.0000050000000000050004em;">∑</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.804292em;"><span style="top:-2.40029em;margin-left:0em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight">i</span><span class="mrel mtight">=</span><span class="mord mtight">1</span></span></span></span><span style="top:-3.2029em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight">n</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.29971000000000003em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.16666666666666666em;"></span><span class="mord">.2</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">5</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">2</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">1</span><span class="mclose">)</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">5</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">7</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">2</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.8888799999999999em;vertical-align:-0.19444em;"></span><span class="mord mathnormal" style="margin-right:0.07153em;">C</span><span class="mord mathnormal">o</span><span class="mord mathnormal">m</span><span class="mord mathnormal" style="margin-right:0.01968em;">pl</span><span class="mord mathnormal">e</span><span class="mord mathnormal">x</span><span class="mord mathnormal">i</span><span class="mord mathnormal">d</span><span class="mord mathnormal">a</span><span class="mord mathnormal">d</span><span class="mord mathnormal">e</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">:</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.02778em;">O</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mclose">)</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.8777699999999999em;vertical-align:-0.19444em;"></span><span class="mord mathnormal" style="margin-right:0.05764em;">E</span><span class="mord mathnormal">s</span><span class="mord mathnormal">p</span><span class="mord mathnormal">a</span><span class="mord mathnormal">ço</span><span class="mord">⠀</span><span class="mord mathnormal" style="margin-right:0.03588em;">g</span><span class="mord mathnormal">a</span><span class="mord mathnormal">s</span><span class="mord mathnormal">t</span><span class="mord mathnormal">o</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">:</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.02778em;">O</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mclose">)</span></span></span></span></span></div></figure><p id="9b95c8e2-89f6-4626-978c-80bf7e114750" class="">
</p><p id="8db6e006-3a0e-4cd0-89aa-defffa1d822c" class="">Código:</p><pre id="96eabedc-72db-436a-aedb-b9031e34b7d1" class="code"><code>def ord_intersec(vetor_a, vetor_b):  
  if vetor_a == [] or vetor_b == []:
    return []
  elif vetor_a[-1]  &gt; vetor_b[-1]:
    maior, menor = vetor_a, vetor_b
  else:
    maior, menor = vetor_b, vetor_a
  
  vetor_c = []
  pos1, pos2 = 0, 0
  while pos1 &lt; len(maior):
    if maior[pos1] &gt; menor[pos2]:
      pos1 += 1
    elif maior[pos1] &lt; menor[pos2]:
      pos2 += 1 
    else:
      vetor_c.append(maior[pos1])
      pos1 += 1
      pos2 += 1
  
  return vetor_c

v_a = [10,6,4,2,1]
v_b = [11,9,6,5,4]

print(ord_intersec(v_a, v_b), end=&#x27;\n\n&#x27;)</code></pre></div></p></div></p><p id="7d24a6d0-2656-42ff-aa0a-6bfece8a6fc4" class=""><div class="indented"><p id="f8ad7324-c22c-4764-a229-5198e83aa514" class=""><strong>b. A e B estão em ordem arbitrária.</strong><div class="indented"><p id="43c848af-bc97-4b97-ae7f-49e38a1b3ee3" class="">Ideia para solução:<div class="indented"><p id="fa41ebc0-56a6-4822-b864-175610c303eb" class="">Para resolver essa questão, iremos verificar qual é o menor vetor em tamanho e criaremos um laço “for” com tal vetor, e dentro desse laço criaremos outro “for” com o maior vetor. Assim, iremos comparar todos os elementos em busca dos iguais e retorná-los em uma lista.</p></div></p><p id="58d925fe-0666-4dd0-9fa3-ee082cdea576" class="">Pseudocódigo:<div class="indented"><pre id="cc5dda7a-bc46-4395-8651-174a34939874" class="code"><code>algoritmo intersec(vetor_a, vetor_b): Vetor de Inteiros
{-
	Entrada: Dois vetores de Inteiros
	Saída: Vetor contendo a interseção dos vetores passados como argumento
-}
	início
	  Se vetor_a = Vazio || vetor_b = Vazio, então
	    retorne Vazio
	  Se len(vetor_a)  &gt; len(vetor_b), então
	    maior = vetor_a
		  menor = vetor_b
	  Senão
	    maior = vetor_b
			menor = vetor_a
	  
	  vetor_c := []
	  Para cada i em menor, faça
	    Para cada j em maior, faça
	      Se i = j, então
	        vetor_c.append(i)
	
	  retorne vetor_c
	fim</code></pre></div></p><p id="993040fc-5cca-42cf-a93a-53d2650745ea" class="">
</p><p id="e9c651ff-0044-4204-8773-51f21cd6d5a5" class="">Análise de Complexidade:</p><figure id="74c7276f-624d-4253-9bb2-2c6c023c90b4" class="equation"><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><div class="equation-container"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><mstyle scriptlevel="0" displaystyle="false"><msubsup><mo>∑</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><mi mathvariant="normal">.</mi><mstyle scriptlevel="0" displaystyle="false"><msubsup><mo>∑</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>m</mi></msubsup><mi mathvariant="normal">.</mi><mn>3</mn><mo>=</mo><mn>3</mn><mo stretchy="false">(</mo><mi>n</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo><mo stretchy="false">(</mo><mi>n</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo><mo>=</mo><mn>3</mn><mo stretchy="false">(</mo><mi>n</mi><mtext>²</mtext><mo>+</mo><mn>2</mn><mi>n</mi><mo>+</mo><mn>1</mn><mo stretchy="false">)</mo><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><mi>C</mi><mi>o</mi><mi>m</mi><mi>p</mi><mi>l</mi><mi>e</mi><mi>x</mi><mi>i</mi><mi>d</mi><mi>a</mi><mi>d</mi><mi>e</mi><mo>:</mo><mi>O</mi><mo stretchy="false">(</mo><mi>n</mi><mtext>²</mtext><mo stretchy="false">)</mo><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><mi>E</mi><mi>s</mi><mi>p</mi><mi>a</mi><mi>ç</mi><mi>o</mi><mtext>⠀</mtext><mi>g</mi><mi>a</mi><mi>s</mi><mi>t</mi><mi>o</mi><mo>:</mo><mi>O</mi><mo stretchy="false">(</mo><mi>n</mi><mo stretchy="false">)</mo></mstyle></mstyle></mrow><annotation encoding="application/x-tex">\textstyle\sum_{i=1}^n . \textstyle\sum_{i=1}^m . 3 = 3(n + 1)(n + 1) = 3(n² + 2n + 1)

\\
⠀
\\
Complexidade: O(n²)

\\
⠀
\\
Espaço⠀gasto: O(n)</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1.104002em;vertical-align:-0.29971000000000003em;"></span><span class="mop"><span class="mop op-symbol small-op" style="position:relative;top:-0.0000050000000000050004em;">∑</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.804292em;"><span style="top:-2.40029em;margin-left:0em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight">i</span><span class="mrel mtight">=</span><span class="mord mtight">1</span></span></span></span><span style="top:-3.2029em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight">n</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.29971000000000003em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.16666666666666666em;"></span><span class="mord">.</span><span class="mspace" style="margin-right:0.16666666666666666em;"></span><span class="mop"><span class="mop op-symbol small-op" style="position:relative;top:-0.0000050000000000050004em;">∑</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.804292em;"><span style="top:-2.40029em;margin-left:0em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight">i</span><span class="mrel mtight">=</span><span class="mord mtight">1</span></span></span></span><span style="top:-3.2029em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight">m</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.29971000000000003em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.16666666666666666em;"></span><span class="mord">.3</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">3</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">1</span><span class="mclose">)</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">1</span><span class="mclose">)</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">3</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mord">²</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">2</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord">1</span><span class="mclose">)</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.8888799999999999em;vertical-align:-0.19444em;"></span><span class="mord mathnormal" style="margin-right:0.07153em;">C</span><span class="mord mathnormal">o</span><span class="mord mathnormal">m</span><span class="mord mathnormal" style="margin-right:0.01968em;">pl</span><span class="mord mathnormal">e</span><span class="mord mathnormal">x</span><span class="mord mathnormal">i</span><span class="mord mathnormal">d</span><span class="mord mathnormal">a</span><span class="mord mathnormal">d</span><span class="mord mathnormal">e</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">:</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.02778em;">O</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mord">²</span><span class="mclose">)</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.8777699999999999em;vertical-align:-0.19444em;"></span><span class="mord mathnormal" style="margin-right:0.05764em;">E</span><span class="mord mathnormal">s</span><span class="mord mathnormal">p</span><span class="mord mathnormal">a</span><span class="mord mathnormal">ço</span><span class="mord">⠀</span><span class="mord mathnormal" style="margin-right:0.03588em;">g</span><span class="mord mathnormal">a</span><span class="mord mathnormal">s</span><span class="mord mathnormal">t</span><span class="mord mathnormal">o</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">:</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.02778em;">O</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mclose">)</span></span></span></span></span></div></figure><p id="17aa9848-0144-4a9e-89d5-6b1a5616df2f" class="">
</p><p id="6042d4b6-b495-41bf-9f9e-d98817fd48be" class="">Código:<div class="indented"><pre id="eb48d3dd-8f7d-458f-a884-7cde6ffd5833" class="code"><code>def intersec(vetor_a, vetor_b):
  if vetor_a == [] or vetor_b == []:
    return []
  elif len(vetor_a)  &gt; len(vetor_b):
    maior, menor = vetor_a, vetor_b
  else:
    maior, menor = vetor_b, vetor_a
  
  vetor_c = []
  for i in menor:
    for j in maior:
      if i == j:
        vetor_c.append(i)

  return vetor_c

a = [5,7,1,2,9,10]
b = [10,6,7,23,1,2]

print(intersec(a,b), end=&#x27;\n\n&#x27;)</code></pre></div></p></div></p></div></p><p id="88383e94-1e98-47f6-8d85-fddc7436e709" class="">
</p><p id="dc40a2de-8f53-48f7-9443-150089aeb479" class="">7<strong>° Dada uma expressão contendo parênteses, literais e operadores aritméticos, elabore um algoritmo para determinar se a expressão está com os parênteses balanceados, ou seja, se para cada parêntese aberto há um parêntese fechando e se os pares de parênteses estão adequadamente aninhados. Você pode supor que a expressão será fornecida como uma string e que a reposta de seu algoritmo será um booleano, onde True significa que a expressão é correta e False, incorreta.</strong></p><pre id="f0e4abef-767b-45f4-889d-e6867f5f0087" class="code"><code>Ex: ((a + b) + (c * d)) é uma expressão correta 
 (( a + b) + 1 é uma expressão incorreta 
 ) (a + b)) + (c * d) é uma expressão incorreta</code></pre><p id="42f468ed-3dd1-41e0-9cc7-1dc7c6c15c1e" class=""><div class="indented"><p id="08910d25-ca1e-4569-91d9-255a162faaf1" class="">Ideia para solução:<div class="indented"><p id="5203cd92-7d72-45bd-9165-8a61c4f0ed7b" class="">Nessa questão, vamos limpar a entrada deixando apenas uma “String” contendo os Parênteses a serem analisados. Assim, passaremos essa nova “String” para um laço de repetição que irá executar até existir “()” na mesma. Iremos substituir os parenteses encontrados por “String” vazia. Por fim, basta comparar se no resultado sobrou algum parentese. Caso sim, então a expressão não está correta.</p></div></p><p id="1f2d178c-a3f8-4077-9453-c6a73399e945" class="">
</p><p id="cacb964c-483c-43a4-8cd4-57b06b87588b" class="">Pseudocódigo:<div class="indented"><pre id="da821e20-06eb-4d3a-b9c7-64625c665eb9" class="code"><code>algoritmo exp_correta(exp): Boleano
{-
	Entrada: String contendo a expressão a ser analisada
	Saída: Boleano True se a expressão for válida, caso não seja válida então retorna Boleano False.
-}
	início
	  parenteses := []
	  total := 0
	  Para c em exp, faça
	    Se c = &quot;(&quot; || c = &quot;)&quot;, então
	      parenteses.append(c)
	  
	  parenteses = &#x27;&#x27;.join(parenteses)
	  Enquanto houver &quot;()&quot; em parenteses, faça  
	    parenteses := parenteses.replace(&#x27;()&#x27;, &#x27;&#x27;) 
	  
	  Se parenteses = &#x27;&#x27;, então
	    retorne True
	  Senão
	    retorne False
	fim</code></pre></div></p><p id="bb149798-94b1-4dbd-9193-e76df7b29a5b" class="">
</p><p id="3ad30a2a-d9d4-485e-b0fd-b55db044c260" class="">Análise de Complexidade:</p><figure id="9f9752c7-03b6-4597-b28c-16e3c4314f63" class="equation"><style>@import url('https://cdnjs.cloudflare.com/ajax/libs/KaTeX/0.13.2/katex.min.css')</style><div class="equation-container"><span class="katex-display"><span class="katex"><span class="katex-mathml"><math xmlns="http://www.w3.org/1998/Math/MathML" display="block"><semantics><mrow><mo stretchy="false">(</mo><mstyle scriptlevel="0" displaystyle="false"><msubsup><mo>∑</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><mi mathvariant="normal">.</mi><mn>5</mn><mo stretchy="false">)</mo><mo>+</mo><mi>n</mi><mo>+</mo><mo stretchy="false">(</mo><mstyle scriptlevel="0" displaystyle="false"><msubsup><mo>∑</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><mstyle scriptlevel="0" displaystyle="false"><msubsup><mo>∑</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><mo stretchy="false">)</mo><mstyle scriptlevel="0" displaystyle="false"><msubsup><mo>∑</mo><mrow><mi>i</mi><mo>=</mo><mn>1</mn></mrow><mi>n</mi></msubsup><mo>=</mo><mn>6</mn><mi>n</mi><mo>+</mo><mi>n</mi><mtext>³</mtext><mo>+</mo><mn>2</mn><mi>n</mi><mtext>²</mtext><mo>+</mo><mn>6</mn><mi>n</mi><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><mi>C</mi><mi>o</mi><mi>m</mi><mi>p</mi><mi>l</mi><mi>e</mi><mi>x</mi><mi>i</mi><mi>d</mi><mi>a</mi><mi>d</mi><mi>e</mi><mo>:</mo><mi>O</mi><mo stretchy="false">(</mo><mi>n</mi><mtext>³</mtext><mo>+</mo><mi>n</mi><mtext>²</mtext><mo stretchy="false">)</mo><mspace linebreak="newline"></mspace><mtext>⠀</mtext><mspace linebreak="newline"></mspace><mi>E</mi><mi>s</mi><mi>p</mi><mi>a</mi><mi>ç</mi><mi>o</mi><mtext>⠀</mtext><mi>g</mi><mi>a</mi><mi>s</mi><mi>t</mi><mi>o</mi><mo>:</mo><mi>O</mi><mo stretchy="false">(</mo><mn>2</mn><mi>n</mi><mo stretchy="false">)</mo></mstyle></mstyle></mstyle></mstyle></mrow><annotation encoding="application/x-tex">(\textstyle\sum_{i=1}^n . 5) + n + (\textstyle\sum_{i=1}^n  \textstyle\sum_{i=1}^n) \textstyle\sum_{i=1}^n = 6n + n³ + 2n² + 6n
\\
⠀
\\
Complexidade: O(n³ + n²)

\\
⠀
\\
Espaço⠀gasto: O(2n)</annotation></semantics></math></span><span class="katex-html" aria-hidden="true"><span class="base"><span class="strut" style="height:1.104002em;vertical-align:-0.29971000000000003em;"></span><span class="mopen">(</span><span class="mop"><span class="mop op-symbol small-op" style="position:relative;top:-0.0000050000000000050004em;">∑</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.804292em;"><span style="top:-2.40029em;margin-left:0em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight">i</span><span class="mrel mtight">=</span><span class="mord mtight">1</span></span></span></span><span style="top:-3.2029em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight">n</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.29971000000000003em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.16666666666666666em;"></span><span class="mord">.5</span><span class="mclose">)</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1.104002em;vertical-align:-0.29971000000000003em;"></span><span class="mopen">(</span><span class="mop"><span class="mop op-symbol small-op" style="position:relative;top:-0.0000050000000000050004em;">∑</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.804292em;"><span style="top:-2.40029em;margin-left:0em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight">i</span><span class="mrel mtight">=</span><span class="mord mtight">1</span></span></span></span><span style="top:-3.2029em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight">n</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.29971000000000003em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.16666666666666666em;"></span><span class="mop"><span class="mop op-symbol small-op" style="position:relative;top:-0.0000050000000000050004em;">∑</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.804292em;"><span style="top:-2.40029em;margin-left:0em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight">i</span><span class="mrel mtight">=</span><span class="mord mtight">1</span></span></span></span><span style="top:-3.2029em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight">n</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.29971000000000003em;"><span></span></span></span></span></span></span><span class="mclose">)</span><span class="mspace" style="margin-right:0.16666666666666666em;"></span><span class="mop"><span class="mop op-symbol small-op" style="position:relative;top:-0.0000050000000000050004em;">∑</span><span class="msupsub"><span class="vlist-t vlist-t2"><span class="vlist-r"><span class="vlist" style="height:0.804292em;"><span style="top:-2.40029em;margin-left:0em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mtight"><span class="mord mathnormal mtight">i</span><span class="mrel mtight">=</span><span class="mord mtight">1</span></span></span></span><span style="top:-3.2029em;margin-right:0.05em;"><span class="pstrut" style="height:2.7em;"></span><span class="sizing reset-size6 size3 mtight"><span class="mord mathnormal mtight">n</span></span></span></span><span class="vlist-s">​</span></span><span class="vlist-r"><span class="vlist" style="height:0.29971000000000003em;"><span></span></span></span></span></span></span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">=</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">6</span><span class="mord mathnormal">n</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.66666em;vertical-align:-0.08333em;"></span><span class="mord mathnormal">n</span><span class="mord">³</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.72777em;vertical-align:-0.08333em;"></span><span class="mord">2</span><span class="mord mathnormal">n</span><span class="mord">²</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:0.64444em;vertical-align:0em;"></span><span class="mord">6</span><span class="mord mathnormal">n</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.8888799999999999em;vertical-align:-0.19444em;"></span><span class="mord mathnormal" style="margin-right:0.07153em;">C</span><span class="mord mathnormal">o</span><span class="mord mathnormal">m</span><span class="mord mathnormal" style="margin-right:0.01968em;">pl</span><span class="mord mathnormal">e</span><span class="mord mathnormal">x</span><span class="mord mathnormal">i</span><span class="mord mathnormal">d</span><span class="mord mathnormal">a</span><span class="mord mathnormal">d</span><span class="mord mathnormal">e</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">:</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.02778em;">O</span><span class="mopen">(</span><span class="mord mathnormal">n</span><span class="mord">³</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span><span class="mbin">+</span><span class="mspace" style="margin-right:0.2222222222222222em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal">n</span><span class="mord">²</span><span class="mclose">)</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0em;vertical-align:0em;"></span><span class="mord">⠀</span></span><span class="mspace newline"></span><span class="base"><span class="strut" style="height:0.8777699999999999em;vertical-align:-0.19444em;"></span><span class="mord mathnormal" style="margin-right:0.05764em;">E</span><span class="mord mathnormal">s</span><span class="mord mathnormal">p</span><span class="mord mathnormal">a</span><span class="mord mathnormal">ço</span><span class="mord">⠀</span><span class="mord mathnormal" style="margin-right:0.03588em;">g</span><span class="mord mathnormal">a</span><span class="mord mathnormal">s</span><span class="mord mathnormal">t</span><span class="mord mathnormal">o</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span><span class="mrel">:</span><span class="mspace" style="margin-right:0.2777777777777778em;"></span></span><span class="base"><span class="strut" style="height:1em;vertical-align:-0.25em;"></span><span class="mord mathnormal" style="margin-right:0.02778em;">O</span><span class="mopen">(</span><span class="mord">2</span><span class="mord mathnormal">n</span><span class="mclose">)</span></span></span></span></span></div></figure><p id="fa5e8058-47b6-4b2a-810d-154019c933dc" class="">
</p><p id="3d0b4397-fc7b-4dbe-8a2e-cb5a9b69824f" class="">Código:<div class="indented"><pre id="41a29659-482e-4be3-9ce8-dc59606f413e" class="code"><code>def exp_correta(exp):
  parenteses = []
  for c in exp:
    if c == &quot;(&quot; or c == &quot;)&quot;:
      parenteses.append(c)
  
  parenteses = &#x27;&#x27;.join(parenteses)
  while (&quot;()&quot; in parenteses):  
    parenteses = parenteses.replace(&#x27;()&#x27;, &#x27;&#x27;) 
  
  if parenteses == &#x27;&#x27;:
    return True
  else:
    return False
    
exp = &quot;((a - c) + (b * d))&quot;
print(exp_correta(exp))</code></pre></div></p><p id="5531eef6-f17f-473d-ae2f-92c4869d637e" class="">
</p></div></p></div></article></body></html>