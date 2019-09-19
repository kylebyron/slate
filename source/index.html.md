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

This reference includes documentation for 3 endpoints: LoginRequest, ListCategoriesRequest and ###

## LoginRequest

This endpoint allows you to login to your account.

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

### Query Parameters

Parameter      | Description
---------      | -----------
ch_id          | The ID of the hashtag.
query_type     | Need description.
type           | Need description.



## Get a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.get(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

## Delete a Specific Kitten

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.delete(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.delete(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -X DELETE
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let max = api.kittens.delete(2);
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "deleted" : ":("
}
```

This endpoint deletes a specific kitten.

### HTTP Request

`DELETE http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to delete

## Get All Kittens

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
let kittens = api.kittens.get();
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

### HTTP Request

`GET http://example.com/api/kittens`
