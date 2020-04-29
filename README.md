DHL Shipping Extension for Magento 2
================================================

The extension DHL Shipping is a plugin to integrate DHL logistics APIs into the Magento 2 platform's
order processing workflow. 

This is a *meta package*, which means it is a compilation of several other composer packages
that only together enable the functionality of the plugin.

Please see the file `composer.json` for the full list of included packages.

## Requirements and Compatibility

Generally, DHL Shipping is compatible with PHP 7.0.6 and later, and Magento 2.2.6 and later.

Please see the packages required in `composer.json` for detailed system requirements.

## Installation Instructions

Install sources:

    composer require dhl/shipping-m2

Refresh Magento 2 database and caches:

    ./bin/magento setup:upgrade
    ./bin/magento cache:flush
    ./bin/magento setup:di:compile

## Uninstallation

Please see the packages required in `composer.json` for individual uninstallation instructions.

To remove the metapackage from the application, run the following command:
    
    composer remove dhl/shipping-m2

## Support

In case of questions or problems, please have a look at the
[Support Portal (FAQ)](http://dhl.support.netresearch.de/) first.

If the issue cannot be resolved, you can contact the support team via the
[Support Portal](http://dhl.support.netresearch.de/) or by sending an email
to <dhl.support@netresearch.de>.

## License

[OSL - Open Software Licence 3.0](http://opensource.org/licenses/osl-3.0.php)

## Copyright

(c) 2020 Netresearch DTT GmbH
