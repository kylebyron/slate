---
title: Hart API Docs Challenge

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='https://hart.com/platform/'>Sign Up for a Developer Key</a>
  - <a href='https://www.linkedin.com/in/kbyron/'>Documentation Powered by Kyle :-)</a>

includes:
  - errors

search: true
---

# API Reference

This reference includes documentation for 3 endpoints: LoginRequest, ListCategoriesRequest and ListPostsInHashtagRequest.

## LoginRequest

This endpoint allows you to login to a TikTok account.

```shell
curl -X GET "http://tiktok/api/LoginRequest?mix_mode&username&email&password"
```

```ruby
ruby ruby ruby
```

### Query Parameters

Parameter | Description
--------- | -----------
mix_mode  | Type: Number. Defaults to 1.
username  | The unique username of the user.
email     | Email address associated with the user's account.
mobile    | Mobile phone number associated with the user's account.
account   | The account number.
password  | The account password.
captcha   | The captcha answer. Optional - only required if captcha was shown.


## ListCategoriesRequest

This endpoint allows you to retrieve a list of popular categories (or hashtags). Returns ListCategoriesResponse.

```shell
curl -X GET "http://tiktok/api/ListCategoriesRequest?category_list&aweme_list&category_type" 
```

```ruby
some code... 
```

### Query Parameters

Parameter      | Description
---------      | -----------
category_list  | A list of categories.
aweme_list     | A list of posts in the category.
category_type  | The type of category. Type: Number.
challenge_info | Information about the category. 
desc           | A description of the category. For example: "Trending"


## ListPostsInHashtagRequest

This endpoint allows you to retrieve a list of posts containing a specific hashtag. Returns ListPostsInHashtagResponse.

```shell
curl -X GET "http://tiktok/api/ListPostsInHashtagRequest?ch_id&query_type&type" 
```

### Query Parameters

Parameter      | Description
---------      | -----------
ch_id          | The ID of the hashtag.
query_type     | Need description.
type           | Need description.





