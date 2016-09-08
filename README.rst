OXID eShop database migration related facts
===========================================

This component provides eShop database migration related information/facts with
the help of `eshop-facts <https://github.com/OXID-eSales/eshop-facts>`__.
Information on how to use ``oe-eshop-edition_facts`` script together with
``oe-eshop-facts`` can be found in the following
`README <https://github.com/OXID-eSales/eshop-facts/blob/master/README.rst>`__.

Output
------

The following information is provided after executing the script:

* ``ESHOP_CE_MIGRATION_PATH`` - Full path to eShop's migration folder dedicated
  to Community edition;
* ``ESHOP_PE_MIGRATION_PATH`` - Full path to eShop's migration folder dedicated
  to Professional edition;
* ``ESHOP_EE_MIGRATION_PATH`` - Full path to eShop's migration folder dedicated
  to Enterprise edition;
* ``ESHOP_PROJECT_MIGRATION_PATH`` - Full path to eShop's migration folder
  dedicated to custom migrations used within a project;

Keep in mind that it's possible to override any variable from the list above
by providing it as an environment variable, e.g. to change the path of eShop
project specific migration folder:

``ESHOP_PROJECT_MIGRATION_PATH=/var/www/project/migrations ./vendor/bin/oe-eshop-facts oe-eshop-migration_facts``

Input
-----

The following environment variables are accepted:

* ``VERBOSE`` - Enables verbose mode which prints out all facts to ``STDOUT``;
* ``ESHOP_VERBOSE_MIGRATION_FACTS`` - Enables verbose mode only for the current
  script.
