# Description 

This repository holds utilities for parsing and extracting useful data from [Transkribus](transkribus.ai) PageXML outputs, such as a utility for identifying text regions (Paragraph Extractor), and a utility to reconcile Trankribus output metadata with the equivalent data in relevant library catalogues (coming shortly). 

**Paragraph Extractor** is a utility that accepts Transkribus PageXML as input and then interprets the text regions on each page/image (such as headers, titles, blocks of text, etc.), which we term "paragraphs". It then returns the raw text of each text region (paragraph) along with its metadata. Note that it **reads PageXML, not AltoXML**. 

**Paragraph Extractor** was developed by James Engels of SOAS University of London for the Divergent Discourses project. The project is a joint study involving SOAS University of London and Leipzig University, funded by the AHRC in the UK and the DFG in Germany. Please acknowledge the project in any use of these materials. Copyright for the project resides with the two univerisities. 

## Paragraph Extractor

`paragraph_extractor.py` takes either a path or a filename as its argument and extracts paragraphs along with metadata. If inputting a filename, the file must be stored in the same directory as the .py file at the same level. The method assumes the Transkribus "text region" is an acceptably accurate 1:1 proxy for a paragraph. 

The program recursively searches input directories for .xml files, so clean file structures are important! 

### Using the Paragraph Extractor

After downloading the `.py` file, navigate to its containing directory with the command line and call it with `python paragraph_extractor.py`. The user will then be prompted to input the filename, directory name, or path to file/directory. The corresponding .csv file will be output in the same directory as the final input object.  



