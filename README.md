magento_tips_tricks
===================

All Tips &amp; Tricks about Magento Development


. Open Magento admin panel

2. Go to System>Cache Management

3. Check all Cache types and in the Actions box select refresh

4. Then select all Cache types and in the Actions box select disable

5. Also click Flush Magento Cache and Flush Cache Storage buttons

```
 rm -rf var/* 
```

```
clear_cache.php
```

```php
$mage_filename = 'app/Mage.php';
require_once $mage_filename;
umask(0);
Mage::run();
Mage::app()->cleanCache();
```


#### Magento theme
http://info.magento.com/rs/magentocommerce/images/Nirvana_Wiese_ClassyLlama_Fitness%20Center_Final.pdf
