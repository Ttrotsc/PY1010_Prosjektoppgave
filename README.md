# Hva gjør programmet

Support dashboard er et program som henter ut nøkkeltall fra supporthenvendelser lagret i et excelark.

Programmet er skrevet i Jupityr notebook og importerer data fra excelarket og konvertere data til arrays, for deretter å gjøre en rekke ulike beregninger.

Eksempel på bruk:
```py
# Leser inn Excel-filen
kundebase = pd.read_excel('support_uke_24.xlsx', sheet_name = "Morse")

#Viser kolonnenavn og første radene i excelarket for å se hva den inneholder
print(kundebase.head())

#konverterer så inn de ulike kolonnene som arrays med nye navn
u_dag = kundebase ['Ukedag'].values
kl_slett = kundebase ['Klokkeslett'].values
varighet = kundebase ['Varighet'].values
score = kundebase ['Tilfredshet'].values
