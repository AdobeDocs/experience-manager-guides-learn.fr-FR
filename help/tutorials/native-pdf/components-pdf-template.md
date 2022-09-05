---
title: Fonction de publication native d’un PDF | Composants d’un modèle de PDF
description: Découvrez les différents composants d’un modèle de PDF et comment les personnaliser et les configurer.
exl-id: 0ddb3b81-42ca-4a66-be7d-051a5175d53a
source-git-commit: a1367a6915e760e533bb984705f4be37596b5477
workflow-type: tm+mt
source-wordcount: '2275'
ht-degree: 0%

---

# Composants d’un modèle de PDF {#components-pdf-template}

Un modèle de PDF comporte quatre composants : Dispositions de pages, feuilles de style, ressources et paramètres. Vous pouvez créer un modèle en personnalisant ces composants individuels et en associant le modèle à un paramètre prédéfini de sortie lors de la génération d’une sortie de PDF. Les sections suivantes couvrent en détail ces composants et leur processus de personnalisation.


## Création et personnalisation de mises en page {#create-customize-page-layout}

Les paramètres du composant Mise en page vous permettent de concevoir la structure d’une page en définissant l’en-tête, le pied de page et la zone de contenu d’une page. L’éditeur de mise en page WYSIWYG vous permet de créer une mise en page pour différentes sections d’un PDF, telles que les pages de couverture recto et verso, le chapitre, la table des matières (table des matières), l’index, la page vierge, la liste des chiffres (LOF), la liste des tableaux (LOT), le glossaire ou de créer une mise en page pour une page personnalisée. Dans les paramètres du modèle de PDF, vous pouvez attribuer une mise en page avec différentes sections dans un PDF, qui sont ensuite utilisées pour générer la sortie du PDF.

### Création d’une mise en page {#create-page-layout}

>[!NOTE]
>
>Il existe des exemples de mise en page prêts à l’emploi. Vous pouvez les personnaliser ou créer de nouvelles mises en page.

1. Dans l’éditeur Web, accédez à la **Sortie** .
1. Développez la barre latérale gauche et cliquez sur **Modèles**.
1. Ouvrez le modèle que vous souhaitez utiliser.
   >[!NOTE]
   >
   >Vous pouvez ouvrir un modèle en double-cliquant sur son nom ou en cliquant sur l’icône > située en regard de son nom.
1. Pour créer une mise en page, effectuez l’une des opérations suivantes :
   * Survol **Disposition de page** et cliquez sur (*Options* icon) **...** et choisissez **Nouvelle mise en page**.
   * Dans le **Modèles** , cliquez sur le panneau **+** en regard de **Modèles** et choisissez **Disposition de page** dans le menu contextuel.

      La boîte de dialogue Ajouter une mise en page s’ouvre alors.

      <img src="assets/add-layout-2.png" alt="Boîte de dialogue Ajouter une mise en page" width="250">
1. Attribuez un nom à la nouvelle mise en page.
   >[!NOTE]
   >
   >Évitez d’utiliser des caractères spéciaux lors de l’attribution d’un nom à une mise en page. Un espace dans le nom est remplacé par un trait de soulignement &quot;_&quot;.
1. Cliquez sur **Terminé**.

   La nouvelle mise en page est créée et ajoutée sous Mises en page .

### Dupliquer une mise en page {#duplicate-page-layout}

1. Dans le **Modèles** du modèle à dupliquer, double-cliquez sur **Disposition de page** ou cliquez sur le bouton **>** avant **Disposition de page**.

   Cette option affiche la liste des mises en page dans le modèle.

1. Pointez sur la mise en page à dupliquer, puis cliquez sur (*Options* icon) **...** et sélectionnez **Dupliquer** dans le menu contextuel.

1. Dans le _Dupliquer la mise en page_ , saisissez le nom de la mise en page.

1. Cliquez sur **Terminé**.
Une copie de la mise en page sélectionnée est créée et ajoutée sous Mises en page.

### Personnalisation de la mise en page {#customize-page-layout}

1. Dans le **Modèles** du modèle à modifier, double-cliquez sur **Disposition de page** ou cliquez sur le bouton **>** avant **Disposition de page**.

   Cette option affiche la liste des mises en page dans le modèle.
1. Pour personnaliser n’importe quelle mise en page, effectuez l’une des opérations suivantes :
   * Double-cliquez sur une mise en page.
   * Pointez sur une mise en page, puis cliquez sur (*Options* icon) **...** et sélectionnez **Modifier** dans le menu contextuel.

   L’éditeur de mise en page s’ouvre alors pour une personnalisation.
1. Une fois que vous avez apporté les modifications souhaitées, cliquez sur *Enregistrer tout* (ou `Crl+S`).

   Pour plus d’informations sur la définition d’éléments de disposition individuels tels que l’en-tête, le pied de page, le numéro de page, le titre, etc., voir [Concevoir une mise en page](design-page-layout.md).

