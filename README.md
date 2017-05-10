Des algorithmes Scratch en LaTeX
------------

Le but de ce travail est de fournir un environnement permettant de
produire avec une syntaxe simple des algorithmes Scratch.

Plutôt qu'inclure des copies d'écran de scratch, il est plus propre et plus
pratique d'inclure des algorithmes constitués de blocs décrits par un texte
modifiable.

Sur le site Melusine, on trouve un excellent travail permettant de produire de
tels algorithmes en Metapost : http://melusine.eu.org/syracuse/G/mp-scratch/

Ici, c'est PSTricks qui est utilisé car c'est le langage graphique utilisé par
l'APMEP, ce qui en fait (selon moi) une référence.

Voici un exemple de résultat et le code correspondant, ci-dessous.  À gauche
l'original avec Scratch et à droite le script en LaTeX avec ScratchTeX.

![enter image description here](https://raw.githubusercontent.com/nicolaspoulain/scratchTeX/master/example.png)

Le code

    \blockflag
    \block{stylo}{effacer tout }
    \block{stylo}{stylo en position d'écriture}
    \block{apparence}{mettre l'effet \lfield{couleur} à \nfield{0} }
    \repeatbegin{répéter \nfield{240} fois }
      \repeatbegin{répéter \nfield{4} fois }
        \block{mouvement}{avancer de 
                \tfield*{operateurs}{\tfield{donnees}{var} * \nfield{10} } \ }
        \block{mouvement}{tourner \larrow de \nfield{90} degrés }
      \repeatend
      \block{mouvement}{tourner \rarrow de \nfield{1.5} degrés }
      \block{stylo}{ajouter \nfield{1} à la couluer du stylo }
    \repeatend
    \block{stylo}{relever le stylo}

