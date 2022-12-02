Component scan permet de discover tout les composants 

L'annotation @SpringBoootApplication active automatiquement le component scan avec sa configuration par défaut

Il scan et découvre tout les [[@Component]] du classpath ( tout les enfants du package)

On peut y ajouter un argument pour préciser le package de depart 