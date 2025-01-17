---
title: Platform Management 8.4.4 release notes
linkTitle: Platform Management 8.4.4 release notes
description: New features, improvements, and bug fixes for the release.
weight: 207
date: 2021-08-12
Hide_readingtime: true
---

## Platform Management 8.4.4 - 1 April 2021

Platform Management 8.4.4 is a patch release, which includes several improvements and bug fixes.

## Improvements

* Added End-of-Support badge on **App Builder** capability and Discontinuance badge on **Mobile Backend Services** capability on _Platform Home_ view.  Added End-of-Support badge on **Application Development** offering and Discontinuance badge on **Mobile Backend Services** offering on _Explore Products_ view. See [Product Update: Changes to Application Development Services](https://devblog.axway.com/featured/product-update-changes-to-application-development-services-appcelerator/) on Axway Developer Blog for more information.
* Added ability to group _Custom Query_ chart data by arbitrary time intervals using the "From/To" or "Period" date range options. E.g., you can now query 14 days in 6 hour intervals, 12 hours in 15 minute intervals, etc.
* Changed date format in analytics chart series exported CSV to improve recognition in spreadsheet applications. The format was changed from ISO-8601 UTC format to "yyyy-MM-dd HH:mm:ss".

## Fixed issues

* Fixed an issue where viewing a saved _Custom Query_ may not select the previously selected date range.
* Fixed an issue where Download Descriptor XML and Download Signing Certificate buttons on the _Identity Provider_ view for SAML protocol identity providers may cause a 404 error instead of prompting download of the desired resource.
