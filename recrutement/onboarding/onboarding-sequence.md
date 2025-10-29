```mermaid
sequenceDiagram
  actor NEW as "Nouveau employé"
  participant ONB as "Onboarding Sys"
  participant ES as "e-Sign"
  participant HRC as "HR Core"
  participant PAY as Paie
  participant IAM as "IAM / IT"

  NEW ->> ONB: Upload pièces (CNI, RIB, diplômes)
  ONB ->> ONB: Vérif complétude & formats
  ONB ->> ES: Soumettre contrat pour signature
  ES -->> ONB: Statut signé
  ONB ->> HRC: Création dossier + matricule
  ONB ->> PAY: Transmission RIB & paramètres paie
  ONB ->> IAM: Création comptes & rôles
  IAM -->> ONB: Identifiants provisoires
  ONB ->> NEW: Envoi welcome pack

```