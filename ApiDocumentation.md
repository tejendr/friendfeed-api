﻿#labels Deprecated
# FriendFeed API Documentation Version 1 #

<font color='red'><b>This version of the FriendFeed API has been deprecated. See <a href='http://friendfeed.com/api/documentation'>http://friendfeed.com/api/documentation</a> for the latest version.</b></font>

# Table of Contents #

  * [Introduction](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Introduction)
  * [Core Concepts](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Core_Concepts)
    * [Requests and Data Formats](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Requests_and_Data_Formats)
    * [Authentication](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Authentication)
    * [JSON Callbacks](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#JSON_Callbacks)
    * [Errors](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Errors)
  * [Reading FriendFeed Feeds](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Reading_FriendFeed_Feeds)
    * [Overview](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Overview)
      * [Feed Formats](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Feed_Formats)
      * [Filtering & Paging](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Filtering_&_Paging)
    * [Methods](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Methods)
      * [/api/feed/user - Fetch Entries from Multiple Users](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/feed/user_-_Fetch_Entries_from_Multiple_Users)
      * [/api/feed/entry - Fetch Multiple Entries by ID](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/feed/entry_-_Fetch_Multiple_Entries_by_ID)
      * [/api/feed/search - Search](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/feed/search_-_Search)
      * [/api/feed/url - Fetch Entries about a URL](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/feed/url_-_Fetch_Entries_about_a_URL)
      * [/api/feed/domain - Fetch Entries from a domain](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/feed/domain_-_Fetch_Entries_from_a_domain)
  * [Publishing To FriendFeed](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Publishing_To_FriendFeed)
    * [Create New Entries](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Create_New_Entries)
      * [/api/share - Publish Links or Messages](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/share_-_Publish_Links_or_Messages)
      * [Upload Images with Entries](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Upload_Images_with_Entries)
    * [Comment and Like Entries](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Comment_and_Like_Entries)
      * [/api/comment - Add or Edit Comments](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/comment_-_Add_or_Edit_Comments)
      * [/api/comment/delete - Delete a Comment](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/comment/delete_-_Delete_a_Comment)
      * [/api/like - "Like" an Entry](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/like_-_"Like"_an_Entry)
      * [/api/like/delete - Delete a "Like"](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/like/delete_-_Delete_a_"Like")
      * [/api/entry/delete - Delete an Entry](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/entry/delete_-_Delete_an_Entry)
      * [/api/entry/hide - Hide an Entry](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/entry/hide_-_Hide_an_Entry)
  * [Get User Profile Information](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Get_User_Profile_Information)
    * [/api/user/NICKNAME/profile - Get services and subscriptions](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/user/NICKNAME/profile_-_Get_services_and_subscriptions)
    * [/api/profiles - Get services and subscriptions for multiple users](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/profiles_-_Get_services_and_subscriptions_for_multiple_user)
    * [/NICKNAME/picture - Get a user's profile picture](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/NICKNAME/picture_-_Get_a_user's_profile_picture)
  * [Get Room Profile Information](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Get_Room_Profile_Information)
    * [/api/room/NICKNAME/profile - Get room url, description, member information](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/room/NICKNAME/profile_-_Get_room_url,_description,_member_i)
    * [/rooms/NICKNAME/picture - Get a rooms's profile picture](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/rooms/NICKNAME/picture_-_Get_a_rooms's_profile_picture)
  * [Get List Profile Information](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Get_List_Profile_Information)
    * [/api/list/NICKNAME/profile - Get list url, description, member information](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/list/NICKNAME/profile_-_Get_list_url,_description,_member_i)
  * [Subscription Management](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Subscription_Management)
    * [/api/user/NICKNAME/subscribe - Subscribe to a user](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/user/NICKNAME/subscribe_-_Subscribe_to_a_user)
    * [/api/room/NICKNAME/subscribe - Subscribe to a room](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/room/NICKNAME/subscribe_-_Subscribe_to_a_room)
  * [Real-time](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Real-time)
  * [Miscellaneous Methods](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Miscellaneous_Methods)
    * [/api/validate - Validate a user's remote key](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/validate_-_Validate_a_user's_remote_key),
    * [/api/services - List all FriendFeed services](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#/api/services_-_List_all_FriendFeed_services),
    * [Obtaining a subset of data using the "include" argument](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Obtaining_a_subset_of_data_using_the_"include"_argumen),
    * [Pre-populated service import forms](http://code.google.com/p/friendfeed-api/wiki/ApiDocumentation#Pre-populated_service_import_forms)

# Introduction #

The [FriendFeed API](http://friendfeed.com/api/) enables developers interact with the [FriendFeed](http://friendfeed.com/) web site programmatically via simple HTTP requests.

This is the technical documentation for the API. Other important links:

  * [FriendFeed API Homepage](http://friendfeed.com/api/)
  * [FriendFeed API Developer Forum](http://groups.google.com/group/friendfeed-api)
  * [FriendFeed API Application Guidelines](http://friendfeed.com/api/guidelines)
  * [FriendFeed API Python, PHP, and C# Libraries](http://code.google.com/p/friendfeed-api/)

# Core Concepts #

## Requests and Data Formats ##

All requests to the FriendFeed API are simple HTTP GET and POST requests. For example, you can fetch the JSON version of the most recent 30 public entries published to FriendFeed by fetching http://friendfeed.com/api/feed/public.

All of the API requests that output feeds are available in four formats: [JSON](http://www.json.org/), a simple form of XML, [RSS 2.0](http://cyber.law.harvard.edu/rss/rss.html), and [Atom 1.0](http://tools.ietf.org/html/rfc4287). JSON is the default output format. To request a different output format, simply add an `format=` argument to the URL:

  * http://friendfeed.com/api/feed/public?format=json
  * http://friendfeed.com/api/feed/public?format=xml
  * http://friendfeed.com/api/feed/public?format=rss
  * http://friendfeed.com/api/feed/public?format=atom

The other API requests, like posting a new comment on an entry, only support the JSON and XML output formats since they do not output feed-oriented data.


## Authentication ##

If you are publishing data to FriendFeed or if you are requesting the feed that includes data from a user with a private feed, your HTTP requests must be authenticated.

All FriendFeed users have a **[Remote Key](http://friendfeed.com/remotekey)** to provide third party applications access to their FriendFeed. A FriendFeed Remote Key is just like a password, except that it is only used for third party applications, so it only provides access to the functionality defined by the API. Users can easily reset it if a third party application abuses the API.

All requests that require authentication use [HTTP Basic Authentication](http://en.wikipedia.org/wiki/Basic_access_authentication). The username should be the user's nickname, and the password should be the user's Remote Key. You can direct user's to http://friendfeed.com/remotekey to get their remote key if they have not memorized it. See the [FriendFeed API Application Guidelines](http://friendfeed.com/api/guidelines) for a complete set of recommendations of how to present authentication in your application.

The Python and PHP libraries available at http://code.google.com/p/friendfeed-api/ implement authentication for all methods that require it.

_**Note**: We are currently exploring adding OAuth support as well. If you are interested in this support, let us know in the [FriendFeed developer forum](http://groups.google.com/group/friendfeed-api)._


## JSON Callbacks ##

The JSON output format supports an additional argument `callback=` that wraps the JSON output in a function call to a function of your choice. This functionality is available to enable you to use the API with JavaScript within a web browser. For example, http://friendfeed.com/api/feed/public?callback=foo outputs:

```
foo({"entries":[...]})
```

Using JSON and callbacks, you can place the FriendFeed API request inside a `<script>` tag, and operate on the results with a function elsewhere in the JavaScript code on the page.

All authentication is ignored if the `callback=` argument is given, so JSON callbacks only work with public feeds.

## Errors ##

FriendFeed returns appropriate HTTP status codes for API requests. In addition to the HTTP status code, FriendFeed includes error information in the response body.  The error response body is formatted as XML if the requested format is format is `xml`, `rss` or `atom`.  Otherwise, the response body is formatted as JSON.

The JSON form of an error response has the following format:

  * `errorCode` - A program readable string describing the error.

The error codes are:

  * `bad-id-format` - Bad format for UUID argument.
  * `bad-url-format` - Bad format for URL argument.
  * `entry-not-found` - Entry with the specified UUID was not found.
  * `entry-required` - Entry UUID argument is required.
  * `forbidden` - User does not have access to entry, room or other entity specified in the request.
  * `image-format-not-supported` - Unsupported image format.
  * `internal-server-error` - Internal error on FriendFeed server.
  * `limit-exceeded` - Request limit exceeded.
  * `not-found` - URL not found.
  * `room-not-found` - Room with specified name not found.
  * `room-required` - Room name argument is required.
  * `title-required` - Entry title argument is required.
  * `unauthorized` - The request requires authentication.
  * `user-not-found` - User with specified nickname not found.
  * `user-required` - User nickname argument is required.
  * `error` - Other unspecified error.

Example error responses using `curl`:

```
# Title is required field for entries.
$ curl --basic --user nickname:remotekey --data comment=hello \
  http://friendfeed.com/api/share
{"errorCode":"title-required"}

# Here's the same error with XML output
$ curl --basic --user nickname:remotekey --data comment=hello \
  http://friendfeed.com/api/share?format=xml
<?xml version="1.0" encoding="utf-8"?>
<error><errorCode>title-required</errorCode></error>
```

# Reading FriendFeed Feeds #

## Overview ##

### Feed Formats ###

The JSON form of the feeds has the following structure:

  * `entries[]`
    * `id` - the FriendFeed entry UUID, used to add comments/likes to the entry
    * `title`
    * `link`
    * `published`
    * `updated`
    * `hidden` - if true, this entry should be hidden based on the user's preferences
    * `anonymous` - if true, user will be present but should not be shown
    * `user{}` - the user who shared this entry
      * `id` - the user's FriendFeed UUID
      * `name` - the user's full name
      * `nickname` - the user's FriendFeed nickname, used in FriendFeed URLs
      * `profileUrl` - the user's profile URL on FriendFeed
    * `service{}` - the service from which the entry came
      * `id` - the service's FriendFeed ID, e.g., "picasa"
      * `name` - the service's official name, e.g., "Picasa Web Albums"
      * `iconUrl` - the URL of the favicon for this service
      * `profileUrl` - the user's profile URL on this service
      * `entryType?` - present if the service has multiple types of entries.  Example values are "favorite" and "publish" for YouTube videos.
    * `comments[]`
      * `date`
      * `id` - the UUID of the comment
      * `user{}` - same structure as the `user{}` structure above
      * `body` - the textual body of the comment
      * `via{}?` - present if this comment came from an API client
        * `name` - the name of the API client, e.g., "Alert Thingy"
        * `url` - the official URL of the API client, e.g., http://www.alertthingy.com/
    * `likes[]`
      * `date`
      * `user{}` - same structure as the `user{}` structure above
    * `media[]` - the videos/images associated with the entry
      * `title?` - the title of the media file
      * `player?` - the player for this media file (e.g., the YouTube.com URL with the embedded video)
      * `link` - the link where the media file came from (e.g., a Flickr photo page)
      * `thumbnails[]` - the thumbnails for this media file
        * `url`
        * `width`
        * `height`
      * `content[]` - the different versions of the media file
        * `url`
        * `type` - the MIME type of the media file
        * `width`
        * `height`
      * `enclosures[]` - any media enclosures (sometimes duplicated with content)
        * `url`
        * `type` - the MIME type of the media file
        * `length`
    * `via{}?` - present if this entry came from an API client
      * `name` - the name of the API client, e.g., "Alert Thingy"
      * `url` - the official URL of the API client, e.g., http://www.alertthingy.com/
    * `room{}?` - if the entry is in a room, the room the entry is in
      * `id` - the room's FriendFeed UUID
      * `name` - the room's display name
      * `nickname` - the room's FriendFeed nickname, used in FriendFeed URLs
      * `url` - the room's URL on FriendFeed
    * `geo{}?` - present if the entry contains geographic information
      * `lat` - the latitude
      * `long` - the longitude
    * `friendof{}?` - present if the entry is from a friend of a friend, same structure as the `user{}` structure above


The simple XML format (`output=xml`) has the same structure as the JSON. The RSS and Atom formats use the standard RSS and Atom attributes for title, link, published, and updated, and include extension elements for all of the other meta-data.

Dates in JSON and dates in the FriendFeed extension elements in the Atom and RSS feeds are in [RFC 3339](http://www.ietf.org/rfc/rfc3339.txt) format in UTC. You can parse them with the `strptime` string `"%Y-%m-%dT%H:%M:%SZ"`.


### Filtering & Paging ###

All of the feed methods below support the following additional arguments:

  * `service` - only return entries from the service with the given ID, e.g., `service=twitter`
  * `start` - return entries starting with the given index, e.g., `start=30`
  * `num` - return `num` entries starting from `start`, e.g., `num=10`


## Methods ##

<table>
<tr><td><b>Method</b> (and link to example)</td><td><b>Description</b></td></tr>
<tr>
<blockquote><td valign='top'><a href='http://friendfeed.com/api/feed/public'>/api/feed/public</a></td>
<td>Returns the most recent public entries on FriendFeed.</td>
</tr>
<tr>
<td valign='top'><a href='http://friendfeed.com/api/feed/user/bret'>/api/feed/user/NICKNAME</a></td>
<td>Returns the most recent entries from the user with the given nickname. If the user has a private feed, authentication is required.</td>
</tr>
<tr>
<td valign='top'><a href='http://friendfeed.com/api/feed/user/bret/comments'>/api/feed/user/NICKNAME/comments</a></td>
<td>Returns the most recent entries the user has commented on, ordered by the date of that user's comments. If the user has a private feed, authentication is required.</td>
</tr>
<tr>
<td valign='top'><a href='http://friendfeed.com/api/feed/user/bret/likes'>/api/feed/user/NICKNAME/likes</a></td>
<td>Returns the most recent entries the user has "liked", ordered by the date of that user's "likes". If the user has a private feed, authentication is required.</td>
</tr>
<tr>
<td valign='top'><a href='http://friendfeed.com/api/feed/user/bret/discussion'>/api/feed/user/NICKNAME/discussion</a></td>
<td>Returns the most recent entries the user has commented on or "liked". If the user has a private feed, authentication is required.</td>
</tr>
<tr>
<td valign='top'><a href='http://friendfeed.com/api/feed/user/bret/friends'>/api/feed/user/NICKNAME/friends</a></td>
<td>Returns entries from a user's friends. If the user has a private feed, authentication is required.  Any friends of the user who have a private feed will be omitted unless authentication is used and the authenticated user has the privileged to see those feeds.</td>
</tr>
<tr>
<td valign='top'><a href='http://friendfeed.com/api/feed/room/friendfeed-news'>/api/feed/room/NICKNAME</a></td>
<td>Returns the most recent entries in the room with the given nickname.  If the room is private, authentication is required.</td>
</tr>
<tr>
<td valign='top'><a href='http://friendfeed.com/api/feed/entry/7ad57cd3-30e6-253a-c745-6345b1bd0e78'>/api/feed/entry/ENTRYID</a></td>
<td>Returns the entry with the given id.  If the entry is private, authentication is required.</td>
</tr>
<tr>
<td valign='top'><a href='http://friendfeed.com/api/feed/home'> /api/feed/home </a></td>
<td>Returns the entries the authenticated user would see on their FriendFeed homepage - all of their subscriptions and friend-of-a-friend entries.  Authentication is always required.<br>
</td>
</tr>
<tr>
<td valign='top'><a href='http://friendfeed.com/api/feed/rooms'> /api/feed/rooms </a></td>
<td>Returns the entries the authenticated user would see on their Rooms page - entries from all of the rooms they are members of. Authentication is always required.</td>
</tr>
<tr>
<td valign='top'><a href='http://friendfeed.com/api/feed/list/personal'> /api/feed/list/NICKNAME </a></td>
<td>Returns entries from the authenticated users list with the given nickname. Authentication is always required.</td>
</tr>
</table></blockquote>

### /api/feed/user - Fetch Entries from Multiple Users ###

Returns the most recent entries from a list of users, specified by nickname:

http://friendfeed.com/api/feed/user?nickname=bret,paul,jim

If more than one nickname is specified, the feed most recent entries from all of the given users. If any one of the users has a private feed, authentication is required.

Using the [FriendFeed Python library](http://code.google.com/p/friendfeed-api/):

```
service = friendfeed.FriendFeed()
feed = service.fetch_multi_user_feed(["bret", "jim", "paul"])
for entry in feed["entries"]:
    print entry["title"]
```

You can also specify by email:

http://friendfeed.com/api/feed/user?emails=example1@example.com,example2@example.com


### /api/feed/entry - Fetch Multiple Entries by ID ###

Returns the requested entries, specified by id:

http://friendfeed.com/api/feed/entry?entry_id=7ad57cd3-30e6-253a-c745-6345b1bd0e78,6f6a36d2-a6c6-fbe7-6bb2-f328c8794eea

Authentication is not required, but private entries will be omitted from unauthenticated results, as will entries the authenticated user does not have permission to view.

### /api/feed/search - Search ###

Executes a search over the entries in FriendFeed. The default scope is over all public entries.

http://friendfeed.com/api/feed/search?q=friendfeed

The query syntax is the same syntax as http://friendfeed.com/search/advanced. The query operators are:

  * `from:` return entries from a specific user, `from:bret`
  * `room:` return entries within a specific room, `room:friendfeed-feedback`
  * `friends:` return entries from all of that user's friends, `friends:bret`
  * `service:` return entries from a particular service, `service:twitter`
  * `intitle:` return entries with specific words in the entry title, `intitle:friendfeed`
  * `incomment:` return entries with specific words in the entry's comments, `incomment:friendfeed`
  * `comment:` return entries that have been commented on by a specific user, `comment:bret`
  * `comments:` return entries with at least this many comments, `comments:10`
  * `like:` return entries liked by a specific user, `like:bret`
  * `likes:` return entries with at least this many likes, `likes:10`
  * `-` exclude a term (word, user, etc.) from your search, `-from:bret`
  * `,` perform an OR, `from:bret,bgolub`


As a convenience feature you can use "me" in place of any nickname and we will replace it with the authenticated user's nickname:

```
curl -u "nickname:remotekey" http://friendfeed.com/api/feed/search?q=friends:me+friendfeed
```

Using the FriendFeed Python library:

```
service = friendfeed.FriendFeed()
feed = service.search("from:bret friendfeed")
for entry in feed["entries"]:
    print entry["title"]
```

### /api/feed/url - Fetch Entries about a URL ###

Returns the most recent entries linking to a given URL.

http://friendfeed.com/api/feed/url?url=http://blog.friendfeed.com/2008/12/simple-update-protocol-update.html

If authentication is used, private entries may be returned, otherwise only public entries will be.

When authenticated, the results may be limited to only entries from the user's friends and subscribed rooms by passing subscribed=1:

```
curl -u "nickname:remotekey" \
'http://friendfeed.com/api/feed/url?url=http://blog.friendfeed.com/2008/12/simple-update-protocol-update.html&subscribed=1'
```

The results may also be limited to a given set of users or rooms by specifying their nicknames:

http://friendfeed.com/api/feed/url?url=http://blog.friendfeed.com/2008/12/simple-update-protocol-update.html&nickname=bret,friendfeed-news

Note that there is a best-effort attempt to resolve URL shorteners, so some entries may contain links that redirect to the specified one.

The service filter is not currently supported on this feed.

### /api/feed/domain - Fetch Entries from a domain ###

Returns the most recent entries linking to URLs in the given domain(s).

http://friendfeed.com/api/feed/domain?domain=blog.friendfeed.com,code.google.com

By default, sub-domains will not be matched (i.e. friendfeed.com will not include blog.friendfeed.com entries). Subdomain matches may be requested by passing inexact=1 (the results of inexact queries will be unsorted for performance reasons):

http://friendfeed.com/api/feed/domain?domain=friendfeed.com&inexact=1

If authentication is used, private entries may be returned, otherwise only public entries will be.

When authenticated, the results may be limited to only entries from the user's friends and subscribed rooms by passing subscribed=1:

```
curl -u "nickname:remotekey" \
  'http://friendfeed.com/api/feed/domain?domain=blog.friendfeed.com,code.google.com&subscribed=1'
```

The results may also be limited to a given set of users or rooms by specifying their nicknames:

http://friendfeed.com/api/feed/domain?domain=blog.friendfeed.com,code.google.com&nickname=bret,friendfeed-news

Note that there is a best-effort attempt to resolve URL shorteners, so some entries may contain links that redirect to ones in the specified domain(s).

The service filter is not currently supported on this feed.

# Publishing To FriendFeed #

All of the calls to publish information to FriendFeed are HTTP requests. You can perform test calls from a web browser using the HTTP Basic Authentication built into your browser at http://friendfeed.com/static/html/apitest.html.

Requests to FriendFeed are rate limited, which, e.g., limits the number and size of thumbnails you can upload in a day. Normal uses should fall well within our rate limits. If you encounter HTTP 403 errors because of rate limits, and you think the limit is erroneous, please let us know in the developer forum.


## Create New Entries ##

### /api/share - Publish Links or Messages ###

A POST request to `/api/share` will publish a new entry on the authenticated user's feed. The arguments are:

  * `title` - **required** - The text of the new entry.
  * `link` - The URL of the new entry. If it is not specified, the new entry will look like a quoted message. If specified, it will look like a link.
  * `comment` - If specified, the given text is posted as a comment under the new entry.
  * `imageN_url`, `imageN_link` - The thumbnail images for the entry, specified from a 0-based index. `image0_url` specifies the URL of the image, which will be resized to the maximum size of a thumbnail and stored on FriendFeed's servers. If `image0_link` is not given, the thumbnail will link to the main `link` URL. If it is specified, the thumbnail will link to the specified `image0_link`.
  * `audioN_url`, `audioN_title` - Audio links (MP3 only for now), specified from a 0-based index. `audio0_url` specifies the URL of the audio, which will appear as a play button below in the post. If `audio0_title` is given, it will be shown while playing, otherwise the entry title will be.
  * `fileN`, `fileN_link` - Uploaded images as described in the [next section](ApiDocumentation#Upload_Images_with_Entries.md).
  * `room` - If specified, the nickname of the room that the entry should be shared in.

Example usage with the [FriendFeed Python library](http://code.google.com/p/friendfeed-api/):

```

service = friendfeed.FriendFeed(nickname, remote_key)

# Publish a text message
service.publish_message("Testing the FriendFeed API")

# Publish a link
service.publish_link("Testing the FriendFeed API", "http://friendfeed.com/api/")

# Publish a link with thumbnail images
service.publish_link(
    title="Testing the FriendFeed API",
    link="http://friendfeed.com/api/",
    image_urls=[
        "http://friendfeed.com/static/images/jim-superman.jpg",
        "http://friendfeed.com/static/images/logo.png",
    ],
)
```

Example usage with `curl`:

```
curl -u "nickname:remotekey" \
  -d "title=Testing+the+FriendFeed+API&link=http://friendfeed.com/" \
  http://friendfeed.com/api/share
```


### Upload Images with Entries ###

The `/api/share` method can also accept uploaded images encoded as `multipart/form-data`. This encoding is the standard used for file uploads within web browsers.

If any images are uploaded with the `/api/share` request, the original and the thumbnail are stored on FriendFeed's servers, and the thumbnail is displayed with the entry.

By default, the thumbnails will link to the destination link for the entry. If you want each uploaded image to link somewhere else, you can specify the link in the `IMAGENAME_link` argument. For example, if your uploaded image is POST argument `file0`, you can specify the link for that thumbnail as `file0_link`.


## Comment and Like Entries ##

### /api/comment - Add or Edit Comments ###

A POST request to `/api/comment` will add a comment or edit an existing comment on a FriendFeed entry. The arguments are:

  * `entry` - **required** - The FriendFeed UUID of the entry to which this comment is attached.
  * `body` - **required** - The textual body of the comment.
  * `comment` - If given, the FriendFeed UUID of the comment to edit. If not given, the request will create a new comment.

Example usage from the Python library:

```
service = friendfeed.FriendFeed(nickname, remote_key)
service.add_comment(
    entry="550e8400-e29b-41d4-a716-446655440000",
    body="Testing the FriendFeed API",
)
```

Example usage with `curl`:

```
curl -u "nickname:remotekey" \
  -d "entry=550e8400-e29b-41d4-a716-446655440000&body=Testing+the+FriendFeed+API" \
  http://friendfeed.com/api/comment
```

### /api/comment/delete - Delete a Comment ###

A POST request to `/api/comment/delete` will delete an existing comment. The arguments are:

  * `entry` - **required** - The FriendFeed UUID of the entry to which this comment is attached.
  * `comment` - **required** - The FriendFeed UUID of the comment to delete.
  * `undelete` - optional - if given, un-delete the given comment if it is already deleted.


### /api/like - "Like" an Entry ###

A POST request to `/api/like` will add a "Like" to a FriendFeed entry for the authenticated user.

  * `entry` - **required** - The FriendFeed UUID of the entry to which this comment is attached

Example usage from the Python library:

```
service = friendfeed.FriendFeed(nickname, remote_key)
service.add_like("550e8400-e29b-41d4-a716-446655440000")
```

Example usage with `curl`:

```
curl -u "nickname:remotekey" \
  -d "entry=550e8400-e29b-41d4-a716-446655440000" \
  http://friendfeed.com/api/like
```


### /api/like/delete - Delete a "Like" ###

A POST request to `/api/like/delete` will delete an existing "Like." The arguments are:

  * `entry` - **required** - The FriendFeed UUID of the entry to which this comment is attached.


### /api/entry/delete - Delete an Entry ###

A POST request to `/api/entry/delete` will delete an existing entry. The arguments are:

  * `entry` - **required** - The FriendFeed UUID of the entry to delete
  * `undelete` - optional - if given, un-delete the given entry if it is already deleted


### /api/entry/hide - Hide an Entry ###

A POST request to `/api/entry/hide` will hide an entry. The arguments are:

  * `entry` - **required** - The FriendFeed UUID of the entry to delete
  * `unhide` - optional - if given, un-hide the given entry if it is already hidden



# Get User Profile Information #

### /api/user/NICKNAME/profile - Get services and subscriptions ###

Returns list of all of the user's subscriptions (people) and services connected to their account (Authentication required for private users):

http://friendfeed.com/api/user/bret/profile

The returned JSON has the form:

  * `status` - private or public
  * `id` - the user's FriendFeed UUID
  * `name` - the user's full name
  * `nickname` - the user's FriendFeed nickname, used in FriendFeed URLs
  * `profileUrl` - the user's profile URL on FriendFeed
  * `services[]` - the services connected to the user's account
    * `id` - the service's FriendFeed ID, e.g., "picasa"
    * `name` - the service's official name, e.g., "Picasa Web Albums"
    * `url` - the official URL of the service, e.g., http://picasaweb.google.com/
    * `iconUrl` - the URL of the favicon for this service
    * `profileUrl`? - the user's profile URL on this service, if any
    * `username`? - the user's username for this service, if any
  * `subscriptions[]` - the users this user is subscribed to
    * `id`
    * `name`
    * `nickname`
    * `profileUrl`
  * `rooms[]` - the rooms this user is a member of
    * `id` - the room's FriendFeed UUID
    * `name` - the room's display name
    * `nickname` - the room's FriendFeed nickname, used in FriendFeed URLs
    * `url` - the room's URL on FriendFeed
  * `lists[]` - the lists this user is a member of (only visible if authenticated as this user)
    * `id` - the list's FriendFeed UUID
    * `name` - the list's display name
    * `nickname` - the list's FriendFeed nickname, used in FriendFeed URLs
    * `url` - the list's URL on FriendFeed

A POST request to /api/user/NICKNAME/profile will change profile fields.  The arguments are:

  * `name` -  optional - The user's full name.
  * `picture` - optional - The user's picture.  The POST data must be encoded as `multipart/form-data` if the picture argument is used.

The response for the POST request is the same as the GET request.

Example usage with `curl`:

```
curl -u "nickname:remotekey" \
  -d "name=MyNewName" \
  http://friendfeed.com/api/user/nickname/profile
```

### /api/profiles - Get services and subscriptions for multiple users ###

Returns subscriptions and services for multiple users.

http://friendfeed.com/api/profiles?nickname=bret,jim,paul,sanjeev

The returned JSON has the form:

  * `profiles` - the list of profiles for each user, each of which conforms to the format of the /api/user/NAME/profile call above.

### /NICKNAME/picture - Get a user's profile picture ###

http://friendfeed.com/bret/picture?size=medium

Size can be "small", "medium", or "large".

# Get Room Profile Information #

### /api/room/NICKNAME/profile - Get room url, description, member information ###

Returns a list of all of the room's members and the url associated with the room (Authentication required for private rooms):

http://friendfeed.com/api/room/friendfeed-news/profile

The returned JSON has the following format:

  * `status` - private or public
  * `description` - a short summary of what the room is about
  * `url` - the room's url on FriendFeed
  * `administrators[]`
    * `id` - the user's FriendFeed UUID
    * `name` - the user's full name
    * `nickname` - the user's FriendFeed nickname, used in FriendFeed URLs
    * `profileUrl` - the user's profile URL on FriendFeed
  * `members[]`
    * `id` - the user's FriendFeed UUID
    * `name` - the user's full name
    * `nickname` - the user's FriendFeed nickname, used in FriendFeed URLs
    * `profileUrl` - the user's profile URL on FriendFeed
  * `id` - the room's FriendFeed UUID
  * `name` - the room's full name

### /rooms/NICKNAME/picture - Get a rooms's profile picture ###

http://friendfeed.com/rooms/friendfeed-feedback/picture?size=medium

Size can be "small", "medium", or "large".

# Get List Profile Information #

### /api/list/NICKNAME/profile - Get list url, description, member information ###

Returns a list of all of the list's members and the url associated with the list (Authentication required):

http://friendfeed.com/api/list/personal/profile

The returned JSON has the following format:

  * `id` - the list's FriendFeed UUID
  * `name` - the list's display name
  * `nickname` - the list's FriendFeed nickname, used in FriendFeed URLs
  * `url` - the list's URL on FriendFeed
  * `users[]`
    * `id` - the user's FriendFeed UUID
    * `name` - the user's full name
    * `nickname` - the user's FriendFeed nickname, used in FriendFeed URLs
    * `profileUrl` - the user's profile URL on FriendFeed
  * `rooms[]`
    * `id` - the room's FriendFeed UUID
    * `name` - the room's full name
    * `nickname` - the room's FriendFeed nickname, used in FriendFeed URLs
    * `profileUrl` - the room's profile URL on FriendFeed

# Subscription Management #

The subscription management methods below require an API key.  An API key is a private key that developers can obtain by sending an email to api@friendfeed.com.  The API key is required so we can track how these methods are used and curtail abuse. http://friendfeed.com/settings/modifications will contain a list of subscription modifications and will show which API client made the change.

Please read the API guidelines before using these methods: http://friendfeed.com/api/guidelines

### /api/user/NICKNAME/subscribe - Subscribe to a user ###

Subscribe to a user:

http://friendfeed.com/api/user/bret/subscribe

Unsubscribe from a user:

http://friendfeed.com/api/user/bret/subscribe?unsubscribe=1

Example usage with `curl`:

```
curl -u "username:nickname" -d "apikey=APIKEY" http://friendfeed.com/api/user/bret/subscribe
```

The returned JSON has the format:

  * `status` -  `subscribed`, `unsusbscribed`, or `requested`

### /api/room/NICKNAME/subscribe - Subscribe to a room ###

Subscribe to a room:

http://friendfeed.com/api/room/friendfeed-news/subscribe

Unsubscribe from a room:

http://friendfeed.com/api/room/friendfeed-news/subscribe?unsubscribe=1

Example usage with `curl`:

```
curl -u "username:nickname" \
  -d "apikey=APIKEY" \
  http://friendfeed.com/api/room/friendfeed-news/subscribe
```

The returned JSON has the format:

  * `status` -  `subscribed`, `unsusbscribed`, or `requested`


# Real-time #

The real-time methods return entry, comment and like updates since a time identified by a token.  The methods return recent updates only.  To read the complete update stream, clients should use long polling or poll the API using the interval specified in the response.

The real-time methods support the following arguments:

  * `token` - Return updates since the time identified by this token. Call /api/updates to get a starting value for the token.
  * `timeout` - If updates are not immediately available, then wait up to this number of seconds for updates before finishing the request.  If the timeout is zero, then the request finishes without waiting.  The server might finish the request before the specified timeout.
  * `format` - The output format, either "json" or "xml".

The structure of the real-time output is:

  * `update`
    * `token` - Use this token to specify the starting time in the next request to get updates.  The token is an opaque string.
    * `incomplete` - If true, then the results might not be complete because the token was older than the time window maintained by the server.
    * `poll_interval` - If using timeout=0 or if the connection to the server fails, then wait this number of seconds before calling the method again.
  * `entries[]` - Same as feed entries except for changes noted here:
    * `is_new` - If true, then this entry is new.
    * `likes[]`
      * `is_new` - If true, then this like is new.
    * `comments[]`
      * `is_new` - If true, then this comment is new.

The real-time methods are served from the host chan.friendfeed.com (all other methods are served from friendfeed.com).

<table>
<tr><td><b>Method</b> (and link to example)</td><td><b>Description</b></td></tr>
<tr>
<blockquote><td valign='top'><a href='http://chan.friendfeed.com/api/updates'>/api/updates</a></td>
<td>Call this method to get a starting value for the update token. This method always returns an empty entries collection.</td>
</tr>
<tr>
<td valign='top'><a href='http://chan.friendfeed.com/api/updates/home'>/api/updates/home</a></td>
<td>Get updates to the users home feed. Authentication is always required.</td>
</tr>
<tr>
<td valign='top'><a href='http://chan.friendfeed.com/api/updates/user/bret/friends'>/api/updates/user/NICKNAME/friends</a></td>
<td> Get updates to a user's friends feed. If the user has a private feed, authentication is required. Any friends of the user who have a private feed will be omitted unless authentication is used and the authenticated user has the privileges to see those feeds.</td>
</blockquote><blockquote></tr>
<tr>
<blockquote><td valign='top'><a href='http://chan.friendfeed.com/api/updates/list/personal'>/api/updates/list/NICKNAME</a></td>
<td>Returns updates to the authenticated user's list with the given nickname.  Authentication is always required.</td>
</blockquote></tr>
<tr>
<blockquote><td valign='top'><a href='http://chan.friendfeed.com/api/updates/room/friendfeed-news'>/api/updates/room/NICKNAME</a></td>
<td>Returns updates to the room with the given nickname. If the room is private, then authentication is required.</td>
</blockquote></tr>
<tr>
<blockquote><td valign='top'><a href='http://chan.friendfeed.com/api/updates/user/bret'>/api/updates/user/NICKNAME</a></td>
<td>Returns updates to the user feed with the given nickname. If the user has a private feed, then authentication is required.</td>
</blockquote></tr>
</table></blockquote>

# Miscellaneous Methods #

### /api/validate - Validate a user's remote key ###

Validates the user's remote key. If the HTTP Basic Authentication nickname and remote key are valid, we return a HTTP 200 status code. Otherwise, we return an HTTP 401 status code.

http://friendfeed.com/api/validate

### /api/services - List all FriendFeed services ###

Lists all services currently supported by FriendFeed:

http://friendfeed.com/api/services

The returned JSON has the format:

  * `services[]`
    * `url` - the official URL of the service, e.g., http://picasaweb.google.com/
    * `iconUrl` - the URL of the favicon for this service
    * `id` - the service's FriendFeed ID, e.g., "picasa"
    * `name` - the service's official name, e.g., "Picasa Web Albums"

### Obtaining a subset of data using the "include" argument ###

If you are only interested in a subset of the data returned from any of our API methods you can provide the "include" argument a list of comma separated values to specify which properties you are interested in.  For example to only include Bret's id and services:

http://friendfeed.com/api/user/bret/profile?include=id,services

This argument is optional.  If it is not provided then all properties will be returned.

### Pre-populated service import forms ###

You can send your users to a page on FriendFeed with a pre-populated form to make it easy for them to add your service to their feed.  For example:

http://friendfeed.com/settings/services/digg?username=foo

For services that use a URL rather than a username:

http://friendfeed.com/settings/services/blog?url=http://example.com/

Optional arguments:
  * `next` - The URL a user will be redirected to after importing a service. http://friendfeed.com/settings/services/blog?url=http://example.com/&next=http://example.com/afteradd will add the feed from "http://example.com/" and redirect the user to "http://example.com/afteradd" afterwords.
  * `nextcancel` - The URL a user will be redirected to after clicking the cancel link.
  * `author` - For the "blog" service only. For feeds with multiple authors only import entries from this author. http://friendfeed.com/settings/services/blog?url=http://example.com/&author=foobar
  * `importcomment` - For the "feed" service only. Import the entry description as a comment. http://friendfeed.com/settings/services/feed?url=http://example.com/&importcomment=1
  * `isstatus` - For the "feed" service only. Display entries as "messages" (no link). http://friendfeed.com/settings/services/feed?url=http://example.com/&isstatus=1