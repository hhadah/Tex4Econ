This is a work-in-progress [website](https://fanwangecon.github.io/Tex4Econ/) of support files for writing various files with latex, produced by [Fan](https://fanwangecon.github.io/). The project includes sample file for papers, exams, homeworks, etc.

Materials gathered from various [projects](https://fanwangecon.github.io/research) in which latex is used. The goal of this repository is to make it easier to find/re-use latex files produced for various projects.

This [overleaf project](https://www.overleaf.com/read/xjsqdwrkfrhq) is synced with this git repository. You can clone the project, pull project to overleaf, and compile in overleaf browser. Specifically: clone the repo; go to your overleaf account and create a project; click on menu under sync with git/github.

The writing/structure is to:
1. Store latex formatting file etc in separate files away from paper tex.
2. For papers, write in tex fragments stored in separate files. Main tex paper file mainly contains structure/outline.
3. Files synced through git/github, pull from github to edit/share with co-authors on [overleaf.com](https://overleaf.com) or edit locally.

Please contact [FanWangEcon](https://fanwangecon.github.io/) for issues or problems.

# [One File Article](https://github.com/FanWangEcon/Tex4Econ/blob/master/singlefile_article/article_fan.tex)

For papers that are not too long, we might write all tex contents on the same page. This is the example single-file paper [**tex**](https://github.com/FanWangEcon/Tex4Econ/blob/master/singlefile_article/article_fan.tex) file, and this is the   [**pdf**](https://github.com/FanWangEcon/Tex4Econ/blob/master/singlefile_article/article_fan.pdf) output. Even for single-file papers, various paper components listed below should be stored separately for clarity and convenience. 

The paper [**Preamble**](https://github.com/FanWangEcon/Tex4Econ/blob/master/fragments/preamble_main.tex) is stored in its own file, and loads in the packages and settings, statistics/phrases/math, and citation from tex fragments listed below. A clear separation should be kept between these files, with the main [**preamble**](https://github.com/FanWangEcon/Tex4Econ/blob/master/fragments/preamble_main.tex) only loading inputs in.

The preamble file can be inserted at the top of a full paper file, for example at the top of this [multi-section file](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections_combine/draft_main.tex).

For one-file article, we could directly load in the various tex fragments below. For example, we load these packages below into [this file](https://github.com/FanWangEcon/Tex4Econ/blob/master/singlefile_article/article_fan.tex).

- **Numbers/Phrases/Math**: various tex fragments store key file components in separate files
    * [*Numbers*](https://github.com/FanWangEcon/Tex4Econ/blob/master/fragments/stats/stats_one.tex): Sometimes, we want to use the same number if various spots in the paper, these numbers should be stored as newcommands so that the number can be updated in one spot.
    * [*Often Used Phrases*](https://github.com/FanWangEcon/Tex4Econ/blob/master/fragments/shorthand/short_text.tex): Generally, there are terms that are used often in a paper. To make it easy to change these terms or to avoid having to rewrite over and over again, these terms could be stored as new commands.
    * [*Often Used Math*](https://github.com/FanWangEcon/Tex4Econ/blob/master/fragments/shorthand/short_text.tex): We might need to reuse various Math Symbols or parts of equations, they should also be stored as newcommands.
    * The aggregate [*PDF*](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections_combine/draft_main.pdf) file, compiling all subsection tex files together.
    * The [*overleaf*](https://www.overleaf.com/read/xjsqdwrkfrhq) file, allowing for live compilation.
- **Citation**: structure to cite efficiently
    * [*Preamble Settings*](https://github.com/FanWangEcon/Tex4Econ/blob/master/fragments/cite/cite_preamble.tex): One file to be loaded into preambles sets citation settings.
    * [*End File Citation Settings*](https://github.com/FanWangEcon/Tex4Econ/blob/master/fragments/cite/cite_end.tex): One file to be loaded at the end of the paper that determines bibliography text display.
    * [*Bib Files*](https://github.com/FanWangEcon/Tex4Econ/tree/master/_bib): Various bib files loaded from [zotero](https://www.zotero.org/) stored in own folder.
- **Packages and Settings**: Package loading etc.
    * [*Package Loading*](https://github.com/FanWangEcon/Tex4Econ/blob/master/fragments/preamble_one.tex)
    * [*Additional Packages and Settings*](https://github.com/FanWangEcon/Tex4Econ/blob/master/fragments/preamble_two.tex)


# [Multi-Section Article](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections_combine/draft_main.tex)

When a paper is longer, it could be difficult to manage long latex files. Compiling could take long periods of time if the full paper requires compilation for any edits in a subsection. The structure below allows for editing paper in subsections and compiling by sections. The structure works locally as well as remotely on browser based compiler.

Inside [overleaf](https://www.overleaf.com/read/xjsqdwrkfrhq), the aggregate tex file that combines all sections together should be set as the main/default file under project options. Then as subsection text fragments are edited inside overleaf, the full pdf file is updated on the right showing current changes.

The same [bib](https://github.com/FanWangEcon/Tex4Econ/tree/master/_bib) file structure and [preamble fragment](https://github.com/FanWangEcon/Tex4Econ/tree/master/fragments) structure is used here as in the single file case above.

- **Aggregate Tex and PDF**: combine subsections together in one joint overall paper file
    * The aggregate [*tex*](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections_combine/draft_main.tex) file, only showing section and subsection headings.
    * The aggregate [*PDF*](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections_combine/draft_main.pdf) file, compiling all subsection tex files together.
    * The [*overleaf*](https://www.overleaf.com/read/xjsqdwrkfrhq) file, allowing for live compilation.
- **Section PDF Compiles**: compile each section separately to reduce compile time and file length.
    * Introduction Conclusion Section: [*Tex Compile*](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections_sandbox/introconclude_sandbox.tex), [*PDF*](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections_sandbox/introconclude_sandbox.pdf)
    * Model Section: [*Tex Compile*](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections_sandbox/model_sandbox.tex), [*PDF*](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections_sandbox/model_sandbox.pdf)
    * Estimation Section: [*Tex Compile*](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections_sandbox/estimate_sandbox.tex), [*PDF*](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections_sandbox/estimate_sandbox.pdf)
- **Section Folders**: each section has own folder.
    * [Introduction Conclusion Section Folder](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/introconclude/)
    * [Model Section Folder](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/model/)
    * [Estimation Section Folder](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/esti/)
- **Section Main Tex Files**: this file gathers subsection inputs together, used for section by section compilation
    * [Introduction Conclusion Section Main File](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/introconclude/main.tex)
    * [Model Section Main File](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/model/model_main.tex)
    * [Estimation Section Main File](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/esti/esti_main.tex)    
- **Subsection Tex Files**: each subsection has own tex file:
    * [Introduction](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/introconclude/intro.tex) from the intro and conclusion folder.
    * [Conclusion](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/introconclude/conclude.tex) from the intro and conclusion folder.
    * [Literature review](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/introconclude/literature.tex) from the intro and conclusion folder.
    * [Introduction](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/introconclude/intro.tex) from the intro and conclusion folder.
    * [Conclusion](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/introconclude/conclude.tex) from the intro and conclusion folder.
    * [Model Subsection One](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/model/model_one.tex) from the model folder.
    * [Model Subsection Two](https://github.com/FanWangEcon/Tex4Econ/blob/master/sections/model/model_one.tex) from the model folder.
