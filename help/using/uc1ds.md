---
title: Configuring the data source
seo-title: Configuring the data source
description: Configuring the data source
seo-description: Learn how to configure the data source for journey simple use case
page-status-flag: never-activated
uuid: 269d590c-5a6d-40b9-a879-02f5033863fc
contentOwner: sauviat
products: SG_CAMPAIGN/CLASSIC
audience: rns
content-type: reference
topic-tags: journeys
discoiquuid: 5df34f55-135a-4ea8-afc2-f9427ce5ae7b
index: n
internal: n
snippet: y
---

# Configuring the data source {#concept_ax3_bcy_w2b}

In our use case, we want to use personalization data for our messages. We also need to check is the person is a woman. This information is stored in the Unified Profile database. The **technical user** needs to check that those fields are defined in the built-in Experience Platform data source.

For additional information on data source configuration, refer to [Configuring a data source](ds.md#concept_s1s_dqt_52b). 

1. In the top bar, click **Data Sources** and select the build-in Experience Platform data source.

![](assets/journey23.png)

1. In the field groups, check that the following fields are selected:

    * _person > name > firstName_
    * _person > name > lastName_
    * _person > gender_
    * _personalEmail > address_

1. Click **Save**.

The data source is now configured and ready to be used in your journey.