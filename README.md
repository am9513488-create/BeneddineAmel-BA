# BeneddineAmel-BA
#beneddine amel biochimie appliqué 07/12/2025

#membre de groupe(

                 #benali samia
                 
                 #meghelli hichem
                 
                 #meghelli souheil
                 
                 #bendada ilyas abderrezzak)
                 
import pandas as pd

#données : séquence ADN, longeur, pourcentage de GC

data = {

    "séquence": ["ATGCGTACGTA","GCTAGCTAGGCC","ATGCGCTAAGT","TACGATCGTA","ATGAAAGGCTT","CGTACGTAGC","TTAACCGGAT"],
    
    "longueur": [11,12,12,10,11,10,10],
    
    "pourcentage GC":[50,66.67,58.33,40,45.45,60,50]
}

#création d'un dataframe (tableau pandas)

df = pd.DataFrame(data)

print("***********creation et affichage***********")

#affichage du tableau

print("tableau des longueur ADN :")

print(df)

#opérations sur les tableaux:

print("***********operations***********")

#1) sélectionner la colonne "longueur"

longueur = df["longueur]

print(longueur)

#2) Affichage avec une bibliothèque de visualisation (matplotlib)

#import matplotlib.pyplot as plt

#données

#sequences = ["ATGCGTACGTA","GCTAGCTAGGCC","ATGCGCGTAAGT","TACGATCGTA","ATGAAAGGCTTA","CGTACGTAGC","TTAACCGGAT"]

#longueur= [11,12,12,10,11,10,10]

#gc_content=[50,66.67,58.33,40,45.45,60,50]

#création d'un DataFram

#data={"séquence": sequences, "Longueur": longueur, "Pourcentage GC":gc_content}

#df= pd.DataFram(data)

#Affichage du tableau de données sous forme de graphique

#plt.figure(figsize=(10,6))

#plt.bar(df["séquence"], df["pourcentage GC"], color='skyblue')

#plt.xlabel("séquences")

#plt.ylabel("Pourcentage GC")

#plt.title("Pourcentage de GC par séquence")

#plt.show()

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
#7)calculer l'écart-type de GC% et de la langeur
printf("\n************* Écart-types *************")
ecart_type_GC = df["pourcentage GC"].std()
ecart_type_longeur = df["longueur"].std()
print(f"Écart-type de %GC : {ecart_type_GC:.2f}")
print(f"Écart-type de la langueur : {ecart_type_longueur:.2f}")






