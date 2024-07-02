# Symfony webapp

Opinionated [Composer](https://getcomposer.org) metapackage for [Symfony](https://symfony.com)-based web applications.

Why? Because modern web applications often require Webpack, the use of Symfony UX live components, sending HTML emails, pagination of results, and more.

## 🚀 Quick start

In a minimal Symfony installation:

```bash
composer require gremo/symfony-webapp
```

See [Creating Symfony Applications](https://symfony.com/doc/current/setup.html#creating-symfony-applications) to create a new (minimal) Symfony application.

If you are not using **Symfony CLI**:

```bash
curl -O https://raw.githubusercontent.com/symfony/skeleton/7.1/composer.json
composer install
```

## 🔍 How it is different

Here are the differences between the Symfony `webapp` metapackage and this project:

<!-- MARKDOWN-AUTO-DOCS:START (CODE:src=./.github/metadata/composer.diff) -->
<!-- The below code snippet is automatically added from ./.github/metadata/composer.diff -->
```diff
@@ -1,13 +1,16 @@
 {
-    "name": "symfony/webapp-pack",
+    "name": "gremo/symfony-webapp",
     "type": "symfony-pack",
     "license": "MIT",
-    "description": "A webapp pack on top of the default skeleton",
+    "description": "Opinionated Composer metapackage for Symfony-based web applications",
     "require": {
+        "babdev/pagerfanta-bundle": "^4.4",
+        "pagerfanta/doctrine-orm-adapter": "^4.6",
+        "pagerfanta/twig": "^4.6",
+        "stof/doctrine-extensions-bundle": "^1.12",
+        "symfony/apache-pack": "*",
         "symfony/asset": "*",
-        "symfony/asset-mapper": "*",
         "symfony/debug-pack": "*",
-        "symfony/doctrine-messenger": "*",
         "symfony/expression-language": "*",
         "symfony/form": "*",
         "symfony/http-client": "*",
@@ -27,9 +30,16 @@
         "symfony/test-pack": "*",
         "symfony/translation": "*",
         "symfony/twig-pack": "*",
+        "symfony/ux-live-component": "^2.18",
         "symfony/ux-turbo": "*",
+        "symfony/ux-twig-component": "^2.18",
         "symfony/validator": "*",
-        "symfony/web-link": "*"
+        "symfony/web-link": "*",
+        "symfony/webpack-encore-bundle": "^2.1",
+        "twig/cssinliner-extra": "^3.1",
+        "twig/html-extra": "^3.10",
+        "twig/inky-extra": "^3.10",
+        "twig/intl-extra": "^3.10"
     },
     "require-dev": {
         "symfony/debug-pack": "*",
```
<!-- MARKDOWN-AUTO-DOCS:END -->

## 📦 Packages

<!-- MARKDOWN-AUTO-DOCS:START (JSON_TO_HTML_TABLE:src=./.github/metadata/require.json) -->
<table class="JSON-TO-HTML-TABLE"><thead><tr><th class="package-th">Package</th><th class="version-th">Version</th><th class="packagist-th">Packagist</th></tr></thead><tbody ><tr ><td class="package-td td_text"><b>babdev/pagerfanta-bundle</b></td><td class="version-td td_text">^4.4</td><td class="packagist-td td_text">https://packagist.org/packages/babdev/pagerfanta-bundle</td></tr>
<tr ><td class="package-td td_text"><b>pagerfanta/doctrine-orm-adapter</b></td><td class="version-td td_text">^4.6</td><td class="packagist-td td_text">https://packagist.org/packages/pagerfanta/doctrine-orm-adapter</td></tr>
<tr ><td class="package-td td_text"><b>pagerfanta/twig</b></td><td class="version-td td_text">^4.6</td><td class="packagist-td td_text">https://packagist.org/packages/pagerfanta/twig</td></tr>
<tr ><td class="package-td td_text"><b>stof/doctrine-extensions-bundle</b></td><td class="version-td td_text">^1.12</td><td class="packagist-td td_text">https://packagist.org/packages/stof/doctrine-extensions-bundle</td></tr>
<tr ><td class="package-td td_text"><b>symfony/apache-pack</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/apache-pack</td></tr>
<tr ><td class="package-td td_text"><b>symfony/asset</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/asset</td></tr>
<tr ><td class="package-td td_text"><b>symfony/debug-pack</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/debug-pack</td></tr>
<tr ><td class="package-td td_text"><b>symfony/expression-language</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/expression-language</td></tr>
<tr ><td class="package-td td_text"><b>symfony/form</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/form</td></tr>
<tr ><td class="package-td td_text"><b>symfony/http-client</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/http-client</td></tr>
<tr ><td class="package-td td_text"><b>symfony/intl</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/intl</td></tr>
<tr ><td class="package-td td_text"><b>symfony/mailer</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/mailer</td></tr>
<tr ><td class="package-td td_text"><b>symfony/maker-bundle</b></td><td class="version-td td_text">^1.0</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/maker-bundle</td></tr>
<tr ><td class="package-td td_text"><b>symfony/mime</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/mime</td></tr>
<tr ><td class="package-td td_text"><b>symfony/monolog-bundle</b></td><td class="version-td td_text">^3.1</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/monolog-bundle</td></tr>
<tr ><td class="package-td td_text"><b>symfony/notifier</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/notifier</td></tr>
<tr ><td class="package-td td_text"><b>symfony/orm-pack</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/orm-pack</td></tr>
<tr ><td class="package-td td_text"><b>symfony/process</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/process</td></tr>
<tr ><td class="package-td td_text"><b>symfony/profiler-pack</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/profiler-pack</td></tr>
<tr ><td class="package-td td_text"><b>symfony/security-bundle</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/security-bundle</td></tr>
<tr ><td class="package-td td_text"><b>symfony/serializer-pack</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/serializer-pack</td></tr>
<tr ><td class="package-td td_text"><b>symfony/stimulus-bundle</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/stimulus-bundle</td></tr>
<tr ><td class="package-td td_text"><b>symfony/string</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/string</td></tr>
<tr ><td class="package-td td_text"><b>symfony/test-pack</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/test-pack</td></tr>
<tr ><td class="package-td td_text"><b>symfony/translation</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/translation</td></tr>
<tr ><td class="package-td td_text"><b>symfony/twig-pack</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/twig-pack</td></tr>
<tr ><td class="package-td td_text"><b>symfony/ux-live-component</b></td><td class="version-td td_text">^2.18</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/ux-live-component</td></tr>
<tr ><td class="package-td td_text"><b>symfony/ux-turbo</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/ux-turbo</td></tr>
<tr ><td class="package-td td_text"><b>symfony/ux-twig-component</b></td><td class="version-td td_text">^2.18</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/ux-twig-component</td></tr>
<tr ><td class="package-td td_text"><b>symfony/validator</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/validator</td></tr>
<tr ><td class="package-td td_text"><b>symfony/web-link</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/web-link</td></tr>
<tr ><td class="package-td td_text"><b>symfony/webpack-encore-bundle</b></td><td class="version-td td_text">^2.1</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/webpack-encore-bundle</td></tr>
<tr ><td class="package-td td_text"><b>twig/cssinliner-extra</b></td><td class="version-td td_text">^3.1</td><td class="packagist-td td_text">https://packagist.org/packages/twig/cssinliner-extra</td></tr>
<tr ><td class="package-td td_text"><b>twig/html-extra</b></td><td class="version-td td_text">^3.10</td><td class="packagist-td td_text">https://packagist.org/packages/twig/html-extra</td></tr>
<tr ><td class="package-td td_text"><b>twig/inky-extra</b></td><td class="version-td td_text">^3.10</td><td class="packagist-td td_text">https://packagist.org/packages/twig/inky-extra</td></tr>
<tr ><td class="package-td td_text"><b>twig/intl-extra</b></td><td class="version-td td_text">^3.10</td><td class="packagist-td td_text">https://packagist.org/packages/twig/intl-extra</td></tr></tbody></table>
<!-- MARKDOWN-AUTO-DOCS:END -->

Development packages:

<!-- MARKDOWN-AUTO-DOCS:START (JSON_TO_HTML_TABLE:src=./.github/metadata/require-dev.json) -->
<table class="JSON-TO-HTML-TABLE"><thead><tr><th class="package-th">Package</th><th class="version-th">Version</th><th class="packagist-th">Packagist</th></tr></thead><tbody ><tr ><td class="package-td td_text"><b>symfony/debug-pack</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/debug-pack</td></tr>
<tr ><td class="package-td td_text"><b>symfony/profiler-pack</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/profiler-pack</td></tr>
<tr ><td class="package-td td_text"><b>symfony/maker-bundle</b></td><td class="version-td td_text">^1.0</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/maker-bundle</td></tr>
<tr ><td class="package-td td_text"><b>symfony/test-pack</b></td><td class="version-td td_text">*</td><td class="packagist-td td_text">https://packagist.org/packages/symfony/test-pack</td></tr></tbody></table>
<!-- MARKDOWN-AUTO-DOCS:END -->

## ❤️ Contributing

All types of contributions are encouraged and valued. See the [contributing](.github/CONTRIBUTING.md) guidelines, the community looks forward to your contributions!

## 📘 License

Released under the terms of the [ISC License](LICENSE).
