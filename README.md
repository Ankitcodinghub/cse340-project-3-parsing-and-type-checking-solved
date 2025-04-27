# cse340-project-3-parsing-and-type-checking-solved
**TO GET THIS SOLUTION VISIT:** [CSE340 Project 3: Parsing and Type Checking Solved](https://www.ankitcodinghub.com/product/cse340-fall-2019-project-3-parsing-and-type-checking-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;36165&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;5&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (5 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE340  Project 3: Parsing and Type Checking Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (5 votes)    </div>
    </div>
In this project, you are asked to write a parser and a type checker for a small language. The parser checks that the input is syntactically correct and the type checker enforces the semantic rules of the language. The semantic rules that your program will enforce relate to declarations and types. In addition, your program will check for unused variables or variables used before they are assigned a value and output corresponding error messages.

The input to your code will be a program and the output will be: • syntax error message if the input program is not syntactically correct

<ul>
<li>if the input program has no syntax error, the output is:</li>
<li>semantic error messages if there is a declaration error or a type mismatch in the input program,</li>
<li>error messages if there are variables that are declared but never used or variables that are used before they are assigned a value, or</li>
<li>information about the types of the symbols declared in the input program if there is no semantic error.</li>
</ul>
In what follows, I describe the language syntax and semantic rules.

<h1>1.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Language Syntax</h1>
<h2>1.1.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Grammar Description</h2>
&nbsp;

&nbsp;

<table width="626">
<tbody>
<tr>
<td width="124">program</td>
<td colspan="2" width="292">→ scope</td>
<td width="209"></td>
</tr>
<tr>
<td width="124">scope</td>
<td colspan="2" width="292">→ LBRACE scope list RBRACE</td>
<td width="209"></td>
</tr>
<tr>
<td width="124">scope list</td>
<td colspan="2" width="292">→ scope</td>
<td width="209"></td>
</tr>
<tr>
<td width="124">scope list</td>
<td colspan="2" width="292">→ var decl</td>
<td width="209"></td>
</tr>
<tr>
<td width="124">scope list</td>
<td colspan="2" width="292">→ stmt</td>
<td width="209"></td>
</tr>
<tr>
<td width="124">scope list</td>
<td colspan="2" width="292">→ scope scope list</td>
<td width="209"></td>
</tr>
<tr>
<td width="124">scope list</td>
<td colspan="2" width="292">→ var decl scope list</td>
<td width="209"></td>
</tr>
<tr>
<td width="124">scope list</td>
<td colspan="2" width="292">→ stmt scope list</td>
<td width="209"></td>
</tr>
<tr>
<td width="124">var decl</td>
<td colspan="2" width="292">→ id list COLON type name SEMICOLON</td>
<td width="209"></td>
</tr>
<tr>
<td width="124">id list</td>
<td colspan="2" width="292">→ ID</td>
<td width="209"></td>
</tr>
<tr>
<td width="124">id list

type name stmt list stmt list stmt stmt assign stmt while stmt while stmt expr expr
</td>
<td colspan="2" width="292">→ ID COMMA id list

→ REAL | INT | BOOLEAN | STRING

→ stmt

→ stmt stmt list

→ assign stmt

→ while stmt

→ ID EQUAL expr SEMICOLON

→ WHILE condition LBRACE stmt list RBRACE

→ WHILE condition stmt

→ arithmetic operator expr expr

→ binary boolean operator expr expr
</td>
<td width="209">ll</td>
</tr>
<tr>
<td colspan="2" width="199">expr</td>
<td colspan="2" width="427">→ relational operator expr expr</td>
</tr>
<tr>
<td colspan="2" width="199">expr</td>
<td colspan="2" width="427">→ NOT expr</td>
</tr>
<tr>
<td colspan="2" width="199">expr</td>
<td colspan="2" width="427">→ primary</td>
</tr>
<tr>
<td colspan="2" width="199">arithmetic operator</td>
<td colspan="2" width="427">→ PLUS | MINUS | MULT | DIV</td>
</tr>
<tr>
<td colspan="2" width="199">binary boolean operator</td>
<td colspan="2" width="427">→ AND | OR | XOR</td>
</tr>
<tr>
<td colspan="2" width="199">relational operator</td>
<td colspan="2" width="427">→ GREATER | GTEQ | LESS | NOTEQUAL | LTEQ</td>
</tr>
<tr>
<td colspan="2" width="199">primary</td>
<td colspan="2" width="427">→ ID | NUM | REALNUM | STRING CONSTANT | bool const</td>
</tr>
<tr>
<td colspan="2" width="199">bool const</td>
<td colspan="2" width="427">→ TRUE | FALSE</td>
</tr>
<tr>
<td colspan="2" width="199">condition</td>
<td colspan="2" width="427">→ LPAREN expr RPAREN</td>
</tr>
<tr>
<td width="124"></td>
<td width="74"></td>
<td width="218"></td>
<td width="209"></td>
</tr>
</tbody>
</table>
Notice that expressions are in prefix notation in this language. This makes parsing easier.

<h2>1.2.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Tokens</h2>
The tokens are included for completeness. You are provided with a getToken() function for the following tokens used in the grammar description:

<table width="626">
<tbody>
<tr>
<td width="144">LBRACE</td>
<td width="28">=</td>
<td width="453">{</td>
</tr>
<tr>
<td width="144">RBRACE</td>
<td width="28">=</td>
<td width="453">}</td>
</tr>
<tr>
<td width="144">COLON</td>
<td width="28">=</td>
<td width="453">:</td>
</tr>
<tr>
<td width="144">SEMICOLON</td>
<td width="28">=</td>
<td width="453">;</td>
</tr>
<tr>
<td width="144">REAL</td>
<td width="28">=</td>
<td width="453">REAL</td>
</tr>
<tr>
<td width="144">INT</td>
<td width="28">=</td>
<td width="453">INT</td>
</tr>
<tr>
<td width="144">BOOLEAN</td>
<td width="28">=</td>
<td width="453">BOOLEAN</td>
</tr>
<tr>
<td width="144">STRING</td>
<td width="28">=</td>
<td width="453">STRING</td>
</tr>
<tr>
<td width="144">WHILE</td>
<td width="28">=</td>
<td width="453">WHILE</td>
</tr>
<tr>
<td width="144">COMMA</td>
<td width="28">=</td>
<td width="453">,</td>
</tr>
<tr>
<td width="144">LPAREN</td>
<td width="28">=</td>
<td width="453">’(’</td>
</tr>
<tr>
<td width="144">RPAREN</td>
<td width="28">=</td>
<td width="453">’)’</td>
</tr>
<tr>
<td width="144">EQUAL</td>
<td width="28">=</td>
<td width="453">=</td>
</tr>
<tr>
<td width="144">PLUS</td>
<td width="28">=</td>
<td width="453">+</td>
</tr>
<tr>
<td width="144">MULT</td>
<td width="28">=</td>
<td width="453">*</td>
</tr>
<tr>
<td width="144">DIV</td>
<td width="28">=</td>
<td width="453">/</td>
</tr>
<tr>
<td width="144">AND</td>
<td width="28">=</td>
<td width="453">^</td>
</tr>
<tr>
<td width="144">OR</td>
<td width="28">=</td>
<td width="453">’|’</td>
</tr>
<tr>
<td width="144">XOR</td>
<td width="28">=</td>
<td width="453">&amp;</td>
</tr>
<tr>
<td width="144">NOT</td>
<td width="28">=</td>
<td width="453">~</td>
</tr>
<tr>
<td width="144">GREATER</td>
<td width="28">=</td>
<td width="453">&gt;</td>
</tr>
<tr>
<td width="144">GTEQ</td>
<td width="28">=</td>
<td width="453">&gt;=</td>
</tr>
<tr>
<td width="144">LESS</td>
<td width="28">=</td>
<td width="453">&lt;</td>
</tr>
<tr>
<td width="144">LTEQ</td>
<td width="28">=</td>
<td width="453">&lt;=</td>
</tr>
<tr>
<td width="144">NOTEQUAL</td>
<td width="28">=</td>
<td width="453">&lt;&gt;</td>
</tr>
<tr>
<td width="144">TRUE</td>
<td width="28">=</td>
<td width="453">TRUE</td>
</tr>
<tr>
<td width="144">FALSE</td>
<td width="28">=</td>
<td width="453">FALSE</td>
</tr>
<tr>
<td width="144">STRING\_CONSTANT</td>
<td width="28">=</td>
<td width="453">” (letter | digit)* “</td>
</tr>
<tr>
<td width="144">ID</td>
<td width="28">=</td>
<td width="453">letter (letter | digit)*</td>
</tr>
<tr>
<td width="144">NUM</td>
<td width="28">=</td>
<td width="453">0 | (pdigit digit*)</td>
</tr>
<tr>
<td width="144">REALNUM</td>
<td width="28">=</td>
<td width="453">NUM . digit digit*</td>
</tr>
</tbody>
</table>
where

<table width="626">
<tbody>
<tr>
<td width="178">letter</td>
<td width="27">=</td>
<td colspan="3" width="421">a | b | c | … | z | A | B | C | … | Z</td>
</tr>
<tr>
<td width="178">digit</td>
<td width="27">=</td>
<td width="36">0 | 1</td>
<td width="10">|</td>
<td width="375">2 | … | 9</td>
</tr>
<tr>
<td width="178">pdigit</td>
<td width="27">=</td>
<td colspan="3" width="421">1 | 2 | 3 | … | 9</td>
</tr>
</tbody>
</table>
<h1>2.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Language Semantics</h1>
<h2>2.1.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Scoping Rules</h2>
Static scoping is used. I have already covered static scoping in class, so you should know the semantics and how references should be resolved. Every scope defines a scope.

<strong>2.2.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Types</strong>

The language has four basic types: INT , REAL , BOOLEAN , and STRING .

<h2>2.3.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Variables</h2>
<table width="144">
<tbody>
<tr>
<td width="144">id list : type name</td>
</tr>
</tbody>
</table>
Variables are declared explicitly in var decl of the form. The names of the declared variables appear in the id list and their type is the type name . <strong>Example </strong>Consider the following program written in our language:

<table width="626">
<tbody>
<tr>
<td width="626">{

x : INT; y : INT; y = x;

}
</td>
</tr>
</tbody>
</table>
This program has two declared variables: x and y . Both have type INT .

<h2>2.4.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Declaration and Reference</h2>
Any occurrence of a name in the program is either a <strong>declaration </strong>or a <strong>reference</strong>. Any occurrence of a name in an id list that is part of a var decl is a declaration of the name. Any other occurrence of a name is considered a reference to that name. Note that the above definitions exclude the built-in type names, which are predeclared as part of the language definition.

Given the following example (the line numbers are not part of the input):

<table width="626">
<tbody>
<tr>
<td width="68">01 {

02
</td>
<td width="558">a : INT;</td>
</tr>
<tr>
<td width="68">03</td>
<td width="558">b : REAL;</td>
</tr>
<tr>
<td width="68">04

05 }
</td>
<td width="558">b = x;</td>
</tr>
</tbody>
</table>
We can categorize all occurrences of names as <strong>declaration </strong>or <strong>reference</strong>:

&nbsp;

Line 2, the occurrence of name a is a declaration

<ul>
<li>Line 3, the occurrence of name b is a declaration</li>
<li>Line 4, the occurrence of name b is a reference</li>
<li>Line 4, the occurrence of name x is a reference</li>
</ul>
<h2>2.5.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Type System</h2>
We describe which assignments are valid (type compatibility) and how to determine the types of expressions (type inference).

<strong>2.5.1.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Type Compatibility Rules</strong>

Type compatibility rules specify which assignments are valid. The Rules are the following.

<ul>
<li><strong>C1: </strong>If the types of the lefthand side of an assignment is INT , BOOLEAN , or STRING , the righthand side of the assignment should have the same type.</li>
<li><strong>C2: </strong>If the type of the lefthand side of an assignment is REAL , the type of the righthand side of the assignment should be INT or REAL .</li>
<li><strong>M1: </strong>Assignments that do not satisfy <strong>C1 </strong>or <strong>C2 </strong>are not valid. In this case, we say that there is a type mismatch.</li>
</ul>
<strong>2.5.2.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Type Inference Rules</strong>

<ul>
<li><strong>C3: </strong>The types of the operands of an arithmetic operator should be REAL or INT</li>
</ul>
<table width="164">
<tbody>
<tr>
<td width="164">binary boolean operator</td>
</tr>
</tbody>
</table>
<ul>
<li><strong>C4: </strong>The type of the operands of ashould be BOOLEAN .</li>
<li><strong>C5: </strong>If neither operand of a relational operator has type INT or REAL , then the operands should have the same type. In this case, both types can be STRING or both types can be BOOLEAN .</li>
<li><strong>C6: </strong>If one of the operands of a relational operator has type INT or REAL , then the other operand should have type INT or REAL . In this case, the two operands can have different types.</li>
<li><strong>C7: </strong>The type of a condition should be BOOLEAN .</li>
<li><strong>C8: </strong>The type of the operand of the NOT operator should be boolean.</li>
<li><strong>I1: </strong>If <strong>C3 </strong>is satisfied, and the type of one of the operands of an arithmetic operator is REAL , the type of the resulting expression is REAL .</li>
<li><strong>I2: </strong>For the PLUS , MINUS , and MULT operators, if the types of the two operands are INT , the type of the resulting expression is INT .</li>
<li><strong>I3: </strong>For the DIV operator, if the types of the two operands are INT , the type of the resulting expression is REAL .</li>
<li><strong>I4: </strong>If the operands of a binary boolean operator are BOOLEAN , the type of the resulting expression is BOOLEAN .</li>
<li><strong>I5: </strong>If <strong>C5 </strong>and <strong>C6 </strong>are satisfied, the type of a relational operator expr expr is BOOLEAN .</li>
<li><strong>I6: </strong>The type of NUM constants is INT</li>
<li><strong>I7: </strong>The type of REALNUM constants is REAL</li>
</ul>
<table width="76">
<tbody>
<tr>
<td width="76">bool const</td>
</tr>
</tbody>
</table>
<ul>
<li><strong>I8: </strong>The type ofconstants is BOOLEAN</li>
</ul>
<strong>I9: </strong>The type of STRING CONSTANT constants is STRING

<ul>
<li><strong>M2: </strong>If <strong>C3</strong>, <strong>C4</strong>, <strong>C5</strong>, <strong>C6</strong>, <strong>C7 </strong>or <strong>C8 </strong>are not satisfied, the type of the expressions is ERROR. In this case, we say that there is a type mismatch.</li>
</ul>
<h1>3.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Parser</h1>
You must write a parser for the grammar, If your parser detects a syntax error in the input, it should output the following message and exit:

Syntax Error

You should start coding by writing the parser first and make sure that your parser generates a syntax error message if the input program is syntactically incorrect. <strong>There will be no partial credit given for syntax checking</strong>

The grammar of the language is not LL(1) i.e. it does not satisfy the conditions for predictive parser with one token lookahead, however, it is still possible to write a recursive descent parser with no backtracking. We can do this by looking ahead at more than one token in some cases and left-factoring some rules.

Two rules like

<table width="626">
<tbody>
<tr>
<td width="102">stmt list</td>
<td width="524">→ stmt</td>
</tr>
<tr>
<td width="102">stmt list</td>
<td width="524">→ stmt stmt list</td>
</tr>
</tbody>
</table>
<table width="69">
<tbody>
<tr>
<td width="69">stmt list</td>
</tr>
</tbody>
</table>
<table width="102">
<tbody>
<tr>
<td width="68"></td>
<td width="35">stmt</td>
</tr>
<tr>
<td width="68">stmt list</td>
<td width="35"></td>
</tr>
</tbody>
</table>
can be parsed by first parsing&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; and then checking if the next token is the beginning of

or in the FOLLOW of&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; . In fact the two rules are equivalent to

<table width="626">
<tbody>
<tr>
<td width="109">stmt list</td>
<td width="516">→ stmt stmt list1</td>
</tr>
<tr>
<td width="109">stmt list1</td>
<td width="516">→ stmt</td>
</tr>
</tbody>
</table>
but you do not need to explicitly left-factor the rules by introducing stmt list1 to parse stmt list .

<h1>4.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Semantic Checking</h1>
Your program will check for the following semantic errors and output the apropriate message when it encounters that error.

<h2>4.1.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Declaration Errors</h2>
<ul>
<li><strong>Variable declared more than once </strong>(error code <strong>1.1</strong>)</li>
</ul>
<table width="55">
<tbody>
<tr>
<td width="55">id list</td>
</tr>
</tbody>
</table>
A variable is declared more than once if appears more than once in the same id list of a var decl or if it appears in twoof two different var decl and <em>locally </em>looking up the

name that appears in one of the two declarations returns the other declaration.

<ul>
<li><strong>Undeclared variable </strong>(error code <strong>2</strong>)</li>
</ul>
If resolving a variable name that appears in a statement other than a declaration returns no declaration, the variable is undeclared.

<ul>
<li><strong>Variable Declared but not used </strong>(error code <strong>3</strong>)</li>
</ul>
If a variable is declared but is not referenced, we say that the variable is declared but not used. We say that a declaration is referenced if some reference to the variable resolves to the declaration. If a declaration is not referenced, we have error code 1.3.

<table width="55">
<tbody>
<tr>
<td width="55">id list</td>
</tr>
</tbody>
</table>
<strong>Redeclaration or reference as a variable for of a built-in type name </strong>If a built-in type name appears inof a variable declaration or appears in a statement other than a declaration statement, your parser should output syntax error.

For each error involving declarations, your type checker should output one line in the following format:

ERROR CODE &lt;code&gt; &lt;symbol_name&gt;

in which <em>&lt;</em>code<em>&gt; </em>should be replaced with the proper code (see the error codes listed above) and <em>&lt;</em>symbol name<em>&gt; </em>should be replaced with the name of the variable that caused the error. Since the test cases will have at most one error each, the order in which these error messages are printed does not matter.

<strong>Note that there will only be at most one declaration error per test case</strong>.

<h2>4.2.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Type Mismatch</h2>
If there are no declaration errors and any of the type constraints (listed in the Type System section above) is violated in the input program, then the output of your program should be:

TYPE MISMATCH &lt;line_number&gt; &lt;constraint&gt;

Where <em>&lt;</em>line number<em>&gt; </em>is replaced with the line number of the line in which the violation occurs and

<em>&lt;</em>constraint<em>&gt; </em>should be replaced with the label of the violated type constraint (possible values are <strong>C1</strong>, <strong>C2</strong>, <strong>C3</strong>, <strong>C4</strong>, <strong>C5</strong>, <strong>C6</strong>, <strong>C7 </strong>or <strong>C8</strong>. (see section on Type System for details of each constraint). Note that you can assume that anywhere a violation can occur it will be on a single line.

<strong>4.2.1.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Type Mistmatch and Other Errors</strong>

<ul>
<li><strong>Type mismatch and C1 and C2 violations </strong>You should not declare C1 or C2 violation if the expression on the RHS has a type mismatch error. If there is a type mismatch error in the expression on the RHS of an assignment (C3, C4, C5, C6, C8), you should not also declare C1 or C2 errors. I illustrate this with an example</li>
</ul>
<table width="139">
<tbody>
<tr>
<td width="63">1: {</td>
<td width="77">x : INT;</td>
</tr>
<tr>
<td width="63">2:</td>
<td width="77">y : STRING;</td>
</tr>
<tr>
<td width="63">3:</td>
<td width="77">z : INT;</td>
</tr>
<tr>
<td width="63">4:

5: }
</td>
<td width="77">z = + x y;</td>
</tr>
</tbody>
</table>
Here, on line 4, we have a violation of C3 because the type of y is STRING which violates C3. Given that C3 is violated, the type of + x y is really not defined and we could conclude that C1 is violated, but you should not declare a C1 violation in this case. Similar examples can be made for other combinations.

<ul>
<li><strong>Type mismatch and C7 Violations </strong>You should not declare C7 violation if the condition has a type mismatch error.</li>
<li><strong>Type Mismatch and Declaration Errors </strong>If there are declaration errors and type mismatch errors, only the output for the declaration errors should be produced.</li>
</ul>
<strong>Note that there will only be at most one type mismatch error per test case</strong>.

&nbsp;

<h2>4.3.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Use of Uninitialized Variables</h2>
For this part, your program should identify variables that are used before they are defined. We say that a <em>variable is used if it appears in an expression</em>. We say that a <em>variable is defined if it appears on the lefthand side of an assignment</em>. A variable is used before it is defined if there is an execution path in which there is a use of the variable that is not preceded by a definition of the variable. Compilers typically call this ”use of an uninitialized variable”. In general determining use of uninitialized variables is involved and requires building a control flow graph of the program. Fortunately, for the language of this project, determining uninitialized uses is relatively easy. First, I will describe the output format, then I will give a more detailed description of how determine uninitialized uses.

The output format for use of uninitialized variables is the following

UNINITIALIZED &lt;name_reference_1&gt; &lt;line_no_reference_1&gt;

UNINITIALIZED &lt;name_reference_2&gt; &lt;line_no_reference_2&gt; …

<table width="539">
<tbody>
<tr>
<td width="130">&lt;name reference i&gt;</td>
<td width="261">is the name of i’th uninitialized variable and</td>
<td width="149">&lt;line no reference i&gt;</td>
</tr>
</tbody>
</table>
Where is the line number in which the i’th uninitialized reference appears.

In what follows, I will explain how to determine uses of uninitialized variables. Consider the program below (the line numbers are not part of the input but are added for ease of reference):

<table width="626">
<tbody>
<tr>
<td width="61">01 {

02
</td>
<td width="565">x1, x2, x3, x4 , x5 : INT;</td>
</tr>
<tr>
<td width="61">03

04
</td>
<td width="565">x3 = 2;</td>
</tr>
<tr>
<td width="61">05

06
</td>
<td width="565">WHILE ( &lt; x1 100 ) {</td>
</tr>
<tr>
<td width="61">07</td>
<td width="565">x1 = + x1 1;</td>
</tr>
<tr>
<td width="61">08</td>
<td width="565">x2 = 1;</td>
</tr>
<tr>
<td width="61">09</td>
<td width="565">x4 = + x2 1;</td>
</tr>
<tr>
<td width="61">10</td>
<td width="565">x1 = + x3 1;</td>
</tr>
<tr>
<td width="61">11</td>
<td width="565">WHILE ( &lt; x1 10 ) {</td>
</tr>
<tr>
<td width="61">12</td>
<td width="565">x5 = + x1 + x3 x5 ;</td>
</tr>
<tr>
<td width="61">13</td>
<td width="565">}</td>
</tr>
<tr>
<td width="61">14</td>
<td width="565">x1 = x5;</td>
</tr>
<tr>
<td width="61">15</td>
<td width="565">x5 = 1;</td>
</tr>
<tr>
<td width="61">16</td>
<td width="565">}</td>
</tr>
<tr>
<td width="61">17

18

19 }
</td>
<td width="565">x2 = + x2 1 ;</td>
</tr>
</tbody>
</table>
<ul>
<li>The use of x1 in the expression &lt; x1 100 is a use of an uninitialized variable. The first time the expression is evaluated, there is no previous definition (assignment) to x1. Note that later evaluations of &lt; x1 10 happen after the assignment x1 = + x1 1; so the use of x1 in &lt; x1 10 counts as initialized.</li>
<li>The use of x1 in x1 = + x1 1; on line 07 is uninitialized because the first time + x1 1 is evaluated, x1 has no initial value.</li>
<li>The use of x2 on line 09 is initialized because it is always preceded by the definition (assignment to) of x2 on line 08.</li>
<li>The use of x3 on line 10 is initialized because it is always preceded by the definition (assignment to) x3 on line 04.</li>
<li>The use of x1 on line 11 is initialized because it is always preceded by the definition (assignment to) x1 on line 10 (also on line 07).</li>
<li>The use of x1 on line 12 is initialized because it is always preceded by the definition (assignment to) x1 on line 10 (also on line 07).</li>
<li>The use of x3 on line 12 is initialized because it is always preceded by the definition (assignment to) x3 on line 04.</li>
<li>The use of x5 on line 12 is not initialized because it is not preceded by a definition (assignment to) x5.</li>
<li>The use of x5 on line 14 is not initialized because it is not preceded by a definition (assignment to) x5. Even though there is a definition (assignment to) of x5 on line 12, we cannot determine (in general) if the body of the loop will be executed, so we assume that the preceding loop did not execute. Note that this situation is different from the use of x1 on line 12 which is guaranteed to be preceded by the definition (assignment to) of x1 on line 10.</li>
<li>The use of x2 on line 18 is not initialized because it is not preceded by a definition (assignment to) x2. Even though x2 is defined (assigned a value) on line 08, we cannot determine (in general) if the body of the loop is executed, so we have to assume that it is not executed.</li>
</ul>
It should be clear from the example, that to determine uninitialized variables, you can treat while stmt

<table width="76">
<tbody>
<tr>
<td width="76">while stmt</td>
</tr>
</tbody>
</table>
as some kind of a scope. If a use is inside a, then all definitions preceding it in the while stmt together with all definitions preceding it in enclosing while stmt should be taken into consideration.

<h2>4.4.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; No Semantic Errors</h2>
If there are no declaration errors, no type mismatch errors and no use of uninitialized variables, then your program should output for each reference of a declared variable name, in the order in which the reference appears in the program, the line number in which the reference appears and the line number of the declaration to which the reference of the name resolves. For this part, the format should be the following

&lt;name_reference_1&gt; &lt;line_no_reference_1&gt; &lt;line_no_declared_1&gt;

&lt;name_reference_2&gt; &lt;line_no_reference_2&gt; &lt;line_no_declared_2&gt; …

Where &lt;name reference i&gt; is the name of a variable and corresponds to i’th name reference in the program. &lt;line no reference i&gt; is the line number in which the i’th reference appears and &lt;line no declared i&gt; is the line number of the declaration corresponding to the i’th reference.

<h1>5.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; More Examples</h1>
<strong>Example 1. </strong>Given the following example (the line numbers are not part of the input):

<table width="626">
<tbody>
<tr>
<td width="61">01 {

02
</td>
<td width="565">x : INT;</td>
</tr>
<tr>
<td width="61">03</td>
<td width="565">y : BOOLEAN;</td>
</tr>
<tr>
<td width="61">04

05 }
</td>
<td width="565">y = x;</td>
</tr>
</tbody>
</table>
The output will be the following:

TYPE MISMATCH 4 C1

<strong>Example 2. </strong>Given the following example (the line numbers are not part of the input):

<table width="626">
<tbody>
<tr>
<td width="61">01 {

02
</td>
<td width="565">x : BOOLEAN;</td>
</tr>
<tr>
<td width="61">03</td>
<td width="565">y : REAL;</td>
</tr>
<tr>
<td width="61">04

05 }
</td>
<td width="565">y = x;</td>
</tr>
</tbody>
</table>
The output will be the following:

TYPE MISMATCH 4 C2

<strong>Example 3. </strong>Given the following example (the line numbers are not part of the input):

<table width="626">
<tbody>
<tr>
<td width="61">01 {

02
</td>
<td width="565">x : BOOLEAN;</td>
</tr>
<tr>
<td width="61">03</td>
<td width="565">x : BOOLEAN;</td>
</tr>
<tr>
<td width="61">04

05 }
</td>
<td width="565">x = x;</td>
</tr>
</tbody>
</table>
The output will be the following:

ERROR CODE 1.1 x

<strong>Example 4. </strong>Given the following example (the line numbers are not part of the input):

<table width="626">
<tbody>
<tr>
<td width="61">01 {

02
</td>
<td width="565">x : INT;</td>
</tr>
<tr>
<td width="61">03</td>
<td width="565">y, x : STRING;</td>
</tr>
<tr>
<td width="61">04</td>
<td width="565">y = 10;</td>
</tr>
<tr>
<td width="61">05

05 }
</td>
<td width="565">x = 10;</td>
</tr>
</tbody>
</table>
The output will be the following:

ERROR CODE 1.1 x

<strong>Example 5. </strong>Given the following example (the line numbers are not part of the input):

<table width="626">
<tbody>
<tr>
<td width="61">01 {

02
</td>
<td width="565">x : INT;</td>
</tr>
<tr>
<td width="61">03</td>
<td width="565">y : STRING;</td>
</tr>
<tr>
<td width="61">04

05 }
</td>
<td width="565">y = “abc”;</td>
</tr>
</tbody>
</table>
The output will be the following:

ERROR CODE 1.3 x

<strong>Example 6. </strong>Given the following example (the line numbers are not part of the input):

<table width="626">
<tbody>
<tr>
<td width="61">01 {

02
</td>
<td width="565">x1 , x2 : INT;</td>
</tr>
<tr>
<td width="61">03</td>
<td width="565">y : INT;</td>
</tr>
<tr>
<td width="61">04</td>
<td width="565">x1 = y;</td>
</tr>
<tr>
<td width="61">05

06 }
</td>
<td width="565">y = + x1 x2;</td>
</tr>
</tbody>
</table>
The output will be the following:

UNINITIALIZED y 4

UNINITIALIZED x2 5

<strong>Example 7. </strong>Given the following example (the line numbers are not part of the input):

<table width="626">
<tbody>
<tr>
<td width="82">01 {

02
</td>
<td width="544">a : INT;</td>
</tr>
<tr>
<td width="82">03</td>
<td width="544">b : INT;</td>
</tr>
<tr>
<td width="82">04</td>
<td width="544">a = 1;</td>
</tr>
<tr>
<td width="82">05</td>
<td width="544">b = 1;</td>
</tr>
<tr>
<td width="82">06</td>
<td width="544">{&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; a : INT;</td>
</tr>
<tr>
<td width="82">07</td>
<td width="544">a = 1;</td>
</tr>
<tr>
<td width="82">08</td>
<td width="544">WHILE ( &gt; a b )</td>
</tr>
<tr>
<td width="82">09</td>
<td width="544">{</td>
</tr>
<tr>
<td width="82">10</td>
<td width="544">a = – a b;</td>
</tr>
<tr>
<td width="82">11</td>
<td width="544">}</td>
</tr>
<tr>
<td width="82">12

13 }
</td>
<td width="544">}</td>
</tr>
</tbody>
</table>
The output will be the following:

<ul>
<li>4 2b 5 3 a 7 6 a 8 6 b 8 3 a 10 6 a 10 6</li>
<li>10 3</li>
</ul>
<h1>6.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Summary of Requirements</h1>
<ol>
<li>If there is a syntax error, the program should output syntax error and exit.</li>
<li>If there is no syntax error and there is a declaration error, the program should output the error message for the declaration error. You can assume that there can be no more than one declaration error in the test case. If the program outputs a declaration error, the program should output no other error message. Specifically, it should not output any type mismatch or uninitialized variable error message.</li>
<li>If there is no syntax error and no declaration error and there is a type mismatch, the program should output the error message for the type mismatch. You can assume that there can be no more than one type mismatch per test case. If the program outputs a type mismatch error message, the program should output no other error message. Specifically, it should not output any uninitialized variable error message.</li>
<li>If there is no syntax error, no declaration error and no type mismatch error, the program should output the list of variables used but not initialized in the format specified in Section 4.3.</li>
<li>If there is no error of any kind, the program should output for each reference, the line number of the reference and the line number of the declaration to which the reference resolves as explained in Section 4.4 above.</li>
</ol>
<h1>7.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Evaluation</h1>
Your submission will be graded on passing the automated test cases.

The test cases (there will be multiple test cases in each category, each with equal weight) will be broken down in the following way (out of 100 points):

<ul>
<li>Parsing: 35 points</li>
<li>Errors involving declarations: 20 points</li>
<li>Type mismatch errors and no semantic error cases: 35 points</li>
<li>Use of uninitialized variables: 10 points</li>
</ul>
There is no partial credit for the parsing category, you need to pass all test cases in that category to get the 35 points. All other categories have partial credit.

<h1>8.&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Implementation Suggestions</h1>
<ol>
<li>the provided code has the main() function in lexer. It is better to have a new file for parser and move the main() function to the parser.</li>
<li>You should first write the parser using the approach we studied in class.
<ul>
<li>The parser will require more than one lookahead in some places.</li>
<li>Do not start on any other part before finishing the parser.</li>
<li>If you do not follow the approach we studied in class methodically, you can end up with a parser that passes almost all cases and for which it is hard to find what is wrong.</li>
<li>In the past, some students could only fix their parser errors by rewriting it completely from scratch.</li>
</ul>
</li>
<li>Semantic checking might affect parsing.
<ul>
<li>If there is syntax error, only the syntax error message should be produced and no other error messages should be produced.</li>
<li>If you produce semantic error messages while parsing, you might end up generating a semantic error message before encountering the syntax error message. That is why you should ”save” your semantic error message and wait until parsing is done to print it.</li>
<li>If your program crashes or has segmentation fault, that can affect the output of syntax checking.</li>
</ul>
</li>
<li>Type checking for expressions.
<ul>
<li>As described in class, you should have parse expr() return a type (am integer value denoting the type).</li>
<li>For the base case expr -&gt; primary , the type can be determined immediately for constants and by looking up the variable type in the case primary is ID .</li>
<li>For the general case, it will be helpful to have a function in which all the type checking rules are implemented. The function takes as input an operator and two types (one is ignored in the case of unary operator) and returns the type of the resulting expressing or detects semantic error.</li>
</ul>
</li>
</ol>
