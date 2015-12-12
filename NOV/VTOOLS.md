
A SURVEY OF ARGUMENT VISUALISATION TOOLS
========================================

ABSTRACT
--------

Argument visualization tools are software visualization tools that, more often than not, illustrate a body of statements also known as arguments in an organized, hierarchy of graphs. This paper compares various analysis made for four common argument visualization tools – Beldevere, ConvinceMe, Reason!Able and Athena. The comparative analysis in this paper establishes a common basis for comparison and discovers unique metrics for comparing distinctive features of the various argument visualization tools explored.

## Introduction

The aim of this paper is to review the visualization tools that can be used i) for representation of temporal events in the form of time lines ii) for representing histories based on argumentation. Forensic reports of crime scenes are typically lengthy and contain large amount of complex information. In order to enhance readability the use of visualization tool is necessary.

Such tools could be based on logical rules for legal arguments. In recent years, there has been a large amount of research on the development of logical tools for legal argument (see, e.g., the work of Gordon (1993, 1995), Hage (1997), Lodder (1998), Prakken (1993, 1997) and Verheij (1996)). Argument forms that have been studied include arguments concerning exceptions to rules, conflicts of reasons and rule applicability. The logical tools that have recently been developed can be categorized under three headings: defeasibility, integration of logical levels, and the process character of argument (Verheij et al. 1997). Therefore it is necessary the development of tools based on those theories with the appropriate graphical user interface, in order to enable end users to visualize crime scenes reports.

Moreover, one can argue that after processing crime report using corpus linguistic tools (reference is needed here on those tools.), those reports could be organized into events and therefore could be visualized in the form of timelines. Such organisation of temporal events in time line could enhance spotting important information and focusing on particular points of a story.

## Materials

EventFlow LifeLines, LifeLines2, LifeFlow are visualization tools developed by the University of Maryland Human – Computer Interaction Lab.

Event sequence analysis is an important task in many domains: medical researchers study the patterns of transfers within the hospital for quality control; transportation experts study accident response logs to identify best practices. In most cases they deal with more than thousands of records. While previous research has focused on searching and browsing, overview tasks are often overlooked. LifeFlow scales to any number of records, summarizes all possible sequences, and highlights the temporal spacing of the events within sequences. Event flow is a simple and intuitive extended version of LifeFlow in order to support both interval – based and point based events. Some of the domains of application are cybersecurity, sport analytics, incident management etc. LifeLines2 , the newest version of LifeLines is an interactive visualization tool for temporal categorical data. It is a framework of simple operators to allow users to manipulate multiple records simultaneously to understand relative temporal relationships across records.  The three operators are Align, Rank, and Filter, and we affectionately call it the ARF framework.  Alignment forces every record to be aligned by a certain feature so the events that occur prior to and after the feature can be compared easily.  Rank and Filter are traditional operators analysts are familiar with, and they augment the Align offers.  In addition, analysts can use temporal summaries to view distribution of multiple event types over time.  Temporal summaries augment filter by allowing temporal constraints to be specified.  Temporal summaries also allow multiple groups of records to be compared.

The following section presents some tools developed for visualizing argumentations. This category includes tool such as CumulA, Argue!, ArgueMed and Araucaria. Those tools are interactive and are based on the argumentation theory for representing facts assumptions and counterattacking clauses taking from large texts which describe a history.



LITERATURE
-----------

Scientists, educationists, enterprises, to mention a few, are constantly looking for ways to improve human performance when it comes to making sense of facts, learning and retaining new knowledge. A step taken by researchers towards achieving effective analysis and retention of facts within a body text is through diagramming of concepts contained within the text. One of the commonly used methods is using mind maps which connects related concepts of a domain in an undirected graph (Anderson, 1993). The major advantage of mind map is the inherent hierarchical structure through which it provides a means to correlate concepts within the domain for which it is created and provides a summarized overview of the target domain or subject.

Researchers have taken this concept a step further not only by automating the diagramming process but in addition they are developing software to be part of the diagram formation decision-making process by determining what statements or arguments are relevant concepts to the diagram and also creating new concepts in order to further classify them. van den Braak, Oostendorp, Prakken, & Vreeswijk (2008) describe argument visualization tools as software that support the construction of arguments in various visualization formats such as tables and graphs. Their work took a critical evaluation of the various efforts of software designers towards building automatic argument visualization tools. Here, not only do they evaluate the software but also the experimentation methods used to evaluate the software in order to validate them.