## Utiliser des feuilles de style pour personnaliser PDF {#stylesheet-customization}

Les paramètres du composant Feuilles de style vous permettent de mettre en forme les composants de mise en page et le contenu DITA à l’aide de l’éditeur WYSIWYG ou de travailler directement avec le fichier CSS. Vous pouvez créer vos propres styles ou personnaliser les propriétés de style par défaut. L’éditeur WYSIWYG vous donne accès à la plupart des propriétés dont vous avez besoin pour mettre en forme votre mise en page ou votre contenu DITA. Pour les personnalisations avancées, vous pouvez travailler directement en mode Source.

### Créer une nouvelle feuille de style {#create-stylesheet}

Bien que les fichiers CSS soient fournis pour le contenu et la mise en page, vous pouvez créer une feuille de style pour appliquer plusieurs personnalisations à un type de style spécifique qui peut ensuite être appliqué à un composant cible. Par défaut, les exemples de fichiers CSS sont regroupés dans le produit. Ces fichiers CSS ont pour but de vous aider à organiser vos informations de style dans le contenu et les mises en page. Vous pouvez choisir de fusionner ces styles dans un ou plusieurs fichiers CSS.

Par défaut, chaque fois que vous créez une mise en page, la variable `layout.css` est inclus dans la nouvelle mise en page. Si vous souhaitez que la mise en page contienne des styles provenant d’un autre fichier CSS, vous pouvez simplement faire glisser et déposer le fichier CSS de votre choix dans la zone d’édition du contenu de la nouvelle mise en page. Pour vérifier si le fichier CSS a été incorporé dans la mise en page, passez en mode Source et vous trouverez un lien vers le fichier CSS dans la variable `<head>` élément .


Pour créer une feuille de style, procédez comme suit :
1. Dans le **Modèles** effectuez l’une des opérations suivantes :
   * Passez la souris sur le **Feuilles de style** et cliquez sur l’icône (*Options* icon) **...** et choisissez **Nouvelle feuille de style**.
   * Cliquez sur le bouton **+** en regard de **Modèles** et choisissez **Feuille de style** dans le menu contextuel.

   La boîte de dialogue Ajouter une feuille de style s’ouvre alors.

   <img src="assets/add-stylesheet.png" alt="Ajouter une feuille de style" width="250">
1. Attribuez un nom à la nouvelle feuille de style.
1. Cliquez sur **Terminé**.

   Une nouvelle feuille de style est créée et ajoutée sous la section Feuilles de style .

### Création d’un style {#create-style}

Par défaut, les fichiers CSS contiennent des styles pour les styles d’en-tête, de paragraphe, de caractère, d’hyperlien, d’image, de tableau, de balise div, de page et d’autres styles. Vous pouvez remplacer le format de style par défaut ou créer un nouveau style.

En règle générale, vous créez un style lorsque vous souhaitez associer un style personnalisé à un élément DITA. Pour que ces styles personnalisés fonctionnent, vous devez vous assurer que vous associez le nom de classe du style à l’attribut outputclass de l’élément DITA.


Pour créer un style, procédez comme suit :
1. Cliquez avec le bouton droit de la souris sur un style, puis choisissez Nouveau style dans le menu contextuel.

   La boîte de dialogue Ajouter un style s’ouvre.

   <img src="assets/add-style.png" alt="Ajouter un style" width="300"/>
1. Dans le **Balise** , choisissez une balise pour laquelle vous souhaitez créer un style.
1. Spécifiez un **Classe** nom.

   Ce nom de classe doit être associé à l’attribut outputclass de la balise dans votre contenu source.
1. Sélectionnez une **Classe Pseudo** pour un style amélioré de l’élément.
1. Cliquez sur **Terminé**.

   Un nouveau style est créé et ajouté sous le style de base.

### Personnalisation d’un style prédéfini ou nouveau {#customize-style}

Une fois que vous avez créé un fichier CSS avec des styles par défaut ou que vous souhaitez personnaliser les styles dans un fichier CSS existant, vous pouvez utiliser l’éditeur de styles pour ce faire.

Pour personnaliser un style, procédez comme suit :
1. Double-cliquez sur **Feuilles de style** ou cliquez sur le bouton **>** avant **Feuilles de style**.

   Il affiche les fichiers CSS par défaut (Contenu et mise en page) et personnalisés.
1. Ouvrez une feuille de style à modifier.

   Pour ouvrir une feuille de style en vue de la modifier, effectuez l’une des opérations suivantes :
   * Double-cliquez sur le nom de la feuille de style.
   * Placez le pointeur de la souris sur le nom de la feuille de style, cliquez sur l&#39;icône (Options)... et choisissez Modifier.

   Cette opération ouvre la feuille de style à modifier et affiche la liste des styles dans le panneau Styles.

   <img src="assets/customize-style.png" alt="Personnalisation du style" width="450">

