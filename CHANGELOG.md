# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## 2.9.0

### Added

- Select "Signed for by recipient" (Empfängerunterschrift) service with DHL Paket National shipments.
- Select "Postal Delivery Duty Paid" (PDDP) service with DHL Paket International shipments.
- Select "Closest Droppoint" (CDP) service with DHL Paket International shipments.

### Changed

- Switch from DHL Business Customer Shipping SOAP API to DHL Parcel DE Shipping REST API.
- The DHL Paket "Print Only If Codeable" config setting can no longer be updated in packaging popup.

### Fixed

- Prevent exception when loading return shipments with no shipment number in admin panel grid.
- Prevent type error when loading service charge amounts from module configuration.

## 2.8.0

### Added

- On the pickup location finder map in checkout, if available, show description of the building/facility etc. a service point is located within.
- The "Bulky Goods" service can now be booked with DHL Paket International shipments.
- Select endorsement (abandon, return) for international, undeliverable shipments.
- Select "Named Person Only" service with DHL Paket National shipments.
- Select "No Neighbor Delivery" service with DHL Paket National shipments.
- Link to Marketplace review page in module configuration.

### Changed

- The "Print Receiver Contact Details" configuration setting is replaced by a "Send Receiver Phone Number" setting that applies to cross-border shipments only.

### Fixed (Shipping Carriers)

- Improve handling of apartment addresses when splitting the recipient street.
- Prevent application crash when API returns empty response.
- Prevent broken styling in module configuration.
- Consider database prefixes in INTERNETMARKE carrier module.
- Calculation of initial packaging popup input field visibilities.

### Fixed (Deutsche Post Direkt)

- Prevent analysis actions on billing address updates.
- Consider website level configuration settings during cron analysis.
- Change deliverability status from "Undeliverable" to "Possibly deliverable" if address was (partially) corrected during address analysis.
- Replace redundant and confusing mass actions by one configurable mass action.
- Initialize orders with "Not analysed" status if "No Automatic Analysis" is configured.
- The configuration setting "automatically cancel" now has higher priority than "automatically put on hold".
- Display status value "Manually edited" in admin panel orders grid.
- Show address autocomplete suggestions in the customer account "Add New Address" form.


## 2.7.1

### Fixed

- Display tracking number in shipment confirmation emails during mass action, reported via issue [#6](https://github.com/netresearch/module-shipping-core/issues/6).
- Remove invalid LESS extend, reported via issue [#6](https://github.com/netresearch/module-shipping-ui/issues/6).
- Apply min length validator to DHL Paket post number input in checkout.

## 2.7.0

### Added

- Show extension-related news in the admin notification inbox.

### Fixed

- Prevent access of undefined array key when booking cross-border on-demand return shipments.
- Do not persist empty QR labels when booking cross-border on-demand return shipments.
- Replace deprecated XHR callback in checkout.
- Fix typing error in checkout service box (DE).

## 2.6.0

Magento 2.4.4 compatibility release

### Added

- Support for Magento 2.4.4

### Removed

- Support for PHP 7.1

## 2.5.0

### Added

- Validate module configuration in admin panel to check if everything is set up properly.
- Send return shipment labels to the customer email address.
- Select delivery locations of type _Parcel Shop_ (Paketshop) for orders with DHL Paket shipping method.
- Show metapackage version number in the _Post & DHL Shipping General Configuration_ group.
- Specify the email notification address for the _DHL Paket Parcel Outlet Routing_ service in packaging popup.
- Import _Return Receiver IDs_ configuration setting via CSV file.

### Changed

- Set selected delivery location as order shipping address.
- Configure the shipping method name as displayed in checkout in the DHL Parcel Germany _Checkout Presentation_ config group.
- Set the title of the _DHL Parcel Germany Returns_ carrier in its _General Settings_ config group.
- Show selected shipping product (instead of carrier title) as track title in the _Shipping and Tracking Information_ section of a shipment.

### Removed

- Obsolete _DHL Parcel Germany Returns_ config fields were removed.

### Fixed

- Display selected delivery location in checkout progress sidebar.

## 2.4.0

### Added

- Book the DHL Paket Warenpost International shipping product.
- Select the content type option "Commercial Goods" for dutiable shipments.

### Fixed

- Skip scheduled update of the Deutsche Post Internetmarke shipping product list if no API credentials are configured.

## 2.3.0

### Added

- Select DHL Paket or Deutsche Post shipping products per order during the Create Shipments mass action.
- Book the DHL Paket Europaket shipping product for EU shipments.

## 2.2.0

### Added

- Create return shipments in Magento Open Source admin panel.

## 2.1.0

### Added

- Magento 2.4.3 compatibility
- Offer DHL Paket Premium service for cross-border shipments.
- Print a logo image on DHL Paket shipping labels.
- Consider area-based customs regulations when booking shipping labels (postal codes and ranges).

### Changed

- Print order number instead of billing number as customer reference on return shipment labels.

### Fixed

- Roll back multi-package Deutsche Post Internetmarke labels on error.
- Prevent CSP violations when loading the location finder map in checkout.
- Prevent empty country dropdown in location finder.
- Display the Additional Fee (service charge) total in PDFs.
- Support database table prefixes.
- Prevent JS/Knockout error in checkout.

## 2.0.1

### Fixed

- Print country on Deutsche Post Internetmarke vouchers.
- Adjust module dependencies.

## 2.0.0

### Added

- Perform post-processing on street splitting algorithm results.
- Properly deduct stock from the correct MSI sources by installing the optional [Shipping Inventory module](https://github.com/netresearch/module-shipping-inventory)

### Changed

- Move to carrier agnostic shipping framework for increased compatibility with other carriers.

### Fixed

- Prevent obsolete service surcharges caused by updated cart or address.
- Allow special house number additions for addresses in Baden-Wuerttemberg
- Prevent services being booked on carts that became virtual after cart item changes.

## 1.5.1

### Changed

- Deutsche Post Direkt ADDRESSFACTORY module version 1.1.2
- Deutsche Post Direkt Autocomplete module version 1.1.1
- Deutsche Post Internetmarke module version 1.1.0
- Update DHL Parcel Germany carrier module to version 1.4.2
- Update DHL UI module to version 1.2.3

## 1.5.0

### Added

- Deutsche Post Internetmarke module version 1.0.0

### Changed

- Deutsche Post Direkt ADDRESSFACTORY module version 1.1.1
- Update DHL Parcel Germany returns module to version 1.1.1
- Update DHL Parcel Germany carrier module to version 1.2.0

## 1.4.0

Customs Regulations Release

### Changed

- Update DHL Parcel Germany carrier module to version 1.4.0
- Update DHL UI module to version 1.2.2
- Update Business Customer Shipping SDK to version 1.1.0

## 1.3.0

Deutsche Post Direkt Release

### Added

- Deutsche Post Direkt ADDRESSFACTORY module version 1.1.0
- Deutsche Post Direkt Autocomplete module version 1.1.0

### Changed

- Update Business Customer Shipping SDK to version 1.0.1
- Update DHL Parcel Germany carrier module to version 1.3.0
- Update DHL UI module to version 1.2.1

## 1.2.0

Magento 2.4 Compatibility Release

### Changed

- Update DHL Parcel Germany carrier module to version 1.2.0
- Update DHL Parcel Germany returns module to version 1.1.0
- Update DHL UI module to version 1.2.0

## 1.1.0

Deutsche Post Warenpost Release

### Changed

- Update DHL Parcel Germany carrier module to version 1.1.0
- update DHL Parcel Germany returns module to version 1.0.1
- Update DHL UI module to version 1.1.0

## 1.0.0

Initial release
