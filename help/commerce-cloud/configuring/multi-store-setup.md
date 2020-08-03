---
title: Multi-Store Setup
description: Multi-Store Setup
---

# Multi-Store Setup {#multi-store}

The AEM CIF Core Components can be used on multiple AEM site structures and the underlying GraphQL client implementation can connect to different Magento stores / store views. This allows projects to implement complex multi-store / multi-site setups.

A video walkthrough detailing options for integrating multiple Magento Store Views with Adobe Experience Manager Sites. 

>[!VIDEO](https://video.tv.adobe.com/v/28952/?quality=12)

AEM Multi-Site Management features of Live Copy and Language Copy are used in conjunction with the Commerce Integration Framework to globally manage sites across regions and locales.

The recommended setup is to use a 1:1 relationship between AEM site and Magento store view.

To connect an AEM site and AEM CIF Core Components so too to a dedicated store view follow the steps below:

## Configuration {#configuration}

1. Configure multiple stores & store views according to the pattern described in [Magento Websites, Stores & Views](https://docs.magento.com/m2/ce/user_guide/stores/websites-stores-views.html)

2. Make sure the connection between AEM & Magento is working.

3. Create a child configuration of the CIF Cloud Service config following these steps:

   * In AEM go to Tools -> General -> Configuration Browser
   * Select the base configuration you created
   * Create a new configuration using the steps described at point 2 above

    This new configuration will be created as a child configuration of the base one. You can now go to Tools -> General -> Configuration Browser and create the configuration settings.

4. Assign the child configuration to an AEM site

   * Go to AEM Sites console
   * Navigate to the region or language root of your site structure e.g. /content/venia/us _or_ /content/venia/us/en for the Venia sample page
   * Select the page and open page properties
   * Select the Advanced tab
   * In the `Configuration` section select the configuration you created at step

## Additional Resources

* [Magento Websites, Stores & Views](https://docs.magento.com/m2/ce/user_guide/stores/websites-stores-views.html)
* [AEM CIF Core Components - Multi store / site configuration](https://github.com/adobe/aem-core-cif-components/wiki/configuration#multi-store--site-configuration)
* [Using Multi-Site Manager](https://docs.adobe.com/content/help/en/experience-manager-learn/sites/translation/multi-site-manager-feature-video-use.html)
* [Reusing Content: Multi Site Manager and Live Copy](https://helpx.adobe.com/experience-manager/6-5/sites/administering/using/msm.html)