# Code-switch Text Generator
An extension to the GCM toolkit to generate code-switched text from monolingual text in two languages. Samples from Flores-200 are provided.

## Installation
1. Clone the original GCM repository with `git clone https://github.com/microsoft/CodeMixed-Text-Generator`.
2. Replace the CodeMixed-Text-Generator/requirements.txt, CodeMixed-Text-Generator/library/GCM Library Mode Demo.ipynb, CodeMixed-Text-Generator/cm_text_generator/data_structure_definitions.py with the ones in this repository.
3. Follow the instructions in the [GCM repo](https://github.com/microsoft/CodeMixed-Text-Generator) to install and set up all necessary libraries.
4. Run the following command to download English NER model: `python -m spacy download en_core_web_md`. The model can be changed according to your own requirements.

### Important things to note:
1. The toolkit currently provides the interactive library mode to address the needs of researchers, linguists and language experts. 
2. Change the language_1 and the language_2 in the file "CodeMixed-Text-Generator/config.ini" to the correspond languages you are dealing with.
3. To restrict the part of speech of the replaced words in the code-mixing sentence, for example to set the replacement to nouns or adjectives only, change the "CodeMixed-Text-Generator/cm_text_generator/data_structure_definitions.py" line 10 and line 21.
4. The translation of name entity can be get from translation engines or search from Internet.
5. The word alignment tool can be changed to GIZA++ if better alignment is needed. Please follow the original GIZA++ Gitlab to install the tool.

## Usage
Simply go to the **library** directory:

```
cd library
```

You can start jupyter notebook here:

```
jupyter notebook --notebook-dir=/Your_Path/CodeMixed-Text-Generator/library
```

Select the `GCM Library Mode Demo` notebook which has examples on how to run the GCM tool.

## Citation  
If you use the tools here and/or the derived data, please cite the following in addition to the original GCM toolkit and Flores data providers.
```
@inproceedings{codeswitch_llm_2024,
  author    = {Huzaifah,Muhammad and Zheng,Weihua and Chanpaisit,Nattapol and  Wu,Kui},
  title     = {Evaluating Code-Switching Translation with Large Language Models},
  year      = {2024}
  booktitle = {LREC-COLING 2024}
}
```