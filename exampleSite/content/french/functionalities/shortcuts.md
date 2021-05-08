---
weight: 3210
title: "Raccourcis"
description: "Comment gérér les raccourcis clavier ?"
titleIcon: "fas fa-keyboard"
categories: ["Fonctionnalités"]
---

# Description
---

Par défaut des raccourcis clavier sont fournis pour permettre d'intéragir plus facilement avec le thème, mais il est possible de définir des raccourcis spécifique par le biais d'un minimum de configuration.  
Par exemple, il est possible d'obtenir la liste des raccourcis disponibles en utilisant le raccourci `Maj + k`.

# Définir un raccourci spécifique
---

Afin de définir un raccourci il faut suivre le process suivant (exemple avec le raccourci **example** du site du thème):

1. Définir la configuration générale du raccourci dans le fichier de configuration spécifique du site (*Cf. lignes surlignées ci-dessous*):
    {{< snippet
        file="templates/configuration/config.fr.toml"
        caption="config.toml (section [params])"
        codelang="toml"
        codeparam="linenos=inline,hl_lines=[\"10-18\"]"
    />}}
2. Définir les libellés informatifs du raccourci qui apparaitront dans le menu d'aide des raccourcis (dans le fichier de traduction *i18n* adéquat):
    {{< snippet
        file="templates/configuration/i18n.fr.yaml"
        caption="fr.yaml"
        codelang="yaml"
        codeparam="linenos=inline,hl_lines=[\"12-17\"]"
    />}}
3. Définir le code javascript associé au raccourci et appelé par le biais de la fonction définie à l'étape 1:
    {{< snippet
        file="templates/configuration/shortcuts.js"
        caption="shortcuts.js"
        codelang="js"
    />}}