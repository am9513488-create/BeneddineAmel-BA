# BeneddineAmel-BA
#Beneddine Amel biochimie appliqué 07/12/2025

#membres de groupe(

                 #Beneddine Amel
                 #Benali Samia
                 #Meghelli Hichem
                 #Meghelli Souheil
                 #Bendada ilyas Abderrezzak)
                 
import pandas as pd

#données : séquence ADN, longeur, pourcentage de GC

data = {

    "séquence": ["ATGCGTACGTA","GCTAGCTAGGCC","ATGCGCTAAGT","TACGATCGTA","ATGAAAGGCTT","CGTACGTAGC","TTAACCGGAT"],
    
    "longueur": [11,12,12,10,11,10,10],
    
    "pourcentage GC":[50,66.67,58.33,40,45.45,60,50]
}

#1)création d'un dataframe (tableau pandas)

df = pd.DataFrame(data)

print("***********creation et affichage***********")

#affichage du tableau

print("tableau des longueur ADN :")

print(df)


#opérations sur les tableaux:

print("***********longueur***********")

#2) sélectionner la colonne "longueur"

longueur = df["longueur"]

print(longueur)



#3)Filtrer les séquences dant la longueur est supérieur a 10 

print("***************Filtrer Longueur > 10***************")

#Filtrer les séquences dant la longueur est supérieur a 10

filtered_df=df [df["longueur"] >10 ]

print(filtered_df,"\n\n")



#4)Calculer la moyenne du pourcentage de GC avec 3 chiffres après la virgule

print("************Calcul de la moyenne************")

#Calculer la moyenne du pourcentage de GC avec 3 chiffres après la virgule

average_gc=df["pourcentage GC"].mean()

print(f"pourcentage moyen de GC :{average_gc:.3f}%","\n\n")




#5)Ajouter une nouvelle colonne

print("****************Ajout d'une nouvelle colonne****************")

#Ajouter une nouvelle colonne "catégorie_gc"

df["catégorie GC"]=df["pourcentage GC"].apply(lambda x:"Riche"if x>55 else ("Moyen"if x>=45 else"Faible"))

print(df)



#6) Ajouter une colonne comptant les 'G' dans chaque séquences 

df["Nb_G"] = df["séquence"].apply(lambda seq: seq.count("G")) 

print("\n***************Nombre de G dans chaque séquences ***************\n") 

print(df) 



#7)calculer l'écart-type de GC% et de la langeur


print("\n************* Écart-types *************")

ecart_type_GC = df["pourcentage GC"].std()


ecart_type_longueur = df["longueur"].std()


print(f"Écart-type de %GC : {ecart_type_GC:.2f}")


print(f"Écart-type de la longueur : {ecart_type_longueur:.2f}\n")



#8)souvegarde le dataframe dans un fichier CSV 

df.to_csv("tableau_sequences.csv", index=False) 








