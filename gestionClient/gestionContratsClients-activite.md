```mermaid
flowchart TD
  Start[Start]
  Create[Création contrat]
  Store[Enregistrement contrat]
  Bill[Émission facture périodique]
  Send[Envoi facture au client]
  Receive[Réception paiement]
  Reconcile[Lettrage & rapprochement]
  Archive[Archivage 10 ans]
  End[End]

  Start --> Create --> Store --> Bill --> Send --> Receive --> Reconcile --> Archive --> End

```