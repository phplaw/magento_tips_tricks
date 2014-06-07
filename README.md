Magento Development Tips and Tricks
===================

All Tips &amp; Tricks about Magento Development
### Magento basic module
http://www.smashingmagazine.com/2012/03/01/basics-creating-magento-module/
Basically, to create a simple magento module, you have to create two files.
```
app/
  |- etc/module/{Package}_{ModuleName}.xml
  |- code/local/{Package}/{ModuleName}/config.xml
```
```
app/etc/module/{Package}_{ModuleName}.xml
```
example:
```
<?xml version="1.0" encoding="UTF-8"?>
<config>
    <modules>
        <SmashingMagazine_LogProductUpdate>

            <!-- Whether our module is active: true or false -->
            <active>true</active>

            <!-- Which code pool to use: core, community or local -->
            <codePool>local</codePool>

        </SmashingMagazine_LogProductUpdate>
    </modules>
</config>
```

That file will define module version, turn module on by default or not and give a place where module files will be stored in
```
app/code/(local|core|community)
```

  
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
http://www.magentocommerce.com/wiki/5_-_modules_and_development/0_-_module_development_in_magento/customizing_magento_using_event-observer_method
http://www.magentocommerce.com/wiki/5_-_modules_and_development/reference/magento_events
http://magento.stackexchange.com/questions/10662/watching-add-to-cart-event-quote-item-id-is-empty
http://inchoo.net/ecommerce/magento/tracking-magento-add-product-to-cart-action-for-analytic-software-purpose/
http://magento.stackexchange.com/questions/4318/dynamically-calculated-prices-save-before-add-to-cart
http://www.magentocommerce.com/boards/viewthread/298696/
http://markshust.com/2012/08/27/create-checkout_cart_product_add_before-observer-magento

### Configuration Nginx for Magento
http://www.magentocommerce.com/wiki/1_-_installation_and_configuration/configuring_nginx_for_magento
http://ashsmith.co/2012/12/creating-a-faster-magento-store-part-one-server-setup/
### Magento System Requirements
http://www.magentocommerce.com/knowledge-base/entry/how-do-i-know-if-my-server-is-compatible-with-magento

### Install Magento on server
```
wget http://www.magentocommerce.com/downloads/assets/1.9.0.1/magento-1.9.0.1.tar.gz
tar xvzf magento-1.9.0.1.tar.gz
mv magento your-directory-name
wget http://www.magentocommerce.com/downloads/assets/1.9.0.0/magento-sample-data-1.9.0.0.tar.gz
# http://www.magentocommerce.com/wiki/1_-_installation_and_configuration/installing_magento_via_shell_ssh
http://www.magentocommerce.com/index.php/getmagento/ce_patches/PATCH_SUPEE-2629_EE_1.12.0.0_v1.sh
http://www.magentocommerce.com/knowledge-base/entry/installing-sample-data-archive-for-magento-ce
```
### Magento installation guide
http://www.magentocommerce.com/knowledge-base/entry/ce18-and-ee113-installing
