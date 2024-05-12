# Reference Cleanup for Submission and Publication

During the paper writing process, often various references are added overtime to the bib file. Some of these are used at the end, others are not. For the purpose of submission to journals, we often need to clean up the bib file, the objective is to:

1. Generate a bib file with only papers referenced in the paper
2. Include when possible DOI links to each reference
3. Check on author names for consistent spelling and middle name usages
4. Check on capitalization consistency
5. Improve on latex referencing keys
6. Update latex reference keys

Software:

- [jabref](https://www.jabref.org/)
- [zotero](https://www.zotero.org/), additionally, also download a plugin for zotero [zotero-better-bibtex](https://retorque.re/zotero-better-bibtex/), follow the installation instructions at [installation guide](https://retorque.re/zotero-better-bibtex/installation/).

## Generate Sublibrary Based on Cited Entries

To generate a smaller bib file that only includes entries that are cited. we do the following:

1. Compile current latex file and find the .aux file ([download in overleaf](https://www.overleaf.com/learn/how-to/View_generated_files)).
2. Download also the full bib file used to compile the paper, note that this is the file that contains potentially a lot of unused entries.
3. In [JabRef](https://www.jabref.org/), Ctrl + O, "bfw_full.bib"
4. In JabRef, Tools, New sublibrary based on AUX file, browse, "bfw_output.aux"
  + Click Parse
  + See if there are any references that are "not found" in the "Result" pane after Parse, and check original document
  + Click Generate
5. Save newly opened untitled bib file with new bib title and use as paper bib file.

Note: tested with JabRef 5.4.

## Bibliography Cleanup, DOI, Names, etc.

Note: tested with Zotero 5.0.96.3 and zotero-better-bibtex 6.1.5

### Zotero Settings

Before importing anything, first make sure [zotero-better-bibtex](https://retorque.re/zotero-better-bibtex/) is installed, and change these settings:

1. In Zotero, Edit, Preferences
2. Better BibTex Tab, Citation key format = [zotero]
3. Export Tab, Fields subtab
  + "Fields to omit": file,abstract,keywords,shortjournal,annotation,shorttitle,options,mendeley-groups,mendeley-tags,eprint,eprinttype,langid
  + "When a reference has both a DOI and a URL", export DOI only.

### Zotero Bib Updating

Given some existing bib file, we want to create a new bib file with various things cleaned up. However, we want to use the same *Citationkey* as exists to avoid having to change the content of a paper.

1. In [zotero](https://www.zotero.org/), File, Import, "bfw_selected.bib", this file might be generated by jabref after selecting out only cited references from a fuller list of references.
2. Review the Citation Key, which is displayed in references details at the top for each entry by Zotero-better-bibtex, make sure they are consistent with existing references.
3. Click on the top right corner of the list of references pane, to open up pull down menu to choose what to display to choose what to show
4. Go through all references and check on DOI availability online
    + Some articles do not have DOI link, JSTOR offers "stable link" sometimes in those cases
    + Include DOI if exists, URL if not, note given our setting earlier, will only export URL to bib file if DOI does not exist
    + For "report" type entries, such as NBER, in zotero, include the following: a) Include *Report Number*; b) Include Series Title; c) include institution; d) include year dash month; e) include URL (if no DOI); f) include the DOI under the *Extra* field, like "DOI: 10.3386/W28920"
5. Check and change Citationkey if needed manually, can also fully reset citation keys based on pre-set formatting in preerences for zotero-better-bibtex.