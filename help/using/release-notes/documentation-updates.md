---
title: Documentation Updates
description: Learn about documentation updates
page-status-flag: never-activated
uuid: 269d590c-5a6d-40b9-a879-02f5033863fc
contentOwner: sauviat
audience: rns
content-type: reference
topic-tags: journeys
discoiquuid: 5df34f55-135a-4ea8-afc2-f9427ce5ae7b
internal: n
snippet: y
---

# Documentation Updates

This page lists all the documentation updates for Journey Orchestration.
You can also consult the Journey Orchestration [Release Notes](../release-notes/release-notes.md).

## June 2020 {#june-2020}

* Added information on how to change the cache duration of the token for a custom authentication data source. [Read more](../datasource/external-data-sources.md#section_wjp_nl5_nhb)
* Updated screenshots and text to reflect the renaming of the **Finished** journey state which has been changed to **Closed (no entrance)**.
* Added information on how the language is defined for the interface. [Read more](../about/user-interface.md)
* The list of statuses of an individual's journey has been moved to the [Test mode logs](../building-journeys/testing-the-journey.md#viewing_logs) section. 

## April 2020 {#april-2020}

* Added a new section on experience event schema definition to help users configure their first event. [Read more](../event/experience-event-schema.md)
* The home page for Journey Orchestration documentation has been updated with additionnal useful links. [Read more](../../journey-orchestration-home.md)

## March 2020 {#march-2020}

* Added parameter descriptions for _actionExecutionErrors_ and _fetchErrors_ in test logs section. [Read more](../building-journeys/testing-the-journey.md#viewing_logs)
* The limitations on custom actions used in a journey have been updated. You can also modify the **URL** field and the **Authentication** parameters. [Read more](../action/about-custom-action-configuration.md)
* New contexual help entries have been added. The custom authentication payload pane (in actions and data sources) now includes a help icon that links to this [section](../datasource/external-data-sources.md#section_wjp_nl5_nhb). 
* Closed journeys can now be stopped. [Read more](../building-journeys/using-the-journey-designer.md)
* The interface description section has been reorganized. [Read more](../about/user-interface.md)
* The triggering of multiple events has been added to the Test mode section [Read more](../building-journeys/testing-the-journey.md#firing_events)
* The Test mode section has been updated regarding the new **Wait time in test** parameter. [Read more](../building-journeys/testing-the-journey.md)
* The Test log section has been updated with external call error codes and responses. [Read more](../building-journeys/testing-the-journey.md#viewing_logs)
* Timezone management is now centralized in the journey properties panel. Read more [here](../building-journeys/changing-properties.md#timezone) and [here](../building-journeys/timezone-management.md)
* The Journey designer section has been updated to reflect recent enhancements. [Read more](../building-journeys/using-the-journey-designer.md)
* The interface description has been updated with information on contextual help. [Read more](../about/user-interface.md#section_ksq_zr1_ffb)
* When browsing **XDM fields**, the friendly name is now displayed. Related sections have been updated. [Read more](../about/user-interface.md#friendly-names-display)

## February 2020 {#february-2020}

* The shortcut section has been udpated. The **C** keyboard shortcut allows you to create a new item in all list screens. [Read more](../about/user-interface.md#section_ksq_zr1_ffb)
* The [data source](../datasource/about-data-sources.md) and [action](../action/action.md) overview pages have been improved.

## January 2020 {#january-2020}

* Fetching limitations have been added for [experience events](../datasource/adobe-experience-platform-data-source.md) and [segments](../functions/functioninsegment.md).
* The [getBestSendTime documentation](../functions/functiongetbestsendtime.md) has been updated.

## December 2019 {#december-2019}

* All screenshots have been updated to reflect interface changes.
* The test mode section has been updated. [Read more](../building-journeys/testing-the-journey.md)
* A warning has been added in the [email send time optimization](../building-journeys/wait-activity.md) and [predictive fatigue scores](../usecase/leveraging-fatigue-scores.md) sections. These capabilities are only available to customers who use the Adobe Campaign Standard Data Service feature.
* Stopped journeys can now be deleted. Related documentation pages have been updated.
* Two colors are now displayed when issues are detected in a journey. Red for errors and orange for warnings. [Read more](../about/troubleshooting.md)
* The advanced expression editor section has been updated. [Read more](../expression/expressionadvanced.md).
* [Conditional instruction](../expression/conditional-instruction.md) and [Collection management](../expression/collection-management-functions.md) sections have been moved and updated.
* The [functions](../expression/functions.md) section has been updated with new examples.
* The [toDateTime function](../functions/functiontodatetime.md) documentation has been updated to reflect timezone syntax changes.
