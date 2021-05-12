# coding-standard

`composer require --dev rmx351/coding-standard`

phpcs.xml
```xml
<?xml version="1.0"?>
<ruleset xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:noNamespaceSchemaLocation="vendor/squizlabs/php_codesniffer/phpcs.xsd">
    <description>Rmx351 coding standard.</description>

    <arg name="colors" />
    <arg name="extensions" value="php" />
    <arg name="parallel" value="80" />

    <!-- Show progress -->
    <arg value="p" />
    <file>application/crm/model/Contract.php</file>

    <!-- Include all rules from the Rmx351 Coding Standard -->
    <rule ref="Rmx351CodingStandard" />
</ruleset>
```
composer.json
```json
"scripts": {
   "cs-check": "phpcs --standard=./phpcs.xml",
   "cs-fix": "phpcbf --standard=./phpcs.xml"
}
```