1. Pour personnaliser un style, double-cliquez sur un style ou cliquez sur l’icône > devant un style pour l’afficher et le personnaliser à l’aide de l’éditeur de styles.

pour plus d’informations sur l’utilisation des styles les plus courants, voir [Utilisation des styles de contenu communs](stylesheet.md)

## Utilisation des ressources {#work-with-resources}

Il s’agit d’un conteneur pour toutes les ressources utilisées pour concevoir un modèle. Vous pouvez le considérer comme un dossier contenant des ressources telles que des images d’arrière-plan, des polices personnalisées, des logos, etc. Chaque fois que vous ajoutez une ressource dans votre modèle, elle est chargée ou archivée dans le dossier de ressources. Vous pouvez ensuite utiliser ces ressources pour personnaliser ou concevoir vos modèles de PDF.

Pour ajouter un fichier de ressource au dossier Resources, procédez comme suit :
1. Pointez sur l’onglet du dossier Ressources, cliquez sur l’icône (Options) ... et sélectionnez Importer.

   La boîte de dialogue Télécharger les ressources s’ouvre.

   <img src="assets/resources-import-assets.png" alt="Charger des ressources" width="300">

   Le chemin d’accès à l’emplacement où le fichier de ressource sera chargé est indiqué dans la variable **Sélectionner le dossier de ressources** champ .
   >[!NOTE]
   >
   >Vous ne pouvez pas modifier le chemin d’accès pour le chargement de ressources. Par défaut, toutes les ressources sont stockées sous la variable `/content/dam/dita-templates/pdf/<PDF-template-name>` dossier.

1. Cliquez sur **Choisir les fichiers** pour parcourir le fichier de ressources à partir de votre ordinateur local

1. Cliquez sur **Charger**.
Le fichier sélectionné est importé et répertorié sous le dossier Ressources .

## Paramètres du PDF avancé {#advanced-pdf-settings}

Utilisez la section Paramètres pour configurer les paramètres avancés de la mise en page du PDF, en commençant par une page impaire ou paire, des formats pour les références croisées et en activant les marques d’impression dans le PDF final généré à l’aide du modèle.

Pour configurer, cliquez sur **Paramètres** dans le **Modèles** pour afficher les options suivantes :

**Général**

Définissez les paramètres de configuration de base pour démarrer un chapitre à partir d’une page impaire ou pair, la structure de la table des matières et définissez le format de ligne de conduite pour les entrées de la table des matières. Vous pouvez définir les paramètres suivants :

* **Toujours commencer le chapitre à partir de**: Permet de définir comment chaque chapitre est publié dans le PDF final. Vous pouvez choisir parmi **Nouvelle page**, **Page impaire** ou **Page paire** options. Si vous choisissez de commencer un nouveau chapitre à partir d’une page impaire, une page vierge est insérée après un chapitre qui se termine sur une page impaire. Par exemple, si votre chapitre se termine à la page 15, le processus de publication insère un 16 vide.<sup>th</sup> afin que le nouveau chapitre puisse commencer à partir du 17<sup>th</sup> page.

* **Démarrage de chaque rubrique à partir d’une nouvelle page**: Si vous souhaitez que chaque rubrique de votre chapitre commence à partir d’une nouvelle page, sélectionnez **Démarrage de chaque rubrique à partir d’une nouvelle page** . Si vous souhaitez que vos rubriques se poursuivent sans espaces de page, désélectionnez cette option.

* **Structure de la table des matières**: Permet de personnaliser la hiérarchie de la table des matières. Il utilise les paramètres supplémentaires suivants :

   * **Utilisation des en-têtes jusqu’au niveau**: Il vous permet d’ajuster le nombre de niveaux d’en-tête à afficher dans la structure de table des matières de votre PDF.
   * **N’affichez pas le numéro de page du premier niveau dans la table des matières**: Sélectionnez cette option pour masquer les numéros de page correspondants pour tous les chapitres contenant des rubriques imbriquées ou enfants. Examinez l’exemple suivant dans lequel une sortie est créée sans sélectionner cette option.

   <img src="assets/page-number-in-toc.png" alt="Charger des ressources" width="250">

   Dans l’exemple ci-dessus, Paramètres avancés du PDF, Annexe et Mentions légales sont les en-têtes de rubrique ou les titres de chapitre de premier niveau. Un numéro de page est affecté à tous ces en-têtes.

   Maintenant, si vous sélectionnez cette option et générez la sortie, vous obtiendrez la table des matières suivante :
   <img src="assets/page-number-missing-in-toc.png" alt="Charger des ressources" width="250">

   Vous pouvez constater ici que le premier chapitre Paramètres avancés du PDF ne reçoit aucun numéro de page, car il contient des rubriques imbriquées ou enfants. En revanche, un numéro de page s’il est affecté à l’Annexe et aux Mentions légales, car il s’agit de rubriques autonomes sans rubrique enfant.

