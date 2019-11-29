# Document chapters
The following chapters/information must be included in the design document (according to the unofficial Snelting tips document):

* Introduction. Gives an overview of the document. Explains separation into packages.
* Detailed class descriptions.
* Sequence diagrams to illustrate common processes.
* Changes relative to the requirements document.
* Large class diagram that shows all classes.

# Tools
Everyone must use the same tools for the design phase because they are usually not compatible with one another.
We decided on using PlantUML and Doxygen for the design phase.

## Workflow

* Write Python class/method stubs with docstrings and type hints.
* Manually create UML sequence diagrams.
* Manually create UML class diagrams that show relations between classes for single packages.
* Manually write introduction.
* Manually write about changes relative to requirements document.
* Run py2puml on Python code to generate a large class diagram that displays signatures and inheritance. Include manually created UML class diagrams in the large class diagram via config file.
* Run Doxygen on Python code to generate tex files that describe classes and their public interfaces.
* Edit LaTeX main file to include our manually created chapters.
