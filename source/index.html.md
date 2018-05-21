---
title: Data Science Cheatsheet

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - R
  - python

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Data Science Cheatsheet

tldr version of common data science concepts and code

# 8. Hypothesis testing

<!-- TODO: -->

## Null Hypothesis Significance Testing (NHST)

H<sub>0</sub> : - null hypothesis

H<sub>a</sub> : - alternative

- Explain the process and logic of Null Hypothesis Significance Testing (NHST).
- Define one-tailed and two-tailed hypothesis testing.
- State and test the assumptions behind the different t-tests.


### H<sub>0</sub> Null hypothesis

*Eg. The population mean IQ score is 100.*

H<sub>0</sub>: µ > µ0

- H<sub>0</sub>: State an assumption about the world
- That is bleak and uninteresting. It's the status quo. Nothing is happening.

### H<sub>a</sub> Alternate hypothesis

*eg. The population mean IQ scores are not 100*

- H<sub>a</sub> contradicts and rejects H<sub>0</sub>
- Next, we state an opposing viewpoint that contradicts H0
- To support HA we must rule out H0 beyond a reasonable doubt

## One tailed t-tests

- Determine when a one-sample t-test should be applied.
- Use technology to compute and interpret a `one-sample t-test`.

## Two sample t-tests

## Paired sample t-tests

- Identify and distinguish between the two-sample and paired sample research designs for continuous variables.
- Use technology to compute a two-sample (independent samples) t-test and paired-samples (dependent samples) t-test.
- Interpret a `two-sample` and `paired-samples t-test`.

#### One sided test

- H<sub>0</sub>: µ > µ0
- H<sub>0</sub>: (mean) > (mean)0

*or*

#### Two sided test
H<sub>a</sub> : : µ ≠ µ0

## P value

If P is very small

We reject H<sub>0</sub>

and then: H<sub>a</sub> is significant

```shell
P-value = p = Pr(x̄ < 36.81|μ = 37)

pt(t,df=n-1)

`P-value = p = Pr(t < 5.83|t = 0) + Pr(t > 5.83|t = 0)`

```

# Latin Terms
- ɑ significance
- µ mean
- P proportion


# Authentication

> To authorize, use this code:

```R
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
```

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "Authorization: meowmeowmeow"
```

```javascript
const kittn = require('kittn');

let api = kittn.authorize('meowmeowmeow');
```

> Make sure to replace `meowmeowmeow` with your API key.

Kittn uses API keys to allow access to the API. You can register a new Kittn API key at our [developer portal](http://example.com/developers).

Kittn expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: meowmeowmeow`

<aside class="notice">
You must replace <code>meowmeowmeow</code> with your personal API key.
</aside>

# Kittens

## Get All Kittens

```R
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

This endpoint retrieves all kittens.

### HTTP Request

`GET http://example.com/api/kittens`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Specific Kitten

```R
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

```R
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
