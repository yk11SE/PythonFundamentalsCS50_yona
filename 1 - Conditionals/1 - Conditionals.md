# Lecture 0 - Functions, Variables

Watch the [Functions, Variables](https://schoolsnsw.sharepoint.com/:v:/s/2025-SoftwareEngineering/EUx0KRRHe65Jj0jS1aqYiwcBNfF4TmbZdfwV92WcLE2uwQ?e=2PQ7fZ) video.

## Problems
1. [Problem 0.1 - Indoor Voice](https://github.com/TempeHS/PythonFundamentals/blob/main/0/PROBLEM0.1.md)
2. [Problem 0.2 - Playback Speed](https://github.com/TempeHS/PythonFundamentals/blob/main/0/PROBLEM0.2.md)
3. [Problem 0.3 - Making Faces](https://github.com/TempeHS/PythonFundamentals/blob/main/0/PROBLEM0.3.md)
4. [Problem 0.4 - Einstein](https://github.com/TempeHS/PythonFundamentals/blob/main/0/PROBLEM0.4.md)
5. [Problem 0.5 - Tip Calculator](https://github.com/TempeHS/PythonFundamentals/blob/main/0/PROBLEM0.5.md)

## Notes
1. [Creating Code with Python](Creating-Code-with-Python)
2. [Functions](#Functions)
3. [Bugs](Bugs)
4. [Improving Your First Python Program](Improving-Your-First-Python-Program)
5. [Variables](Variables)
6. [Comments](Comments)
7. [Pseudocode](Pseudocode)
8. [Further Improving Your First Python Program](Further-Improving-Your-First-Python-Program)
9. [Strings and Paremeters](Strings-and-Paremeters)
10. [A small problem with quotation marks](A-small-problem-with-quotation-marks)
11. [Formatting Strings](Formatting-Strings)
12. [More on Strings](More-on-Strings)
13. [Integers or int](Integers-or-int)
14. [Readability Wins](Readability-Wins)
15. [Float Basics](Float-Basics)
15. [More on Floats](More-on-Floats)
16. [Def](Def)
17. [Returning Values](Returning-Values)
18 [Summing Up](Summing-Up)

---

### Creating Code with Python

Lecture 1
Conditionals
if Statements
Control Flow, elif, and else
or
and
Modulo
Creating Our Own Parity Function
Pythonic
match
Summing Up
Conditionals
Conditionals allow you, the programmer, to allow your program to make decisions: As if your program has the choice between taking the left-hand road or the right-hand road based upon certain conditions.
Built within Python are a set of “operators” that can are used to ask mathematical questions.
> and < symbols are probably quite familiar to you.
>= denotes “greater than or equal to.”
<= denotes “less than or equal to.”
== denotes “equals, though do notice the double equal sign! A single equal sign would assign a value. Double equal signs are used to compare variables.
!= denotes “not equal to.
Conditional statements compare a left-hand term to a right-hand term.
if Statements
In your terminal window, type code compare.py. This will create a brand new file called “compare.”
In the text editor window, begin with the following:

x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x is less than y")
Notice how your program takes the input of the user for both x and y, casting them as integers and saving them into their respective x and y variables. Then, the if statement compares x and y. If the condition of x < y is met, the print statement is executed.

If statements use bool or boolean values (true or false) to decide whether or not to execute. If the statement of x > y is true, the compiler will register it as true and execute the code.
Control Flow, elif, and else
Further revise your code as follows:

x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x is less than y")
if x > y:
    print("x is greater than y")
if x == y:
    print("x is equal to y")
Notice how you are providing a series of if statements. First, the first if statement is evaluated. Then, the second if statement runs its evaluation. Finally, the last if statement runs its evaluation. This flow of decisions is called “control flow.”

Our code can be represented as follows:

True
True
True
False
False
False
start
x < y
"x is less than y"
x > y
"x is greater than y"
x == y
"x is equal to y"
stop
This program can be improved by not asking three consecutive questions. After all, not all three questions can have an outcome of true! Revise your program as follows:

x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x is less than y")
elif x > y:
    print("x is greater than y")
elif x == y:
    print("x is equal to y")
Notice how the use of elif allows the program to make less decisions. First, the if statement is evaluated. If this statement is found to be true, all the elif statements not be run at all. However, if the if statement is evaluated and found to be false, the first elif will be evaluated. If this is true, it will not run the final evaluation.

Our code can be represented as follows:

True
False
True
False
True
False
start
x < y
"x is less than y"
x > y
"x is greater than y"
x == y
"x is equal to y"
stop
While your computer may not notice a difference speed-wise between our first program and this revised program, consider how an online server running billions or trillions of these types of calculations each day could definitely be impacted by such a small coding decision.
There is one final improvement we can make to our program. Notice how logically elif x == y is not a necessary evaluation to run. After all, if logically x is not less than y AND x is not greater than y, x MUST equal y. Therefore, we don’t have to run elif x == y. We can create a “catch-all,” default outcome using an else statement. We can revise as follows:

x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y:
    print("x is less than y")
elif x > y:
    print("x is greater than y")
else:
    print("x is equal to y")
Notice how the relative complexity of this program has decreased through our revision.

Our code can be represented as follows:

<svg aria-roledescription="flowchart-v2" role="graphics-document document" viewBox="-8 -8 244.26251220703125 905.2125244140625" style="max-width: 244.26251220703125px;" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/2000/svg" width="100%" id="mermaid-1687592894522"><style>#mermaid-1687592894522{font-family:"trebuchet ms",verdana,arial,sans-serif;font-size:16px;fill:#333;}#mermaid-1687592894522 .error-icon{fill:#552222;}#mermaid-1687592894522 .error-text{fill:#552222;stroke:#552222;}#mermaid-1687592894522 .edge-thickness-normal{stroke-width:2px;}#mermaid-1687592894522 .edge-thickness-thick{stroke-width:3.5px;}#mermaid-1687592894522 .edge-pattern-solid{stroke-dasharray:0;}#mermaid-1687592894522 .edge-pattern-dashed{stroke-dasharray:3;}#mermaid-1687592894522 .edge-pattern-dotted{stroke-dasharray:2;}#mermaid-1687592894522 .marker{fill:#333333;stroke:#333333;}#mermaid-1687592894522 .marker.cross{stroke:#333333;}#mermaid-1687592894522 svg{font-family:"trebuchet ms",verdana,arial,sans-serif;font-size:16px;}#mermaid-1687592894522 .label{font-family:"trebuchet ms",verdana,arial,sans-serif;color:#333;}#mermaid-1687592894522 .cluster-label text{fill:#333;}#mermaid-1687592894522 .cluster-label span,#mermaid-1687592894522 p{color:#333;}#mermaid-1687592894522 .label text,#mermaid-1687592894522 span,#mermaid-1687592894522 p{fill:#333;color:#333;}#mermaid-1687592894522 .node rect,#mermaid-1687592894522 .node circle,#mermaid-1687592894522 .node ellipse,#mermaid-1687592894522 .node polygon,#mermaid-1687592894522 .node path{fill:#ECECFF;stroke:#9370DB;stroke-width:1px;}#mermaid-1687592894522 .flowchart-label text{text-anchor:middle;}#mermaid-1687592894522 .node .label{text-align:center;}#mermaid-1687592894522 .node.clickable{cursor:pointer;}#mermaid-1687592894522 .arrowheadPath{fill:#333333;}#mermaid-1687592894522 .edgePath .path{stroke:#333333;stroke-width:2.0px;}#mermaid-1687592894522 .flowchart-link{stroke:#333333;fill:none;}#mermaid-1687592894522 .edgeLabel{background-color:#e8e8e8;text-align:center;}#mermaid-1687592894522 .edgeLabel rect{opacity:0.5;background-color:#e8e8e8;fill:#e8e8e8;}#mermaid-1687592894522 .labelBkg{background-color:rgba(232, 232, 232, 0.5);}#mermaid-1687592894522 .cluster rect{fill:#ffffde;stroke:#aaaa33;stroke-width:1px;}#mermaid-1687592894522 .cluster text{fill:#333;}#mermaid-1687592894522 .cluster span,#mermaid-1687592894522 p{color:#333;}#mermaid-1687592894522 div.mermaidTooltip{position:absolute;text-align:center;max-width:200px;padding:2px;font-family:"trebuchet ms",verdana,arial,sans-serif;font-size:12px;background:hsl(80, 100%, 96.2745098039%);border:1px solid #aaaa33;border-radius:2px;pointer-events:none;z-index:100;}#mermaid-1687592894522 .flowchartTitleText{text-anchor:middle;font-size:18px;fill:#333;}#mermaid-1687592894522 :root{--mermaid-font-family:"trebuchet ms",verdana,arial,sans-serif;}</style><g><marker orient="auto" markerHeight="12" markerWidth="12" markerUnits="userSpaceOnUse" refY="5" refX="10" viewBox="0 0 10 10" class="marker flowchart" id="flowchart-pointEnd"><path style="stroke-width: 1; stroke-dasharray: 1, 0;" class="arrowMarkerPath" d="M 0 0 L 10 5 L 0 10 z"></path></marker><marker orient="auto" markerHeight="12" markerWidth="12" markerUnits="userSpaceOnUse" refY="5" refX="0" viewBox="0 0 10 10" class="marker flowchart" id="flowchart-pointStart"><path style="stroke-width: 1; stroke-dasharray: 1, 0;" class="arrowMarkerPath" d="M 0 5 L 10 10 L 10 0 z"></path></marker><marker orient="auto" markerHeight="11" markerWidth="11" markerUnits="userSpaceOnUse" refY="5" refX="11" viewBox="0 0 10 10" class="marker flowchart" id="flowchart-circleEnd"><circle style="stroke-width: 1; stroke-dasharray: 1, 0;" class="arrowMarkerPath" r="5" cy="5" cx="5"></circle></marker><marker orient="auto" markerHeight="11" markerWidth="11" markerUnits="userSpaceOnUse" refY="5" refX="-1" viewBox="0 0 10 10" class="marker flowchart" id="flowchart-circleStart"><circle style="stroke-width: 1; stroke-dasharray: 1, 0;" class="arrowMarkerPath" r="5" cy="5" cx="5"></circle></marker><marker orient="auto" markerHeight="11" markerWidth="11" markerUnits="userSpaceOnUse" refY="5.2" refX="12" viewBox="0 0 11 11" class="marker cross flowchart" id="flowchart-crossEnd"><path style="stroke-width: 2; stroke-dasharray: 1, 0;" class="arrowMarkerPath" d="M 1,1 l 9,9 M 10,1 l -9,9"></path></marker><marker orient="auto" markerHeight="11" markerWidth="11" markerUnits="userSpaceOnUse" refY="5.2" refX="-1" viewBox="0 0 11 11" class="marker cross flowchart" id="flowchart-crossStart"><path style="stroke-width: 2; stroke-dasharray: 1, 0;" class="arrowMarkerPath" d="M 1,1 l 9,9 M 10,1 l -9,9"></path></marker><g class="root"><g class="clusters"></g><g class="edgePaths"><path marker-end="url(#flowchart-pointEnd)" style="fill:none;" class="edge-thickness-normal edge-pattern-solid flowchart-link LS-A LE-B" id="L-A-B-0" d="M144.07813167572021,39L144.07813167572021,43.166666666666664C144.07813167572021,47.333333333333336,144.07813167572021,55.666666666666664,144.16146500905356,64.08333333333333C144.24479834238687,72.5,144.41146500905356,81,144.49479834238687,85.25L144.57813167572021,89.5"></path><path marker-end="url(#flowchart-pointEnd)" style="fill:none;" class="edge-thickness-normal edge-pattern-solid flowchart-link LS-B LE-C" id="L-B-C-0" d="M125.99952440343179,158.85889272771158L119.13814648060234,168.0386606064263C112.27676855777288,177.21842848514106,98.55401271211399,195.57796424257052,91.69263478928453,210.9243987879519C84.83125686645508,226.27083333333334,84.83125686645508,238.60416666666666,84.83125686645508,244.77083333333334L84.83125686645508,250.9375"></path><path marker-end="url(#flowchart-pointEnd)" style="fill:none;" class="edge-thickness-normal edge-pattern-solid flowchart-link LS-C LE-D" id="L-C-D-0" d="M84.83125686645508,289.9375L84.83125686645508,294.1041666666667C84.83125686645508,298.2708333333333,84.83125686645508,306.6041666666667,91.40283224298916,318.4070704250101C97.97440761952323,330.20997418335355,111.1175583725914,345.4824483667071,117.68913374912547,353.1186854583839L124.26070912565957,360.75492255006066"></path><path marker-end="url(#flowchart-pointEnd)" style="fill:none;" class="edge-thickness-normal edge-pattern-solid flowchart-link LS-D LE-E" id="L-D-E-0" d="M124.86328932546682,408.6601576497466L117.09649186749515,418.02929804145555C109.32969440952347,427.3984384331645,93.79609949358009,446.1367192165822,86.02930203560841,461.67252627495776C78.26250457763672,477.2083333333333,78.26250457763672,489.5416666666667,78.26250457763672,495.7083333333333L78.26250457763672,501.875"></path><path marker-end="url(#flowchart-pointEnd)" style="fill:none;" class="edge-thickness-normal edge-pattern-solid flowchart-link LS-E LE-F" id="L-E-F-0" d="M78.26250457763672,540.875L78.26250457763672,545.0416666666666C78.26250457763672,549.2083333333334,78.26250457763672,557.5416666666666,85.51341499139902,569.7600274359183C92.7643254051613,581.97838820517,107.2661462326859,598.0817764103399,114.51705664644818,606.1334705129249L121.76796706021048,614.1851646155098"></path><path marker-end="url(#flowchart-pointEnd)" style="fill:none;" class="edge-thickness-normal edge-pattern-solid flowchart-link LS-F LE-G" id="L-F-G-0" d="M125.02421023867932,668.1585800888378L118.49986384330862,677.5009003283446C111.97551744793789,686.8432205678515,98.92682465719649,705.5278610468653,92.40247826182578,721.0368479530388C85.87813186645508,736.5458348592123,85.87813186645508,748.8791681925455,85.87813186645508,755.0458348592123L85.87813186645508,761.2125015258789"></path><path marker-end="url(#flowchart-pointEnd)" style="fill:none;" class="edge-thickness-normal edge-pattern-solid flowchart-link LS-G LE-H" id="L-G-H-0" d="M85.87813186645508,800.2125015258789L85.87813186645508,804.3791681925455C85.87813186645508,808.5458348592123,85.87813186645508,816.8791681925455,91.32757005084319,825.2125015258789C96.77700823523132,833.5458348592123,107.67588460400755,841.8791681925455,113.12532278839568,846.0458348592123L118.5747609727838,850.2125015258789"></path><path marker-end="url(#flowchart-pointEnd)" style="fill:none;" class="edge-thickness-normal edge-pattern-solid flowchart-link LS-B LE-D" id="L-B-D-0" d="M163.1567389480086,158.85889272771158L169.8514502041714,168.0386606064263C176.54616146033422,177.21842848514106,189.93558397265977,195.57796424257052,196.63029522882258,214.1743987879519C203.32500648498535,232.77083333333334,203.32500648498535,251.60416666666666,203.32500648498535,268.4375C203.32500648498535,285.2708333333333,203.32500648498535,300.1041666666667,196.92009777511794,315.1570704250101C190.51518906525052,330.20997418335355,177.7053716455157,345.4824483667071,171.30046293564826,353.1186854583839L164.89555422578084,360.75492255006066"></path><path marker-end="url(#flowchart-pointEnd)" style="fill:none;" class="edge-thickness-normal edge-pattern-solid flowchart-link LS-D LE-F" id="L-D-F-0" d="M164.2929740259736,408.6601576497466L171.8931048172786,418.02929804145555C179.49323560858363,427.3984384331645,194.69349719119364,446.1367192165822,202.2936279824987,464.92252627495776C209.8937587738037,483.7083333333333,209.8937587738037,502.5416666666667,209.8937587738037,519.375C209.8937587738037,536.2083333333334,209.8937587738037,551.0416666666666,202.8095150267081,566.5100274359183C195.72527127961249,581.97838820517,181.5567837854213,598.0817764103399,174.47254003832572,606.1334705129249L167.3882962912301,614.1851646155098"></path><path marker-end="url(#flowchart-pointEnd)" style="fill:none;" class="edge-thickness-normal edge-pattern-solid flowchart-link LS-F LE-H" id="L-F-H-0" d="M164.13205311276133,668.1585800888378L170.48973284146533,677.5009003283446C176.84741257016935,686.8432205678515,189.56277202757735,705.5278610468653,195.92045175628132,724.2868479530388C202.27813148498535,743.0458348592123,202.27813148498535,761.8791681925455,202.27813148498535,778.7125015258789C202.27813148498535,795.5458348592123,202.27813148498535,810.3791681925455,196.82869330059725,821.9625015258789C191.37925511620912,833.5458348592123,180.48037874743287,841.8791681925455,175.03094056304477,846.0458348592123L169.58150237865664,850.2125015258789"></path></g><g class="edgeLabels"><g class="edgeLabel"><g transform="translate(0, 0)" class="label"><foreignObject height="0" width="0"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="edgeLabel"></span></div></foreignObject></g></g><g transform="translate(84.83125686645508, 213.9375)" class="edgeLabel"><g transform="translate(-15.612500190734863, -12)" class="label"><foreignObject height="24" width="31.225000381469727"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="edgeLabel">True</span></div></foreignObject></g></g><g class="edgeLabel"><g transform="translate(0, 0)" class="label"><foreignObject height="0" width="0"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="edgeLabel"></span></div></foreignObject></g></g><g transform="translate(78.26250457763672, 464.875)" class="edgeLabel"><g transform="translate(-15.612500190734863, -12)" class="label"><foreignObject height="24" width="31.225000381469727"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="edgeLabel">True</span></div></foreignObject></g></g><g class="edgeLabel"><g transform="translate(0, 0)" class="label"><foreignObject height="0" width="0"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="edgeLabel"></span></div></foreignObject></g></g><g transform="translate(85.87813186645508, 724.2125015258789)" class="edgeLabel"><g transform="translate(-15.612500190734863, -12)" class="label"><foreignObject height="24" width="31.225000381469727"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="edgeLabel">True</span></div></foreignObject></g></g><g class="edgeLabel"><g transform="translate(0, 0)" class="label"><foreignObject height="0" width="0"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="edgeLabel"></span></div></foreignObject></g></g><g transform="translate(203.32500648498535, 270.4375)" class="edgeLabel"><g transform="translate(-18.368749618530273, -12)" class="label"><foreignObject height="24" width="36.73749923706055"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="edgeLabel">False</span></div></foreignObject></g></g><g transform="translate(209.8937587738037, 521.375)" class="edgeLabel"><g transform="translate(-18.368749618530273, -12)" class="label"><foreignObject height="24" width="36.73749923706055"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="edgeLabel">False</span></div></foreignObject></g></g><g transform="translate(202.27813148498535, 780.7125015258789)" class="edgeLabel"><g transform="translate(-18.368749618530273, -12)" class="label"><foreignObject height="24" width="36.73749923706055"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="edgeLabel">False</span></div></foreignObject></g></g></g><g class="nodes"><g transform="translate(144.07813167572021, 19.5)" id="flowchart-A-40" class="node default flowchart-label"><rect height="39" width="58.54999923706055" y="-19.5" x="-29.274999618530273" ry="19.5" rx="19.5" style=""></rect><g transform="translate(-16.899999618530273, -12)" style="" class="label"><rect></rect><foreignObject height="24" width="33.79999923706055"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="nodeLabel">start</span></div></foreignObject></g></g><g transform="translate(144.07813167572021, 132.96875)" id="flowchart-B-41" class="node default flowchart-label"><polygon style="" transform="translate(-43.96875,43.96875)" class="label-container" points="43.96875,0 87.9375,-43.96875 43.96875,-87.9375 0,-43.96875"></polygon><g transform="translate(-16.96875, -12)" style="" class="label"><rect></rect><foreignObject height="24" width="33.9375"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="nodeLabel">x &lt; y</span></div></foreignObject></g></g><g transform="translate(84.83125686645508, 270.4375)" id="flowchart-C-43" class="node default flowchart-label"><rect height="39" width="130.25" y="-19.5" x="-65.125" ry="0" rx="0" style="" class="basic label-container"></rect><g transform="translate(-57.625, -12)" style="" class="label"><rect></rect><foreignObject height="24" width="115.25"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="nodeLabel">"x is less than y"</span></div></foreignObject></g></g><g transform="translate(144.07813167572021, 383.90625)" id="flowchart-D-45" class="node default flowchart-label"><polygon style="" transform="translate(-43.96875,43.96875)" class="label-container" points="43.96875,0 87.9375,-43.96875 43.96875,-87.9375 0,-43.96875"></polygon><g transform="translate(-16.96875, -12)" style="" class="label"><rect></rect><foreignObject height="24" width="33.9375"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="nodeLabel">x &gt; y</span></div></foreignObject></g></g><g transform="translate(78.26250457763672, 521.375)" id="flowchart-E-47" class="node default default flowchart-label"><rect height="39" width="156.52500915527344" y="-19.5" x="-78.26250457763672" ry="0" rx="0" style="" class="basic label-container"></rect><g transform="translate(-70.76250457763672, -12)" style="" class="label"><rect></rect><foreignObject height="24" width="141.52500915527344"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="nodeLabel">"x is greater than y"</span></div></foreignObject></g></g><g transform="translate(144.07813167572021, 639.0437507629395)" id="flowchart-F-49" class="node default default flowchart-label"><polygon style="" transform="translate(-48.16875076293945,48.16875076293945)" class="label-container" points="48.16875076293945,0 96.3375015258789,-48.16875076293945 48.16875076293945,-96.3375015258789 0,-48.16875076293945"></polygon><g transform="translate(-21.168750762939453, -12)" style="" class="label"><rect></rect><foreignObject height="24" width="42.337501525878906"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="nodeLabel">x == y</span></div></foreignObject></g></g><g transform="translate(85.87813186645508, 780.7125015258789)" id="flowchart-G-51" class="node default default flowchart-label"><rect height="39" width="126.0625" y="-19.5" x="-63.03125" ry="0" rx="0" style="" class="basic label-container"></rect><g transform="translate(-55.53125, -12)" style="" class="label"><rect></rect><foreignObject height="24" width="111.0625"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="nodeLabel">"x is equal to y"</span></div></foreignObject></g></g><g transform="translate(144.07813167572021, 869.7125015258789)" id="flowchart-H-53" class="node default default flowchart-label"><rect height="39" width="55.07500076293945" y="-19.5" x="-27.537500381469727" ry="19.5" rx="19.5" style=""></rect><g transform="translate(-15.162500381469727, -12)" style="" class="label"><rect></rect><foreignObject height="24" width="30.325000762939453"><div style="display: inline-block; white-space: nowrap;" xmlns="http://www.w3.org/1999/xhtml"><span class="nodeLabel">stop</span></div></foreignObject></g></g></g></g></g></svg>


True
False
True
False
start
x < y
"x is less than y"
x > y
"x is greater than y"
"x is equal to y"
stop
or
or allows your program to decide between one or more alternatives. For example, we could further edit our program as follows:

x = int(input("What's x? "))
y = int(input("What's y? "))

if x < y or x > y:
    print("x is not equal to y")
else:
    print("x is equal to y")
Notice that the result of our program is the same, but the complexity is decreased and the efficiency of our code is increased.

At this point, our code is pretty great. However, could the design be further improved? We could further edit our code as follows:

x = int(input("What's x? "))
y = int(input("What's y? "))

if x != y:
    print("x is not equal to y")
else:
    print("x is equal to y")
Notice how we removed the or entirely, and simply asked “is x not equal to y?” We ask one and only one question. Very efficient!

For the purpose of illustration, we could also change our code as follows:

x = int(input("What's x? "))
y = int(input("What's y? "))

if x == y:
    print("x is equal to y")
else:
    print("x is not equal to y")
Notice that the == operator evaluates if what is on the left and right are equal to one another. That use of double equal signs is very important. If you use only one equal sign, an error will likely be thrown by the compiler.

Our code can be illustrated as follows:

True
False
start
x == y
"x is equal to y"
"x is not equal to y"
stop
and
Similar to or, and can be used within conditional statements.
Execute in the terminal window code grade.py. Start your new program as follows:

score = int(input("Score: "))

if score >= 90 and score <= 100:
    print("Grade: A")
elif score >=80 and score < 90:
    print("Grade: B")
elif score >=70 and score < 80:
    print("Grade: C")
elif score >=60 and score < 70:
    print("Grade: D")
else:
    print("Grade: F")
Notice that executing python grade.py you will be able to input a score and get a grade. However, notice how there are potentials for bugs.

Typically, we do not want to ever trust our user to input the correct information. We could improve our code as follows:

  score = int(input("Score: "))

  if 90 <= score <= 100:
      print("Grade: A")
  elif 80 <= score < 90:
      print("Grade: B")
  elif 70 <= score < 80:
      print("Grade: C")
  elif 60 <= score < 70:
      print("Grade: D")
  else:
      print("Grade: F")
Notice how Python allows you to chain together the operators and conditions in a way quite uncommon to other programming languages.

Still, we can further improve our program:

score = int(input("Score: "))

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
elif score >= 60:
    print("Grade: D")
else:
    print("Grade: F")
Notice how the program is improved by asking fewer questions. This makes our program easier to read and far more maintainable in the future.

You can learn more in Python’s documentation on control flow.
Modulo
In mathematics, parity refers to whether a number is either even or odd.
The modulo % operator in programming allows one to see if two numbers divide evenly or divide and have a remainder.
For example, 4 % 2 would result in zero, because it evenly divides. However, 3 % 2 does not divide evenly and would result in a number other than zero!
In the terminal window, create a new program by typing code parity.py. In the text editor window, type your code as follows:

x = int(input("What's x? "))

if x % 2 == 0:
    print("Even")
else:
    print("Odd")
Notice how our users can type in any number 1 or greater to see if it is even or odd.

Creating Our Own Parity Function
As discussed in Lecture 0, you will find it useful to create a function of your own!
We can create our own function to check whether a number is even or odd. Adjust your code as follows:

def main():
    x = int(input("What's x? "))
    if is_even(x):
        print("Even")
    else:
        print("Odd")


def is_even(n):
    if n % 2 == 0:
        return True
    else:
        return False


main()
Notice that one reason our if statement is_even(x) works, even though there is no operator there. This is because our function returns a bool (or boolean), true or false, back to the main function. The if statement simply evaluates whether or not is_even of x is true or false.

Pythonic
In the programming world, there are types of programming that are called “Pythonic” in nature. That is, there are ways to program that are sometimes only seen in Python programming. Consider the following revision to our program:
def main():
    x = int(input("What's x? "))
    if is_even(x):
        print("Even")
    else:
        print("Odd")


def is_even(n):
    return True if n % 2 == 0 else False


main()
Notice that this return statement in our code is almost like a sentence in English. This is a unique way of coding only seen in Python.

We can further revise our code and make it more and more readable:

def main():
    x = int(input("What's x? "))
    if is_even(x):
        print("Even")
    else:
        print("Odd")


def is_even(n):
    return n % 2 == 0


main()
Notice that the program will evaluate what is happening within the n % 2 == 0 as either true or false and simply return that to the main function.

match
Similar to if, elif, and else statements, match statements can be used to conditionally run code that matches certain values.
Consider the following program:
  name = input("What's your name? ")

  if name == "Harry":
      print("Gryffindor")
  elif name == "Hermione":
      print("Gryffindor")
  elif name == "Ron": 
      print("Gryffindor")
  elif name == "Draco":
      print("Slytherin")
  else:
      print("Who?")
Notice the first three conditional statements print the same response.

We can improve this code slightly with the use of the or keyword:
  name = input("What's your name? ")

  if name == "Harry" or name == "Hermione" or name == "Ron": 
      print("Gryffindor")
  elif name == "Draco":
      print("Slytherin")
  else:
      print("Who?")
Notice the number of elif statements has decreased, improving the readability of our code.

Alternatively, we can use match statements to map names to houses. Consider the following code:
  name = input("What's your name? ")

  match name: 
      case "Harry":
          print("Gryffindor")
      case "Hermione":
          print("Gryffindor")
      case "Ron": 
          print("Gryffindor")
      case "Draco":
          print("Slytherin")
      case _:
          print("Who?")
Notice the use of the _ symbol in the last case. This will match with any input, resulting in similar behavior as an else statement.

A match statement compares the value following the match keyword with each of the values following the case keywords. In the event a match is found, the respective indented code section is executed and the program stops the matching.
We can improve the code:
  name = input("What's your name? ")

  match name: 
      case "Harry" | "Hermione" | "Ron":
          print("Gryffindor")
      case "Draco":
          print("Slytherin")
      case _:
          print("Who?")
Notice, the use of the single vertical bar |. Much like the or keyword, this allows us to check for multiple values in the same case statement.

Summing Up
You now have the power within Python to use conditional statements to ask questions and have your program take action accordingly. In this lecture, we discussed…

Conditionals;
if Statements;
Control flow, elif, and else;
or;
and;
Modulo;
Creating your own function;
Pythonic coding;
and match.