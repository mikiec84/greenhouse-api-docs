# Candidates

An organization's candidates.

## The candidate object

```json
{
    "id": 53883394,
    "first_name": "John",
    "last_name": "Locke",
    "company": "The Tustin Box Company",
    "title": "Man of Mystery",
    "created_at": "2017-08-15T03:31:46.591Z",
    "updated_at": "2017-09-28T12:29:30.497Z",
    "last_activity": "2017-09-28T12:29:30.481Z",
    "is_private": false,
    "photo_url": "https://prod-heroku.s3.amazonaws.com/people/photos/053/883/394/original/corgi.jpg?AWSAccessKeyId=AKIAIK36UTOKQ5F2YNMQ&Expires=1509193807&Signature=cg%2BhyNTvvNgTTzWtsMJJZvPRYH4%3D",
    "attachments": [
        {
            "filename": "John_Locke_Offer_Packet_09_27_2017.pdf",
            "url": "https://prod-heroku.s3.amazonaws.com/person_attachments/data/077/683/131/original/John_Locke_Offer_Packet_09_27_2017.pdf?AWSAccessKeyId=AKIAIK36UTOKQ5F2YNMQ&Expires=1509193807&Signature=R5TbJPzD7TO5NgX8K8Y0yogPstY%3D",
            "type": "offer_packet"
        }
    ],
    "application_ids": [
        69102626,
        65153308
    ],
    "phone_numbers": [
        {
            "value": "555-555-5555",
            "type": "mobile"
        }
    ],
    "addresses": [
        {
            "value": "123 City Street\nNew York, Ny 10001",
            "type": "home"
        }
    ],
    "email_addresses": [
        {
            "value": "test@work.com",
            "type": "work"
        },
        {
            "value": "test@example.com",
            "type": "personal"
        }
    ],
    "website_addresses": [
        {
            "value": "mysite.com",
            "type": "personal"
        }
    ],
    "social_media_addresses": [
        {
            "value": "twitter.com/test"
        }
    ],
    "recruiter": {
        "id": 92120,
        "first_name": "Greenhouse",
        "last_name": "Admin",
        "name": "Greenhouse Admin",
        "employee_id": null
    },
    "coordinator": null,
    "tags": [
        "Python",
        "Ruby"
    ],
    "applications": [
        {
            "id": 69102626,
            "candidate_id": 53883394,
            "prospect": false,
            "applied_at": "2017-09-27T12:03:02.728Z",
            "rejected_at": "2017-09-27T12:11:40.877Z",
            "last_activity_at": "2017-09-28T12:29:30.481Z",
            "source": {
                "id": 16,
                "public_name": "LinkedIn (Prospecting)"
            },
            "credited_to": {
                "id": 165372,
                "first_name": "Joel",
                "last_name": "Job Admin",
                "name": "Joel Job Admin",
                "employee_id": null
            },
            "rejection_reason": {
                "id": 9504,
                "name": "Hired another candidate",
                "type": {
                    "id": 1,
                    "name": "We rejected them"
                }
            },
            "rejection_details": {},
            "jobs": [
                {
                    "id": 149995,
                    "name": "DevOps Engineer"
                }
            ],
            "status": "rejected",
            "current_stage": {
                "id": 1073533,
                "name": "Take Home Test"
            },
            "answers": [],
            "prospect_detail": {
                "prospect_pool": null,
                "prospect_stage": null,
                "prospect_owner": null
            }
        },
        {
            "id": 65153308,
            "candidate_id": 53883394,
            "prospect": false,
            "applied_at": "2017-08-15T03:31:46.637Z",
            "rejected_at": null,
            "last_activity_at": "2017-09-28T12:29:30.481Z",
            "source": {
                "id": 12,
                "public_name": "Meetups"
            },
            "credited_to": {
                "id": 566819,
                "first_name": "Bob",
                "last_name": "Smith",
                "name": "Bob Smith",
                "employee_id": null
            },
            "rejection_reason": null,
            "rejection_details": null,
            "jobs": [
                {
                    "id": 299100,
                    "name": "Data Scientist - BK"
                }
            ],
            "status": "active",
            "current_stage": {
                "id": 2966800,
                "name": "Face to Face"
            },
            "answers": [],
            "prospect_detail": {
                "prospect_pool": null,
                "prospect_stage": null,
                "prospect_owner": null
            }
        }
    ],
    "educations": [
        {
            "id": 561227,
            "school_name": "University of Michigan - Ann Arbor",
            "degree": "Bachelor's Degree",
            "discipline": "Computer Science"
        }
    ],
    "employments": [],
    "custom_fields": {
        "desired_salary": "1000000000",
        "work_remotely": true,
        "graduation_year": "2018"
    },
    "keyed_custom_fields": {
        "desired_salary": {
            "name": "Desired Salary",
            "type": "short_text",
            "value": "1000000000"
        },
        "work_remotely": {
            "name": "Work Remotely",
            "type": "boolean",
            "value": true
        },
        "graduation_year_1": {
            "name": "Graduation Year",
            "type": "single_select",
            "value": "2018"
        }
    }
}
```

### Noteworthy attributes

