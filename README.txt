Levelten Fusion

fusion_core needs to be in sites/all/themes/ or sites/all/themes/contrib folder
levelten_starter needs to be in sites/all/themes or sites/all/themes/custom folder

starter theme .info file

Change name of levelten_starter to name of theme
In the .info file of levelten_starter, change css/levelten-starter-style.css to css/themename-style.css
This file includes classnames and ID's of all elements in the page.tpl.php file. Use this to add styles to main structure, background images and colors, sidebar changes to default headings and font, etceteras

Change the name of local-sample.css to local.css . This file is used to override styles declared within fusion_core, system core or contrib modules. Copy the selector into this file exactly as it was originally defined and override whatever properties are needed. DO NOT add this file to the css list within the .info file. Doing this will force it to load with your other stylesheets and can potentially be overriden by default styles. By not adding the name to .info it will load after all of the other stylesheets.

There are six additional stylesheets in the .info file, they are
blocks.css
  used for styling blocks that are not part of a view, selectors must reference blocks
views.css
  used for styling views, must reference a views classname or a custom views classname
panels.css
  used to override default panel styles, must reference panel or pane in selector
content.css
  used to style node content, try to reference node in selector
theme-skins.css
  custom skinr styles that only apply to current theme
default-skins.css
  reusable skins, do not add anything to this file without adding it to the default levelten_starter theme
  
CSS coding standards
Levelten follows the CSS conventions set by Drupal. http://drupal.org/node/302199 which includes �

Comments should use doxygen format to separate blocks of code related to sections of site. One line comments can be used to highlight a special case. 
Selectors should be on a single line with a space before the opening curly bracket
Tabs should be expanded and set to 2 spaces
Properties should be on a single line and listed alphabetically. When properties need to be created for specific browsers, ignore the extension when alphabetizing.

ex. 
  background: #FFF;
  -moz-border-radius: 3px;
  -webkit-border-radius: 3px;
  border-radius: 3px;
  color: #000;
  
Place properties with extensions before standards properties so they aren't overriden by browser extension.