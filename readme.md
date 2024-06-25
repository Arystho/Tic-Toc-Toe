///IA joue 'O', joueur humain joue 'X'
///Configuration actuelle :
 
c [ ][ ][ ]
b [ ][X][ ]
a [ ][ ][ ]
   1  2  3
 
/// L'IA va tester tout les coups possibles pour 'O'
 
c [ ][ ][ ]
b [ ][X][ ]
a [O][ ][ ]
   1  2  3
 
/// Et simuler l'impact de ce coup, c'est a dire simuler le prochain coup de l'adversaire.
 
c [ ][ ][ ]
b [ ][X][ ]
a [O][X][ ]
   1  2  3
 
/// ici :
/// Si l'IA joue a3 :
 
c [ ][ ][ ]
b [ ][X][ ]
a [O][X][O]
   1  2  3
 
/// Elle va perdre, renvoi d'une valeur négative.
 
alors que si elle joue c2 :
 
c [ ][O][ ]
b [ ][X][ ]
a [O][X][O]
   1  2  3
 
/// Elle renverra un poids nul (0) car personne ne gagne.