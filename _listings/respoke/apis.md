---
name: Respoke
x-slug: respoke
description: Respoke makes it incredibly easy to add real-time communications capabilities
  to the things you build. Integrate text chat, audio calling, video collaboration,
  screen sharing, and peer-to-peer data with just a few lines of JavaScript.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/respoke-web-communications-300x101.jpg
x-kinRank: "9"
x-alexaRank: "0"
tags: Sessions
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/respoke/apis.md
specificationVersion: "0.14"
apis:
- name: Respoke REST API Admin Sessions
  x-api-slug: respoke-rest-api
  description: Log in with the account username and password. Get an Admin-Token.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/respoke-web-communications-300x101.jpg
  humanURL: https://www.respoke.io
  baseURL: https://api.respoke.io/v1//admin-sessions/
  tags: Admin,Sessions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/respoke/adminsessions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/respoke/adminsessions-post-openapi.md
- name: Respoke REST API Permissions
  x-api-slug: respoke-rest-api
  description: Full API permissions are obtained by POSTing your username and password
    to [base]/adminsessions.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/respoke-web-communications-300x101.jpg
  humanURL: https://www.respoke.io
  baseURL: https://api.respoke.io/v1//adminsessions/
  tags: Adminsessions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/respoke/adminsessions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/respoke/adminsessions-post-openapi.md
- name: Respoke REST API App Auth Sessions
  x-api-slug: respoke-rest-api
  description: Your users authenticate to Respoke using an App-Token obtained when
    they POST your tokenId to [base]/appauthsessions.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/respoke-web-communications-300x101.jpg
  humanURL: https://www.respoke.io
  baseURL: https://api.respoke.io/v1//appauthsessions/
  tags: Appauthsessions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/respoke/appauthsessions-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/respoke/appauthsessions-post-openapi.md
- name: Respoke REST API
  x-api-slug: respoke-rest-api
  description: Respoke makes it incredibly easy to add real-time communications capabilities
    to the things you build. Integrate text chat, audio calling, video collaboration,
    screen sharing, and peer-to-peer data with just a few lines of JavaScript.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/respoke-web-communications-300x101.jpg
  humanURL: https://www.respoke.io
  baseURL: https://api.respoke.io/v1/
  tags: Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/respoke/openapi.md
x-common:
- type: x-account-management
  url: https://portal.respoke.io/#/account?section=Profile
- type: x-application-management
  url: https://portal.respoke.io/#/apps
- type: x-authentication
  url: https://docs.respoke.io/tutorials/brokered-auth.html
- type: x-billing-management
  url: https://portal.respoke.io/#/account?section=Payments
- type: x-blog
  url: http://blog.respoke.io/
- type: x-blog-rss
  url: http://blog.respoke.io/rss
- type: x-change-log
  url: https://docs.respoke.io/reference/changelog.html
- type: x-developer
  url: https://portal.respoke.io
- type: x-documentation
  url: https://docs.respoke.io/
- type: x-email
  url: info@respoke.io
- type: x-facebook
  url: https://www.facebook.com/respokeIO
- type: x-forum
  url: http://community.respoke.io/
- type: x-github
  url: https://github.com/respoke
- type: x-google-plus
  url: https://plus.google.com/+RespokeIo
- type: x-javascript-library
  url: https://docs.respoke.io/js-library/respoke.html
- type: x-node-js-library
  url: http://respoke.github.io/node-respoke-admin
- type: x-pricing
  url: https://www.respoke.io/#pricing
- type: x-selfservice-registration
  url: https://www.respoke.io/#sign-up-form
- type: x-starter-apps
  url: https://docs.respoke.io/tutorials/example-apps.html
- type: x-terms-of-service
  url: https://www.respoke.io/files/respoke-tos-20141007.pdf
- type: x-twitter
  url: https://twitter.com/respoke
- type: x-website
  url: https://www.respoke.io
- type: x-website
  url: http://respoke.io
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---