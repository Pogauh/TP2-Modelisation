```mermaid
sequenceDiagram
  actor PROS as Prospect
  participant PL as "Plateforme MKT"
  participant MAIL as "Service Email"
  participant DB as "DB Marketing"

  PROS ->> PL: Opt-in + préférences
  PL ->> DB: Stocke consentement & prefs
  PL ->> PL: Segmentation (règles)
  PL ->> MAIL: Envoi campagne ciblée
  MAIL -->> PROS: Réception newsletter
  alt Désinscription
    PROS ->> PL: Demande désinscription
    PL ->> DB: Marquage & purge données
  end

```