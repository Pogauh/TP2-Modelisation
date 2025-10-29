```mermaid
flowchart TD
  Start[Start]
  Collect[Collecte opt-in]
  Store[Enregistrement & vérif double opt-in]
  Segment[Segmentation listes]
  Send[Envoi campagne]
  Track[Suivi ouverture / clics]
  Unsub[Traitement désinscription]
  Purge[Purge si demandé]
  End[End]

  Start --> Collect --> Store --> Segment --> Send --> Track
  Track --> Unsub --> Purge --> End

```