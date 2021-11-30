# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

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
