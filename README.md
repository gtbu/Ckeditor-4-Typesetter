# Ckeditor-4-Typesetter

* The zip's are a replacement of the directory include/thirdparty/ckeditor.

* The plugins are for manual installation. 

* >> Here<a href=https://ckeditor.com/cke4/builder/download/85e2cfe7d2261e150e06ec1a20267d6e target=_blank> always the newest version</a>.

* Versions also for Typesetter 5.1.1 are at <a href=http://typesetter5.bplaced.net/Ckeditor target=_blank> Bplaced</a>.

Ckeditor.com offers several skins for ckeditor. 

For Typesetter exists a <a href=https://github.com/gtbu/CKE_Themes >
skinswitcher-plugin </a> for installation under /addons.

* Further plugins for manual installation in the CMS are at github (sestolab and akilli and others) and at pluginza.com (always watch dependencies! - some are old and incompatiuble)

*** Many users will now get a popup that version 4.21 is not quite safe and should be replaced with version 4.24 LTS .
The LTS - version needs a commercial license !
*** A momentary tip from  https://github.com/ckeditor/ckeditor4/issues/5519  :  Add in include/tool/Editing.php at line 640  :  'versionCheck'   => false,
*** At this line You can also enter Your license key  :    licenseKey: 'your-license-key', 

----------------------------------------------------------------------------------------------------
Ckeditor has a problem with bootstrap5-icons : < i... > < /i > which are removed automatic.

To configure CKEditor to allow the <i> tag with the bi bi-heart class, you can use the Advanced Content Filter (ACF) settings. Here are the steps:
1. Disable ACF:         Add the following line to your CKEditor configuration file:
   CKEDITOR.config.allowedContent = true;    //    This will disable the ACF and allow all HTML elements and attributes.

2. Customize ACF:   If you want to allow specific tags and attributes, you can configure the allowedContent option. For example:
   CKEDITOR.config.allowedContent = 'i[*];';         //     This will allow the <i> tag with any attributes.

3. Version Check: If you are encountering version-related security warnings, you can disable version checking by adding the following line to your configuration file:
   CKEDITOR.config.versionCheck = false;   //       This will prevent the warning about the version being insecure.

By following these steps, you should be able to configure CKEditor to allow the <i> tag .
