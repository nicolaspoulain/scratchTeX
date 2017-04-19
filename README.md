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

Voici un exemple de résultat et le code correspondant, ci-dessous.

![enter image description here](https://raw.githubusercontent.com/nicolaspoulain/scratchTeX/master/example.png)

Le code

    \blockFlag
    \block{mouvement}{s'orienter à \field*{90}}
    \block{stylo}{effacer tout }
    \block{stylo}{stylo en position d'écriture}
    \block{stylo}{mettre la taille du stylo à \field{1}}
    \begin{blockLoop}{répéter \field{240} fois }
      \begin{blockLoop}{répéter \field{4} fois }
        \block{mouvement}{avancer de \field{100} }
        \block{mouvement}{tourner de \field{90} degrés}
      \end{blockLoop}
      \block{mouvement}{tourner de \field{1.5} degrés}
      \block{stylo}{ajouter \field{1} à la couleur du stylo}
    \end{blockLoop}

