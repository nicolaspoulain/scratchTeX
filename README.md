Des algorithmes Scratch En LaTeX
------------

Voici un exemple de résultat

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

