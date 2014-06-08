

Option 1.
=========================
```php
<?php echo Mage::helper('catalog')->__('Text here');?>
```
Then add the text in ```app/locale/{lang_ISO}/Mage_Catalog.csv```
```
"Text here","Translation here"
```
Option 2.
=========================
```php
<?php echo $this->__('Text here');?>
```

Then add the text in ```app/design/frontend/{interface}/{theme}/locale/{lang_ISO}/translate.csv``` like this:
```
"Text here","Translation here"
```

To include links in the text follow this pattern:
```php
<?php echo $this->__('some <a href="%s">text here</a>', Mage::getUrl('some/url/here'));
```
Then add to your csv file this line:
```
"some <a href=""%s"">text here</a>","translated <a href=""%s"">text here</a>"
```
```%s``` is a placeholder that will be replaced by the second parameter of ```__``` method.
Also when adding it to the csv file make sure you double the quotes inside the text so ```<a href="%s"></a>``` should be added to the csv file like ```<a href=""%s""></a>```

If you need to know how to translate in static block, you should read this article:
http://jagdeepbanga.com/blog/magento_how_add_translation_ability_into_cms_page_or_static_block.html