In their analyses, van den Braak et al. (2008) use validity and reliability metrics as the basis to scrutinize the visualization tools, their experiments as well as their results. They define internal validity to be the extent to which the dependent and independent variables interact without external influence and external validity as extent to which results of the experiment are able to scale to real world beyond the samples of subjects included in the experiments. In addition, the reliability of their results were also scrutinized. van den Braak et al. (2008) points that “validity implies reliability but not the the other way around” as such, the concept being measured is accurately measured where validity is concerned, on the other hand, reliability is concerned with the accuracy of the measurement method.

However, van den Braak et al. (2008) analyses were limited by unique features of each software visualization tool. The fact that each of these argument visualization tools can be observed from different design goals and perspectives make them challenging for comparison. Harrell (2005) develops a set of criteria which he establishes as a basis for comparison for the various argument visualization tools. The criteria comprised two classifications. The first classification involved the meta-cognitive process of the argument including how premises, propositions and supporting statements are represented. The second classification leaned towards the user experience of the visualization application. The emphasis for this classification was on the fluidity of the visualization. This includes moveability of the visual elements and the elasticity of the textual elements to resize and contain/wrap text.

This paper takes a middle ground to establish a general basis of comparison from a software design perspective whilst trying to connect with the unique features of each argument visualization tools logical design. In particular, for each visualization tool examined, we will first of all examine the software’s user interface from the perspective of the user and usability metrics, which is a general metric for all visualization tools. Then specifically, we will use software verification and validation(ref) to probe into the particular logical design goals of the unique features of each of the argument visualisation tools.

## Timeline visualization tools

## EventFlow

Monroe M, et al. (2012) presented EventFlow which is an interactive visual query tool with the task of finding interesting and important event sequences. Although the tool can be used in any kind of data the models was tested against medical data. The tool can be used on point-based events and on interval-based events. It can be used in multiple records and it can display the records either as individual display or as aggregated display. The development of the EventFlow was based on three major spheres: temporal logic, temporal querying and temporal visualization. This tool provides to the user the following tools to manipulate the display of the events. The aim of those mechanisms is to help the user to reduce the volume of the information displayed on the screen and thus make it easier for the user to understand the data. Those mechanisms are:

-   Interval Opacity: in some cases the sequences of event points may be more important than the duration of the interval events. In these instances the bright colour of the interval background may serve as distraction. To reduce this complexity users are able to control opacity.

-   Highlighting: as datasets become more complex it becomes more difficult to identify and thus analyse single features, particularly the interplay between intervals. To account for this EventFlow gives the user the ability to highlight areas.

-   Interval event merging: EventFlow provides a simple interface that allows for multiple interval events of the same category to be merged into a single event either by eliminating gaps or by eliminating overlaps between events.

-   Temporal Range Limits: EventFlow allows for spatial zooming into any region of the display. This feature only provides further insight into the aggregated display.

To sum up, the main contributions of EventFlow are:

-   A visual representation of interval events for both individual and aggregated displays.

-   A set of controls for simplifying and exploring records containing interval events.

-   A simple visual query language for professionals in nontechnical fields that allows users to specify the presence or absence of both point and interval events

## LifeLines and LifeLines2

LifeLines (Plaisant C., et al., 1996) provide a general visualization environment for personal histories that can be applied to medical and court records, professional histories and other types of biographical data. A one screen overview shows multiple facets of the records. Aspects, for example medical conditions or legal cases, are displayed as individual time lines, while icons indicate discrete events, such as physician consultations or legal reviews. Line colour and thickness illustrate relationships or significance, rescaling tools and filters allow users to focus on part of the information. LifeLines reduce the chances of missing information, facilitate spotting anomalies and trends, streamline access to details, while remaining tailorable and easily transferable between applications. The properties of this tool can be summarized as follows:

-   Aspects are displayed as individual time lines.

-   Icons indicate discrete events.

-   Line colour and thickness illustrate relationships or significance.

-   Rescale tools and filters allow focusing on part of the information.

-   The general visualization environment is not computationally demanding.

-   Requires only high level data descriptions.

-   Dynamic highlighting unveils relationships between events.

