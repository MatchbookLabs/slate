# Surveys

## Get all surveys

```http
GET /surveys HTTP/1.1
Authorization: token YOUR_GETFEEDBACK_ACCESS_TOKEN
Content-Type: application/json
```

> The above command returns JSON structured like this:

```json
{
  "surveys": [
    {
      "id": 1,
      "name": "Customer Feedback",
      "questions_count": 1,
      "background_image_brightness": 0,
      "merge_keys": [],
      "embedded_answer_key_errors": [],
      "language": "en",
      "locale": "en-US",
      "folder_id": null,
      "use_rich_text": null,
      "multilanguage": false,
      "enabled_languages": [],
      "financial_data_paths": [],
      "financial_data_field": null,
      "store_ipdata": null,
      "only_defined_merge_keys": null,
      "discard_invalid_values": null,
      "public_host_settings": {
          "host": "localhost:3000",
          "protocol": "http"
      },
      "font_override": null,
      "background_display_override": null,
      "background_type_override": null,
      "background_color_override": null,
      "question_color_override": null,
      "answer_color_override": null,
      "button_color_override": null,
      "user_id": 1,
      "created_at": "2020-08-31T11:58:03.668-07:00",
      "updated_at": "2020-08-31T11:58:03.668-07:00",
      "started_responses_count": 0,
      "completed_responses_count": 0,
      "limited_responses_count": 0,
      "notification_level": "all",
      "show_incomplete_responses": null,
      "send_incomplete_responses": null,
      "walkthrough": 0,
      "shares": {
          "shares": []
      },
      "survey_shares": {
          "survey_shares": []
      },
      "publish_to_id": null,
      "draft_id": null,
      "theme": {
          "id": 1,
          "name": "Default",
          "category": "colors",
          "background_image_brightness": 0,
          "font": "Open Sans",
          "background_display": "fill",
          "background_type": "color",
          "background_color": 16777215,
          "question_color": 3355443,
          "answer_color": 3355443,
          "button_color": 10066329,
          "background_image": null
      },
      "logo_media_object": null,
      "background_image_override": null
    }
  ]
}
```

### HTTP Request

`GET /surveys`

### URL Parameters

Parameter | Description
--------- | -----------
**filter** | When `shared`, returns user's shared surveys, otherwise returns user's active surveys

## Get a specific survey

```http
GET /surveys/:survey_id HTTP/1.1
Authorization: token YOUR_GETFEEDBACK_ACCESS_TOKEN
Content-Type: application/json
```

> The above command returns JSON structured like this:

