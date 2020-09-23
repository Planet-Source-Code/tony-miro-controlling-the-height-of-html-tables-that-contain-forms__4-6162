<div align="center">

## Controlling the Height of HTML Tables that Contain Forms


</div>

### Description

When working with HTML forms and ASP the order of the tags CAN and WILL make a difference! This article details some traps that HTML newbies can run into when designing ASP pages.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Tony Miro](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/tony-miro.md)
**Level**          |Beginner
**User Rating**    |4.2 (21 globes from 5 users)
**Compatibility**  |ASP \(Active Server Pages\), VbScript \(browser/client side\)

**Category**       |[Internet/ Browsers/ HTML](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/internet-browsers-html__4-9.md)
**World**          |[ASP / VbScript](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/asp-vbscript.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/tony-miro-controlling-the-height-of-html-tables-that-contain-forms__4-6162/archive/master.zip)





### Source Code

<p><font face="Verdana">While trying to create a toolbar using HTML forms in an
ASP page, I created the HTML form within a table using the following code:<br>
<br>
</font></p>
<table border="0" cellPadding="0" cellSpacing="0" width="100%">
 <tbody>
  <tr>
   <td bgColor="#d0d5df" width="100%"><font face="Verdana"><font size="2">&lt;Table
    border=&quot;0&quot; cellspacing=&quot;0&quot; cellpadding=&quot;0&quot;
    style=&quot;HEIGHT: 30px; WIDTH: 100%&quot;&gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp; &lt;tr &gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &lt;td bgcolor=&quot;navy&quot;
    width=&quot;1%&quot;&gt;<br>
    &nbsp;&nbsp; </font>&nbsp;&nbsp;&nbsp; <font size="2">&lt;/td&gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &lt;td bgcolor=&quot;navy&quot;
    width=&quot;99%&quot; align=&quot;left&quot; valign=&quot;center&quot;&gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    &lt;form method=&quot;POST&quot; action=&quot;&lt;%= strURL%&gt;&quot;
    id=form1 name=form1&gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    &lt;input type=&quot;submit&quot; value=&quot;&lt;%= strEditBtnCaption
    %&gt;&quot; name=&quot;cmdEdit&quot;&gt;<br>
    </font>&nbsp;&nbsp;&nbsp; <font size="2">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    &lt;/form&gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &lt;/td&gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp; &lt;/tr&gt;<br>
    &lt;/Table&gt;</font></font></td>
  </tr>
 </tbody>
</table>
<p>&nbsp;</p>
<p><font face="Verdana">&nbsp;&nbsp;&nbsp; The code worked but I ended up with a
blue background that was &quot;taller&quot; than I wanted it to be, as shown in
the screen print below.</font></p>
<p align="center"><font face="Verdana"><img border="0" src="http://www.planet-source-code.com/vb/tutorial/asp/images/FormInsideTable.jpg" width="419" height="307"></font></p>
<p><font face="Verdana">&nbsp;&nbsp;&nbsp; I tried changing the &lt;TABLE&gt;,
&lt;TR&gt;, and &lt;TD&gt; heights but nothing worked!!!</font></p>
<p><font face="Verdana">&nbsp;&nbsp;&nbsp; Finally, I decided to move the
&lt;FORM&gt; tags outside of the &lt;TABLE&gt; tags and this is what happened:</font></p>
<table border="0" cellPadding="0" cellSpacing="0" width="100%">
 <tbody>
  <tr>
   <td bgColor="#d0d5df" width="100%"><font face="Verdana"><font size="2"><br>
    &nbsp;&nbsp;&nbsp; &lt;form method=&quot;POST&quot; action=&quot;&lt;%=
    strURL%&gt;&quot; id=form1 name=form1&gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &lt;Table
    border=&quot;0&quot; cellspacing=&quot;0&quot; cellpadding=&quot;0&quot;
    style=&quot;HEIGHT: 30px; WIDTH: 100%&quot;&gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &lt;tr
    &gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    &lt;td bgcolor=&quot;navy&quot; width=&quot;1%&quot;&gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    &lt;/td&gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    &lt;td bgcolor=&quot;navy&quot; width=&quot;99%&quot;
    align=&quot;left&quot; valign=&quot;center&quot;&gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
    &lt;input type=&quot;submit&quot; value=&quot;&lt;%= strEditBtnCaption
    %&gt;&quot; name=&quot;cmdEdit&quot;&gt;<br>
    &nbsp;&nbsp; </font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font size="2">&lt;/td&gt;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &lt;/tr&gt;<br>
    </font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <font size="2">&lt;/Table&gt;<br>
    </font>&nbsp;&nbsp; <font size="2">&lt;/form&gt;</font></font></td>
  </tr>
 </tbody>
</table>
<p align="center"><font face="Verdana">&nbsp;&nbsp;&nbsp;&nbsp; It produced
different/better results!!! Now I can control the height of&nbsp; the blue
background to look the way I want it to look!!!<br>
<br>
<br>
<img border="0" src="http://www.planet-source-code.com/vb/tutorial/asp/images/tableInsideForm.jpg" width="419" height="307"></font></p>