The LifeLines can be used for point-based events and interval-based events, it can use one record each time and is uses an individual record display.

LifeLines can:

1 - Reduce the chances of missing information. Because the data entry is performed over a long period of time by different people the LifeLines overview assists users in reviewing a disparate record. Yet unseen, or recently added and updated information can be revealed by highlighting.

2 - Facilitate the spotting of anomalies and trends. Intervals are easier to estimate on a timeline than in a table of dates. Repetitions of series of events result in visible patterns.

3 - Streamline the access to details. LifeLines act as large menus from which large numbers of detail screens can be accessed in a single step

4 - Remain simple and tailorable to various applications. The long term success of any record format depends on its sharability among collaborating services. LifeLines only uses high level data that can act as reference pointers to other services records.

Lifelines2 is an extension of Lifelines. Lifelines was designed to summarize the entirety of a single personal history record (e.g. a medical record). In contrast, Lifelines2 displays selected subsets of the records. The output of a query (e.g. Find all patients and Partners Health Care [14]. Each record is vertically stacked on alternating background colour and identified by its ID on the left. For example in the case of the above query in medical records, Asthma and pneumonia diagnosis events appear as coloured triangle icons on the timeline. By default all records are presented using the same absolute time scale (with the corresponding years or month labels displayed at the top) and the display is fitted so that the entire date range fits in the screen. As in Lifelines, zooming on the horizontal axis and panning is possible. Tool tips provide details, and records can be closed (one by one or all at a time) into a compact silhouette using smaller icons and less space. Left click onto the visualization centres and zooms in. Right click zooms out. Any click onto the record ID area resets the display to the initial fitted overview. On the right side a control panel provides access to align, rank, and filter the display. Menus are data-driven. A user can choose any event category to align all the records.

The records are listed in alphabetical order by default but users can rank records by the number of occurrences of an event category. The records can be ranked by the number of events, bringing to the top the more severe cases. Users can also filter by the number of occurrences of events (e.g. removing records that contain only one pneumonia event). Users can also filter out records that do not contain a specified sequence of events (e.g. asthma followed by pneumonia). Finally the legend area can also be used to turn on and off certain types of events from the display to focus on a subset of event types. With alignment the developers of this tool believe that Lifelines2 provides a simple yet effective mean of quickly exploring the data to look for potential temporal patterns across multiple records. When aligned, relative time spans can be compared easily, and one single zoom allows users to see the details around all sentinel events in view simultaneously. Overall the need to zoom and pan is greatly reduced, as is the need to keep in memory the scale of time ranges from record to record being compared. Ranking and filtering complement alignment by reordering or narrowing the set of records interactively to suit a user’s changing focus.

Compared to LifeLines, LifeLines2 can used on point – based event but it can be used on many records.

## LifeFlow

LifeFlow (Wongsuphasawat, K. et al., 2011) developed for the event sequence analysis. LifeFlow is scalable, can summarize all possible sequences, and represents the temporal spacing of the events within sequences. LifeFlow can summarize not only all possible sequences but also the temporal spacing of the events within sequences. The properties of LifeFlow are:

-   interactive visual overview of event sequences

-   It is scalable to any number of records

-   It summarizes all possible sequences

-   It represents the temporal spacing of the events within sequences

-   Human Activities, Electronic Health records, Traffic Incident Logs, Usability Study Logs, Web Logs and more

-   LifeFlow allows users to see not only all possible sequences but also their prevalence

-   It summarizes information about the time gap between events

-   Easy to use after a 15 minutes of training

-   Raw data are displayed on horizontal timeline

-   Coloured triangles represent events

-   Each row represents a record

LifeFLow is implemented in Java SE 6.0 and includes the following interaction features to support exploration:

-   Zooming – The horizontal zoom changes time granularity while the vertical zoom allows the users to see rare sequences in more detail.

-   Tooltip – When users move the mouse cursor over an event bar a tooltip displays the full sequence of events, and some statistical information, such as mean time between events, standard deviation, etc.

-   Overlay distribution of gap between events – Hovering the cursor over a bar displays the distribution of time gaps overlaid on the Lifeflow.

-   Sort – Users can sort the sequences with the same parent in different ways: by the number of records that the bars represent (tallest bar on top) or by the average time to previous event (shortest time on top). The default is to sort by number of records.

-   Integration with LifeLines2 – LifeFlow can function as a standalone tool but combining with LifeLines2 facilitates exploration by allowing users to review individual records as details on demand. By clicking on any event bar, users select all records that are included in that bar. Selected records are highlighted in the LifeLines2 view. Users can then choose to keep only the selection and remove everything else, or vice versa. In a symmetrical fashion, selecting a record in the LifeLines2 view highlights the pattern contained in that record in the LifeFlow view, allowing the users to find other records that contain the same sequence.

-   Align – Inspired by LifeLines2, LifeFlow allows users to choose any event type to be the alignment point. This supports tasks such as “what happened to the patients before and after they went to the ICU?” By default, the alignment point is not specified, so all records are aligned by the first event in the record. When users chose an alignment event, two trees of sequences are built: one tree for the sequences before the alignment (from right to left) and another tree for the sequences after the alignment (from left to right).

-   Including non-temporal attributes – Records usually also contain non-temporal attributes, e.g., patient’s gender. While LifeFlow does not focus on displaying those attributes, it allows users to select a non-temporal attribute and groups records by that attribute before the sequences are aggregated.

-   Include/Exclude event types – Using the legend on the left side of the screen users can check or uncheck event types to include or exclude them from the sequences. This simple functionality allows powerful transformations of the display to answer questions.

-   Displaying all event bars with equal height – When data includes a large number of sequences, it could be difficult to review the rare sequences because they are represented with very thin bars. This option displays all leaf nodes using equal height regardless of the number of records, makes it easier to review and select rare sequences.

LifeFlow concerns event-based points, for many records and offers the options of individual record display and the aggregated records display

BELVEDERE
---------

![](http://selene.hud.ac.uk/u1273400/images/vtools_media/image1.png)

Belvedere argument visualization tool is designed specifically to enhance argumentation skills in the science domain. It therefore sets-up arguments for and against hypotheses (Suthers, Weiner, Connelly, & Paolucci, 1995). In terms of internal validity, van den Braak et al. (2008) gave Belvedere a pass mark and summarizes its features as a tool for scientific argument skill enhancement and a collaborative tool that stimulates discussions amongst users. Suthers et al.(1995) identified difficulties students have when discussing and discovering new concepts. It is these difficulties that they assert Beldevere addresses. These difficulties include recognizing abstract relationship between arguments, keeping track of relevant elements of a complex debate, criteria for scientific argumentation, limited domain knowledge and lack of intrinsic motivation. Design goals of Beldevere to solve this problem include using a repository of diagram objects to represent concrete concepts. An advisor is used to keep students on track without deviating from the focus of the discussion. Beldevere provides scientific argumentation criteria by prompting students to support their arguments with empirical evidence statements. A database of common knowledge areas in science is also accessible to the students and customizable by administrators. Finally, by providing concurrent, multi-user access, participants can collaborate on the same topic, thus mental stimulation and motivation is provided by the diagramming solution Beldevere provides.

User interface goals of Beldevere include keeping the user focused on cognitive effort rather than on learning to use the program. Colors can be used to distinguish various view points such as different theories of different users. A free hand drawing tool is provided and labels are used for both links and objects. Graphical shapes have the ability to resize themselves to fit their contents in addition, when a graphical object is moved, its links are retained in order to maintain the logical connection.

Though internally valid, Beldevere strength was also its weakness. The flexibility of Beldevere made it prone to inconsistency of the use of its objects and links. For instance a student can use different objects on the same concept and could therefore easily lose track of the objects true relationship.

CONVICE ME
----------

![](http://selene.hud.ac.uk/u1273400/images/vtools_media/image2.png)

Convince Me is an open source, free java application.  It is used as a visualisation tool that operates by providing a metric on the credibility of inferences drawn by the users based on the arguments the users provide. In addition to generating visualization of arguments, it also assists the user to analyze the arguments. With the Convince Me tool, nodes represent either evidence or hypothesis. The concept behind of the Convince me tool is based on Thagard’s Explanatory Coherence theory (Thagard, 1997). This connectionist model, also called ECHO, can provide argument coherence feedback to the user on arguments proposed.  The overall goals of the model is to 
- categorize the proposed arguments as either evidence or hypothesis
- measure the reliability and believability of proposed evidence
- connect arguments with explanatory arguments to support or contradict propositions

The term echo is derived from the fact that after each of the above goals-cycles, feedback is provided by the applications to provide coherence of the arguments. Schank & Ranney (1995) assert that that Convince Me attempts to help users reconcile data against theory which tends to be vague even for professional scientific reasoning experts and therefore *lends a sophistication to novices' discriminative criteria across contexts, making their epistemic categorizations more expert-like both during, and after, its use*.  Further, Schank & Ranney(1995) attributes to Convince Me a measure of utility that enables its user derive the coherency of their arguments by scoring a correlation between the believability of a user to his own propositions and that of the program using the ECHO algorithm.

Convince Me is a user-friendly tool that uses casual networks and simple nodes designed generally to foster scientific reasoning. Explanatory and contradictory relations are represented by solid or dashed links between the nodes. Convince Me gains its strength from not only the analysis of the users arguments but also by generating new arguments to stimulate reasoning.




## REASON!ABLE

Reason!Able is a visualization tool that facilitates the reasoning skills of the user by constructing a mapping tree that guides the user to map arguments to specific attributes (Van Gelder, 2002).

![](http://selene.hud.ac.uk/u1273400/images/vtools_media/image3.png)

Argument tree nodes in Reason!Able consists of claims, reasons and objections. Reason’s and objectives can give rise to new premises.

ATHENA
------

Athena standard is commended by Harrell (2005) for its versatility when it comes down to argument construction. In terms of its user interface and usability, Athena standard creates argument diagrams by representing arguments found within philosophical texts (Harrell, 2005). With Athena, the user can draw boxes and texts separately and move them around. After linking boxes with lines, the boxes can be further moved about on the screen by dragging and the connected lines will remain intact. The connecting lines can also indicate support or objection by changing the color from default (support) to red (objection). In addition he boxes can also exhibit other attributes to indicate the strength of the argument.

![](http://selene.hud.ac.uk/u1273400/images/vtools_media/image4.png)



## Visualization tools for stories

Verheij (2003) discussed artificial arguments assistants for defeasible argumentation. He presented two systems ARGUE! based on CUMULA and ARGUMED based on DEFLOG. Argument assistance systems can serve in a context of more than one user: such argument mediation systems can be used to keep track of diverging positions and assist in the evaluation of opinions. More specifically, argument assistance systems are aids to drafting and generating arguments by :

-   administering and supervising the argument process,

-   keeping track of the issues that are raised and the assumptions that are made

-   keeping track of the reasons that have been adduced for and against a conclusion,

-   evaluating the justification status of the statements made,

-   checking whether the users of the system obey the pertaining rules of argument.

## CUMULA

CUMULA (Verheij, 1996) is a procedural model of argumentation with arguments and counterarguments. . It is based on two main assumptions. The first assumption is that argumentation is a process during which arguments are constructed and counterarguments are adduced. The second assumption is that the arguments used in argumentation are defeasible, in the sense that whether they justify their conclusion depends on the counterarguments available at a stage of the argumentation process. If an argument no longer justifies its conclusion it is said to be defeated. The defeat of an argument is caused by a counterargument (that is itself undefeated).

Arguments are assigned a defeat status, either undefeated or defeated. The defeat status of an argument depends on three factors:

-   the structure of the argument;

-   the attacks by counterarguments;

-   the argumentation stage.

To summarize, CUMULA shows:

1.  how the subordination and coordination of arguments is related to argument defeat.

2.  how the defeat of arguments can be described in terms of their structure, counterarguments, and the stage of the argumentation process, and independent of the logical language.

3.  how both inference and justification can be formalized in one model.

## Argue!

The Argue!-system (Verheij, B., 1998a) is a system for computer-mediated defeasible argumentation with a graphical user interface. Central actions of defeasible argumentation are inference, justification and attack. Argumentation starts with making a statement .statements can be if two types: assumption and issues. The Argue!-system is an evaluative system for argument mediation: the user provides the argumentation data such as assumptions, issues, reasons, and attacks. The system determines the justification status of statements i.e., whether they are justified, unjustified, or neither. When the user enters new argumentation data, statements obtain their initial value: assumptions are initially justified, issues are initially neither justified nor unjustified. Justified statements are shown in white boxes, unjustified statements in crossed white boxes, statements that are neither justified nor unjustified in grey boxes. The Argue!-system has two built-in algorithms that help determining the justification status of arguments: ‘evaluate’ and ‘jump’. The system evaluates the statements when the user clicks the ‘Evaluate’-button. The system evaluates statements in rounds: the justification statuses of statements are used as input for computing their status in the next. The Argue!-system has the following two evaluation rules:

-   If a statement is an assumption, it is justified.

-   If a statement is an issue, and has justified support, it is justified.

The second central action of defeasible argumentation is justification. When a new issue is raised it can be justified by giving support for it in the form of an assumption. The third central action of defeasible argumentation is attack. The user has added a defeater, visualized by a special visual shape that consists of two connected rectangles. The argument configuration contained in the first rectangle is challenging the argument configuration in the second is challenged. The defeater represents that the new issue is a counterargument.

Reinstatement is typical for defeasible argumentation. An argument is said to be reinstated if it becomes undefeated after being undefeated.

## ARGUMED

The ArguMed-system is an example of a system for computer0mediated defeasible argumentations. The argumentation theory of the ArguMed-system is an adaption of CumulA-model, a procedural model of argumentation with arguments and counterarguments.

The ArguMed-system has been designed in an attempt to enhance the familiarity of the interface and the transparency of the underlying argumentation theory of its precursor, the Argue!-system. The ArguMed-system’s user interface is template-based, as is currently common in window-style user interfaces. The user gradually constructs arguments, by filling in templates that correspond to common argument patterns. An innovation of the ArguMed-system is that it uses dedicated templates for different types of argument moves. Whereas existing mediation systems are issue-based), the ArguMed-system allows free argumentation, as in the CumulA-model. In contrast with the CumulA-model, which has a very general notion of defeat, defeat in the ArguMed-system is only of Pollock’s undercutter-type. The system allows three types of argument moves, viz. making a statement, adding a reason and its conclusion, and providing an (undercutter-type) exception blocking the connection between a reason and a conclusion.

ARGUMED (Verheij, 1998b) is the evolution of the ARGUE!. Instead of using forms to enter argumentative data, the user can interact though the screen with the program. With respect to the argumentation theory, attack is no longer limited to undercutting exceptions, but it is possible to attack any statement. Moreover the arrows used to represent support or attack, are considered as conditional statements, which allow a natural treatment of warrants and undercutters. The dialectical arguments consist of statements that can have two types of connections between them: a statement can support another, or a statement can attack another. The former is indicated by a pointed arrow between statements, the latter by an arrow ending in a cross.

In general, dialectical arguments are finite structures that result from a finite number of applications of three kinds of construction types:

1.  Making a statement.

2.  Supporting a previously made statement by a reason for it.

3.  Attacking a previously made statement by a reason against it.

The evaluation of dialectical arguments with respect to a set of prima facie justified assumptions is naturally constrained as follows:

1.  A statement is justified if and only if (a) it is an assumption, against which there is no defeating reason, or (b) it is an issue, for which there is a justifying reason. A statement is defeated if and only if there is a defeating reason against it.

2.  A reason is justifying if and only if the reason and the conditional underlying the corresponding supporting argument step are justified.

3.  A reason is defeating if and only if the reason and the conditional underlying the corresponding attacking argument step are justified.

## Araucaria

Reed and Rowe (2004) presented a software which aimed to help the diagramming process of argumentation analysis, the Araucaria.

The Araucaria system provides an interface which supports the diagramming process, and then saves the result using AML, an open standard, designed in XML, for describing argument structure. Araucaria aims to be of use not only in pedagogical situations, but also in support of research activity. As a result, it has been designed from the outset to handle more advanced argumentation theoretic concepts such as schemes, which capture stereotypical patterns of reasoning. The software is also designed to be compatible with a number of applications, including dialogic interaction and online corpus provision. The assumptions behind Araucaria follow the same pattern: a single text might be analysed in several different ways, depending upon a variety of analytical choices. The judgements concerning the delimitation of argument components can vary, depending upon the aims of the analyst and the clarity of the text itself.

The Araucaria program can be split into three main sections:

• The main window which allows argument diagrams to be constructed from pre-existing text files.

• An editor for schemes and scheme sets.

• An interface to the Araucaria DB online repository of marked up arguments.

When Araucaria loads, the program displays its main window which can be used to load text files and create argument diagrams from the text. When a text file is loaded, the text appears in the left-hand panel. A portion of this text may be selected with the mouse. If the mouse is then clicked in the large panel on the right, a node corresponding to that portion of the text is created and drawn at the bottom of the panel. When two or more nodes have been defined in this way, they can be connected in pairs by selecting one node with the mouse and dragging the mouse to the other node. The first node selected is the premise of an argument, and the second node is the conclusion.

Araucaria supports labels on diagrams that relate to two further aspects of argument: ownership and evaluation. Each premise or conclusion can be associated with one or more owners. An owner can be defined in the ownership editor dialog. Each owner has a three-letter acronym associated with it, which is used to label a node on the main argument diagram. Each node and support arrow in a diagram can also have an associated evaluation, which can be used to represent the confidence placed in a premise or support. To attach an evaluation to one or more parts of the diagram, the nodes and/or support arrows are selected and the evaluation editor is used to define the associated evaluation. Evaluations are displayed as labels next to the node or arrow on the main diagram.

Araucaria allows the user to define argumentation schemes and to group them together into schemesets. The scheme editor allows a scheme to be defined by specifying its name, conclusion, premises and critical questions. A schemeset containing a number of schemes can then be saved in a schemeset file.

Araucaria employs a tree structure for mapping out the relationships between components in an argument, and allows the user to manipulate that structure.


EVALUATION
----------

The designers of software argument visualization tools purport that visualization tools improve reasoning and these claims are not without some logical proof. When compared to textual data, the visualization tools have structure and perform to some extend a level of summarization that would have been cumbersome and time consuming for a human to do. However, the accuracy of the visualization output needs further exploration. In other words, what the argument visualization tools lack are proper metrics to bench mark their performance in relation to their purpose and in relation to each other.

CONCLUSION
----------

Software visualization tools perform a worthy cause in assisting the user to better understand better the information they are attempting to process. Software argument visualization tools attempts to make their users better reasoners. These can perform feats of faster information processing however, the accuracy and relevance of the processed information requires appropriate software verification and validation tools are used to appraise the software’s ability to improve the user’s reasoning.

REFERENCES
==========

Anderson, J. V. (1993). Mind mapping: A tool for creative thinking. *Business Horizons*, *36*(1), 41–46. http://doi.org/10.1016/S0007-6813(05)80102-8

Harrell, M. (2005). Using argument diagramming software in the classroom. *Teaching Philosophy*, *28*(2), 163–177.

Schank, P., & Ranney, M. (1995, May). Improved reasoning with Convince Me. In Conference companion on Human factors in computing systems (pp. 276-277). ACM.

Suthers, D., Weiner, A., Connelly, J., & Paolucci, M. (1995). Belvedere: Engaging students in critical discussion of science and public policy issues. In *Proceedings of the 7th World Conference on Artificial Intelligence in Education* (pp. 266–273). Washington, DC. Retrieved from http://lilt.ics.hawaii.edu/papers/1995/suthers-et-al-aied95.pdf

Thagard, P. (1997). Probabilistic Networks and Explanatory Coherence. *Automated Abduction: Inference to the Best Explanation*.

van den Braak, S. W., Oostendorp, H. van, Prakken, H., & Vreeswijk, G. A. (2008). A critical review of argument visualization tools: Do users become better reasoners? In *Workshop Notes of the ECAI-06 Workshop on Computational Models of Natural Argument* (pp. 67–75).

Van Gelder, T. (2002). Argument mapping with reason! able. *The American Philosophical Association Newsletter on Philosophy and Computers*, *2*(1), 85–90.

Gordon, T.F.,1993. The Pleadings Game. An Artificial Intelligence Model of Procedural Justice, dissertation.

Gordon, T.F.,1995. The Pleadings Game. An Artificial Intelligence Model of Procedural Justice, Dordrecht: Kluwer Academic Publishers 1995.

Hage, J., 1996. A Theory of Legal Reasoning and a Logic to Match, Artificial Intelligence and Law, Vol. 4,, pp. 199-273.

Lodder, A.R., 1998. DiaLaw – on legal justification and dialog games, dissertation, Universiteit Maastricht.

Plaisant, Catherine, Brett Milash, Anne Rose, Seth Widof, and Ben Shneiderman. “LifeLines : Visualizing Personal Histories.” CHI-96, 1996, 221–27.

Prakken, H., 1993. Logical tools for modelling legal argument, doctoral thesis, Amsterdam: Vrije Universiteit.

Prakken, H., 1997. Logical Tools for Modelling Legal Argument. A Study of Defeasible Reasoning in Law, Dordrecht: Kluwer Academic Publishers 1997.

Reed, C.A., and Rowe, G.W.A, 2004. Araucaria: Software for argument analysis, diagramming and representation. International Journal of Artificial Intelligence Tools,14, 961-980.

Vergeij, B., 2003. Artificial argument assistants for defeasible argumentation. Artificial Intelligence, 150, 291-324.

Verheij, B., 1996. Rules, reasons, arguments. Formal studies of argumentation and defeat, Dissertation, Universiteit Maastricht.

Verheij, B., 1998a. ARGUE!—An implemented system for computer-mediated defeasible argumentation, in: H. La Poutré, J. van den Herik (Eds.), NAIC’98. Proceedings of the Tenth Netherlands/Belgium Conference on Artificial Intelligence, CWI, Amsterdam.

Verheij, B., 1998b. ARGUMED—A template-based argument mediation system for lawyers, in: J.C. Hage, T.J.M. Bench-Capon, A.W. Koers, C.N.J. de Vey Mestdagh, C.A.F.M. Grütters (Eds.), Legal Knowledge Based Systems. JURIX: The Eleventh Conference, Gerard Noodt Instituut, Nijmegen.

Wongsuphasawat, Krist, John Gomez, Catherine Plaisant, Taowei Wang, Ben Shneiderman, and Meirav Taieb-Maimon. “LifeFlow: Visualizing an Overview of Event Sequences.” CHI-2011, n.d., 1747–56.

Gordon, T.F.,1993. The Pleadings Game. An Artificial Intelligence Model of Procedural Justice, dissertation.

Gordon, T.F.,1995. The Pleadings Game. An Artificial Intelligence Model of Procedural Justice, Dordrecht: Kluwer Academic Publishers 1995.

Hage, J., 1996. A Theory of Legal Reasoning and a Logic to Match, Artificial Intelligence and Law, Vol. 4,, pp. 199-273.

Lodder, A.R., 1998. DiaLaw – on legal justification and dialog games, dissertation, Universiteit Maastricht.

Plaisant, Catherine, Brett Milash, Anne Rose, Seth Widof, and Ben Shneiderman. “LifeLines : Visualizing Personal Histories.” CHI-96, 1996, 221–27.

Prakken, H., 1993. Logical tools for modelling legal argument, doctoral thesis, Amsterdam: Vrije Universiteit.

Prakken, H., 1997. Logical Tools for Modelling Legal Argument. A Study of Defeasible Reasoning in Law, Dordrecht: Kluwer Academic Publishers 1997.

Reed, C.A., and Rowe, G.W.A, 2004. Araucaria: Software for argument analysis, diagramming and representation. International Journal of Artificial Intelligence Tools,14, 961-980.

Vergeij, B., 2003. Artificial argument assistants for defeasible argumentation. Artificial Intelligence, 150, 291-324.

Verheij, B., 1996. Rules, reasons, arguments. Formal studies of argumentation and defeat, Dissertation, Universiteit Maastricht.

Verheij, B., 1998a. ARGUE!—An implemented system for computer-mediated defeasible argumentation, in: H. La Poutré, J. van den Herik (Eds.), NAIC’98. Proceedings of the Tenth Netherlands/Belgium Conference on Artificial Intelligence, CWI, Amsterdam.

Verheij, B., 1998b. ARGUMED—A template-based argument mediation system for lawyers, in: J.C. Hage, T.J.M. Bench-Capon, A.W. Koers, C.N.J. de Vey Mestdagh, C.A.F.M. Grütters (Eds.), Legal Knowledge Based Systems. JURIX: The Eleventh Conference, Gerard Noodt Instituut, Nijmegen.

Wongsuphasawat, Krist, John Gomez, Catherine Plaisant, Taowei Wang, Ben Shneiderman, and Meirav Taieb-Maimon. “LifeFlow: Visualizing an Overview of Event Sequences.” CHI-2011, n.d., 1747–56.

