---
layout: page
title: autoFontGroupSize
parent_title: mPDF Variables
permalink: /reference/mpdf-variables/autofontgroupsize.html
---

<div id="bpmbook" class="bpmbook" style="direction:ltr;">
<div class="topic_user_field">
<div id="U0">
<p>(mPDF &gt;= 2.3&nbsp; &lt;6.0)</p>
<p>autoFontGroupSize – Specify the chunk size of text to group when auto-detecting languages using SetAutoFont</p>
<h2>Value</h2>

<div class="alert alert-info" role="alert">void <b>autoFontGroupSize</b></div>
<p>Specify the chunk size of text to group when auto-detecting languages using <a href="/reference/mpdf-functions/setautofont.html">SetAutoFont()</a>.</p>

<div class="alert alert-info" role="alert"><b>Note:</b> This variable is removed from mPDF v 6.0</div>
<p>Bigger chunks (3) allows reversal of whole sentences of RTL text, not just letters in individual words; the disadvantage is that it may include bits of other languages either side, forcing them in the font used for the "foreign" language.

Smaller chunks (1) - analysing word by word - takes more processing time, and cannot reverse RTL sentences. In text with CJK language, it makes it harder for mPDF to correctly identify between e.g. Korean and Chinese which share some characters. Thus words may be identified alternately as Korean or Chinese.</p>
<h2>Values</h2>
<p class="manual_param_dt"><span class="parameter">autoFontGroupSize</span></p>
<p class="manual_param_dd"><b>Values</b>

1: individual words are analysed

2: words are analysed to see if they are distinctive of a particular language, and then surrounding text that is compatible is grouped together with these words

3: as big chunks as possible are grouped, including ASCII characters and punctuation

<span class="smallblock">DEFAULT</span>: 2</p>
<h2>Changelog</h2>
<table class="bpmTopic"> <thead>
<tr> <th>Version</th><th>Description</th> </tr>
</thead> <tbody>
<tr>
<td>2.3</td>
<td>Variable was added.</td>
</tr>
</tbody> </table>
<h2>Examples</h2>

{% highlight php %}
Example #1

{% endhighlight %}

{% highlight php %}
<?php

<?php

include("../mpdf.php");

$mpdf=new mPDF('utf-8'); 

$html = "

<style>

p { font-family: FreeSerif; }

</style>

<p>Most of this text is in English, but has occasional words in Chinese:来自商务 or Vietnamese: Một khảo sát mới cho biết, or maybe even Arabic: الابيض</p>

<p>الابيض "بشدة" تفجير</p>

<p>其截至 WHO 年底 2005 笔</p>

";

$mpdf->SetAutoFont();

$mpdf->autoFontGroupSize = 1;

$mpdf->WriteHTML($html);

$mpdf->autoFontGroupSize = 2;

$mpdf->WriteHTML($html);

$mpdf->autoFontGroupSize = 3;

$mpdf->WriteHTML($html);

$html2 = "<p>In this example, the word boundaries from different languages are already defined by marking with &amp;lt;span&amp;gt; tags</p>

<p>Most of this text is in English, but has occasional words in Chinese:<span>来自商务</span> or Vietnamese: <span>Một khảo sát mới cho biết</span>, or maybe even Arabic: <span>الابيض</span></p>

";

$mpdf->WriteHTML($html2);

$mpdf->Output();

?>

See the result of this as a PDF file
{% endhighlight %}

<h2>See Also</h2>
<ul>
<li class="manual_boxlist"><a href="/reference/mpdf-variables/uselang.html">useLang</a> - Specify whether to recognise and support the HTML attribute lang</li>
<li class="manual_boxlist"><a href="/reference/mpdf-variables/autofontgroupsize.html">SetAutoFont()</a> - Use AutoFont to auto-detect text language in HTML input</li>
<li class="manual_boxlist"><a href="index0c23.html?tid=346">disableMultilingualJustify</a> - Specify whether to disable text justification in multilingual documents</li>
<li class="manual_boxlist"><a href="/fonts-languages/lang-v5-x.html">lang</a> - Information on mPDF support for the HTML attribute lang</li>
</ul>
</div>
</div>
