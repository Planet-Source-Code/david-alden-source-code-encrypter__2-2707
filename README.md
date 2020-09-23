<div align="center">

## Source code encrypter


</div>

### Description

Scramble the source of any chunk of code, or the entire webpage, using this creative script. The encrypted code will still be interpreted properly by the browser, just difficult for us humans to read. It is recommended that you use this script to encrypt only the part(s) of your webpage that require encryption (ie: a script), rather than the entire page. This helps minimize the chance of any problems.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[David Alden](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/david-alden.md)
**Level**          |Advanced
**User Rating**    |4.1 (82 globes from 20 users)
**Compatibility**  |
**Category**       |[Security](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/security__2-74.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/david-alden-source-code-encrypter__2-2707/archive/master.zip)





### Source Code

```
<html>
<head>
<title>Source code encrypter</title>
<style type="text/css">
	A.darklink:link	{ text-decoration: none;color: white;};
	A.darklink:visited	{ text-decoration: none;color: white;};
	A.darklink:hover	{ text-decoration: none;color: aqua;};
	A.menulink:link	{ text-decoration: none;color: white;};
	A.menulink:visited	{ text-decoration: none;color: white;};
	A.menulink:hover	{ text-decoration: none;color: white;};
	A:link { text-decoration: underline;color: black;};
	A:visited { text-decoration: underline;color: red;};
	A:hover { text-decoration: none;color: black;};
   BODY {
     font-size: 10pt;
     font-family: arial;
     }
   P {
     font-size: 10pt;
     font-family: arial;
     }
   TD {
     font-size: 10pt;
     font-family: arial;
     }
   TD.header {
     font-size: 16pt;
     font-family: arial;
     color: ffc000;
     }
   H1 {
     font-size: 16pt;
     font-family: arial;
     }
   H3 {
     font-family: arial;
     }
 	</style>
</head>
<body bgcolor="#FFFFFF" leftmargin="0" topmargin="0" marginwidth="0" marginheight="0" link="#000000" vlink="#FF0000" "#000000">
   <table width="100%" border="0" align="center">
    <tr valign="top">
     <td height="103">
      <div align="center">
        <p><font face="Arial, Helvetica, sans-serif" size=2>
      <font face=Verdana><font size="2" face="Arial, Helvetica, sans-serif" color="#3399FF"><b><br>
      Source code encrypter:</b></font><font size="2" face="Arial, Helvetica, sans-serif"><br>
      <b><br>
      <font color="#333333">Script works with Netscape 4+ AND Internet Explorer
      4+ </font></b></font></font>
      <p align=left><font size="2" face="Arial, Helvetica, sans-serif" color="#666666"><b><font color="#333333">Description:</font></b><font color="#333333">
       Scramble the source of any chunk of code, or the entire webpage,
       using this creative script. The encrypted code will still be interpreted
       properly by the browser, just difficult for us humans to read. It
       is recommended that you use this script to encrypt only the part(s)
       of your webpage that require encryption (ie: a script), rather than
       the entire page. This helps minimize the chance of any problems.
       </font><br>
       <font color="#333333"><br>
       <b>Demo:</b> Enter a chunk of HTML code below, and press the Encrypt
       button to scramble it:</font><br>
       </font>
       <script language=JavaScript>
<!--
var i=0;
var ie=(document.all)?1:0;
var ns=(document.layers)?1:0;
function initStyleElements() /* Styles for Buttons Init */
{
var c = document.pad;
if (ie)
{
//c.text.style.backgroundColor="#DDDDDD";
c.compileIt.style.backgroundColor="#C0C0A8";
c.compileIt.style.cursor="hand";
c.select.style.backgroundColor="#C0C0A8";
c.select.style.cursor="hand";
c.view.style.backgroundColor="#C0C0A8";
c.view.style.cursor="hand";
c.retur.style.backgroundColor="#C0C0A8";
c.retur.style.cursor="hand";
c.clear.style.backgroundColor="#C0C0A8";
c.clear.style.cursor="hand";
}
else return;
}
/* Buttons Enlightment of "Compilation" panel */
function LightOn(what)
{
if (ie) what.style.backgroundColor = '#E0E0D0';
else return;
}
function FocusOn(what)
{
if (ie) what.style.backgroundColor = '#EBEBEB';
else return;
}
function LightOut(what)
{
if (ie) what.style.backgroundColor = '#C0C0A8';
else return;
}
function FocusOff(what)
{
if (ie) what.style.backgroundColor = '#DDDDDD';
else return;
}
/* Buttons Enlightment of "Compilation" panel */
function generate() /* Generation of "Compilation" */
{
code = document.pad.text.value;
if (code)
{
document.pad.text.value='Compiling...Please wait!';
setTimeout("compile()",1000);
}
else alert('First enter something to compile and then press CompileIt')
}
function compile() /* The "Compilation" */
{
document.pad.text.value='';
compilation=escape(code);
document.pad.text.value="<script>\n<!--\ndocument.write(unescape(\""+compilation+"\"));\n//-->\n<\/script>";
i++;
if (i=1) alert("Page compiled 1 time!");
else alert("Page compiled "+i+" times!");
}
function selectCode() /* Selecting "Compilation" for Copying */
{
if(document.pad.text.value.length>0)
{
document.pad.text.focus();
document.pad.text.select();
}
else alert('Nothing for be selected!')
}
function preview() /* Preview for the "Compilation" */
{
if(document.pad.text.value.length>0)
{
pr=window.open("","Preview","scrollbars=1,menubar=1,status=1,width=700,height=320,left=50,top=110");
pr.document.write(document.pad.text.value);
}
else alert('Nothing for be previewed!')
}
function uncompile() /* Decompiling a "Compilation" */
{
if (document.pad.text.value.length>0)
{
source=unescape(document.pad.text.value);
document.pad.text.value=""+source+"";
}
else alert('You need compiled code to uncompile it!')
}
// -->
</script>
         <!-- Compilation Panel -->
         <form method=post name=pad align=center>
          <textarea rows=11 name=text cols=58 style="background-color:#EBEBEB;width:95%"></textarea>
          <br>
          <br>
          <input type=button value=Encrypt name=compileIt onClick=generate() onMouseOver=LightOn(this) onMouseOut=LightOut(this)>
          <input type=button value=Select name=select onClick=selectCode() onMouseOver=LightOn(this) onMouseOut=LightOut(this)>
          <input type=button value=Preview name=view onClick=preview() onMouseOver=LightOn(this) onMouseOut=LightOut(this)>
          <input type=button value=Source name=retur onClick=uncompile() onMouseOver=LightOn(this) onMouseOut=LightOut(this)>
          <input type=reset value=Clear name=clear onMouseOver=LightOn(this) onMouseOut=LightOut(this)>
         </form>
         <!-- Compilation Panel -->
  		</td>
 	   </tr>
	  </table>
</body>
</html>
```

