
Sous Chefs
-------------
**newslynx-sc-google-analytics** provides access to the following Sous Chefs

Google Analytics Pageviews by Device Type for content Items
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Computes the total pageviews for content items by device type.
-  This Sous Chef runs the python module
   ``newslynx_sc_google_analytics.ContentDeviceSummaries``.
-  API Slug: ``google-analytics-to-content-device-summaries``

Development
^^^^^^^^^^^

Pass runtime options to ``google-analytics-to-content-device-summaries``
and stream output. **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx sc newslynx_sc_google_analytics/google_analytics_to_content_device_summaries.yaml option=value1

Alernatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_google_analytics/google_analytics_to_content_device_summaries.yaml --recipe=recipe.yaml

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_google_analytics/google_analytics_to_content_device_summaries.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=google-analytics-to-content-device-summaries **options

Alerternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=google-analytics-to-content-device-summaries --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alernatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Options
^^^^^^^

In addition to default recipe options,
``google-analytics-to-content-device-summaries`` also accepts the
following

-  ``days``

   -  Should be rendered with a ``number`` form.
   -  Accepts inputs of type:

      -  ``numeric``

   -  Defaults to ``30``

-  ``content_item_types``

   -  Should be rendered with a ``text`` form.
   -  Choose from:

      -  ``video``
      -  ``article``
      -  ``slideshow``
      -  ``interactive``
      -  ``podcast``
      -  ``all``

   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``all``

Metrics
^^^^^^^

``google-analytics-to-content-device-summaries`` generates the following
Metrics

-  ``ga_pageviews_mobile``

   -  Display name: ``Mobile Pageviews``

   -  Type: ``count``

   -  Content Levels:

      -  ``summary``
      -  ``comparison``

   -  Org Levels:

      -  ``summary``

-  ``ga_pageviews_tablet``

   -  Display name: ``Tablet Pageviews``

   -  Type: ``count``

   -  Content Levels:

      -  ``summary``
      -  ``comparison``

   -  Org Levels:

      -  ``summary``

-  ``ga_pageviews_desktop``

   -  Display name: ``Desktop Pageviews``

   -  Type: ``count``

   -  Content Levels:

      -  ``summary``
      -  ``comparison``

   -  Org Levels:

      -  ``summary``



Google Analytics Domain Facets For Content Items
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Creates faceted metrics for pageviews by referrer for content items.
-  This Sous Chef runs the python module
   ``newslynx_sc_google_analytics.ContentDomainFacets``.
-  API Slug: ``google-analytics-to-content-domain-facets``

Development
^^^^^^^^^^^

Pass runtime options to ``google-analytics-to-content-domain-facets``
and stream output. **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx sc newslynx_sc_google_analytics/google_analytics_to_content_domain_facets.yaml option=value1

Alernatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_google_analytics/google_analytics_to_content_domain_facets.yaml --recipe=recipe.yaml

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_google_analytics/google_analytics_to_content_domain_facets.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=google-analytics-to-content-domain-facets **options

Alerternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=google-analytics-to-content-domain-facets --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alernatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Options
^^^^^^^

In addition to default recipe options,
``google-analytics-to-content-domain-facets`` also accepts the following

-  ``days``

   -  Should be rendered with a ``number`` form.
   -  Accepts inputs of type:

      -  ``numeric``

   -  Defaults to ``30``

-  ``max_facets``

   -  Should be rendered with a ``number`` form.
   -  Accepts inputs of type:

      -  ``numeric``

   -  Defaults to ``20``

-  ``content_item_types``

   -  Should be rendered with a ``text`` form.
   -  Choose from:

      -  ``video``
      -  ``article``
      -  ``slideshow``
      -  ``interactive``
      -  ``podcast``
      -  ``all``

   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``all``

Metrics
^^^^^^^

``google-analytics-to-content-domain-facets`` generates the following
Metrics

-  ``ga_pageviews_by_domain``

   -  Display name: ``Pageviews By Refering Domain``
   -  This is a **faceted** metric.

   -  Type: ``count``

   -  Content Levels:

      -  ``summary``

-  ``ga_pageviews_by_article_referrer``

   -  Display name: ``Pageviews By Refering article.``
   -  This is a **faceted** metric.

   -  Type: ``count``

   -  Content Levels:

      -  ``summary``



Google Analytics Timeseries For Content Items
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

-  Computes a timeseries of pageviews, entrances, and exits for content
   items.
-  This Sous Chef runs the python module
   ``newslynx_sc_google_analytics.ContentTimeseries``.
-  API Slug: ``google-analytics-to-content-timeseries``

