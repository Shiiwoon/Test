


# RESUME Leçon 8
# EXPRESSION REGULIERE

## Methode : 

#### Search
> **Def** : Permet de rechercher un motif dans une chaine de caractère.

    Syntax : re.search('motif','chaineDeCaractère')
    
    Exemple : 
    ch=["Wagateki wo kurauu","Ryuujin no kaioken","Heros's Never Die"]
    re.search('uu','ch') # Recherche les chaine de caractères contenant 'uu'
    
-   Sub
-   FindAll
-   Compile
-   Match
-   Split


<span style="color:blue">blue</span>

## Racourci :

-   **\d** : Equivalent de [0-9]
-   **\D** : Equivalent de [^0-9]
-   **\s** : Equivalent de [' '\t\n\r\f\v] (espace, tabulation, retour à la ligne, ect)
-   **\S** : Equivalent de [^' '\t\n\r\f\v] 
-   **\w** : Equivalent de [a-zA-Z0-9_]
-   **\W** : Equivalent de [^a-zA-Z0-9_]

## Caractère spéciale :

-   **\\** : Caractère qui annule la signification de base

Exemple:

        '^\^' > chaine qui commence par ^
        '^\D' > chaine qui commance par un chiffre

-   **^** : Expression qui commence par ce qui suit ^

Exemple:

        '^06' > chaine qui commence par 06
        '^F' > chaine qui commance par F
-   **$** : Expression qui ce termine par ce qui precéde $

Exemple:

        '1994$' > chaine qui ce termine par 1994
        '\$$' > chaine qui ce termine par un $
        
        
-   **.** : Caractère (joker) qui correspond à n'importe quel caractère.

Exemple:

        'Gr.s' > Gros, Gras, Gr0s, GrWagateki Wo Kuraus / chaine qui contient n'importe quoi entre Gr et s 
        'w.w' > wow,www,waw,wagateki wo kurauw / chaine qui contient n'importe quoi entre w et w 

-   **[]** : Caractère possible

Exemple:

        '^[xyz]' > Commence par x ou y ou z   
        '[A-Z]' > Chaine ayant uniquement des majuscules
        
-   **|** : Caractère possible

Exemple:

        '^0(1|6)' > Commence par 01 ou 06
        '\d\d(-|/)\d\d' > Chaine qui contient 4 chiffre avec un soit un espace soit un slash entre le 2eme et le 3eme chiffre
        
##### Quantificateur
-   **?** : Quantificateur 0 ou 1

Exemple:

        'Gr(.)?s' > Grs,Gras,Gros
        'w(.)?w' > ww, www, wow ,ect   
        
-   **+** : Quantificateur au moin 1 ( 1 ou plus)

Exemple:

        'Gr(.)+s' > Gras,GrRyuujin no kaiokens, ect
        'w(.)?w' > www, wit's high noonw, ect
        
-   **\*** : Quantificateur 0 ou 1 ou plus

Exemple:

        'Gr(.)?s' > Grs, Gras, GrRyuujin no kaiokens
        'w(.)?w' > ww, www, wit's high noonw, ect 
        
-   **{}** : Quantificateur personalisable

Exemple:


        'w{3}' > www  / w qui ce répète exatement 3 fois de suite
        '(Die ){3}' > Die Die Die / Groupe de caractère Die' ' qui ce répète 3 fois de suite
        '(ll)'{1,2} > file, fille // Groupe de caractère ll qui ce répète 1 à 2 fois de suite
        'u{,10}' > lol(0fois), bruh(1fois), gruu(2fois),...,Muuuuuuuuuugen(10fois) // Caractère u ce répète de 0 à 10 fois
        'a{1,}' > a, laa, yaaa, ect // Caractère a qui ce répète au moins 1 fois
        


        

        
        

