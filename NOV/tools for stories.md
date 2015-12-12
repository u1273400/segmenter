**Visualization tools for stories**

Verheij (2003) discussed artificial arguments assistants for defeasible
argumentation. He presented two systems ARGUE! based on CUMULA and ARGUMED based
on DEFLOG. Argument assistance systems can serve in a context of more than one
user: such argument mediation systems can be used to keep track of diverging
positions and assist in the evaluation of opinions. More specifically, argument
assistance systems are aids to drafting and generating arguments by :

-   administering and supervising the argument process,

-   keeping track of the issues that are raised and the assumptions that are
    made

-   keeping track of the reasons that have been adduced for and against a
    conclusion,

-   evaluating the justification status of the statements made,

-   checking whether the users of the system obey the pertaining rules of
    argument.

**CUMULA**

CUMULA (Verheij, 1996) is a procedural model of argumentation with arguments and
counterarguments. . It is based on two main assumptions. The first assumption is
that argumentation is a process during which arguments are constructed and
counterarguments are adduced. The second assumption is that the arguments used
in argumentation are defeasible, in the sense that whether they justify their
conclusion depends on the counterarguments available at a stage of the
argumentation process. If an argument no longer justifies its conclusion it is
said to be defeated. The defeat of an argument is caused by a counterargument
(that is itself undefeated).

Arguments are assigned a defeat status, either undefeated or defeated. The
defeat status of an argument depends on three factors:

-   the structure of the argument;

-   the attacks by counterarguments;

-   the argumentation stage.

To summarize, CUMULA shows:

1.  how the subordination and coordination of arguments is related to argument
    defeat.

2.  how the defeat of arguments can be described in terms of their structure,
    counterarguments, and the stage of the argumentation process, and
    independent of the logical language.

3.  how both inference and justification can be formalized in one model.

**Argue!**

The Argue!-system (Verheij, B., 1998a) is a system for computer-mediated
defeasible argumentation with a graphical user interface. Central actions of
defeasible argumentation are inference, justification and attack. Argumentation
starts with making a statement .statements can be if two types: assumption and
issues. The Argue!-system is an evaluative system for argument mediation: the
user provides the argumentation data such as assumptions, issues, reasons, and
attacks. The system determines the justification status of statements i.e.,
whether they are justified, unjustified, or neither. When the user enters new
argumentation data, statements obtain their initial value: assumptions are
initially justified, issues are initially neither justified nor unjustified.
Justified statements are shown in white boxes, unjustified statements in crossed
white boxes, statements that are neither justified nor unjustified in grey
boxes. The Argue!-system has two built-in algorithms that help determining the
justification status of arguments: ‘evaluate’ and ‘jump’. The system evaluates
the statements when the user clicks the ‘Evaluate’-button. The system evaluates
statements in rounds: the justification statuses of statements are used as input
for computing their status in the next. The Argue!-system has the following two
evaluation rules:

-   If a statement is an assumption, it is justified.

-   If a statement is an issue, and has justified support, it is justified.

The second central action of defeasible argumentation is justification. When a
new issue is raised it can be justified by giving support for it in the form of
an assumption. The third central action of defeasible argumentation is attack.
The user has added a defeater, visualized by a special visual shape that
consists of two connected rectangles. The argument configuration contained in
the first rectangle is challenging the argument configuration in the second is
challenged. The defeater represents that the new issue is a counterargument.

Reinstatement is typical for defeasible argumentation. An argument is said to be
reinstated if it becomes undefeated after being undefeated.

**ARGUMED**

The ArguMed-system is an example of a system for computer0mediated defeasible
argumentations. The argumentation theory of the ArguMed-system is an adaption of
CumulA-model, a procedural model of argumentation with arguments and
counterarguments.

The ArguMed-system has been designed in an attempt to enhance the familiarity of
the interface and the transparency of the underlying argumentation theory of its
precursor, the Argue!-system. The ArguMed-system’s user interface is
template-based, as is currently common in window-style user interfaces. The user
gradually constructs arguments, by filling in templates that correspond to
common argument patterns. An innovation of the ArguMed-system is that it uses
dedicated templates for different types of argument moves. Whereas existing
mediation systems are issue-based), the ArguMed-system allows free
argumentation, as in the CumulA-model. In contrast with the CumulA-model, which
has a very general notion of defeat, defeat in the ArguMed-system is only of
Pollock’s undercutter-type. The system allows three types of argument moves,
viz. making a statement, adding a reason and its conclusion, and providing an
(undercutter-type) exception blocking the connection between a reason and a
conclusion.

ARGUMED (Verheij, 1998b) is the evolution of the ARGUE!. Instead of using forms
to enter argumentative data, the user can interact though the screen with the
program. With respect to the argumentation theory, attack is no longer limited
to undercutting exceptions, but it is possible to attack any statement. Moreover
the arrows used to represent support or attack, are considered as conditional
statements, which allow a natural treatment of warrants and undercutters. The
dialectical arguments consist of statements that can have two types of
connections between them: a statement can support another, or a statement can
attack another. The former is indicated by a pointed arrow between statements,
the latter by an arrow ending in a cross.

In general, dialectical arguments are finite structures that result from a
finite number of applications of three kinds of construction types:

1.  Making a statement.

2.  Supporting a previously made statement by a reason for it.

3.  Attacking a previously made statement by a reason against it.

The evaluation of dialectical arguments with respect to a set of prima facie
justified assumptions is naturally constrained as follows:

