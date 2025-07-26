---
title: "Opret bruger"
layout: default
parent: For system administratorer
nav_order: 1
---

# **Opret bruger**

```mermaid
flowchart LR
       id1["Klargør brugeroprettelse"]  --> id2["Opret bruger"]  --> id["Tilknyt til Zulip"] --> id4["Inviter bruger"]
```
## Klargør brugeroprettelse

Når der er anmodet om oprettelse af en bruger skal du først og fremmest sikre dig at du har:
- brugerens fuldenavn
- brugerens email
- brugerens tilknytning til OS2 (medlemsstatus/observatør/leverandør/m.v)
- oplysning om hvilke produkt grupper brugeren skal tilknyttes

Når du har disse oplysninger klar kan du gå igang

## Opret Brugere - manuelt ( uden FKA integration)
Denne handling foretages i Authentic, af en bruger som har Administrations rettighed ( Brugertype: administrator eller Ejer )

Handlingen triggers af et Github request (jvf Anmod om bruger oprettelse)

Derudover genereres der et stærkt PW tilbrugeren i et dertil egnet værktøj, hvilket kunne være 1Password: [https://1password.com/password-generator](https://1password.com/password-generator)

Arbejdsgangen er som flg:
- Åben Authentic [https://authentik.os2samtale.open-public.org](https://authentik.os2samtale.open-public.org)
    - Log ind med email og PW 
  
- Åben administrationsmodulet i Authentic -link i øverste højre hjørne [Admin Interface](https://authentik.os2samtale.open-public.org/if/admin/)
  
-  Opret ny bruger 
   - Åben menupunktet Directory (tryk på pilen ud for menupunkt i den menu der er vist i venstre side af vinduet)
   -  Vælg undermenuen User
   -   Vælg den grønne knap create (oven over listen af brugere)
   -   Udfyld pop op vinduet med flg
     -  Username : brugerens email addresse
     -  Name : brugerens fulde navn - for virksomheder inkluderes virksomheden i parantes efter navnet
     -   Email:  brugerens email addresse
     -  Attributter : bruges ikke direkte lige nu men vil følge senere   
   - Tryk på knappen create
- Opret kodeord til brugeren
  - Åben 1 pw strong PW generator [https://1password.com/password-generator](https://1password.com/password-generator)
  - Generer et stærkt PW
  - Åben Pass go [https://snap.dglive.net/](https://snap.dglive.net/)
  - Kopier det stærke PW ind i kanalen
  - Vælg funktionen generate url
  - Lad udløbsdato blive på 1 uge
  - Vælg funktionen copy Url
  - Kopier Url's ind i email til brugeren

## Tilknyt til Zulip
Denne handling foregår både i Authentic og i Zulip (indtil videre)
- Tilknyt brugeren til Zulip
  - Vælg menuen Groups ( under directory)
  -  Vælg gruppen Zulip
  -  Vælg Users i den vandrette menu i toppn
  - Vælg funktionen Add eksisting user
  - Tryk på plusset i popup menuen
  - Vælg brugeren i listen ( marker i krydsfeltet)
  - Vælg add
  - Tilknyt brugeren til kanaler i Zulip
  
## Inviter Brugeren
Denne handling foretages ved at sende en mail fra OS2samtale@os2.eu
- Opret en mail til brugeren fra OS2Samtale@os2.eu
  - Inkluder link til OS2samtale [https://os2samtale.os2.eu/](https://os2samtale.os2.eu/)
  - Informer om at brugernavnet er mailaddressen
  - Inkluder link til secure Pasword (se opret pasword)
  - Informer om hvilke grupper brugeren er tilknyttet og hvilke brugerrettigheder denne har
  - Inkluder ling til code of conduct (når denne er på plads)
- Opret evt en mail til den der har anmodet om at få brugeren oprettet og informer om at det er sket. 
