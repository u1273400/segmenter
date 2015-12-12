**Introduction**

The aim of this paper is to review the visualization tools that can be used i) for representation of temporal events in the form of time lines ii) for representing histories based on argumentation. Forensic reports of crime scenes are typically lengthy and contain large amount of complex information. In order to enhance readability the use of visualization tool is necessary.

Such tools could be based on logical rules for legal arguments. In recent years, there has been a large amount of research on the development of logical tools for legal argument (see, e.g., the work of Gordon (1993, 1995), Hage (1997), Lodder (1998), Prakken (1993, 1997) and Verheij (1996)). Argument forms that have been studied include arguments concerning exceptions to rules, conflicts of reasons and rule applicability. The logical tools that have recently been developed can be categorized under three headings: defeasibility, integration of logical levels, and the process character of argument (Verheij et al. 1997). Therefore it is necessary the development of tools based on those theories with the appropriate graphical user interface, in order to enable end users to visualize crime scenes reports.

Moreover, one can argue that after processing crime report using corpus linguistic tools (reference is needed here on those tools.), those reports could be organized into events and therefore could be visualized in the form of timelines. Such organisation of temporal events in time line could enhance spotting important information and focusing on particular points of a story.

**Materials **

EventFlow LifeLines, LifeLines2, LifeFlow are visualization tools developed by the University of Maryland Human – Computer Interaction Lab.

Event sequence analysis is an important task in many domains: medical researchers study the patterns of transfers within the hospital for quality control; transportation experts study accident response logs to identify best practices. In most cases they deal with more than thousands of records. While previous research has focused on searching and browsing, overview tasks are often overlooked. LifeFlow scales to any number of records, summarizes all possible sequences, and highlights the temporal spacing of the events within sequences. Event flow is a simple and intuitive extended version of LifeFlow in order to support both interval – based and point based events. Some of the domains of application are cybersecurity, sport analytics, incident management etc. LifeLines2 , the newest version of LifeLines is an interactive visualization tool for temporal categorical data. It is a framework of simple operators to allow users to manipulate multiple records simultaneously to understand relative temporal relationships across records.  The three operators are Align, Rank, and Filter, and we affectionately call it the ARF framework.  Alignment forces every record to be aligned by a certain feature so the events that occur prior to and after the feature can be compared easily.  Rank and Filter are traditional operators analysts are familiar with, and they augment the Align offers.  In addition, analysts can use temporal summaries to view distribution of multiple event types over time.  Temporal summaries augment filter by allowing temporal constraints to be specified.  Temporal summaries also allow multiple groups of records to be compared.

The following section presents some tools developed for visualizing argumentations. This category includes tool such as CumulA, Argue!, ArgueMed and Araucaria. Those tools are interactive and are based on the argumentation theory for representing facts assumptions and counterattacking clauses taking from large texts which describe a history.

***Timeline visualization tools***

***EventFlow***

Monroe M, et al. (2012) presented EventFlow which is an interactive visual query tool with the task of finding interesting and important event sequences. Although the tool can be used in any kind of data the models was tested against medical data. The tool can be used on point-based events and on interval-based events. It can be used in multiple records and it can display the records either as individual display or as aggregated display. The development of the EventFlow was based on three major spheres: temporal logic, temporal querying and temporal visualization. This tool provides to the user the following tools to manipulate the display of the events. The aim of those mechanisms is to help the user to reduce the volume of the information displayed on the screen and thus make it easier for the user to understand the data. Those mechanisms are:

-   Interval Opacity: in some cases the sequences of event points may be more important than the duration of the interval events. In these instances the bright colour of the interval background may serve as distraction. To reduce this complexity users are able to control opacity.

-   Highlighting: as datasets become more complex it becomes more difficult to identify and thus analyse single features, particularly the interplay between intervals. To account for this EventFlow gives the user the ability to highlight areas.

-   Interval event merging: EventFlow provides a simple interface that allows for multiple interval events of the same category to be merged into a single event either by eliminating gaps or by eliminating overlaps between events.

-   Temporal Range Limits: EventFlow allows for spatial zooming into any region of the display. This feature only provides further insight into the aggregated display.

To sum up, the main contributions of EventFlow are:

-   A visual representation of interval events for both individual and aggregated displays.

-   A set of controls for simplifying and exploring records containing interval events.

-   A simple visual query language for professionals in nontechnical fields that allows users to specify the presence or absence of both point and interval events

***LifeLines and LifeLines2***

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

