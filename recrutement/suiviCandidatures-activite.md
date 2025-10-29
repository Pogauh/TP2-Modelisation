```mermaid
flowchart TD
  Start[Start]
  Submit[Soumission candidature]
  Check[Contrôle complétude]
  Dup{Doublon ?}
  Merge[Confirmation / merge]
  Index[Indexation CV & création fiche]
  Score[Scoring automatique]
  Review[Pré-sélection RH]
  Share[Transmission manager]
  Archive[Plan purge 2 ans]
  End[End]

  Start --> Submit --> Check --> Dup
  Dup -- Oui --> Merge --> Index
  Dup -- Non --> Index
  Index --> Score --> Review
  Review --> Share --> Archive --> End

```