```json
{
  "survey": {
    "id": 1,
    "name": "Customer Feedback",
    "questions_count": 1,
    "background_image_brightness": 0,
    "merge_keys": [],
    "embedded_answer_key_errors": [],
    "language": "en",
    "locale": "en-US",
    "folder_id": null,
    "use_rich_text": null,
    "multilanguage": false,
    "enabled_languages": [],
    "financial_data_paths": [],
    "financial_data_field": null,
    "store_ipdata": null,
    "only_defined_merge_keys": null,
    "discard_invalid_values": null,
    "public_host_settings": {
      "host": "localhost:3000",
      "protocol": "http"
    },
    "font_override": null,
    "background_display_override": null,
    "background_type_override": null,
    "background_color_override": null,
    "question_color_override": null,
    "answer_color_override": null,
    "button_color_override": null,
    "user_id": 1,
    "created_at": "2020-08-31T11:58:03.668-07:00",
    "updated_at": "2020-08-31T11:58:03.668-07:00",
    "started_responses_count": 0,
    "completed_responses_count": 0,
    "limited_responses_count": 0,
    "notification_level": "all",
    "show_incomplete_responses": null,
    "send_incomplete_responses": null,
    "walkthrough": 0,
    "shares": {
      "shares": []
    },
    "survey_shares": {
      "survey_shares": []
    },
    "publish_to_id": null,
    "draft_id": null,
    "share_token": "OSaqbk1T",
    "whitelabeled": null,
    "automagic_salesforce_sync": null,
    "merge_field_encryption": null,
    "draft_salesforce_credential_id": null,
    "draft_pardot_credential_id": null,
    "draft_differs": false,
    "last_published": null,
    "publishing": null,
    "response_graph_token": "eJyrViouLSpLrYzPTFGyMtRRSkksSY3PzCtJLSpLzFGyAvIrlWoB_JENEA.3uhiolOl_0WP7iG_h6vYj0HyUSudQ-Bn0TJqKG0CLHo",
    "server_held_change_count": 0,
    "theme": {
      "id": 1,
      "name": "Default",
      "category": "colors",
      "background_image_brightness": 0,
      "font": "Open Sans",
      "background_display": "fill",
      "background_type": "color",
      "background_color": 16777215,
      "question_color": 3355443,
      "answer_color": 3355443,
      "button_color": 10066329,
      "background_image": null
    },
    "logo_media_object": null,
    "user": {
      "id": 1,
      "email": "dev@getfeedback.com",
      "name": "Flabongo Don",
      "status": "active",
      "source": "organic",
      "permissions": 5,
      "time_zone": null,
      "team_id": 1,
      "has_invalid_card": false,
      "card_expiration_date": null,
      "is_team_owner": true,
      "default_tab": "surveys"
    },
    "background_image_override": null,
    "custom_domain": null,
    "salesforce_credential": null,
    "pardot_credential": null,
    "ordered_components": [
      {
        "id": 1,
        "survey_id": 1,
        "type": "CoverPage",
        "markup": null,
        "title": "Hey There.",
        "required": true,
        "randomize": false,
        "show_media": false,
        "is_question": false,
        "description": "Thanks for using GetFeedback. We're eager to hear anything that's on your mind.",
        "show_description": true,
        "has_grid_items": false,
        "stats": {},
        "choices_stats": [],
        "answers_count": 0,
        "mappable_field_types": [],
        "randomize_grid_items": false,
        "lhs_condition_ids": [],
        "target_action_ids": [],
        "comment_enabled": false,
        "comment_header": "",
        "commentable": false,
        "alignment": null,
        "show_top_media": true,
        "should_hide_merge_fields": false,
        "can_hide_merge_fields": false,
        "is_embedded_auto": false,
        "embedded_answer_key": "gf_q[1]",
        "is_embedded_answerable": false,
        "is_email_embeddable": false,
        "button_text": "Let's Get Started",
        "choices": [],
        "grid_items": [],
        "media_object": null,
        "top_media_object": null,
        "ordered_rules": [],
        "translations": []
      },
      {
        "id": 2,
        "survey_id": 1,
        "type": "ShortAnswer",
        "markup": null,
        "title": "What would you like to tell us?",
        "required": true,
        "randomize": false,
        "show_media": true,
        "is_question": true,
        "description": null,
        "show_description": true,
        "has_grid_items": false,
        "stats": {},
        "choices_stats": [],
        "answers_count": 0,
        "mappable_field_types": [
          "string",
          "textarea"
        ],
        "randomize_grid_items": false,
        "lhs_condition_ids": [],
        "target_action_ids": [],
        "comment_enabled": false,
        "comment_header": "",
        "commentable": false,
        "alignment": null,
        "show_top_media": false,
        "should_hide_merge_fields": false,
        "can_hide_merge_fields": false,
        "is_embedded_auto": true,
        "embedded_answer_key": "gf_q[2]",
        "is_embedded_answerable": false,
        "is_email_embeddable": false,
        "multiline": true,
        "choices": [],
        "grid_items": [],
        "media_object": null,
        "top_media_object": null,
        "ordered_rules": [],
        "translations": []
      },
      {
        "id": 3,
        "survey_id": 1,
        "type": "ThankYouPage",
        "markup": null,
        "title": "Thanks! We appreciate it.",
        "required": true,
        "randomize": false,
        "show_media": true,
        "is_question": false,
        "description": "We've just been notified and will follow up shortly.",
        "show_description": true,
        "has_grid_items": false,
        "stats": {},
        "choices_stats": [],
        "answers_count": 0,
        "mappable_field_types": [],
        "randomize_grid_items": false,
        "lhs_condition_ids": [],
        "target_action_ids": [],
        "comment_enabled": false,
        "comment_header": "",
        "commentable": false,
        "alignment": null,
        "show_top_media": false,
        "should_hide_merge_fields": false,
        "can_hide_merge_fields": false,
        "is_embedded_auto": false,
        "embedded_answer_key": "gf_q[3]",
        "is_embedded_answerable": false,
        "is_email_embeddable": false,
        "button_text": "Done",
        "button_url": null,
        "choices": [],
        "grid_items": [],
        "media_object": null,
        "top_media_object": null,
        "ordered_rules": [],
        "translations": []
      }
    ],
    "campaigns": [
      {
        "id": 2,
        "survey_id": 1,
        "type": "WebLink",
        "token": "feedback",
        "ended_at": null,
        "expiry_period": null,
        "custom_urls": [],
        "logo_media_object": null
      },
      {
        "id": 1,
        "survey_id": 1,
        "type": "WebLink",
        "token": "ZD3EgRWm",
        "ended_at": null,
        "expiry_period": null,
        "custom_urls": [],
        "logo_media_object": null
      }
    ],
    "pardot_object_mappings": [],
    "salesforce_mapping_failure_strategy": {
      "id": 1,
      "email_notifications_enabled": false,
      "email_summaries_enabled": false,
      "email_summaries_sent_count": 0,
      "email_summary_scheduled_for": null
    },
    "rules": [],
    "defined_merge_keys": []
  }
}
```

### HTTP Request

`GET /surveys/:survey_id`

## Send to a list from Getfeedback

```http
POST /surveys/:survey_id/send_invites HTTP/1.1
Authorization: token YOUR_GETFEEDBACK_ACCESS_TOKEN
Content-Type: application/json
```

> The above command returns JSON structured like this:

```json
{
  "total_recipients": 10,
  "subject": "[name] - Take this survey",
  "title": "Here's your survey!"
}
```

This endpoint sends out invites in bulk

### HTTP Request

`POST /surveys/:survey_id/send_invites`

### URL Parameters

Parameter | Description
--------- | -----------
**anonymize** | When true, disables click & open tracking as well as disallows relating responses to recipient records
**from_email_name** | Sender's name
**from_email_domain** | Sender's email domain
**subject** | Email invite subject
**title** | Email invite title
**body** | Email invite body
**button_label** | Email invite button label
**subscriber_list** | An array of objects that include these keys: `email`, `first_name` and `last_name`