Lifelines2 is an extension of Lifelines. Lifelines was designed to summarize the entirety of a single personal history record (e.g. a medical record). In contrast, Lifelines2 displays selected subsets of the records. The output of a query (e.g. Find all patients and Partners Health Care \[14\]. Each record is vertically stacked on alternating background colour and identified by its ID on the left. For example in the case of the above query in medical records, Asthma and pneumonia diagnosis events appear as coloured triangle icons on the timeline. By default all records are presented using the same absolute time scale (with the corresponding years or month labels displayed at the top) and the display is fitted so that the entire date range fits in the screen. As in Lifelines, zooming on the horizontal axis and panning is possible. Tool tips provide details, and records can be closed (one by one or all at a time) into a compact silhouette using smaller icons and less space. Left click onto the visualization centres and zooms in. Right click zooms out. Any click onto the record ID area resets the display to the initial fitted overview. On the right side a control panel provides access to align, rank, and filter the display. Menus are data-driven. A user can choose any event category to align all the records.

The records are listed in alphabetical order by default but users can rank records by the number of occurrences of an event category. The records can be ranked by the number of events, bringing to the top the more severe cases. Users can also filter by the number of occurrences of events (e.g. removing records that contain only one pneumonia event). Users can also filter out records that do not contain a specified sequence of events (e.g. asthma followed by pneumonia). Finally the legend area can also be used to turn on and off certain types of events from the display to focus on a subset of event types. With alignment the developers of this tool believe that Lifelines2 provides a simple yet effective mean of quickly exploring the data to look for potential temporal patterns across multiple records. When aligned, relative time spans can be compared easily, and one single zoom allows users to see the details around all sentinel events in view simultaneously. Overall the need to zoom and pan is greatly reduced, as is the need to keep in memory the scale of time ranges from record to record being compared. Ranking and filtering complement alignment by reordering or narrowing the set of records interactively to suit a user’s changing focus.

Compared to LifeLines, LifeLines2 can used on point – based event but it can be used on many records.

***LifeFlow***

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

LifeFlow concerns event-based points, for many records and offers the options of individual record display and the aggregated records display.

**References**

-   Gordon, T.F.,1993. The Pleadings Game. An Artificial Intelligence Model of Procedural Justice, dissertation.

-   Gordon, T.F.,1995. The Pleadings Game. An Artificial Intelligence Model of Procedural Justice, Dordrecht: Kluwer Academic Publishers 1995.

-   Hage, J., 1996. A Theory of Legal Reasoning and a Logic to Match, Artificial Intelligence and Law, Vol. 4,, pp. 199-273.

-   Lodder, A.R., 1998. DiaLaw – on legal justification and dialog games, dissertation, Universiteit Maastricht.

-   <span id="_Ref417936929" class="anchor"></span>Plaisant, Catherine, Brett Milash, Anne Rose, Seth Widof, and Ben Shneiderman. “LifeLines : Visualizing Personal Histories.” CHI-96, 1996, 221–27.

-   Prakken, H., 1993. Logical tools for modelling legal argument, doctoral thesis, Amsterdam: Vrije Universiteit.

-   Prakken, H., 1997. Logical Tools for Modelling Legal Argument. A Study of Defeasible Reasoning in Law, Dordrecht: Kluwer Academic Publishers 1997.

-   Reed, C.A., and Rowe, G.W.A, 2004. Araucaria: Software for argument analysis, diagramming and representation. International Journal of Artificial Intelligence Tools,14, 961-980.

-   Vergeij, B., 2003. Artificial argument assistants for defeasible argumentation. Artificial Intelligence, 150, 291-324.

-   Verheij, B., 1996. Rules, reasons, arguments. Formal studies of argumentation and defeat, Dissertation, Universiteit Maastricht.

-   Verheij, B., 1998b. ARGUMED—A template-based argument mediation system for lawyers, in: J.C. Hage, T.J.M. Bench-Capon, A.W. Koers, C.N.J. de Vey Mestdagh, C.A.F.M. Grütters (Eds.), Legal Knowledge Based Systems. JURIX: The Eleventh Conference, Gerard Noodt Instituut, Nijmegen.

-   <span id="_Ref417942987" class="anchor"></span>Wongsuphasawat, Krist, John Gomez, Catherine Plaisant, Taowei Wang, Ben Shneiderman, and Meirav Taieb-Maimon. “LifeFlow: Visualizing an Overview of Event Sequences.” CHI-2011, n.d., 1747–56.
