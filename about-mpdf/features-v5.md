---
layout: page
title: Features v5
parent_title: About mPDF
permalink: /about-mpdf/features-v5.html
---

<div id="bpmbook" class="bpmbook" style="direction:ltr;">
<div class="topic_user_field">
<div id="U0">
<h2>Main features</h2>
<ul>
<li>Accepts UTF-8 encoded HTML</li>
<li>Supports almost all languages including <acronym title="Right-to-Left document, used for Hebrew and Arabic languages">RTL</acronym> (arabic and hebrew), and <acronym title="Chinese-Japanese-Korean languages">CJK</acronym> - (chinese-japanese-korean)</li>
<li>Bookmarks</li>
<li>CSS stylesheets</li>
<li>Word spacing and character spacing for justification</li>
<li>Nested block-level elements (e.g. P, DIV) including margins, borders, padding, line-height, background colours etc.</li>
<li>Support (partial)&nbsp;for floating and fixed-position block-elements</li>
<li>Page layout and orientation</li>
<li>Text-justification and hyphenation</li>
<li>Page numbering</li>
<li>Odd and even paging with mirrored margins</li>
<li>Page headers &amp; footers</li>
<li>Columns</li>
<li>Tables - nested tables, rotated, or autosized to fit on a page</li>
<li>Table of contents</li>
<li>Index</li>
<li>Watermarks</li>
<li>Images in JPG, GIF, PNG, SVG, BMP or WMF format</li>
<li>Password protection</li>
<li>Annotations</li>
<li>Barcodes (EAN13, UPC-A/E, Code 11, 39, 93, 128, Codabar, MSI, IMB, Planet, Postnet, RM4SCC etc.)</li>
<li>Import another PDF file and use as a template</li>
<li>Embedded font subsets</li>
<li>PDF/A-1b support (ISO 19005-1:2005)</li>
<li>PDF/X-1a support</li>
</ul>
<p>&nbsp;</p>
<h2>More Information</h2>
<p>mPDF has a number of enhancements over the original FPDF, HTML2FPDF and UPDF scripts:</p>
<p><b>UTF-8 encoded</b> HTML is accepted as the standard input.</p>
<p><a href="/fonts-languages/arabic-rtl-text-v5-x.html">Right-to-left languages</a> are supported, with automatic detection of RTL characters within a document. Transposes: tables, lists, text justification and table cell alignment, as well as full text reversal for RTL characters. Automatically detects non-RTL characters and displays these in original order.</p>
<p><a href="/what-else-can-i-do/bookmarks.html">Bookmarks</a> and <a href="/setting-pdf-file-properties/document-metadata.html">Meta tag information</a> are supported in all character sets.</p>
<p>A single CSS stylesheet can be used for all pages, with <a href="/fonts-languages/font-substitution-5-x.html">font substitution</a> automatically for CJK characters.</p>
<p><a href="/fonts-languages/character-substitution.html">Character substitution</a> can optionally be used to automatically replace any characters that do not exist in the current font.</p>
<p><a href="/what-else-can-i-do/text-justification.html">Word spacing and character spacing</a> are both used to justify text; works in unicode mode&nbsp;and CJK&nbsp;characters&nbsp;as well.</p>
<p><b>Nested block-level elements</b> (e.g. P, DIV) are supported, with comprehensive CSS&nbsp;support e.g.&nbsp;margins, borders, padding, line-height, background colours etc.</p>
<p><a href="/css-stylesheets/introduction.html">CSS style attributes</a> now fully support font, font-size, color, and background color (for highlighting) plus many more.</p>
<p><a href="/tables/tables.html">Table</a> cell padding and borders are supported.</p>
<p><b>Text-indent for 1st line of paragraph</b>, and hanging indents are supported.</p>
<p><b>List indenting</b> can be defined.</p>
<p><a href="/html-support/custom-html-tags.html">Custom tags</a> added&nbsp;- PAGEBREAK, COLUMNBREAK, INDEXENTRY</p>
<p><a href="/what-else-can-i-do/columns.html">Multiple columns</a> can be started and stopped anywhere on the page with column height adjusted (and optionally aligned to justify).</p>
<p><a href="/tables/tables.html">Tables</a> can be <b>rotated</b>,&nbsp;or <b>autosized</b> -&nbsp;font-size is reduced if required to fit the page. Background colour for TR rows is supported.</p>
<p><a href="/paging/double-sided-documents.html">Odd and even paging</a> can be used with inner and outer margins alternated.</p>
<p>A more complex definition of <a href="/headers-footers/headers-footers.html">headers and footers</a> allows left/center/right parts to be defined, each with their own font-styles, and including code to allow the date/time to be inserted as well as page numbers.</p>
<p>A <a href="/what-else-can-i-do/table-of-contents.html">table of contents</a> can be generated automatically, which can be inserted at the front of the document, based on custom tags used throughout the HTML code. (Based on Richard Bondi's extension to FPDF.)</p>
<p>An <a href="/what-else-can-i-do/index.html">Index</a> can be generated at the end of the document based on custom tags used throughout the HTML code.</p>
<p><b>Non-breaking space</b> &nbsp; is supported&nbsp;when using fonts that have a character representing chr(160) (not all of them).&nbsp;</p>
<p><a href="/what-else-can-i-do/watermarks.html">Watermarks</a> as text or images can be used e.g. for 'DRAFT', and will appear as a transparency over other elements.</p>
<p>Intelligent <a href="/what-else-can-i-do/text-justification.html">word-wrapping</a> will avoid 'orphan' punctuation or superscript moving to the next line.</p>
<p>Automatic hyphenation is optional.</p>
<p>All <b>HTML entities</b> are supported, as well as decimal and hex e.g. &amp;apos;&nbsp;&amp;#8812; or &amp;#x21a4;</p>
<p><a href="/setting-pdf-file-properties/password-protection.html">Password protection</a> can be set for the PDF file.</p>
<p>NB The original commands from FPDF can be used e.g. Write(), but some are altered to allow UTF-8 encoding and RTL text to be processed e.g. use WriteCell() and WriteMultiCell() instead of Cell() and MultiCell().</p>
</div>
</div>
