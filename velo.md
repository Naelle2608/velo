# Sujet de Bac Terminale NSI Exercice 2 
# 1) a)
flotte[26] renvoie {'type' : 'classique', 'etat' : 1, 'station' : 'Coliseum'}
# 1) b)
flotte[80]['etat'] renvoie la valeur 0.
# 1) c)
flotte[99]['etat'] renverra une erreur car la clé 99 n'existe pas.

4) def velo_finder(coordonnees):
    velo_dispo = []
    for id_velo in flotte:
        d = distance(coordonnees, stations[flotte[id_velo]['station']])
        if d < 800 and flotte[id_velo]['etat'] == 1:
            velo_dispo.append((flotte[id_velo]['station'], d, id_velo))
    return velo_dispo
