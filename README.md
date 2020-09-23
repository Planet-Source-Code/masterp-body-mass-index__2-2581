<div align="center">

## Body Mass Index


</div>

### Description

This little script calculates your body mass index and gives a comment on your rating. Just input your weight in pounds and your height in inches and press calculate.
 
### More Info
 
Weight in pounds <br>

Height in inches


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[masterp](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/masterp.md)
**Level**          |Intermediate
**User Rating**    |4.6 (23 globes from 5 users)
**Compatibility**  |
**Category**       |[Calculators & Science](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/calculators-science__2-71.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/masterp-body-mass-index__2-2581/archive/master.zip)





### Source Code

```
<html>
<HEAD>
<TITLE>Body Mass Index</TITLE>
<style>
.input{ font-family: MS sans serif;font-size: 15px; border: 1px inset black}
.button{ font-family: MS sans serif;font-size: 15px; border: 1px inset black; background: #000099; color: #FFFFFF; font-weight: bold}
</style>
</HEAD>
</HEAD>
<BODY BGCOLOR="#FFFFFF" text="000000">
COMMENTS:
Enter your weight in pounds and your height in inches<BR>
in the form below and press the "Calculate" button<BR>
<BR>
<FORM NAME="BMI" method=POST>
<table border=1 cellspacing=0 cellpadding=2 bordercolorlight=000000 bordercolordark=ffffff bgColor=#ffffff width=80%>
<tr bgColor=#cccccc>
  <td>
  <TABLE border=0 cellspacing=2 cellpadding=2 width=100%>
  <TR>
    <TD><DIV ALIGN=CENTER>Your Weight (lbs)</DIV></TD>
    <TD><DIV ALIGN=CENTER>Your Height (in)</DIV></TD>
    <TD><DIV ALIGN=CENTER>Your BMI</DIV></TD>
    <TD><DIV ALIGN=CENTER>My Comment</DIV></TD>
  </TR>
  <TR>
    <TD><INPUT TYPE=TEXT class=input NAME=weight SIZE=10 onFocus="this.form.weight.value=''"></TD>
    <TD><INPUT TYPE=TEXT class=input NAME=height SIZE=10 onFocus="this.form.height.value=''"></TD>
    <TD><INPUT TYPE=TEXT class=input NAME=bmi SIZE=8 ></TD>
    <TD><INPUT TYPE=TEXT class=input NAME=my_comment size=40></TD>
  </TR>
  <TR>
    <TD colspan=4 align=center><INPUT class=button TYPE="button" VALUE="Calculate" onClick="computeform(this.form)">
                 <INPUT class=button TYPE="reset" VALUE="Reset" onClick="ClearForm(this.form)">
    </TD>
  </TR>
  </TABLE>
  </td>
</tr>
</table>
</FORM>
<SCRIPT LANGUAGE="JAVASCRIPT">
<!-- hide this script tag's contents from old browsers
function ClearForm(form)
{
  form.weight.value = "";
  form.height.value = "";
  form.bmi.value = "";
  form.my_comment.value = "";
}
function bmi(weight, height)
 {
     bmindx=weight/eval(height*height);
     return bmindx;
}
function checkform(form)
 {
    if (form.weight.value==null||form.weight.value.length==0 || form.height.value==null||form.height.value.length==0)
    {
      alert("\nPlease complete the form first");
      return false;
    }
    else if (parseFloat(form.height.value) <= 0||
        parseFloat(form.height.value) >=500||
        parseFloat(form.weight.value) <= 0||
        parseFloat(form.weight.value) >=500)
   {
        alert("\nReally know what you're doing? \nPlease enter values again. \nWeight in kilos and \nheight in cm");
        ClearForm(form);
        return false;
    }
    return true;
}
function computeform(form)
 {
    if (checkform(form))
    {
      //Convert weight from lbs to kg
      var weight = form.weight.value*.4536;
      //Convert height from cm to meters
      var height = form.height.value*.025400;
      //compute bmi
      yourbmi=Math.round(bmi(weight, height));
      form.bmi.value=yourbmi;
      if (yourbmi >40)
     {
       form.my_comment.value="You are grossly obese, consult your physician!";
     }
     else if (yourbmi >30 && yourbmi <=40)
     {
       form.my_comment.value="Umm... You are obese, want some liposuction?";
     }
     else if (yourbmi >27 && yourbmi <=30)
     {
       form.my_comment.value="You are very fat, do something before it's too late";
     }
     else if (yourbmi >22 && yourbmi <=27)
     {
       form.my_comment.value="You are fat, need dieting and exercise";
     }
     else if (yourbmi >=21 && yourbmi <=22)
     {
       form.my_comment.value="I envy you. Keep it up!!";
     }
     else if (yourbmi >=18 && yourbmi <21)
     {
       form.my_comment.value="You are thin, eat more.";
     }
     else if (yourbmi >=16 && yourbmi <18)
     {
       form.my_comment.value="You are starving. Go Find some food!";
     }
     else if (yourbmi <16)
     {
       form.my_comment.value="You're grossly undernourished, need hospitalization ";
     }
    }
    return;
}
 // -- done hiding from old browsers -->
</SCRIPT>
</HEAD>
</body>
</HTML>
```

