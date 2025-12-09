# BeneddineAmel-BA
#beneddine amel biochimie appliqué 07/12/2025
#membre de groupe(
                 #benali samia
                 #meghelli hichem
                 #meghelli souheil)
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