| Attribute | Description |
|-----------|-------------|
| id | The candidate's unique identifier |
| company | The company at which the candidate currently works
| title | The candidate's current title
| is_private | Whether the candidate is private or not. One of: ["true", "false"]
| application_ids | Array of [application](#applications) IDs associated with this candidate. Can contain none, one, or several application IDs.
| phone_numbers[].type | One of: ["home", "work", "mobile", "skype", "other"]
| addresses[].type | One of: ["home", "work", "other"]
| email_addresses[].type | One of: ["personal", "work", "other"]
| website_addresses[].type | One of: ["personal", "company", "portfolio", "blog", "other"]
| recruiter | The recruiter [user](#users) who is responsible for this candidate.
| coordinator | The coordinator [user](#users) who is responsible for this candidate.
| attachments[].type | One of: ["admin_only", "public", "cover_letter", "offer_packet", "resume", "take_home_test"]
| attachments[].url | URLs expire in 30 days.
| custom_fields | Contains a hash of the custom fields configured for this resource. The properties in this hash reflect the active custom fields as of the time this method is called.
| keyed_custom_fields | This contains the same information as custom_fields but formatted in a different way that includes more information.  This will tell you the type of custom field data to expect, the text name of custom field, and the value.  The key of this hash is the custom field's immutable field key, which will not change even if the name of the custom field is changed in Greenhouse.

## GET: List Candidates

```shell
curl 'https://harvest.greenhouse.io/v1/candidates'
  -H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

> The above command returns JSON structured like this:

```json
[
 {
    "id": 53883394,
    "first_name": "John",
    "last_name": "Locke",
    "company": "The Tustin Box Company",
    "title": "Man of Mystery",
    "created_at": "2017-08-15T03:31:46.591Z",
    "updated_at": "2017-09-28T12:29:30.497Z",
    "last_activity": "2017-09-28T12:29:30.481Z",
    "is_private": false,
    "photo_url": "https://prod-heroku.s3.amazonaws.com/people/photos/053/883/394/original/corgi.jpg?AWSAccessKeyId=AKIAIK36UTOKQ5F2YNMQ&Expires=1509193807&Signature=cg%2BhyNTvvNgTTzWtsMJJZvPRYH4%3D",
    "attachments": [
        {
            "filename": "John_Locke_Offer_Packet_09_27_2017.pdf",
            "url": "https://prod-heroku.s3.amazonaws.com/person_attachments/data/077/683/131/original/John_Locke_Offer_Packet_09_27_2017.pdf?AWSAccessKeyId=AKIAIK36UTOKQ5F2YNMQ&Expires=1509193807&Signature=R5TbJPzD7TO5NgX8K8Y0yogPstY%3D",
            "type": "offer_packet"
        }
    ],
    "application_ids": [
        69103370,
        65153308
    ],
    "phone_numbers": [
        {
            "value": "555-555-5555",
            "type": "mobile"
        }
    ],
    "addresses": [
        {
            "value": "123 City Street\nNew York, Ny 10001",
            "type": "home"
        }
    ],
    "email_addresses": [
        {
            "value": "test@work.com",
            "type": "work"
        }
    ],
    "website_addresses": [
        {
            "value": "mysite.com",
            "type": "personal"
        }
    ],
   "social_media_addresses": [],
    "recruiter": {
        "id": 92120,
        "first_name": "Greenhouse",
        "last_name": "Admin",
        "name": "Greenhouse Admin",
        "employee_id": null
    },
    "coordinator": null,
    "tags": [
        "Python",
        "Ruby"
    ],
    "applications": [
        {
            "id": 69103370,
            "candidate_id": 53883394,
            "prospect": true,
            "applied_at": "2017-09-27T12:21:37.234Z",
            "rejected_at": null,
            "last_activity_at": "2017-09-28T12:29:30.481Z",
            "source": {
                "id": 16,
                "public_name": "LinkedIn (Prospecting)"
            },
            "credited_to": {
                "id": 92120,
                "first_name": "Greenhouse",
                "last_name": "Admin",
                "name": "Greenhouse Admin",
                "employee_id": null
            },
            "rejection_reason": null,
            "rejection_details": null,
            "jobs": [
                {
                    "id": 87752,
                    "name": "Full Stack Engineer"
                }
            ],
            "status": "active",
            "current_stage": null,
            "answers": [],
            "prospect_detail": {
                "prospect_pool": {
                    "id": 224,
                    "name": "Cold Outreach: Sourced"
                },
                "prospect_stage": {
                    "id": 817,
                    "name": "Contacted"
                },
                "prospect_owner": {
                    "id": 92120,
                    "name": "Greenhouse Admin"
                }
            }
        },
        {
            "id": 65153308,
            "candidate_id": 53883394,
            "prospect": false,
            "applied_at": "2017-08-15T03:31:46.637Z",
            "rejected_at": null,
            "last_activity_at": "2017-09-28T12:29:30.481Z",
            "source": {
                "id": 12,
                "public_name": "Meetups"
            },
            "credited_to": {
                "id": 566819,
                "first_name": "Bob",
                "last_name": "Smith",
                "name": "Bob Smith",
                "employee_id": null
            },
            "rejection_reason": null,
            "rejection_details": null,
            "jobs": [
                {
                    "id": 299100,
                    "name": "Data Scientist - BK"
                }
            ],
            "status": "active",
            "current_stage": {
                "id": 2966800,
                "name": "Face to Face"
            },
            "answers": [],
            "prospect_detail": {
                "prospect_pool": null,
                "prospect_stage": null,
                "prospect_owner": null
            }
        }
    ],
    "educations": [
        {
            "id": 561227,
            "school_name": "University of Michigan - Ann Arbor",
            "degree": "Bachelor's Degree",
            "discipline": "Computer Science"
        }
    ],
    "employments": [],
    "custom_fields": {
        "desired_salary": "1000000000",
        "work_remotely": true,
        "graduation_year": "2018"
    },
    "keyed_custom_fields": {
        "desired_salary": {
            "name": "Desired Salary",
            "type": "short_text",
            "value": "1000000000"
        },
        "work_remotely": {
            "name": "Work Remotely",
            "type": "boolean",
            "value": true
        },
        "graduation_year_1": {
            "name": "Graduation Year",
            "type": "single_select",
            "value": "2018"
        }
     }
  } 
]
```

List all of an organization's candidates.

### HTTP Request

`GET https://harvest.greenhouse.io/v1/candidates`

### Querystring parameters

| Parameter | Description |
|-----------|-------------|
| per_page | Return up to this number of objects per response. Must be an integer between 1 and 500. Defaults to 100.
| page | A cursor for use in pagination.  Returns the n-th chunk of `per_page` objects.
| created_before | Return only candidates that were created before this timestamp. Timestamp must be in in [ISO-8601] (#general-considerations) format.
| created_after | Return only candidates that were created after this timestamp. Timestamp must be in in [ISO-8601] (#general-considerations) format.
| updated_before | Return only candidates that were updated before this timestamp. Timestamp must be in in [ISO-8601] (#general-considerations) format.
| updated_after | Return only candidates that were updated after this timestamp. Timestamp must be in in [ISO-8601] (#general-considerations) format.
| job_id | If supplied, only return candidates that have applied to this job. Will return both when a candidate has applied to a job and when they're a prospect for a job.
| email | If supplied, only return candidates who have a matching e-mail address. If supplied with job_id, only return a candidate with a matching e-mail with an application on the job.

<br>

[See noteworthy response attributes.] (#the-candidate-object)

## GET: Retrieve Candidate

```shell
curl 'https://harvest.greenhouse.io/v1/candidates/{id}'
  -H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

> The above command returns JSON structured like this:

```json
{
    "id": 53883394,
    "first_name": "John",
    "last_name": "Locke",
    "company": "The Tustin Box Company",
    "title": "Man of Mystery",
    "created_at": "2017-08-15T03:31:46.591Z",
    "updated_at": "2017-09-28T12:29:30.497Z",
    "last_activity": "2017-09-28T12:29:30.481Z",
    "is_private": false,
    "photo_url": "https://prod-heroku.s3.amazonaws.com/people/photos/053/883/394/original/corgi.jpg?AWSAccessKeyId=AKIAIK36UTOKQ5F2YNMQ&Expires=1509193807&Signature=cg%2BhyNTvvNgTTzWtsMJJZvPRYH4%3D",
    "attachments": [
        {
            "filename": "John_Locke_Offer_Packet_09_27_2017.pdf",
            "url": "https://prod-heroku.s3.amazonaws.com/person_attachments/data/077/683/131/original/John_Locke_Offer_Packet_09_27_2017.pdf?AWSAccessKeyId=AKIAIK36UTOKQ5F2YNMQ&Expires=1509193807&Signature=R5TbJPzD7TO5NgX8K8Y0yogPstY%3D",
            "type": "offer_packet"
        }
    ],
    "application_ids": [
        69102626,
        65153308
    ],
    "phone_numbers": [
        {
            "value": "555-555-5555",
            "type": "mobile"
        }
    ],
    "addresses": [],
    "email_addresses": [
        {
            "value": "test@work.com",
            "type": "work"
        },
        {
            "value": "test@example.com",
            "type": "personal"
        }
    ],
    "website_addresses": [
        {
            "value": "mysite.com",
            "type": "personal"
        }
    ],
    "social_media_addresses": [],
    "recruiter": {
        "id": 92120,
        "first_name": "Greenhouse",
        "last_name": "Admin",
        "name": "Greenhouse Admin",
        "employee_id": null
    },
    "coordinator": null,
    "tags": [
        "Python",
        "Ruby"
    ],
    "applications": [
        {
            "id": 69102626,
            "candidate_id": 53883394,
            "prospect": false,
            "applied_at": "2017-09-27T12:03:02.728Z",
            "rejected_at": "2017-09-27T12:11:40.877Z",
            "last_activity_at": "2017-09-28T12:29:30.481Z",
            "source": {
                "id": 16,
                "public_name": "LinkedIn (Prospecting)"
            },
            "credited_to": {
                "id": 165372,
                "first_name": "Joel",
                "last_name": "Job Admin",
                "name": "Joel Job Admin",
                "employee_id": null
            },
            "rejection_reason": {
                "id": 9504,
                "name": "Hired another candidate",
                "type": {
                    "id": 1,
                    "name": "We rejected them"
                }
            },
            "rejection_details": {},
            "jobs": [
                {
                    "id": 149995,
                    "name": "DevOps Engineer"
                }
            ],
            "status": "rejected",
            "current_stage": {
                "id": 1073533,
                "name": "Take Home Test"
            },
            "answers": [],
            "prospect_detail": {
                "prospect_pool": null,
                "prospect_stage": null,
                "prospect_owner": null
            }
        },
        {
            "id": 65153308,
            "candidate_id": 53883394,
            "prospect": false,
            "applied_at": "2017-08-15T03:31:46.637Z",
            "rejected_at": null,
            "last_activity_at": "2017-09-28T12:29:30.481Z",
            "source": {
                "id": 12,
                "public_name": "Meetups"
            },
            "credited_to": {
                "id": 566819,
                "first_name": "Bob",
                "last_name": "Smith",
                "name": "Bob Smith",
                "employee_id": null
            },
            "rejection_reason": null,
            "rejection_details": null,
            "jobs": [
                {
                    "id": 299100,
                    "name": "Data Scientist - BK"
                }
            ],
            "status": "active",
            "current_stage": {
                "id": 2966800,
                "name": "Face to Face"
            },
            "answers": [],
            "prospect_detail": {
                "prospect_pool": null,
                "prospect_stage": null,
                "prospect_owner": null
            }
        }
    ],
    "educations": [
        {
            "id": 561227,
            "school_name": "University of Michigan - Ann Arbor",
            "degree": "Bachelor's Degree",
            "discipline": "Computer Science"
        }
    ],
    "employments": [],
    "custom_fields": {
        "desired_salary": "1000000000",
        "work_remotely": true,
        "graduation_year": "2018"
    },
    "keyed_custom_fields": {
        "desired_salary": {
            "name": "Desired Salary",
            "type": "short_text",
            "value": "1000000000"
        },
        "work_remotely": {
            "name": "Work Remotely",
            "type": "boolean",
            "value": true
        },
        "graduation_year_1": {
            "name": "Graduation Year",
            "type": "single_select",
            "value": "2018"
        }
    }
}
```

Retrieve a candidate by its `id`.

### HTTP Request

`GET https://harvest.greenhouse.io/v1/candidates/{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the candidate to retrieve

<br>

[See noteworthy response attributes.] (#the-candidate-object)

## DELETE: Delete Candidate

```shell
curl -X DELETE 'https://harvest.greenhouse.io/v1/candidates/{id}'
-H "On-Behalf-Of: {greenhouse user ID}"
-H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

> The above returns a JSON response, structured like this:

```json
{
  "message": "Person 29622362 has been deleted."
}
```

Delete a candidate by `id`.

### HTTP Request

`DELETE https://harvest.greenhouse.io/v1/candidates/{id}`

### Headers

Header | Description
--------- | -----------
On-Behalf-Of | ID of the user issuing this request. Required for auditing purposes.

<br>

[See noteworthy response attributes.] (#the-candidate-object)

## PATCH: Edit Candidate

```shell
curl -X PATCH 'https://harvest.greenhouse.io/v1/candidates/{id}'
-H "On-Behalf-Of: {greenhouse user ID}"
-H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

> The above command takes a JSON request, structured like this:

```json
{
  "first_name": "New",
  "last_name": "Name",
  "company": "The Tustin Box Company",
  "title": "Man of Mystery",
  "is_private": true,
  "phone_numbers": [
    {
      "value": "555-1212",
      "type": "mobile"
    }
  ],
  "addresses": [
    {
      "value": "123 Fake St.",
      "type": "home"
    }
  ],
  "email_addresses": [
    {
      "value": "john.locke+work@example.com",
      "type": "work"
    },
    {
      "value": "john.locke@example.com",
      "type": "personal"
    }
  ],
  "website_addresses": [
    {
      "value": "johnlocke.example.com",
      "type": "personal"
    }
  ],
  "social_media_addresses": [
    {
      "value": "linkedin.example.com/john.locke"
    },
    {
      "value": "@johnlocke"
    }
  ],
  "tags": [
    "Walkabout",
    "Orientation"
  ],
  "custom_fields": [
    {
        "id": 1234,
        "value": "Some new value"
    },
    {
        "name_key": "single_select_field_name",
        "value": 12345
   },
   {
        "id": 5678,
        "delete_value": "true"
   }
  ]
}
```
> The above returns a JSON response, structured like this:

```json
[
  {
      "id": 53883394,
      "first_name": "New",
      "last_name": "Name",
      "company": "The Tustin Box Company",
      "title": "Man of Mystery",
      "created_at": "2017-08-15T03:31:46.591Z",
      "updated_at": "2017-09-28T12:54:34.257Z",
      "last_activity": "2017-09-28T12:54:34.243Z",
      "is_private": true,
      "photo_url": "https://prod-heroku.s3.amazonaws.com/people/photos/053/883/394/original/corgi.jpg?AWSAccessKeyId=AKIAIK36UTOKQ5F2YNMQ&Expires=1509195274&Signature=NHilozZgXPHOI9uvpKTnf3A50Gc%3D",
      "attachments": [
          {
              "filename": "John_Locke_Offer_Packet_09_28_2017.pdf",
              "url": "https://prod-heroku.s3.amazonaws.com/person_attachments/data/077/815/020/original/John_Locke_Offer_Packet_09_28_2017.pdf?AWSAccessKeyId=AKIAIK36UTOKQ5F2YNMQ&Expires=1509195274&Signature=Vb7z8GlHJXvwqhvx%2BTrIZ32zaVo%3D",
              "type": "offer_packet"
          }
      ],
      "application_ids": [
          65153308
      ],
      "phone_numbers": [
          {
              "value": "555-1212",
              "type": "mobile"
          }
      ],
      "addresses": [
          {
              "value": "123 Fake Street",
              "type": "home"
          }
      ],
      "email_addresses": [
          {
              "value": "john.locke+work@example.com",
              "type": "work"
          },
          {
              "value": "john.locke@example.com",
              "type": "personal"
          }
      ],
      "website_addresses": [
          {
              "value": "johnlocke.example.com",
              "type": "personal"
          }
      ],
       "social_media_addresses": [
          {
            "value": "linkedin.example.com/john.locke"
          },
          {
            "value": "@johnlocke"
          }
      ],
      "recruiter": {
          "id": 92120,
          "first_name": "Greenhouse",
          "last_name": "Admin",
          "name": "Greenhouse Admin",
          "employee_id": null
      },
      "coordinator": null,
      "tags": [
          "Walkabout",
          "Orientation"
      ],
      "applications": [
          {
              "id": 65153308,
              "candidate_id": 53883394,
              "prospect": false,
              "applied_at": "2017-08-15T03:31:46.637Z",
              "rejected_at": null,
              "last_activity_at": "2017-09-28T12:54:34.243Z",
              "source": {
                  "id": 12,
                  "public_name": "Meetups"
              },
              "credited_to": {
                  "id": 566819,
                  "first_name": "Bob",
                  "last_name": "Smith",
                  "name": "Bob Smith",
                  "employee_id": "ABC12345"
              },
              "rejection_reason": null,
              "rejection_details": null,
              "jobs": [
                  {
                      "id": 299100,
                      "name": "Data Scientist - BK"
                  }
              ],
              "status": "active",
              "current_stage": {
                  "id": 2966800,
                  "name": "Face to Face"
              },
              "answers": [],
              "prospect_detail": {
                  "prospect_pool": null,
                  "prospect_stage": null,
                  "prospect_owner": null
              }
          }
      ],
      "educations": [],
      "employments": [],
      "custom_fields": {
        "current_salary": "$23k",
        "desired_salary": "$42k"
      },
      "keyed_custom_fields": {
        "current_salary": {
          "name": "Current salary",
          "type": "short_text",
          "value": "$23k"
        },
        "desired_salary": {
          "name": "Desired salary",
          "type": "short_text",
          "value": "$42k"
        }
     }
  }     
]
```

Update or `patch` a single candidate by its `id`.

### HTTP Request

`PATCH https://harvest.greenhouse.io/v1/candidates/{id}`

### Headers

Header | Description
--------- | -----------
On-Behalf-Of | ID of the user issuing this request. Required for auditing purposes.

### JSON Body Parameters

Parameter | Required | Type | Description
--------- | ----------- | ----------- | -----------
first_name | No | string | The candidate's first name
last_name | No | string | The candidate's last name
company | No | string | The candidate's company
title | No | string | The candidate's title
is_private | Whether the candidate is private or not. One of: ["true", "false"]
phone_numbers[] | No | phone_number | Array of phone numbers. Passing an empty array will clear all.
addresses[] | No | address | Array of addresses. Passing an empty array will clear all.
email_addresses[] | No | email_address | Array of email addresses. Passing an empty array will clear all.
website_addresses[] | No | website_address | Array of website addresses. Passing an empty array will clear all.
social_media_addresses[] | No | social_media_address | Array of social media addresses. Passing an empty array will clear all.
tags[] | No | string | Array of tags as strings. Passing an empty array will clear all.
custom_fields[] | No |  custom_field | Array of hashes containing new custom field values.  Passing an empty array does nothing.

### Custom Field Parameters

The custom field parameter structure is different in the PATCH method then in GET methods and responses.  Certain type of custom fields require different elements to be included, while deleting a field requires a specific argument.  What follows is the description of each item in a custom field element and what is required depending on the type.

Parameter | Required for | Description
---------- | -------------- | ----------------
id | all | The custom field id for this particular custom field.  One of this or name_key is required.
name_key | all | The field key for this custom field. This can be found in Greenhouse while editing custom options as "Immutable Field Key"  This or id is required for all custom field elements.
value | all | The value field contains the new custom field value.  In most cases this will be a string or a number.  In the case of single-select or multi-select custom fields, this will be a custom field option id or an array of custom field option ids, respectively. In the case of single-select fields, this can also be a string that matches an existing option value name exactly.
unit | currency | This contains the currency unit for a currency custom field. It is only required when updating a currency custom field.  This should accept any 3-character currency code from the ISO-4217 standard.
delete_value  | n/a | When this element is included with a value of "true" (note, string true, not boolean true) the custom field value will be removed from Greenhouse.  Note that updating a custom field value to nil or a blank string will not work, as validations require these to be non-blank values.

<br>

[See noteworthy response attributes.] (#the-candidate-object)

## POST: Add Candidate Application

```shell
curl -X POST 'https://harvest.greenhouse.io/v1/candidates/{id}/applications'
-H "On-Behalf-Of: {greenhouse user ID}"
-H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

> The above command takes a JSON request, structured like this:

```
{
  "job_id": 266926,
  "source_id": 7,
  "initial_stage_id": 2708728,
  "referrer": {
    "type": "id",
    "value": 770
  },
  "attachments": [{
    "filename": "resume.pdf",
    "type": "resume",
    "content": "MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6...",
    "content_type": "application/pdf"
}
```

> The above command returns a JSON response, structured like this:

```json
{
  "id": 38776620,
  "candidate_id": 15803530,
  "prospect": false,
  "applied_at": "2016-11-08T19:50:49.746Z",
  "rejected_at": null,
  "last_activity_at": "2016-11-04T19:46:40.377Z",
  "source": {
    "id": 7,
    "public_name": "Indeed"
  },
  "credited_to": {
        "id": 770,
        "first_name": "Moon",
        "last_name": "Colorado",
        "name": "Moon Colorado",
        "employee_id": null
    },
  "rejection_reason": null,
  "rejection_details": null,
  "jobs": [
    {
      "id": 266926,
      "name": "Construction Project Manager"
    }
  ],
  "status": "active",
  "current_stage": {
    "id": 1945557,
    "name": "Application Review"
  },
  "answers": [],
  "custom_fields": {
    "birthday": "1992-01-27",
    "bio": "This is my bio"
  },
  "prospect_detail": {
    "prospect_pool": null,
    "prospect_stage": null,
    "prospect_owner": null
  }
}
```

Create a new application for this candidate or prospect. If a prospect, this will add a new candidate application to the given job on their profile, this will not convert their existing prospect application into a candidate application.

### HTTP Request

`POST https://harvest.greenhouse.io/v1/candidates/{id}/applications`

### Headers

Header | Description
--------- | -----------
On-Behalf-Of | ID of the user issuing this request. Required for auditing purposes.

### JSON Body Parameters

Parameter | Required | Type | Description
--------- | ----------- | ----------- | ----------- | -----------
job_id | Yes | integer | The ID of the job you want to create an application to for this candidate
source_id | No | integer | The id of the source to be credited for this application
initial_stage_id | No | integer | The ID of the job stage this application will be created in.
referrer | No | object | An object representing the referrer
referrer[type] | No | string | A string representing the type of referrer: 'id', 'email', or 'outside'
referrer[value] | No | string | The id of the user who made the referral (not the referrer id)
attachments | No | array | An array of attachments to be uploaded to this application. See [Add Attachment] (#post-add-attachment) for parameters.

## POST: Add Attachment

```shell
curl -X POST 'https://harvest.greenhouse.io/v1/candidates/{id}/attachments'
-H "On-Behalf-Of: {greenhouse user ID}"
-H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```
> The above command takes a JSON request, structured like this:

```json
{
  "filename" : "resume.pdf",
  "type" : "resume",
  "content" : "R0lGODlhAQABAIAAAAUEBAAAACwAAAAAAQABAAACAkQBADs...",
  "content_type" : "application/pdf"
}
```

> The above command returns a JSON response, structured like this:

```json
{
  "filename": "resume.pdf",
  "url": "https://prod-heroku.s3.amazonaws.com/...",
  "type": "resume",
  "content_type": "application/pdf"
}
```

Post an attachment to a candidate's profile by the candidate `id`.

### HTTP Request

`POST https://harvest.greenhouse.io/v1/candidates/{id}/attachments`

### Headers

Header | Description
--------- | -----------
On-Behalf-Of | ID of the user issuing this request. Required for auditing purposes.


### JSON Body Parameters

Parameter | Required | Type | Description
--------- | ----------- | ----------- | -----------
filename | Yes | string | Name of the file
type | Yes | string | One of: ["resume", "cover_letter", "admin_only"]
content | No | string | Base64 encoded content of the attachment (if you are providing content, you do not need to provide url)
url | No | string | Url of the attachment (if you are providing the url, you do not need to provide the content)
content_type | No* | string | The content-type of the document you are sending.  When using a URL, this generally isn't needed, as the responding server will deliver a content type.  This should be included for encoded content.  Accepted content types are: <ul><li>"application/atom+xml"</li><li>"application/javascript"</li><li>"application/json"</li><li>"application/msgpack"</li><li>"application/pdf"</li><li>"application/rss+xml"</li><li>"application/vnd.ms-excel"</li><li>"application/vnd.openxmlformats-<br>officedocument.spreadsheetml.sheet"</li><li>"application/vnd.openxmlformats-<br>officedocument.wordprocessingml.document"</li><li>"application/xml"</li><li>"application/x-www-form-urlencoded"</li><li>"application/x-yaml"</li><li>"application/zip"</li><li>"multipart/form-data"</li><li>"image/bmp"</li><li>"image/gif"</li><li>"image/jpeg"</li><li>"image/png"</li><li>"image/tiff"</li><li>"text/calendar"</li><li>"text/css"</li><li>"text/csv"</li><li>"text/html"</li><li>"text/javascript"</li><li>"text/plain"</li><li>"text/vcard"</li><li>"video/mpeg"</li></ul>

\* \- content_type is not required for purposes of backward compatibility. It is _strongly_ recommended that you always include content type for document uploads.

## POST: Add Candidate

```shell
curl -X POST 'https://harvest.greenhouse.io/v1/candidates'
-H "On-Behalf-Of: {greenhouse user ID}"
-H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

> The above command takes a JSON request, structured like this:

```json
{
  "first_name": "John",
  "last_name": "Locke",
  "company": "The Tustin Box Company",
  "title": "Man of Mystery",
  "is_private": false,
  "phone_numbers": [
    {
      "value": "555-1212",
      "type": "mobile"
    }
  ],
  "addresses": [
    {
      "value": "123 Fake St.",
      "type": "home"
    }
  ],
  "email_addresses": [
    {
      "value": "john.locke+work@example.com",
      "type": "work"
    },
    {
      "value": "john.locke@example.com",
      "type": "personal"
    }
  ],
  "website_addresses": [
    {
      "value": "johnlocke.example.com",
      "type": "personal"
    }
  ],
  "social_media_addresses": [
    {
      "value": "linkedin.example.com/john.locke"
    },
    {
      "value": "@johnlocke"
    }
  ],
  "tags": [
    "Walkabout",
    "Orientation"
  ],
  "applications": [
    {
      "job_id": 215725
    },
     {
      "job_id": 185289
    }
  ]
}
```
> The above returns a JSON response, structured like this:

```json
{
    "id": 57683957,
    "first_name": "John",
    "last_name": "Locke",
    "company": "The Tustin Box Company",
    "title": "Man of Mystery",
    "created_at": "2017-09-28T13:27:54.735Z",
    "updated_at": "2017-09-28T13:27:55.229Z",
    "last_activity": "2017-09-28T13:27:55.213Z",
    "is_private": false,
    "photo_url": null,
    "attachments": [],
    "application_ids": [
        69201605,
        69201604
    ],
    "phone_numbers": [
        {
            "value": "555-1212",
            "type": "mobile"
        }
    ],
    "addresses": [
        {
            "value": "123 Fake St.",
            "type": "home"
        }
    ],
    "email_addresses": [
        {
            "value": "john.locke@example.com",
            "type": "personal"
        },
        {
            "value": "john.locke+work@example.com",
            "type": "work"
        }
    ],
    "website_addresses": [
        {
            "value": "johnlocke.example.com",
            "type": "personal"
        }
    ],
    "social_media_addresses": [
        {
            "value": "@johnlocke"
        },
        {
            "value": "linkedin.example.com/john.locke"
        }
    ],
    "recruiter": null,
    "coordinator": null,
    "tags": [
        "Orientation",
        "Walkabout"
    ],
    "applications": [
        {
            "id": 69201605,
            "candidate_id": 57683957,
            "prospect": false,
            "applied_at": "2017-09-28T13:27:54.873Z",
            "rejected_at": null,
            "last_activity_at": "2017-09-28T13:27:55.213Z",
            "source": null,
            "credited_to": null,
            "rejection_reason": null,
            "rejection_details": null,
            "jobs": [
                {
                    "id": 185289,
                    "name": "Product Specialist"
                }
            ],
            "status": "active",
            "current_stage": {
                "id": 1355395,
                "name": "Application Review"
            },
            "answers": [],
            "prospect_detail": {
                "prospect_pool": null,
                "prospect_stage": null,
                "prospect_owner": null
            }
        },
        {
            "id": 69201604,
            "candidate_id": 57683957,
            "prospect": false,
            "applied_at": "2017-09-28T13:27:54.812Z",
            "rejected_at": null,
            "last_activity_at": "2017-09-28T13:27:55.213Z",
            "source": null,
            "credited_to": null,
            "rejection_reason": null,
            "rejection_details": null,
            "jobs": [
                {
                    "id": 215725,
                    "name": "Operations Manger "
                }
            ],
            "status": "active",
            "current_stage": {
                "id": 1579673,
                "name": "Application Review"
            },
            "answers": [],
            "prospect_detail": {
                "prospect_pool": null,
                "prospect_stage": null,
                "prospect_owner": null
            }
        }
    ],
    "educations": [],
    "employments": [],
    "custom_fields": {
        "desired_salary": null,
        "work_remotely": null,
        "graduation_year": null
    },
    "keyed_custom_fields": {
        "desired_salary": null,
        "work_remotely": null,
        "graduation_year_1": null
    }
}
```

Create a new candidate.

### HTTP Request

`POST https://harvest.greenhouse.io/v1/candidates`

### Headers

Header | Description
--------- | -----------
On-Behalf-Of | ID of the user issuing this request. Required for auditing purposes.

### JSON Body Parameters

Parameter | Required | Type | Description
--------- | ----------- | ----------- | -----------
first_name | Yes | string | The candidate's first name
last_name | Yes | string | The candidate's last name
company | No | string | The candidate's company
title | No | string | The candidate's title
phone_numbers[] | No | phone_number | Array of phone numbers. Passing an empty array will clear all.
addresses[] | No | address | Array of addresses. Passing an empty array will clear all.
email_addresses[] | No | email_address | Array of email addresses. Passing an empty array will clear all.
website_addresses[] | No | website_address | Array of website addresses. Passing an empty array will clear all.
social_media_addresses[] | No | social_media_address | Array of social media addresses. Passing an empty array will clear all.
tags[] | No | string | Array of tags as strings. Passing an empty array will clear all.
custom_fields[] | No |  custom_field | Array of hashes containing new custom field values.  Passing an empty array does nothing.
recruiter | No | Object | An object representing the candidate's recruiter
recruiter[id] | No | Integer | The ID of the recruiter - either id or email must be present.
recruiter[email] | No | String | The email of the recruiter - either id or email must be present.
coordinator | No | Object | An object representing the candidate's coordinator
coordinator[id] | No | Integer | The ID of the coordinator - either id or email must be present.
coordinator[email] | No | String | The email of the coordinator - either id or email must be present.
custom_fields | No | Array | Array of custom field value objects - See "Custom Field Parameters" under [Edit candidate] (#patch-edit-candidate) for parameters.
activity_feed_notes | No | Array | An array of activity feed objects. See [Add Note] (#post-add-note) for parameters.
applications | Yes | Array | An array of application objects. At least one required. See [Add Application] (#post-add-candidate-application) for parameters.

<br>

[See noteworthy response attributes.] (#the-candidate-object)

## POST: Add Note

```shell
curl -X POST 'https://harvest.greenhouse.io/v1/candidates/{id}/activity_feed/notes'
-H "On-Behalf-Of: {greenhouse user ID}"
-H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

> The above command takes a JSON request, structured like this:

```
{
  "user_id": "158108",
  "body": "John Locke was moved into Recruiter Phone Screen for Accounting Manager on 03/27/2014 by Boone Carlyle",
  "visibility": "admin_only"
}
```

> The above command returns a JSON response, structured like this:

```json
{
  "id": 226809052,
  "created_at": "2015-07-17T16:29:31Z",
  "body": "John Locke was moved into Recruiter Phone Screen for Accounting Manager on 03/27/2014 by Boone Carlyle",
  "user": {
     "id": 214,
        "first_name": "Boone",
        "last_name": "Carlyle",
        "name": "Boone Carlyle",
        "employee_id": null
  },
  "private": false,
  "visiblity": "admin_only",
  "visibility": "admin_only"
}
```

Create a candidate note.

### HTTP Request

`POST https://harvest.greenhouse.io/v1/candidates/{id}/activity_feed/notes`

### Headers

Header | Description
--------- | -----------
On-Behalf-Of | ID of the user issuing this request. Required for auditing purposes.


### JSON Body Parameters

Parameter | Required | Type | Description
--------- | ----------- | ----------- | -----------
user_id | Yes | integer |   The ID of the user creating the note
body | Yes | string | Note body
visibility* | Yes | string | One of: `"admin_only"`, `"private"`, `"public"`

\* - Due to a legacy typo, the response includes the same value as `visiblity`. It is safe to ignore this value, but it is maintained for backward compatibility.


## POST: Add Prospect

```shell
curl -X POST 'https://harvest.greenhouse.io/v1/prospects'
-H "On-Behalf-Of: {greenhouse user ID}"
-H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

> The above command takes a JSON request, structured like this:

```json
{
  "first_name": "John",
  "last_name": "Locke",
  "company": "The Tustin Box Company",
  "title": "Man of Mystery",
  "is_private": false,
  "phone_numbers": [
    {
      "value": "555-1212",
      "type": "mobile"
    }
  ],
  "addresses": [
    {
      "value": "123 Fake St.",
      "type": "home"
    }
  ],
  "email_addresses": [
    {
      "value": "john.locke+work@example.com",
      "type": "work"
    },
    {
      "value": "john.locke@example.com",
      "type": "personal"
    }
  ],
  "website_addresses": [
    {
      "value": "johnlocke.example.com",
      "type": "personal"
    }
  ],
  "social_media_addresses": [
    {
      "value": "linkedin.example.com/john.locke"
    },
    {
      "value": "@johnlocke"
    }
  ],
  "tags": [
    "Walkabout",
    "Orientation"
  ],
  "application": {
    "job_ids": [123, 456, 789],
    "source_id": 1234,
    "referrer": {
      "type": "id",
      "value": 770
    },
    "custom_fields": [],
    "attachments": []
  }
}
```
> The above returns a JSON response, structured like this:

```json
{
  "id": 29843268,
  "first_name": "John",
  "last_name": "Locke",
  "company": "The Tustin Box Company",
  "title": "Man of Mystery",
  "is_private": false,
  "created_at": "2016-12-21T19:45:01.467Z",
  "updated_at": "2016-12-21T19:45:01.907Z",
  "last_activity": "2016-12-21T19:45:01.867Z",
  "photo_url": null,
  "attachments": [],
  "application_ids": [
    38776657
  ],
  "phone_numbers": [
    {
      "value": "555-1212",
      "type": "mobile"
    }
  ],
  "addresses": [
    {
      "value": "123 Fake St.",
      "type": "home"
    }
  ],
  "email_addresses": [
    {
      "value": "john.locke@example.com",
      "type": "personal"
    },
    {
      "value": "john.locke+work@example.com",
      "type": "work"
    }
  ],
  "website_addresses": [
    {
      "value": "johnlocke.example.com",
      "type": "personal"
    }
  ],
  "social_media_addresses": [
    {
      "value": "@johnlocke"
    },
    {
      "value": "linkedin.example.com/john.locke"
    }
  ],
  "recruiter": null,
  "coordinator": null,
  "tags": [
    "Orientation",
    "Walkabout"
  ],
  "applications": [
    {
      "id": 38776657,
      "candidate_id": 29843268,
      "prospect": true,
      "applied_at": "2016-12-21T19:45:01.757Z",
      "rejected_at": null,
      "last_activity_at": "2016-12-21T19:45:01.867Z",
      "source": null,
      "credited_to": null,
      "rejection_reason": null,
      "rejection_details": null,
      "jobs": [],
      "status": "active",
      "current_stage": null,
      "answers": [],
      "custom_fields": {
        "test": "A test value"
      },
      "keyed_custom_fields": {
         "test": {
            "name": "Test",
            "type": "long_text",
            "value": "A test value"
          }
        }
     }
  ],
  "educations": [],
  "custom_fields": {
    "current_salary": "$123,000",
    "desired_salary": "$150,000"
  },
  "keyed_custom_fields": {
    "current_salary": {
      "name": "Current salary",
      "type": "short_text",
      "value": "$123,000"
    },
    "desired_salary": {
      "name": "Desired salary",
      "type": "short_text",
      "value": "$150,000"
    }
  }
}
```

Create a new prospect. The difference between a prospect and a candidate is that a prospect can be on no jobs or many jobs. A prospect application cannot be added to a job stage. When a prospect is ready to be added to a job stage, they can be converted to a candidate in Greenhouse. Alternatively, you can add a candidate application to a prospect's profile by using the [Add Candidate Application] (#post-add-candidate-application) endpoint. The organization must be able to create prospects to set this field.

### HTTP Request

`POST https://harvest.greenhouse.io/v1/prospects`

### Headers

Header | Description
--------- | -----------
On-Behalf-Of | ID of the user issuing this request. Required for auditing purposes.

### JSON Body Parameters

Parameter | Required | Type | Description
--------- | ----------- | ----------- | -----------
first_name | Yes | string | The prospect's first name
last_name | Yes | string | The prospect's last name
company | No | string | The prospect's company
title | No | string | The prospect's title
phone_numbers[] | No | phone_number | Array of phone numbers. Passing an empty array will clear all.
addresses[] | No | address | Array of addresses. Passing an empty array will clear all.
email_addresses[] | No | email_address | Array of email addresses. Passing an empty array will clear all.
website_addresses[] | No | website_address | Array of website addresses. Passing an empty array will clear all.
social_media_addresses[] | No | social_media_address | Array of social media addresses. Passing an empty array will clear all.
tags[] | No | string | Array of tags as strings. Passing an empty array will clear all.
custom_fields[] | No |  custom_field | Array of hashes containing new custom field values.  Passing an empty array does nothing.
recruiter | No | Object | An object representing the prospect's recruiter
recruiter[id] | No | Integer | The ID of the recruiter - either id or email must be present.
recruiter[email] | No | String | The email of the recruiter - either id or email must be present.
coordinator | No | Object | An object representing the prospect's coordinator
coordinator[id] | No | Integer | The ID of the coordinator - either id or email must be present.
coordinator[email] | No | String | The email of the coordinator - either id or email must be present.
custom_fields | No | Array | Array of custom field value objects - See "Custom Field Parameters" under [Edit candidate] (#patch-edit-candidate) for parameters.
activity_feed_notes | No | Array | An array of activity feed objects. See [Add Note] (#post-add-note) for parameters.
application | No | Hash | As opposed to candidate, a prospect is a single application object that contains multiple job ids.  A prospect in Greenhouse can be attached to zero or many jobs.  If the request does not contain an application object, the person will be created as a jobless prospect.  The source_id, referrer, custom_fields, and attachments parameters in this object match the format of the [Add Application] (#post-add-application) endpoint.
application[job_ids] | No | Array | This element is unique to the prospects endpoint. This contains an array of job ids to which the prospect will be assigned.  Note that even if the application object is included, this may still be blank or omitted and the request will create a jobless prospect. A normal use case for this would be creating a jobless prospect but still wanting to attach their resume or identify their source.

<br>

[See noteworthy response attributes.] (#the-candidate-object)

## PUT: Anonymize Candidate

```shell
curl -X PUT 'https://harvest.greenhouse.io/v1/candidates/{id}/anonymize?fields={field_names}'
-H "On-Behalf-Of: {greenhouse user ID}"
-H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

> The above command returns a JSON response, structured like this:

```json
{
    "id": 53883394,
    "first_name": "Anonymized",
    "last_name": "53883394",
    "company": null,
    "title": null,
    "created_at": "2017-08-15T03:31:46.591Z",
    "updated_at": "2017-09-28T13:36:04.725Z",
    "last_activity": "2017-09-28T13:31:37.929Z",
    "is_private": false,
    "photo_url": "https://prod-heroku.s3.amazonaws.com/people/photos/053/883/394/original/corgi.jpg?AWSAccessKeyId=AKIAIK36UTOKQ5F2YNMQ&Expires=1509197765&Signature=pr0qNjZvTvLCV2td9hebhEa7P3Y%3D",
    "attachments": [
        {
            "filename": "John_Locke_Offer_Packet_09_28_2017.pdf",
            "url": "https://prod-heroku.s3.amazonaws.com/person_attachments/data/077/815/020/original/John_Locke_Offer_Packet_09_28_2017.pdf?AWSAccessKeyId=AKIAIK36UTOKQ5F2YNMQ&Expires=1509197765&Signature=rV%2FW668FnnG4EFGLJbHrnY%2B7Mvs%3D",
            "type": "offer_packet"
        }
    ],
    "application_ids": [
        69201279
    ],
    "phone_numbers": [],
    "addresses": [
        {
            "value": "123 City Street\nNew York, Ny 10001",
            "type": "home"
        }
    ],
    "email_addresses": [],
    "website_addresses": [
        {
            "value": "mysite.com",
            "type": "personal"
        }
    ],
    "social_media_addresses": [],
    "recruiter": {
        "id": 92120,
        "first_name": "Greenhouse",
        "last_name": "Admin",
        "name": "Greenhouse Admin",
        "employee_id": null
    },
    "coordinator": null,
    "tags": [
        "Python",
        "Ruby"
    ],
    "applications": [
        {
            "id": 69201279,
            "candidate_id": 53883394,
            "prospect": false,
            "applied_at": "2017-09-28T13:21:22.749Z",
            "rejected_at": null,
            "last_activity_at": "2017-09-28T13:31:37.929Z",
            "source": {
                "id": 7,
                "public_name": "Indeed"
            },
            "credited_to": {
                "id": 566993,
                "first_name": "Jane",
                "last_name": "Smith",
                "name": "Jane Smith",
                "employee_id": null
            },
            "rejection_reason": null,
            "rejection_details": null,
            "jobs": [
                {
                    "id": 213967,
                    "name": "Head of Product"
                }
            ],
            "status": "active",
            "current_stage": {
                "id": 1567309,
                "name": "Application Review"
            },
            "answers": [],
            "prospect_detail": {
                "prospect_pool": null,
                "prospect_stage": null,
                "prospect_owner": null
            }
        }
    ],
    "educations": [
        {
            "id": 561227,
            "school_name": "University of Michigan - Ann Arbor",
            "degree": "Bachelor's Degree",
            "discipline": "Computer Science"
        }
    ],
    "employments": [],
    "custom_fields": {
        "desired_salary": null,
        "work_remotely": null,
        "graduation_year": null
    },
    "keyed_custom_fields": {
        "desired_salary": null,
        "work_remotely": null,
        "graduation_year_1": null
    }
}
```

Anonymize the data associated with a candidate.

### HTTP Request

`PUT https://harvest.greenhouse.io/v1/candidates/{id}/anonymize?fields={field_names}`

### Headers

Header | Description
--------- | -----------
On-Behalf-Of | ID of the user issuing this request. Required for auditing purposes.


### Querystring Parameters

Parameter | Required | Type | Description
--------- | ----------- | ----------- | -----------
fields | Yes | comma-delimited string | The set of field names that should be anonymized on the candidate from the following list: full_name, current_company, current_title, tags, phone_numbers, emails, social_media_links, websites, addresses, location, custom_candidate_fields, source, recruiter, coordinator, attachments, application_questions, referral_questions, notes, rejection_notes, email_addresses, activity_items, innotes, inmails, rejection_reason, scorecards_and_interviews, offers, credited_to, headline, all_offer_versions, and follow_up_reminders.

## PUT: Merge Candidates

```shell
curl -X PUT 'https://harvest.greenhouse.io/v1/candidates/merge'
-d '{ "primary_candidate_id": 73821, "duplicate_candidate_id": 839283 }'
-H "Content-Type: application/json"
-H "On-Behalf-Of: {greenhouse user ID}"
-H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

> The above command returns a JSON response, structured like this:

```json
{
    "id": 55961742,
    "first_name": "Justin",
    "last_name": "Locke",
    "company": "The Tustin Box Company",
    "title": "Man of Mystery",
    "created_at": "2017-09-07T22:54:06.629Z",
    "updated_at": "2017-09-28T13:41:43.655Z",
    "last_activity": "2017-09-28T13:41:43.631Z",
    "is_private": false,
    "photo_url": null,
    "attachments": [
        {
            "filename": "Justin Locke resume.pdf",
            "url": "https://prod-heroku.s3.amazonaws.com/person_attachments/data/048/999/636/original/Byron%20Sonnett%20resume.pdf?AWSAccessKeyId=AKIAIK36UTOKQ5F2YNMQ&Expires=1509198103&Signature=Zc%2BenNvJyxH4FatQBRFz8248GUM%3D",
            "type": "resume"
        },
         {
            "filename": "Justin Locke cover leter.pdf",
            "url": "https://prod-heroku.s3.amazonaws.com/person_attachments/data/048/999/636/original/Byron%20Sonnett%20resume.pdf?AWSAccessKeyId=AKIAIK36UTOKQ5F2YNMQ&Expires=1509198103&Signature=Zc%2BenNvJyxH4FatQBRFz8248GUM%3D",
            "type": "cover_letter"
        }
    ],
    "application_ids": [
        67398864
    ],
    "phone_numbers": [
        {
            "value": "222-555-4608",
            "type": "home"
        }
    ],
    "addresses": [],
    "email_addresses": [
        {
            "value": "justin.locke@example.com",
            "type": "personal"
        }
    ],
    "website_addresses": [
        {
            "value": "example.com",
            "type": "other"
        }
    ],
    "social_media_addresses": [],
    "recruiter": null,
    "coordinator": null,
    "tags": [
        "Comp Sci"
    ],
    "applications": [
        {
            "id": 67398864,
            "candidate_id": 55961742,
            "prospect": false,
            "applied_at": "2017-09-07T23:00:25.746Z",
            "rejected_at": null,
            "last_activity_at": "2017-09-28T13:41:43.631Z",
            "source": {
                "id": 7,
                "public_name": "Indeed"
            },
            "credited_to": {
                "id": 92121,
                "first_name": "Jane",
                "last_name": "Smith",
                "name": "Jane Smith",
                "employee_id": "456"
            },
            "rejection_reason": null,
            "rejection_details": null,
            "jobs": [
                {
                    "id": 213967,
                    "name": "Product Manager"
                }
            ],
            "status": "active",
            "current_stage": {
                "id": 1567309,
                "name": "Application Review"
            },
            "answers": [],
            "prospect_detail": {
                "prospect_pool": null,
                "prospect_stage": null,
                "prospect_owner": null
            }
        }
    ],
    "educations": [
        {
            "id": 561227,
            "school_name": "University of Michigan - Ann Arbor",
            "degree": "Bachelor's Degree",
            "discipline": "Computer Science"
        }
    ],
    "employments": [],
      "custom_fields": {
        "desired_salary": "120K",
        "work_remotely": true,
        "graduation_year": "2018"
    },
    "keyed_custom_fields": {
        "desired_salary": {
            "name": "Desired Salary",
            "type": "short_text",
            "value": "120K"
        },
        "work_remotely": {
            "name": "Work Remotely",
            "type": "boolean",
            "value": true
        },
        "graduation_year_1": {
            "name": "Graduation Year",
            "type": "single_select",
            "value": "2018"
        }
    }
}
```

Merge two candidates into one.

### HTTP Request

`PUT https://harvest.greenhouse.io/v1/candidates/merge`

### Headers

Header | Description
--------- | -----------
On-Behalf-Of | ID of the user issuing this request. Required for auditing purposes.

### JSON Body Parameters

Parameter | Required | Type | Description
--------- | ----------- | ----------- | -----------
primary\_candidate\_id | Yes | integer | The id of the first candidate that will be merged. This candidate will also be the result of the merge.
duplicate\_candidate\_id | Yes | integer | The id of the second candidate that will be merged. ***This candidate will cease to exist after the merge is complete.***
