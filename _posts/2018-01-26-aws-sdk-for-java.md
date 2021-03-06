---
title: "AWS SDK for Java, version 2.0"
author: Sean Sullivan
date: '2018-01-26'
categories: 'cloud'
tags:
- aws
- java
- scala
- cloud
- albany
- newyork
- 2018
---

The Capital Region AWS User Group met on January 18th at the [Nanotech Complex](https://sunypoly.edu/research/albany-nanotech-complex.html) in Albany New York. [CommerceHub](https://www.commercehub.com/) hosted the meeting at their main office.

The topic of this month's meetup was the AWS SDK for Java. At HBC, our development teams use the SDK to access AWS services such as DynamoDB, S3, CloudWatch, and SNS. The v1 SDK has been a core building block at HBC since 2014.

In June 2017, Amazon released a new implementation of the SDK for Java.

![aws-sdk-image](/assets/images/aws-sdk-for-java/aws-sdk-java-version-2_0-june-2017.png)

The version 2.0 SDK is available as a developer preview. HBC is evaluating the new SDK and we look forward to using it in production later this year.

![aws-sdk-image](/assets/images/aws-sdk-for-java/aws-sdk-java-version-2_0-github-v2-sdk.png)

Our engineering team has already started incorporating the v2 SDK into our helper libraries:

- gfc-aws-cloudwatch -- [pull request](https://github.com/gilt/gfc-aws-cloudwatch/pull/8/)
- gfc-s3-cache -- [pull request](https://github.com/gilt/gfc-s3-cache/pull/4)

The v2 API uses  [java.util.concurrent.CompletableFuture](https://docs.oracle.com/javase/8/docs/api/java/util/concurrent/CompletableFuture.html) to encapsulate the result of an AWS service call. HBC's Scala libraries will use [FutureConverters](https://github.com/scala/scala-java8-compat/blob/master/src/main/scala/scala/compat/java8/FutureConverters.scala) to convert Java CompletableFuture objects into Scala Future objects.

![aws-sdk-image](/assets/images/aws-sdk-for-java/aws-sdk-java-version-2_0-futureconverters.png)

If you want to learn more about the v2 SDK, review my slidedeck or watch Kyle Thomson's re:invent 2017 presentation.

[![aws-sdk-java-speakerdeck-albany-image](/assets/images/aws-sdk-for-java/AWS_SDK_for_Java-speakerdeck-albany-480.png)](https://speakerdeck.com/sullis/aws-sdk-for-java-version-2-dot-0-albany-ny-january-18-2018) [![aws-reinvent-2017-kyle-thomson-image](/assets/images/aws-sdk-for-java/aws-sdk-java-version-2_0-kyle-reinvent-youtube-480.png)](https://www.youtube.com/watch?v=byRois3s5Yc)
