<h1>jQuery responsiveMenu</h1>

<h2>Présentation</h2>

<p>jQuery responsiveMenu est un plugin jQuery dont la fonction est d'animer un menu "responsive".
<br>
<br>
Une démonstration du menu est visible <a href="http://www.bellefondblog.com/demo/responsive-menu/" target="_blank">ici</a>.
</p>

<h2>Licence</h2>

<p>GNU GENERAL PUBLIC LICENSE Version 3</p>

<h2>Requis avec le plugin</h2>
<ul>
	<li>jQuery 1.10.2 (Il est probable que le plugin fonctionne aussi avec des versions antérieures de jQuery, mais aucun test n'a été effectué),</li>
	<li>Le plugin jQuery Tap peut être utilisé en option.</li>
</ul>

<h2>Comment l'utiliser ?</h2>

<h3>Inclusion des fichiers CSS et JS nécessaires</h3>
<pre>
<link href="css/responsive-menu.css" rel="stylesheet" type="text/css">
<script type="text/javascript" src="js/jquery-1.10.2.min.js"></script>
<!-- jQuery Tap n'est pas obligatoire -->
<script type="text/javascript" src="js/jquery.tap.min.js"></script>
<script type="text/javascript" src="js/jquery.responsiveMenu.js"></script>
</pre>

<h2>Structure HTML</h2>

<pre>
&lt;nav class="responsive-menu clearfix" id="responsive-menu"&gt;
  &lt;ul&gt;
    &lt;li&gt;&lt;a href="#"&gt;Wordpress&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;&lt;a href="#"&gt;Zend Framework&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;&lt;a href="#"&gt;Php&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;&lt;a href="#"&gt;Java&lt;/a&gt;&lt;/li&gt;
    &lt;li&gt;&lt;a href="#"&gt;Android&lt;/a&gt;&lt;/li&gt;
  &lt;/ul&gt;
&lt;/nav&gt;
</pre>

<h2>Appel du plugin</h2>

<pre>
jQuery(document).ready(function ($) { 
    $('#responsive-menu').responsiveMenu(); 
});
</pre>

<h2>Options</h2>
<p>Les différentes options sont à passer sous la forme d’un objet littéral à la méthode responsiveMenu() :</p>

<pre>
    $('#responsive-menu').responsiveMenu({ 
	    slide                  : 'ul', 
	    action                 : 'tap, click', 
	    nomadDeviceScreenWidth : 568, 
	    duration               : 400, 
	    triggerClassName       : 'trigger', 
	    openClassName          : 'open', 
	    title                  : '&nbsp;'
}); 
</pre>
<p><i>Ces options sont celles par défaut.</i>
<br>
<br>
Détail des options :</p>

<table>
<thead>
<tr>
<th>Clef</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td> slide</td>
<td>Element qui est «slidé».<br /> Peut être une balise html, une classe css ou un id.<br /> <strong>Type: String, valeur par défaut: ul</strong></td>
</tr>
<tr>
<td> action</td>
<td>Evénement déclencheur.<br /> Pour que tap fonctionne il faut le plugin jQuery Tap.<br /> <strong>Type: String, <strong>valeur par défaut</strong>: tap, click</strong></td>
</tr>
<tr>
<td>nomadDeviceScreenWidth</td>
<td>Largeur en pixels de l&rsquo;écran à partir de laquelle le menu change d&rsquo;apparence.<br /> Doit correspondre à la valeur fixée dans la Media Query.<br /> <strong>Type: Number , <strong>valeur par défaut</strong>: 568</strong></td>
</tr>
<tr>
<td> duration</td>
<td>Vitesse du slide<br /> <strong>Type: Number or String, <strong>valeur par défaut:</strong>400</strong><br /> On peut utiliser les 3 chaines de caractères représentant une des trois vitesses prédéfinies dans jQuery &laquo;&nbsp;slow&nbsp;&raquo;,&nbsp;&raquo;normal&nbsp;&raquo;, ou &laquo;&nbsp;fast&nbsp;&raquo;</td>
</tr>
<tr>
<td> triggerClassName</td>
<td>Classe css s&rsquo;appliquant au trigger<br /> <strong>Type: String, <strong>valeur par défaut:</strong> trigger</strong></td>
</tr>
<tr>
<td>openClassName</td>
<td>Classe css s&rsquo;appliquant au container du menu lorsqu&rsquo;il est déplié<br /> <strong>Type: String, <strong>valeur par défaut:</strong>open</strong></td>
</tr>
<tr>
<td> title</td>
<td>Le titre du menu<br /> <strong>Type: String, <strong>valeur par défaut:</strong> &amp;nbsp;</strong></td>
</tr>
</tbody>
</table>

