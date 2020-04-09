## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/SIFRI28/LINHAX/edit/master/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/SIFRI28/LINHAX/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

<title>Calendrier du mois</title>
</head>
<body bgcolor="#FFFFFF" text="#000000">
 
<h1 style="font-family:Verdana,Arial; font-weight:normal">Calendrier du mois</h1>
 
<script type="text/javascript">
<!--
var d = new Date();
var dm = d.getMonth() + 1;
var dan = d.getYear();
if(dan < 999) dan+=1900;
calendrier(dm,dan);
 
function calendrier(mois,an) {
nom_mois = new Array
("Janvier","F&eacute;vrier","Mars","Avril","Mai","Juin","Juillet",
"Ao&ucirc;t","Septembre","Octobre","Novembre","D&eacute;cembre");
jour = new Array ("Lu","Ma","Me","Je","Ve","Sa","Di");
 
var police_entete = "Verdana,Arial"; /* police entête de calendrier  */
var taille_pol_entete = 3;           /* taille de police 1-7 entête de calendrier  */
var couleur_pol_entete = "#FFFF00";     /* couleur de police entête de calendrier  */
var arrplan_entete = "#000066";        /* couleur d'arrière plan entête de calendrier  */
var police_jours = "Verdana,Arial"; /* police affichage des jours  */
var taille_pol_jours = 3;           /* taille de police 1-7 affichage des jours  */
var coul_pol_jours = "#000000";     /* couleur de police affichage des jours  */
var arrplan_jours = "#D0F0F0";        /* couleur d'arrière plan affichage des jours  */
var couleur_dim = "red";        /* couleur de police pour dimanches  */
var couleur_cejour = "#FFFF00";        /* couleur d'arrière plan pour aujourd'hui  */
 
var maintenant = new Date();
var ce_mois = maintenant.getMonth() + 1;
var cette_annee = maintenant.getYear();
if(cette_annee < 999) cette_annee+=1900;
var ce_jour = maintenant.getDate();
var temps = new Date(an,mois-1,1);
var Start = temps.getDay();
if(Start > 0) Start--;
else Start = 6;
var Stop = 31;
if(mois==4 ||mois==6 || mois==9 || mois==11 ) --Stop;
if(mois==2) {
 Stop = Stop - 3;
 if(an%4==0) Stop++;
 if(an%100==0) Stop--;
 if(an%400==0) Stop++;
}
document.write('<table border="3" cellpadding="1" cellspacing="1">');
var entete_mois = nom_mois[mois-1] + " " + an;
inscrit_entete(entete_mois,arrplan_entete,couleur_pol_entete,taille_pol_entete,police_entete);
var nombre_jours = 1;
for(var i=0;i<=5;i++) {
  document.write("<tr>");
  for(var j=0;j<=5;j++) {
    if((i==0)&&(j < Start))
     inscrit_cellule("&#160;",arrplan_jours,coul_pol_jours,taille_pol_jours,police_jours);
    else {
      if(nombre_jours > Stop)
        inscrit_cellule("&#160;",arrplan_jours,coul_pol_jours,taille_pol_jours,police_jours);
      else {
        if((an==cette_annee)&&(mois==ce_mois)&&(nombre_jours==ce_jour))
         inscrit_cellule(nombre_jours,couleur_cejour,coul_pol_jours,taille_pol_jours,police_jours);
        else
         inscrit_cellule(nombre_jours,arrplan_jours,coul_pol_jours,taille_pol_jours,police_jours);
        nombre_jours++;
        }
      }
    }
    if(nombre_jours > Stop)
      inscrit_cellule("&#160;",arrplan_jours,couleur_dim,taille_pol_jours,police_jours);
    else {
      if((an==cette_annee)&&(mois==ce_mois)&&(nombre_jours==ce_jour))
        inscrit_cellule(nombre_jours,couleur_cejour,couleur_dim,taille_pol_jours,police_jours);
      else
        inscrit_cellule(nombre_jours,arrplan_jours,couleur_dim,taille_pol_jours,police_jours);
      nombre_jours++;
    }
    document.write("<\/tr>");
  }
document.write("<\/table>");
}
 
function inscrit_entete(titre_mois,couleurAP,couleurpolice,taillepolice,police) {
document.write("<tr>");
document.write('<td align="center" colspan="7" valign="middle" bgcolor="'+couleurAP+'">');
document.write('<font size="'+taillepolice+'" color="'+couleurpolice+'" face="'+police+'"><b>');
document.write(titre_mois);
document.write("<\/b><\/font><\/td><\/tr>");
document.write("<tr>");
for(var i=0;i<=6;i++)
  inscrit_cellule(jour[i],couleurAP,couleurpolice,taillepolice,police);
document.write("<\/tr>");
}
 
function inscrit_cellule(contenu,couleurAP,couleurpolice,taillepolice,police) {
document.write('<td align="center" valign="middle" bgcolor="'+couleurAP+'">');
document.write('<font size="'+taillepolice+'" color="'+couleurpolice+'" face="'+police+'"><b>');
document.write(contenu);
document.write("<\/b><\/font><\/td>");
}
//-->
</script>
