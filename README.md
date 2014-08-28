Elasticsearch Powered Magento Fulltext Search
================================================================================
This is a fork of https://github.com/jreinke/magento-elasticsearch.
Unfortunatley [jreinke](https://github.com/jreinke) stoped development on this.

The module is based on [Elastica](https://github.com/ruflin/Elastica) 1.3 and
should support Elasticsearch 1.3.

As improvements it includes search by option attributes and category names.
Search by option attributes adds dropdown values to the search index so you can
search for the same values as you see in filteres (e.g. color "red"). Search
by category names is disabled by default but I found it very handy if somebody
enters a category name you will see all products in that category (e.g.
"chairs").


Installation
--------------------------------------------------------------------------------
Just plain composer install for magento. Additionally it needs a mage module for
including composer autoloading. That's not included in composer requirements to
leave the choice to you. I recommend
[firegento/psr0autoloader](https://github.com/magento-hackathon/Magento-PSR-0-Autoloader).


Usage
--------------------------------------------------------------------------------

* Go to System > Configuration > Catalog > Catalog Search
* Select Elasticsearch search engine
* Configure server connection parameters
* Specify index name (default is magento)
* Optionally enable search by category names
* Optionally defines your custom search parameters
* Optionally boost some product attributes in Catalog > Attributes > Manage Attributes
* Reindex catalog search index
