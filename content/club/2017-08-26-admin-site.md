---
title: "Règles d'administration du site"
description: ""
author: "llicour"
date: 2017-08-26T19:28:00
draft: false
categories: ["club"]
tags: []
original_category: "bureau"
---

Règles d'administration au quotidien du site
Templates

Page principale

&nbsp;

Amélioration de la gestion des liens d'article
J'ai ajouté la fonctionnalité permettant d'avor plus que 3 liens dans les articles
Chacune des 3 zones peut maintenant contenir une infinité de sous-liens
&nbsp;
Il faut utiliser le caractère # comme délimiteur dans chacun des champs, en faisant attention de respecter le même nombre de sous champs (sinon, le champs est ignoré)
&nbsp;
Exemple 1 (valide) :
LienA : [http://linka#http://linkb#http](http://linka#http://linkb#http)://linkc
Texte du lienA : texte1#texte2#texte3
&nbsp;

Exemple 2 (invalide) :
LienA : [http://linka#http://linkb#http](http://linka#http://linkb#http)://linkc
Texte du lienA : texte1#texte2#texte3#texte4
&nbsp;

Dans l'exemple 1, 3 liens seront affichés, décrit par le champ A (texte1, text2 et text3)
Dans l'exemple 2, aucun lien ne sera affiché, car les 2 champs ne contiennent pas le même nombre de sous champs
&nbsp;
Backup
emplacement fichiers de backup
créer un backup
downloader fichier backup
purger vieux fichiers
&nbsp;
&nbsp;

Customisation du site
Override fichiers
/administrator/components/com_content/models/forms/article.xml

=&gt; /administrator/templates/system/forms/com_content/article.xml

(override possible avec plugin override-xml-forms)

article non publié par défaut à la création
article en vedette par défaut à la création

/layouts/joomla/content/intro_image.php

=&gt; /template/rt_isotope/html/layouts/joomla/content/intro_image.php

images d'intro des articles retaillées automatiquement en largeur 200 (=w200 sur google photo)

/components/com_content/views/article/tmpl/default_links.php

=&gt; /template/rt_isotope/html/com_content/article/default_links.php

les 3 champs liens d'article sont maintenant considérés comme des liste de valeur, avec # comme séparateur (permet d'avoir une infinité de liens d'article)

&nbsp;

&nbsp;

Extensions installées

&nbsp;

nom
lien
description

override-xml-forms
[http://icueproject.com/products/override-xml-forms](http://icueproject.com/products/override-xml-forms)

permet l'override de fichiers form xml (paramètres de formulaire)

KC Admin QuickIcons
[https://www.keashly.net/joomla/administration/kc-admin-quickicons](https://www.keashly.net/joomla/administration/kc-admin-quickicons)
Ajout de raccourcis dans le menu joomla