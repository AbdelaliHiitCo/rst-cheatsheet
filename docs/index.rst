IadCbBundle
===========

Iad club business Bundle

|Build Status|

|SensioLabsInsight|

Bundles
-------

-  `IadClubBusinessBundle </IadClubBusinessBundle/README.md>`__: Club
   business bundle
-  `IadTrainingBundle </IadTrainingBundle/README.md>`__:

Installation
------------

Require the **iad-holding/cb-bundle** package in your ``composer.json``
and update your dependencies.

::

    $ composer require iad-holding/cb-bundle

Register the bundle in the ``app/AppKernel.php``:

.. code:: php

    // app/AppKernel.php
    public function registerBundles()
    {
        return array(
            // club business
            new Iad\Bundle\ClubBusinessBundle\IadClubBusinessBundle(),

            // RcpBundle
            new Iad\Bundle\TrainingBundle\IadTrainingBundle(),
        );
    }

Doctrine
--------

Add bundles to mapping:

.. code:: yaml

    doctrine:
        orm:
            auto_mapping: false
            mappings:
                IadClubBusinessBundle: ~
                IadTrainingBundle: ~

Tests
-----

Install dependencies:

::

    $ composer install

Run test:

::

    $ phpunit [--coverage-html <path>]

.. |Build Status| image:: http://jenkins.iadholding.com/buildStatus/icon?job=CbBundle/develop
   :target: http://jenkins.iadholding.com/buildStatus/icon?job=CbBundle/develop
.. |SensioLabsInsight| image:: https://insight.sensiolabs.com/projects/0653dd4e-a9e5-41b9-bdc6-c77ac0d2c790/mini.png
   :target: https://insight.sensiolabs.com/projects/0653dd4e-a9e5-41b9-bdc6-c77ac0d2c790
