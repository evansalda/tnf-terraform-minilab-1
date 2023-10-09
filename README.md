# Introduction

Tout au long de ce module, vous réaliserez des exercices qui vous donneront l’occasion de mettre en application les notions de terraform qui vous sont présentées.

Pour chaque exercice, vous créerez le répertoire nuumfactory-labs/mini-lab/exercice-\<numéro-d'exercice\> dédié à l'exercice en question.

Vous créerez ensuite dans ce répertoire un fichier **provider.tf** avec le contenu suivant :

```
provider "aws" {
  region = "eu-west-3"
  profile = "nuumfactory-student"
}
```