#programme cout d'expedition de colis
#Dimension du colis
def dimension():
    hauteur=float(input("Entrer la hauteur de votre colis :"))
    largeur=float(input("Entrer la largeur de votre colis :"))
    longueur=float(input("Entrer la longeur de votre colis :"))
    return hauteur,largeur,longueur

#coutExpedition Avion
def coutExpeditionAvion(poidsVolumetrique,prixLivre):
    return poidsVolumetrique*prixLivre

#coutExpedition pour Bateau  
def coutExpeditionBateau(poidsVolumetrique,prixLivre):
    return poidsVolumetrique*prixLivre
    
#condition
def choix():
    choix=0
    while choix != 1 and choix != 2: choix = int(input("Les moyens d'expédition sont :\n1-Avion\n2-Bateau\nSélectionner le moyen d'expédition de votre choix : "))
    if choix == 1:
        poidsVolumetrique = (hauteur * largeur * longueur) / 166
        return coutExpeditionAvion(poidsVolumetrique, prixLivre)
    elif choix == 2:
        poidsVolumetrique = (hauteur * largeur * longueur) / 1728
        return coutExpeditionBateau(poidsVolumetrique, prixLivre)
    else:
        print("Veuillez choisir 1 ou 2.") 
           
if __name__=="__main__":
    #prix en $ par livre de marchandise
    prixLivre=10
    hauteur,largeur,longueur=dimension()
    fraisTotal=choix()
    print("Le cout total a payer est de ",float(fraisTotal),"$")  
