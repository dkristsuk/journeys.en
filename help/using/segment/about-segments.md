---
title: About Platform segments
description: Learn how to configure a Platform segment
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

# About Platform segments {#about-segments}

>[!NOTE]
>
>The segment tab and the creation/modification of segments will be available on June 15th.

If you're using the [Platform Segmentation Service](https://docs.adobe.com/content/help/en/experience-platform/segmentation/home.html) to create your segments, you can leverage them in Journey Orchestration. Thanks to a dedicated event activity, you can make individuals enter or move forward in a journey based on Platform segment entrances and exits. This also allows you to build complex conditions in your journeys using the simple or advanced expression editor.

Let's say you have a "silver customer" segment. With this activity, you can make all new silver customers enter a journey and send them a series of personalized messages. You can alsdo easily build conditions based on this segment.

Here are the possibilities Journey Orchestration offer you with segments:

* Access the list of Platform segments. See [Creating a segment](../segment/creating-a-segment.md).
* Create segments directly in Journey Orchestration the same way you create them using the Segmentation Service. See [Creating a segment](../segment/creating-a-segment.md).
* Leverage segments in your journeys' conditions using the simple or advanced expression editor. See [Using segments in conditions](../segment/using-a-segment.md).
* Add a **Segment qualification** event to your journey in order to listen to the entrances and exits of profiles in Platform segments. See [Events activities](../building-journeys/event-activities.md#segment-qualification).

