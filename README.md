<div align="center">

## Character and Strings


</div>

### Description

This is in continuation of tutorials I am writing

about C. Todays topic is Character and Strings.

Experts please skip this tutorials.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Indee](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/indee.md)
**Level**          |Beginner
**User Rating**    |3.0 (15 globes from 5 users)
**Compatibility**  |C
**Category**       |[Documents](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/documents__3-27.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/indee-character-and-strings__3-1025/archive/master.zip)





### Source Code

<html><head><title>Tutorial-Characters and Strings</title><meta content="text/html; charset=windows-1252" http-equiv="Content-" type="type" /><meta content="Inder Mohan Singh" name="Author" /><meta http-equiv="Keywords" content="C Tutorials characters strings " /><meta http-equiv="Description" content="Tutorials on C language" /><style type="text/css">
<!--
 BODY{font-family: Arial; font-size:12pt}
 H1{color:#5f9ea0; font-size:20pt}
 H4{color:#0000FF}
 H3{color:#004080}
 B{background:#fffacd}
 -->
</style>
</head><body><center><h1><b>CHARACTER AND STRINGS</b></h1></center><br /><p>Ok atlast after a long gap I am writing the third tutorial explaining the concept of C language. Today's topic is character and strings. <b>Experts skip this articles</b>.</p><h3>Characters</h3><p>Another very imortant data in c is <b>char</b>, which stands for <i>character</i>. A character is a 1-byte value that can be used to hold printable character or integers in the range -128 to +127. A character constant is enclosed between single quotes. Ok let's see a sample program.</p><h4>A Simple Example using characters</h4><table border="0" cellpadding="0" cellspacing="0" ><tr><td align="left"><p>#include<stdio.h><br /><br />/* Sample Program */<br /><br />void main ()<br />{<br />     char ch;<br /><br />     char = 'A';<br />     printf(" %c", ch);<br /><br />     ch = 'B';<br />     printf("%c", ch);<br /><br />     ch = 'C';<br />     printf("%c", ch);<br /><br />}<br />Output of this program will be: ABC<br /><br /></p></td></tr></table><br /><p>Although it is possible to use <b>scanf()</b> to read a single character from the keyboard, a more common way is to use library function <b>getche()</b>. The <b>getche()</b> function waits until a key is pressed and then returns the result. Let see another sample program. This program will display <b>"you pressed my magic key" </b>if <b>I</b> is pressed. (<b>Tip</b>: another use of <b>getche()</b> function is to hold the output displayed on the screen until a key is pressed.) This program also illustrates that character can be used in if statements.<br /><br /><h4>Another Simple Example using characters</h4><table border="0" cellpadding="0" cellspacing="0" ><tr><td align="left"><p>#include<stdio.h><br /><br />/* Sample Program */<br /><br />void main ()<br />{<br />     char ch;<br /><br />     ch = getche();   /* read one character from the keyboard */<br />     if(ch== 'I')<br />     printf("you pressed my magic Key\n");<br /><br />}<br /><br /></p></td></tr></table><br /><h3>Strings</h3><p>In C, a <i>string</i> is an array of characters terminated by a null.(Tip: in C, a null is essentially the same as 0.)C does not have a "string" type. Instead, it is declared as an array of characters and use the various string function found in the library to manipulate them. Array will come later in my tutorials but a few basic principles are required here.</p><p>Well array can be of number of dimensions but for this tutorial I am going to stick to one-dimensional array. A <i>one-dimensional array </i>is a list of variables of the same type. We can create such an array by placing the size of the array, enclosed between square brackets, after the array name. For example following fragment declares an 80-element character array called <b>str</b>.</p>                <b> char str[80]; </b><br /><p>To reference a specific element, place the index between square brackets after the array name. All arrays in C are indexed from zero. Therefore, str[0] is the first element, str[1] is the second element, with str[79] being the 80th and last element.</p><p>It is most important to remember that no <i>bounds-checking </i>performed. If not careful, it is possible for program to "run off the end" of an array. A simple method of preventing this is to always use an array that is large enough to hold whatever will be put into it. Remember that all strings end in a null. Therefore array must be atleast one character larger than the largest string so that it can accommodate the null terminator. A null in C is specified as the character constant <b>'\0'</b>. As an example, a character array large enough to hold the word"hello" will need at least six characters long, five for the string and one for the null terminator, as shown below:</p><center><table border="1" cellspacing="0" cellpadding="10"><tr><td>h</td><td>e</td><td>l</td><td>l</td><td>o</td><td>'\0'</td></tr></table></center><p>To read a string from the keyboard, first create a character array to hold the string and then use the library function <b>gets()</b>. The <b>gets()</b> function takes the name of the string as an argument and reads characters from the keyboard . let's see an example program.</p><h4> Simple Example using strings</h4><table border="0" cellpadding="0" cellspacing="0" ><tr><td align="left"><p>#include<stdio.h><br />#include<string.h><br /><br />/* Sample Program */<br /><br />void main ()<br />{<br />     char str[80];<br /><br />     printf("Enter your name: ");<br />     gets(str);<br />     printf("hello %s", str);<br />}<br /><br /></p></td></tr></table><br /><p>Notice that the format command <b>%s</b> is used to cause <b>printf() </b>to print a string.</p><p>There are several standard functions used to manipulate strings. The two most common are <b>strlen()</b>, which returns the length of a string, and <b>strcpy()</b>, which copies a string from one string to another. They have the syntax <b>strlen(string)</b> and <b>strcpy(destination, source)</b> respectively. Copying a larger string to a smaller string, or reading a string into variable that is not large enough to store it can cause unpredictable results. Always check that the destination string is large enough to accommodate the source string. Let see an example showing these two library functions.</p><h4>Another Simple Example using strings</h4><table border="0" cellpadding="0" cellspacing="0" ><tr><td align="left"><p>#include<stdio.h><br />#include<string.h><br /><br />/* Sample Program */<br /><br />void main ()<br />{<br />     char str[8];<br />     char newstr[8];<br /><br />     printf("Please enter your name: ");<br />     gets(str);<br />     printf("Hello %s.\n", str);<br />     printf("There are %d letters in your name.\n",strlen( str));<br />     strcpy(newstr, str);<br />     printf("newstr is %s.\n", newstr);<br />}<br /><br /></p></td></tr></table><br /><p>Ok guys! thats enough for this tutorial next tutorial will be about <b>OPERATORS IN C</b><br /><center>Bye for now!!</center></body></html>

