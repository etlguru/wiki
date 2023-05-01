---
author: Peter Jonson
title: Twitter Reader
description: Twitter Reader
draft: false
tags: ['Reader', 'Twitter']
date: 2022-12-25
group: advanced-etl-processor-enterprise-reader
menu: advanced-etl-processor-enterprise
layout: docs
---

{{< image class="mx-auto d-block"  src="/images/etl/advanced-etl-processor/transforming-data/reader/data_reader_properties_twitter.png" title="Twitter Reader" >}}

## Source data

Following data can be extracted from twitter

### Tweets

- Id
- Name
- Tweet
- CreatedAt
- Retweets
- Favorites
- Favorited
- Source
- InReplyToScreenName
- MediaURL

### Mentions

- Id
- Name
- Tweet
- CreatedAt
- Retweets
- Favorites
- Favorited
- Source
- InReplyToScreenName
- MediaURL

### Friends

- Id
- Name
- ScreenName
- Description
- Status
- Location
- URL
- ImageURL
- TimeZone
- CreatedAt
- StatusCount
- FollowersCount
- FriendsCount
- FavoritesCount
- ListedCount
- IsProtected
- GeoEnabled

### Followers

- Id
- Name
- ScreenName
- Description
- Status
- Location
- URL
- ImageURL
- TimeZone
- CreatedAt
- StatusCount
- FollowersCount
- FriendsCount
- FavoritesCount
- ListedCount
- IsProtected
- GeoEnabled

### Direct Messages

- Id
- Message
- Sender
- CreatedAt

Only last 100 records are loaded

- [Connecting to Twitter]({{<ref "/knowledgebase/connections/connecting-to-twitter" >}})
