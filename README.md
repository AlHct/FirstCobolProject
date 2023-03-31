# FirstCobolProject
Contexte

Au terme d'une formation en COBOL, mes camarades et moi-même avons réalisé un projet de trois jours permettant de mettre en lien différentes tables et bases de données DB2 modélisant les commandes et réapprovisionnements de produits d'un site de grande distribution.
Cet exécutable JCL mettait en lien différents programmes avec entrées et sorties de fichiers ainsi que des requêtes SQL donnant accès à des tables de bases de données DB2 permettant de mettre à jour les commandes des clients, le stock des produits ainsi que les quantités de réapprovisionnement du site en question.


Ainsi parmi les programmes que nous avons créé que l'on peut retrouver dans le dossier SOURCE on peut distinguer:

Le programme D6STOCK qui permettait de récupérer les données des tables des commandes des clients et des produits présents dans le stock du site ainsi que les stocks d'approvisionnement. Ces données étaient stockées dans un fichier. D'autres variables sont calculées telles que les quantités cumulées de commandes selon le produit ou encore les quantités cumulées de produits approvisionnés.

Le programme D6REAPRO permet de trier les produits dont le stock est suffisant et ceux dont les quantités sont insuffisantes et sont à réapprovisionner. Les données des différents produits sont triées entre le fichier de produits à réapprovisionner et le fichier des produits pour lesquels le stock est suffisant.

Le programme D6MAJAPP permettait de déterminer les quantités à réapprovisionner et mettre à jour les stocks des tables appro.

Le programme D6LIVRAISON permettait de mettre à jour les stock et quantités des différents produits des tables Produits et clients.

Le dossier contient également les codes d'éxecution JCL (CNTL, D6PROJET) ainsi que les codes d'importation des tables DB2 (SPUFI, DCLGEN).

Pour une meileure compréhension du programme, vous pouvez vous référer au dossier Modèle qui contient des diagrammes modélisant le programe ainsi que la représentation merise des tables DB2 et les schémas des algorithmes des programmes individuels.
