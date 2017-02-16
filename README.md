Escaping Quote Strategy for Doctrine
=====================================

As said in [Doctrine Documentation](http://docs.doctrine-project.org/projects/doctrine-orm/en/latest/reference/basic-mapping.html)
is you want to use protected keywords for table or column name you will have to explicitly use ticks in the definition.

This will break NamingStrategy provide by doctrine and required you to know what words are protected
in the database you use.

With this implementation of the QuoteStrategy interface you will not have to bother with it anymore.

Just add our EscapingQuoteStrategy to Doctrine configuration :

```php

$configuration->setQuoteStrategy(new EscapingQuoteStrategy());

```