* **Format de filet**: Utilisez la liste déroulante pour sélectionner des lignes de filet de conduite en pointillé, Plein ou Espace afin de connecter les niveaux d’en-tête aux numéros de page correspondants.
Pour appliquer la structure de table des matières et le style des niveaux d’en-tête, voir [Ajout d’une table des matières de chapitre](design-page-layout.md#add-chapter-toc).

   >[!NOTE]
   >
   >Si vous êtes un développeur CSS, vous pouvez également définir le format de filet de conduite directement dans le fichier CSS.
* **Marqueur de continuation de tableau**: Sélectionnez cette option pour définir des marqueurs pour les tables longues qui s’étendent sur plusieurs pages. <!--For more information on using table continuation markers, see Use table continuation markers.-->

**Disposition de page**

Les paramètres de mise en page vous permettent de contrôler entièrement la spécification de la mise en page à utiliser pour une section spécifique de votre document. Par exemple, pour sélectionner une mise en page pour la table des matières, cliquez sur le menu déroulant sous le champ Table des matières et sélectionnez la mise en page que vous avez conçue pour générer la table des matières.

Si vous n’avez pas créé de mise en page pour une section spécifique de votre document, vous pouvez simplement choisir une mise en page qui sert de mise en page par défaut pour ces sections ou rubriques. La mise en page par défaut est ensuite appliquée à toutes les sections qui n’ont pas de mise en page dédiée.

De même, si vous souhaitez une page de couverture et une page précédente, une mise en page doit être créée et appliquée dans les paramètres. Sinon, votre PDF ne contiendra pas les pages de couverture et d’arrière-plan.


Pour plus d’informations sur les mises en page, voir [Concevoir une mise en page](design-page-layout.md).

**Imprimer**

Configurez les paramètres de production d’impression pour attribuer des repères d’impression, sélectionner des modèles de couleur et spécifier les propriétés liées à l’impression de la sortie de votre PDF.

* **Marques de l’imprimante**: Lors de la préparation d’un document en vue de l’impression, des repères d’impression sont ajoutés aux bordures de page afin de faciliter l’alignement, le rognage et la sélection des couleurs lors de l’impression. Si vous sélectionnez une marque d’imprimante, la limite de page est étendue pour s’adapter à la marque, qui est ajustée lors de l’impression. Vous pouvez choisir d’afficher les repères d’impression suivants dans la sortie de votre PDF :
   * **Traits de rognage**: Sélectionnez l’option permettant de placer une marque à chaque coin de la zone de rognage pour indiquer où le papier doit être coupé après impression.
   * **Marques de fond perdu**: Sélectionnez cette option pour placer une marque à chaque coin de la zone de fond perdu afin d’indiquer la zone de rognage de l’image étendue.
   * **Marques d’enregistrement**: Sélectionnez cette option pour placer une marque en dehors de la zone de recadrage afin d’aligner les différentes séparations dans un document de couleur.
   * **Bars de couleurs**: Sélectionnez cette option pour ajouter une bande de couleurs en dehors de la zone de rognage afin de maintenir la cohérence des couleurs et d’ajuster la densité de l’encre lors de l’impression.

   Définissez des dimensions pour les marques d’imprimante sélectionnées à l’aide du **Largeur de ligne**, **Couleur de ligne**, et **Largeur de la zone de fond perdu** options.

* **Taille de la zone de média**: Il s’agit de la taille globale de la page, y compris la zone étendue occupée par les repères d’impression. Utilisez l’option de liste déroulante pour sélectionner la taille de page de votre sortie de PDF ou créer votre propre taille personnalisée.

* **Espace colorimétrique**: Vous avez la possibilité de choisir parmi des espaces colorimétriques de RGB ou CMJN pour imprimer votre document de PDF. Sélectionnez RGB pour afficher le PDF généré numériquement et CMJN pour l’impression physique. Les couleurs définies dans le document sont converties dans l’espace colorimétrique choisi.
   >[!NOTE]
   >
   >Un profil colorimétrique ICC est nécessaire pour la création du PDF/A en cas d’utilisation de l’espace colorimétrique CMJN.

   <!--For more information on applying these print settings, see *Printing preferences*.-->

**Références croisées**

Utilisez l’onglet Référence croisée pour définir la manière dont les références croisées sont publiées dans le PDF. Vous pouvez mettre en forme les références croisées pour le titre de la rubrique, les tableaux, les chiffres, etc. <!--For more information, see *Format cross-references*.-->
