---
layout: post 
tag: MT
title: 퀴즈 대비
date: 2018.09.11
---

## MT  

### MT Process  

**Anaylsis**   
Relevant translation units?  
Relevant properties and relations?  
<br>
**Transfer**  
Target langauge units  
<br>
**Synthesis/Generation**  
Be arranged(linearized, spelled out, ...)  
<br>
### MT Pyramid  

**Depth of analysis**  
SL sentence -> Word structure -> Syntatic structure -> Semantic structure -> Interlingua -> Semantic structure -> Syntactic structure -> Word structure -> TL Sentence   

**MT Flow**  
Morphological Analysis -> Morphological Synthesis  
Syntatic Analysis -> Syntatic Synthesis  
Semantic Analysis -> Semantic Synthesis  

**Intermediate Representations**  
Direct (word-for-word) translation  
- Word structure only (without sentence structure)  

Transfer-based translation  
- Syntactic structure (parse tree): PS-tree, D-tree  
- Semantic structure (case structure)  

Interlingua-based translation  
- Interlingua (pivot)  

<br>
### Syntatic Structures  

**Phrase structure(PS-tree)**  
Grouping of syntatic units into bigger ones  
- Annotated by phrase type(NP, VP, ...)  

Heads (often) explicitly marked  
<br>
**Dependency structure(D-tree)**  
Relation between words  
- Directed: head (governor) -> dependent  
- Annotated by syntactic function (Sub, Obj, ...)  

Phrase structure implicitly present  

