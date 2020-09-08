# Responses
<aside class="notice">
A response object represents a single survey taker experience. It holds a collection of answers to every question in the survey. It also includes metadata about the taker collected by the GetFeedback system.
</aside>

## Get All Responses

```http
GET /surveys/:survey_id/responses HTTP/1.1
Authorization: token YOUR_GETFEEDBACK_ACCESS_TOKEN
Content-Type: application/json
```

```json
{
  "active_models": [
    {
      "id": 525,
      "token": "cTmIyeFWNwqTJcZbEpHYmA",
      "status": "completed",
      "created_at": "2014-03-17T17:22:10.055-07:00",
      "updated_at": "2014-03-17T17:22:36.041-07:00",
      "merge_map": {
        "xid": "xxxxxxxxxxxxxxxxxx"
      },
      "answers": [
        {
          "id": 509,
          "type": "MultipleChoiceAnswer",
          "component_id": 73,
          "created_at": "2014-03-17T17:22:35.906-07:00",
          "choices": [
            {
              "id": 52,
              "text": "Yes",
              "is_other": false
            }
          ]
        },
        {
          "id": 507,
          "type": "RatingAnswer",
          "component_id": 92,
          "created_at": "2014-03-17T17:22:34.097-07:00",
          "number": 4,
          "scale": 5
        }
      ],
    },
    { },
    ...
  ]
}
```

### HTTP Request

`GET /surveys/:survey_id/responses`

### Query Parameters

Parameter | Description
--------- | -----------
**since** | Timestamp from which to return responses. If set with an ISO 8601 datestamp, responses are returned in ascending timestamp ordered by the `since_field` (see below). If not set or an incorrect format is passed, returns responses in descending timestamp order by `created_at`.
**since_field** | If using since, date on responses to compare to. Can be `created_at`, `updated_at`, or `completed_at`. When set to `completed_at`, status is filtered to only completed responses. Defaults to `created_at`.
**until** | If using since, timestamp to which to return responses. If set with an ISO 8601 datestamp, it will be the endcap date to the since param.
**status** | Can be set to started or completed and then only responses in that state will be returned. If not set, returns all responses.
**per_page** | Responses to return per page. Defaults to 30. Maximum 100.
**page** | Page number when paging through responses. Note there is no server cursor state.


### Definitions

**merge_map:** Parameters that were appended to the URL when the taker opened the survey.

**component_id:** Identifier for the survey question the answer represents.

<aside class="success">
Responses are returned in descending timestamp order by created_at.
</aside>

## Get a Specific Response

```http
GET /surveys/:survey_id/responses/:id HTTP/1.1
Authorization: token YOUR_GETFEEDBACK_ACCESS_TOKEN
Content-Type: application/json
```

> The above command returns JSON structured like this:

```json
{
  "response": {
    "id": 101413,
    "token": "du7x49xk6A29BpVmU2fwm4",
    "status": "completed",
    "created_at": "2020-04-14T13:12:44.394-07:00",
    "updated_at": "2020-04-14T13:12:44.394-07:00",
    "completed_at": "2020-04-14T13:12:44.394-07:00",
    "limited": false,
    "merge_map": {},
    "platform": null,
    "browser": null,
    "country_code_with_emoji": null,
    "answers": [
      {
        "id": 102025,
        "type": "NetPromoter",
        "component_id": 9,
        "text": null,
        "created_at": "2020-04-14T13:12:44.439-07:00",
        "updated_at": "2020-04-14T13:12:44.439-07:00",
        "response_id": 101413,
        "comment": "",
        "embedded": false,
        "number": 9,
        "grid_item": null
      },
      {
        "id": 102026,
        "type": "CustomerSatisfaction",
        "component_id": 10,
        "text": null,
        "created_at": "2020-04-14T13:12:44.501-07:00",
        "updated_at": "2020-04-14T13:12:44.501-07:00",
        "response_id": 101413,
        "comment": "",
        "embedded": false,
        "number": 3,
        "grid_item": null
      },
      {
        "id": 102027,
        "type": "CustomerEffort",
        "component_id": 11,
        "text": null,
        "created_at": "2020-04-14T13:12:44.533-07:00",
        "updated_at": "2020-04-14T13:12:44.533-07:00",
        "response_id": 101413,
        "comment": "",
        "embedded": false,
        "number": 6,
        "grid_item": null
      }
    ]
  }
}
```

### HTTP Request

`GET /responses/:id`

`GET /surveys/:survey_id/responses/:id`

### URL Parameters

Parameter | Description
--------- | -----------
**id** | The `id` of the response to retrieve
**survey_id** | The `id` of the parent survey of the response to retrieve
