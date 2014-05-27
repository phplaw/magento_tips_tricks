Magento Development Tips and Tricks
===================

All Tips &amp; Tricks about Magento Development

There’s a setting called “Display demo store notice” in: 
```
System -> Configuration -> Design -> HTML Head 
```

*Change base url im magento*
```
select * from core_config_data where path like '%base%url%';
update core_config_data set value = 'http://domainname/' where path = 'web/unsecure/base_url'; update core_config_data set value = 'http://domainname/' where path = 'web/secure/base_url';
```

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

#### Magento Books
http://www.packtpub.com/magento-1-8-development-cookbook-2e/book

http://www.magentocommerce.com/knowledge-base/entry/ce18-and-ee113-installing#install-sample

http://www.magentocommerce.com/knowledge-base/entry/installing-the-sample-data-for-magento

http://www.magentocommerce.com/wiki/recover/restore_base_url_settings
http://jagdeepbanga.com/blog/magento-get-base-url-skin-url-media-url-js-url-store-url-and-current-url.html

### Have to read
http://docs.nexcess.net/article/changing-magento-base-urls.html
### Magento extensions
http://www.iwdextensions.com/magento-one-step-checkout-module.html
### Sites was built with Magento
http://www.vipplaza.com/


### Magento events
http://www.magentocommerce.com/wiki/5_-_modules_and_development/reference/magento_events
http://magento.stackexchange.com/questions/10662/watching-add-to-cart-event-quote-item-id-is-empty
http://inchoo.net/ecommerce/magento/tracking-magento-add-product-to-cart-action-for-analytic-software-purpose/
http://magento.stackexchange.com/questions/4318/dynamically-calculated-prices-save-before-add-to-cart
http://www.magentocommerce.com/boards/viewthread/298696/
http://markshust.com/2012/08/27/create-checkout_cart_product_add_before-observer-magento

### Configuration Nginx for Magento
http://www.magentocommerce.com/wiki/1_-_installation_and_configuration/configuring_nginx_for_magento
http://ashsmith.co/2012/12/creating-a-faster-magento-store-part-one-server-setup/

