# Ckeditor-4-Typesetter

* The zip's are a replacement of the directory include/thirdparty/ckeditor.

* The plugins are for manual installation. 

* >> Here<a href=https://ckeditor.com/cke4/builder/download/85e2cfe7d2261e150e06ec1a20267d6e target=_blank> always the newest version</a>.

* Older Versions - also for Typesetter 5.1.1 - are at <a href=http://typesetter5.bplaced.net/Ckeditor target=_blank> Bplaced</a>.

Ckeditor.com offers several skins for ckeditor. <hr>
2/2025 : Ckeditor4 has now several skins for choice : The skin can be changed with an entry in the <a href="https://github.com/gtbu/Typesetter-5.3-p8/blob/main/include/thirdparty/ckeditor/config.js">config.js</a> : config.skin =

*For Typesetter exists also a <a href=https://github.com/gtbu/CKE_Themes > skinswitcher-plugin </a> for installation under /addons. The master from 3/2025 has an inbulit Skin-switch.

*** Many users will since 2025 get a popup that version 4.21 is not quite safe and should be replaced with version 4.24 LTS .
The LTS - version needs a commercial license !
*** A momentary tip from  https://github.com/ckeditor/ckeditor4/issues/5519  :  Add in include/tool/Editing.php at line 640  :  'versionCheck'   => false,
*** At this line You can also enter Your license key  :    licenseKey: 'your-license-key', 

<hr size=1>
Ckeditor has a problem with bootstrap5-icons : < i... > < /i > which are removed automatic.

To configure CKEditor to allow the <i> tag with the bi bi-heart class, you can use the Advanced Content Filter (ACF) settings. 

Here are the steps: (Add in include/tool/Editing.php ~ at line 640 : )

1. Disable ACF:         Add the following line to your CKEditor configuration file:
   CKEDITOR.config.allowedContent = true;    //    This will disable the ACF and allow all HTML elements and attributes.

2. Customize ACF:   If you want to allow specific tags and attributes, you can configure the allowedContent option. For example:
   CKEDITOR.config.allowedContent = 'i[*];';         //     This will allow the <i> tag with any attributes.

3. Version Check: If you are encountering version-related security warnings, you can disable version checking by adding the following line to your configuration file:
   CKEDITOR.config.versionCheck = false;   //       This will prevent the warning about the version being insecure.

By following these steps, you should be able to configure CKEditor to allow the <i> tag .

<pre>                 'versionCheck'              => false,
					  'allowedContent'            => true,
					  'extraAllowedContent'		  => 'i[*],iframe[align,......
</pre>    
<hr size=1>

PLUGINS :

* Further plugins for manual installation in the CMS (under settings -> ckeditor) are at github (sestolab and akilli and others) and at pluginza.com (always watch dependencies! - some are old and incompatible with ckeditor 4.22)

* Manually added Plugins are installed under data/ckeditor. They are registered in data/ckeditor/config.php. 