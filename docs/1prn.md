---
layout: default
title: 1PRN
author: Jordi Villà-Freixa
permalink: /1prn/
---
 <head>
    <meta charset="utf-8">
    <title>{{ page.title }}</title>
<script src="https://cdn.jsdelivr.net/npm/babel-polyfill/dist/polyfill.min.js"></script>
    <!-- Web component polyfill (only loads what it needs) -->
<script src="https://cdn.jsdelivr.net/npm/@webcomponents/webcomponentsjs/webcomponents-lite.js" charset="utf-8"></script>
    <!-- Required to polyfill modern browsers as code is ES5 for IE... -->
<script src="https://cdn.jsdelivr.net/npm/@webcomponents/webcomponentsjs/custom-elements-es5-adapter.js" charset="utf-8"></script>

<link rel="stylesheet" type="text/css" href="https://www.ebi.ac.uk/pdbe/pdb-component-library/css/pdbe-molstar-1.2.1.css">
<script type="text/javascript" src="https://www.ebi.ac.uk/pdbe/pdb-component-library/js/pdbe-molstar-component-1.2.1.js"></script>
<style>
        #myViewer{
          float:none;
          width:400px;
          height:400px;
          position:relative;
        }
    </style>
  </head>

<h1> Anàlisi de les relacions seqüència-estructura-funció de la proteïna de membrana porina (PDB: 1PRN)</h1>

- [Estructura secundària](#estructura-secundària)
- [Estructura supersecundària](#estructura-supersecundària)
- [Plegament](#plegament)
- [Funció](#funció)


 El codi [PDB:1PRN](https://www.rcsb.org/structure/1prn) correspon a l'estructura de la proteïna H-RAS p21,codi [UNIPROT:P39767](https://www.uniprot.org/uniprot/P39767), una proteïna de membrana en bacteris, amb una gran conservació de seqüència que es pot comprovar amb un simple BLAST i un posterior alineament amb el mateix servidor d'NCBI, per exemple.


|![](/figures/1prn_msa.png)|
|:--:|
|MSA simple obtingut a partir de la cerca amb BLAST contra  la base de dades no redundant.|


La seqüència de la proteïna al PDB és

```fasta
>1PRN_1|Chain A|PORIN|Rhodobacter blasticus (1075)
EISLNGYGRFGLQYVEDRGVGLEDTIISSRLRINIVGTTETDQGVTFGAKLRMQ
WDDGDAFAGTAGNAAQFWTSYNGVTVSVGNVDTAFDSVALTYDSEMGYEASSFG
DAQSSFFAYNSKYDASGALDNYNGIAVTYSISGVNLYLSYVDPDQTVDSSLVTE
EFGIAADWSNDMISLAAAYTTDAGGIVDNDIAFVGAAYKFNDAGTVGLNWYDNG
LSTAGDQVTLYGNYAFGATTVRAYVSDIDRAGADTAYGIGADYQFAEGVKVSGS
VQSGFANETVADVGVRFDF
```

Pots visualitzar la proteïna en aquesta finestra proveïda per [Mol*](https://molstar.org):

<p>
<div id="myViewer">
<pdbe-molstar id="pdbeMolstarComponent" molecule-id="1prn" hide-controls="true"></pdbe-molstar>
</div>
</p>
<br>  

## Estructura secundària

L'estructura presenta és constituïda pràcticament només per fulles beta

|![](/figures/1prn_2nd.png)|
|:--:|
|Imatge de la proteïna mostrant els elements d'estructura secundària.|

La següent figura mostra la seqüència de la proteïna i les regions amb hèlix alfa (groc) i fulles beta (verd)

|![](/figures/1prn_seq.png)|
|:--:|
|Seqüència de la proteïna mostrant els elements d'estructura secundària|

## Estructura supersecundària

La figura mostra l'estructura amb un codi de colors progressiu que permet identificar la regió N-terminal (blau) i la regió C-terminal (vermell).

|![](/figures/1prn_rainbow.png)|
|:--:|
|Imatge de la proteïna amb la representació amb colors de fred (blau) a calent (vermell) en funció de la seqüència.|

Totes les imatges s'han visualitzat amb [Chimera](/code/1prn.py). Podem observar com es repeteix un motiu $\beta$-hairpin. 

|![](/figures/1prn_hairpin.png)|
|:--:|
|Exemple de $\beta$-hairpin en l'estructura de PDB:1PRN.|

## Plegament

Es tracta d'una proteïna __all $\beta$__, amb un plegament de tipus *Transmembrane beta-barrel* quin representant és PDB:3PRN [segons la clasificació a SCOP](https://scop.mrc-lmb.cam.ac.uk/term/8025499)

|![](/figures/3PRN_SCOP.png)|
|:--:|
|Estructura jeràrquica del domini al qual pertany PDB:1PRN, representada a SCOP per PDB:3PRN|

i de domini que forma part de la superfamília *Porin* [segons CATH](http://www.cathdb.info/search?q=1prn).

## Funció

Podem començar per [cercar a PFAM el codi uniprot de la proteïna](http://pfam.xfam.org/protein/P39767). Veiem que es tracta d'una proteïna amb un sol domini *Porin_4* ben caracteritzat.

Podem aleshores explorar l'entrada per a aquest domini específic: PFAM: P39767, i hi trobem informació sobre els porus Porin en bacteris. El domini concret Ras està altament distribuït, trobat en  [18 arquitectures diferents](http://pfam.xfam.org/family/P39767#tabview=tab1), vora [1600 espècies](http://pfam.xfam.org/family/P39767#tabview=tab7), totes corresponents a bacteris.

L'estudi del [logo HMM](http://pfam.xfam.org/family/P39767#tabview=tab4) ens mostra un domini amb una gran concentració de residus hidrofòbics alternant amb residus polar o carregats. Sobre l'estructura es pot observar com els residus polars d'organitzen a l'interior de la propteïna i a les "tapes" del barril, mentre que els hidrofòbics es col·loquen en les regions d'interacció amb la membrana, com correspon a una proteïna quina funció és el transport de substàncies polars.
