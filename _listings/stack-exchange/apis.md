---
name: Stack Exchange
x-slug: stack-exchange
description: After someone asks a question, members of the community propose answers.
  Others vote on those answers. Very quickly, the answers with the most votes rise
  to the top. You don???t have to read through a lot of discussion to find the best
  answer.    Like to...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
x-kinRank: "8"
x-alexaRank: "126"
tags: Posts
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/apis.md
specificationVersion: "0.14"
apis:
- name: Stack Exchange Get Posts
  x-api-slug: stack-exchange
  description: "Fetches all posts (questions and answers) on the site.\n \nIn many
    ways this method is the union of /questions and /answers, returning both sets
    of data albeit only the common fields.\n \nMost applications should use the question
    or answer specific methods, but /posts is available for those rare cases where
    any activity is of intereset. Examples of such queries would be: \"all posts on
    Jan. 1st 2011\" or \"top 10 posts by score of all time\".\n \nThe sorts accepted
    by this method operate on the follow fields of the post object:\n - activity -
    last_activity_date\n - creation - creation_date\n - votes - score\n  activity
    is the default sort.\n \n It is possible to create moderately complex queries
    using sort, min, max, fromdate, and todate.\n \nThis method returns a list of
    posts."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//posts
  tags: Posts
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/posts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/posts-get-openapi.md
- name: Stack Exchange Get Post
  x-api-slug: stack-exchange
  description: "Fetches a set of posts by ids.\n \nThis method is meant for grabbing
    an object when unsure whether an id identifies a question or an answer. This is
    most common with user entered data.\n \n{ids} can contain up to 100 semicolon
    delimited ids, to find ids programatically look for post_id, answer_id, or question_id
    on post, answer, and question objects respectively.\n \nThe sorts accepted by
    this method operate on the follow fields of the post object:\n - activity - last_activity_date\n
    - creation - creation_date\n - votes - score\n  activity is the default sort.\n
    \n It is possible to create moderately complex queries using sort, min, max, fromdate,
    and todate.\n \nThis method returns a list of posts."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//posts/{ids}
  tags: Posts
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/postsids-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/postsids-get-openapi.md
- name: Stack Exchange Get Post Comments
  x-api-slug: stack-exchange
  description: "Gets the comments on the posts identified in ids, regardless of the
    type of the posts.\n \nThis method is meant for cases when you are unsure of the
    type of the post id provided. Generally, this would be due to obtaining the post
    id directly from a user.\n \n{ids} can contain up to 100 semicolon delimited ids,
    to find ids programatically look for post_id, answer_id, or question_id on post,
    answer, and question objects respectively.\n \nThe sorts accepted by this method
    operate on the follow fields of the comment object:\n - creation - creation_date\n
    - votes - score\n  creation is the default sort.\n \n It is possible to create
    moderately complex queries using sort, min, max, fromdate, and todate.\n \nThis
    method returns a list of comments."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//posts/{ids}/comments
  tags: Posts,Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/postsidscomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/postsidscomments-get-openapi.md
- name: Stack Exchange Get Post Revisions
  x-api-slug: stack-exchange
  description: "Returns edit revisions for the posts identified in ids.\n \n{ids}
    can contain up to 100 semicolon delimited ids, to find ids programatically look
    for post_id, answer_id, or question_id on post, answer, and question objects respectively.\n
    \nThis method returns a list of revisions."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//posts/{ids}/revisions
  tags: Posts,Revisions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/postsidsrevisions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/postsidsrevisions-get-openapi.md
- name: Stack Exchange Get Posts Suggested Edits
  x-api-slug: stack-exchange
  description: "Returns suggsted edits on the posts identified in ids.\n \n - creation
    - creation_date\n - approval - approval_date\n - rejection - rejection_date\n
    \ creation is the default sort.\n \n {ids} can contain up to 100 semicolon delimited
    ids, to find ids programatically look for post_id, answer_id, or question_id on
    post, answer, and question objects respectively.\n \nThis method returns a list
    of suggested-edits."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//posts/{ids}/suggested-edits
  tags: Posts,Suggested Edits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/postsidssuggestededits-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/postsidssuggestededits-get-openapi.md
- name: Stack Exchange Add Comment Post
  x-api-slug: stack-exchange
  description: "Create a new comment.\n \nUse an access_token with write_access to
    create a new comment on a post.\n \nThis method returns the created comment."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2//posts/{id}/comments/add
  tags: Posts,Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/postsidcommentsadd-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/postsidcommentsadd-post-openapi.md
- name: Stack Exchange
  x-api-slug: stack-exchange
  description: After someone asks a question, members of the community propose answers.
    Others vote on those answers. Very quickly, the answers with the most votes rise
    to the top. You don???t have to read through a lot of discussion to find the best
    answer.    Like to...
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/253-stack-exchange.jpg
  humanURL: http://stackexchange.com
  baseURL: https://api.stackexchange.com//2.2
  tags: Posts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/posts/master/_listings/stack-exchange/openapi.md
x-common:
- type: x-authentication
  url: https://api.stackexchange.com/docs/authentication
- type: x-base
  url: https://api.stackexchange.com/
- type: x-blog
  url: http://stackexchange.com/blogs
- type: x-blog-rss
  url: http://blog.stackoverflow.com/feed/
- type: x-crunchbase
  url: http://www.crunchbase.com/company/stack-exchange
- type: x-crunchbase
  url: https://crunchbase.com/organization/stack-exchange
- type: x-developer
  url: http://api.stackexchange.com/
- type: x-email
  url: legal@stackexchange.com
- type: x-email
  url: team@stackexchange.com
- type: x-email
  url: team+api@stackexchange.com
- type: x-error-codes
  url: https://api.stackexchange.com/docs/error-handling
- type: x-github
  url: https://github.com/StackExchange
- type: x-javascript-sdk
  url: https://api.stackexchange.com/docs/js-lib
- type: x-privacy
  url: https://stackexchange.com/legal/privacy-policy
- type: x-rate-limits
  url: https://api.stackexchange.com/docs/throttle
- type: x-selfservice-registration
  url: https://stackapps.com/users/login?returnurl=/apps/oauth/register
- type: x-support
  url: https://stackexchange.com/about/contact
- type: x-terms-of-service
  url: http://stackexchange.com/legal/api-terms-of-use
- type: x-twitter
  url: https://twitter.com/StackExchange
- type: x-website
  url: http://stackexchange.com
- type: x-website
  url: https://stackexchange.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---