---
title: Platform Management 8.1.0 release notes
linkTitle: Platform Management 8.1.0 release notes
description: New features, improvements, and bug fixes for the release.
weight: 219
date: 2021-08-12
Hide_readingtime: true
---

## Platform Management 8.1.0 - 23 September 2020

Platform Management 8.1.0 is a minor release, which includes new features, improvements, and bug fixes.

## New features

* Introduced a new _Activity_ view accessible from the notifications (bell) icon in the common header or the left-hand menu on the user's _Account_ view. The _Activity_ view shows additions, deletions, and changes performed by or on the user and changes to the organization and its apps and services for the user's current organization.
* Introduced a new org _Activity_ view accessible from the left-hand menu on the _Organization_ view. The _Activity_ view shows changes to the organization, its subscriptions, and its apps and services.
* Introduced a new app _Activity_ view accessible from the left-hand menu on any app view. The _Activity_ view shows events related to the apps.
* Added the ability to download _Analytics_ view charts as an image.
* Added modules used by _Titanium_ applications to the _App Overview_.
* Added four widgets to the _Metric Overview_ available for organizations which have **Amplify Central** provisioned showing occurrences of Central Asset, Central Environment, Catalog Item, and Catalog Subscription events.
* Selecting a time range on _Analytics_ view charts will now "zoom in" on that date range.

## Improvements

* Revised the _Latest Activity_ and _Notifications_ accessible from the notifications icon in the common header. Their entries are now combined into a single list of _Recent Activity_. Clicking on an entry in this list takes the user to the user _Activity_ view to see more details about the event.
* Improved resolution (i.e., number of data points shown) on _Analytics_ view charts.
* Improved labels on the x-axis of charts on _Analytics_ views.
* Changed the _Subscriptions_ section of the _Organization_ overview to show only active subscriptions on initial load. Terminated, inactive, and pending subscriptions can be viewed by selecting that status from the dropdown above the table.
* Added a link to the _Titanium SDK Prerequisites_ documentation on the _Get Started with App Builder_ guide. This documentation shows supported dependency versions and their download locations.
* All applications deployed using **Amplify Runtime Services** now show a type value of "Runtime Service" on the all apps table.

## Fixed issues

* Fixed an issue where users may not be able to edit their _Account_ information in Safari.
* Fixed an issue where Firefox for Android was shown as an unsupported browser (it's totally supported!)
* Fixed an issue where the organization _Usage_ view may not have shown the correct entitlement quotas when viewing usage for prior months.
* Fixed an issue where **Amplify Runtime Services** application access logs may not have been properly format response times greater than one second.
* Fixed an issue where application names may not have been included in exported chart or table data.
