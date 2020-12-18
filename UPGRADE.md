The upgrade instructions are available at [OroCommerce website](https://doc.oroinc.com/backend/setup/upgrade-to-new-version/).

This file includes only the most important items that should be addressed before attempting to upgrade or during the upgrade of a vanilla Oro application.

Please also refer to [CHANGELOG.md](CHANGELOG.md) for a list of significant changes in the code that may affect the upgrade of some customizations.

## 4.2.0

The File storage component was implement. Directories `var/attchment` and `var/import-export` are no longer used as storage
and has been removed from the git source code.

Files from these directories must be moved to new locations:

 - files from `var/attachment` to `var/data/attachments`;
 - files from `var/attachment/protected_mediacache` to `var/data/protected_mediacache`;
 - files from `var/import-export` to `var/data/importexport`.
 
Files for import should be placed into `var/data/importexport/files` instead of `var/import_export/files`.

Files for product images import should be placed into `var/data/importexport/product_images` instead of `var/import_export/product_images`.

Directory `public/uploads` has been removed.

## 4.1.0

The minimum required PHP version is 7.3.13.

Upgrade PHP before running `composer install` or `composer update`, otherwise composer may download wrong versions of the application packages.

## 3.1.0

The minimum required PHP version is 7.1.26.

Upgrade PHP before running `composer install` or `composer update`, otherwise composer may download wrong versions of the application packages.