Development
^^^^^^^^^^^

Pass runtime options to ``google-analytics-to-content-timeseries`` and
stream output. **NOTE** Will not execute the SousChef's ``load`` method.

.. code:: bash

    $ newslynx sc newslynx_sc_google_analytics/google_analytics_to_content_timeseries.yaml option=value1

Alernatively pass in a recipe file

.. code:: bash

    $ newslynx sc newslynx_sc_google_analytics/google_analytics_to_content_timeseries.yaml --recipe=recipe.yaml

API Usage
^^^^^^^^^

Add this Sous Chef to your authenticated org

.. code:: bash

    $ newslynx api sous-chefs create -d=newslynx_sc_google_analytics/google_analytics_to_content_timeseries.yaml

Create a Recipe with this Sous Chef with command line options.

.. code:: bash

    $ newslynx api recipes create sous_chef=google-analytics-to-content-timeseries **options

Alerternatively pass in a recipe file.

.. code:: bash

    $ newslynx api recipes create sous_chef=google-analytics-to-content-timeseries --data=recipe.yaml

Save the outputted ``id`` of this recipe, and execute it via the API.
**NOTE** This will place the recipe in a task queue.

.. code:: bash

    $ newslynx api recipes cook id=<id>

Alernatively, run the Recipe, passing in arbitrary runtime options, and
stream it's output: **NOTE** Will not execute the SousChef's ``load``
method.

.. code:: bash

    $ newslynx api recipes cook id=<id> --passthrough **options

Options
^^^^^^^

In addition to default recipe options,
``google-analytics-to-content-timeseries`` also accepts the following

-  ``days``

   -  Should be rendered with a ``number`` form.
   -  Accepts inputs of type:

      -  ``numeric``

   -  Defaults to ``30``

-  ``content_item_types``

   -  Should be rendered with a ``text`` form.
   -  Choose from:

      -  ``video``
      -  ``article``
      -  ``slideshow``
      -  ``interactive``
      -  ``podcast``
      -  ``all``

   -  Accepts inputs of type:

      -  ``string``

   -  Defaults to ``all``

Metrics
^^^^^^^

``google-analytics-to-content-timeseries`` generates the following
Metrics

-  ``ga_pageviews``

   -  Display name: ``Pageviews``

   -  Type: ``count``

   -  Content Levels:

      -  ``timeseries``
      -  ``summary``
      -  ``comparison``

   -  Org Levels:

      -  ``timeseries``
      -  ``summary``

-  ``ga_exits``

   -  Display name: ``Exits``

   -  Type: ``count``

   -  Content Levels:

      -  ``timeseries``
      -  ``summary``
      -  ``comparison``

   -  Org Levels:

      -  ``timeseries``
      -  ``summary``

-  ``ga_entrances``

   -  Display name: ``Entrances``

   -  Type: ``count``

   -  Content Levels:

      -  ``timeseries``
      -  ``summary``
      -  ``comparison``

   -  Org Levels:

      -  ``timeseries``
      -  ``summary``

-  ``ga_total_time_on_page``

   -  Display name: ``Total Time on Page``

   -  Type: ``count``

   -  Content Levels:

      -  ``timeseries``
      -  ``summary``
      -  ``comparison``

   -  Org Levels:

      -  ``timeseries``
      -  ``summary``

-  ``ga_avg_time_on_page``

   -  Display name: ``Average Time on Page``

   -  This is a **computed** metric with the formula:

      -  ROUND({ga\_total\_time\_on\_page} / NULLIF({ga\_pageviews}, 0),
         2)

   -  Content Levels:

      -  ``timeseries``
      -  ``summary``
      -  ``comparison``

   -  Org Levels:

      -  ``timeseries``
      -  ``summary``

-  ``ga_per_external``

   -  Display name: ``Percent External Traffic``

   -  This is a **computed** metric with the formula:

      -  ROUND({ga\_entrances} / NULLIF({ga\_pageviews}, 0), 2)

   -  Content Levels:

      -  ``timeseries``
      -  ``summary``
      -  ``comparison``

   -  Org Levels:

      -  ``timeseries``
      -  ``summary``

-  ``ga_per_internal``

   -  Display name: ``Percent Internal Traffic``

   -  This is a **computed** metric with the formula:

      -  ROUND(1 - ({ga\_entrances} / NULLIF({ga\_pageviews}, 0)), 2)

   -  Content Levels:

      -  ``timeseries``
      -  ``summary``
      -  ``comparison``

   -  Org Levels:

      -  ``timeseries``
      -  ``summary``