1.  A statement is justified if and only if (a) it is an assumption, against
    which there is no defeating reason, or (b) it is an issue, for which there
    is a justifying reason. A statement is defeated if and only if there is a
    defeating reason against it.

2.  A reason is justifying if and only if the reason and the conditional
    underlying the corresponding supporting argument step are justified.

3.  A reason is defeating if and only if the reason and the conditional
    underlying the corresponding attacking argument step are justified.

**Araucaria**

Reed and Rowe (2004) presented a software which aimed to help the diagramming
process of argumentation analysis, the Araucaria.

The Araucaria system provides an interface which supports the diagramming
process, and then saves the result using AML, an open standard, designed in XML,
for describing argument structure. Araucaria aims to be of use not only in
pedagogical situations, but also in support of research activity. As a result,
it has been designed from the outset to handle more advanced argumentation
theoretic concepts such as schemes, which capture stereotypical patterns of
reasoning. The software is also designed to be compatible with a number of
applications, including dialogic interaction and online corpus provision. The
assumptions behind Araucaria follow the same pattern: a single text might be
analysed in several different ways, depending upon a variety of analytical
choices. The judgements concerning the delimitation of argument components can
vary, depending upon the aims of the analyst and the clarity of the text itself.

The Araucaria program can be split into three main sections:

• The main window which allows argument diagrams to be constructed from
pre-existing text files.

• An editor for schemes and scheme sets.

• An interface to the Araucaria DB online repository of marked up arguments.

When Araucaria loads, the program displays its main window which can be used to
load text files and create argument diagrams from the text. When a text file is
loaded, the text appears in the left-hand panel. A portion of this text may be
selected with the mouse. If the mouse is then clicked in the large panel on the
right, a node corresponding to that portion of the text is created and drawn at
the bottom of the panel. When two or more nodes have been defined in this way,
they can be connected in pairs by selecting one node with the mouse and dragging
the mouse to the other node. The first node selected is the premise of an
argument, and the second node is the conclusion.

Araucaria supports labels on diagrams that relate to two further aspects of
argument: ownership and evaluation. Each premise or conclusion can be associated
with one or more owners. An owner can be defined in the ownership editor dialog.
Each owner has a three-letter acronym associated with it, which is used to label
a node on the main argument diagram. Each node and support arrow in a diagram
can also have an associated evaluation, which can be used to represent the
confidence placed in a premise or support. To attach an evaluation to one or
more parts of the diagram, the nodes and/or support arrows are selected and the
evaluation editor is used to define the associated evaluation. Evaluations are
displayed as labels next to the node or arrow on the main diagram.

Araucaria allows the user to define argumentation schemes and to group them
together into schemesets. The scheme editor allows a scheme to be defined by
specifying its name, conclusion, premises and critical questions. A schemeset
containing a number of schemes can then be saved in a schemeset file.

Araucaria employs a tree structure for mapping out the relationships between
components in an argument, and allows the user to manipulate that structure.

 

**References**

-   Gordon, T.F.,1993. The Pleadings Game. An Artificial Intelligence Model of
    Procedural Justice, dissertation.

-   Gordon, T.F.,1995. The Pleadings Game. An Artificial Intelligence Model of
    Procedural Justice, Dordrecht: Kluwer Academic Publishers 1995.

-   Hage, J., 1996. A Theory of Legal Reasoning and a Logic to Match, Artificial
    Intelligence and Law, Vol. 4,, pp. 199-273.

-   Lodder, A.R., 1998. DiaLaw – on legal justification and dialog games,
    dissertation, Universiteit Maastricht.

-   Plaisant, Catherine, Brett Milash, Anne Rose, Seth Widof, and Ben
    Shneiderman. “LifeLines : Visualizing Personal Histories.” CHI-96, 1996,
    221–27.

-   Prakken, H., 1993. Logical tools for modelling legal argument, doctoral
    thesis, Amsterdam: Vrije Universiteit.

-   Prakken, H., 1997. Logical Tools for Modelling Legal Argument. A Study of
    Defeasible Reasoning in Law, Dordrecht: Kluwer Academic Publishers 1997.

-   Reed, C.A., and Rowe, G.W.A, 2004. Araucaria: Software for argument
    analysis, diagramming and representation. International Journal of
    Artificial Intelligence Tools,14, 961-980.

-   Vergeij, B., 2003. Artificial argument assistants for defeasible
    argumentation. Artificial Intelligence, 150, 291-324.

-   Verheij, B., 1996. Rules, reasons, arguments. Formal studies of
    argumentation and defeat, Dissertation, Universiteit Maastricht.

-   Verheij, B., 1998a. ARGUE!—An implemented system for computer-mediated
    defeasible argumentation, in: H. La Poutré, J. van den Herik (Eds.),
    NAIC’98. Proceedings of the Tenth Netherlands/Belgium Conference on
    Artificial Intelligence, CWI, Amsterdam.

-   Verheij, B., 1998b. ARGUMED—A template-based argument mediation system for
    lawyers, in: J.C. Hage, T.J.M. Bench-Capon, A.W. Koers, C.N.J. de Vey
    Mestdagh, C.A.F.M. Grütters (Eds.), Legal Knowledge Based Systems. JURIX:
    The Eleventh Conference, Gerard Noodt Instituut, Nijmegen.

-   Wongsuphasawat, Krist, John Gomez, Catherine Plaisant, Taowei Wang, Ben
    Shneiderman, and Meirav Taieb-Maimon. “LifeFlow: Visualizing an Overview of
    Event Sequences.” CHI-2011, n.d., 1747–56.
