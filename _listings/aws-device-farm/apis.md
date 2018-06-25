---
name: AWS Device Farm
x-slug: aws-device-farm
description: AWS Device Farm is an app testing service that lets you test and interact
  with your Android, iOS, and web apps on many devices at once, or reproduce issues
  on a device in real time. View video, screenshots, logs, and performance data to
  pinpoint and fix issues before shipping your app.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Mobile-Services_AWSDeviceFarm.png
x-kinRank: "10"
x-alexaRank: "0"
tags: Sessions
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/aws-device-farm/apis.md
specificationVersion: "0.14"
apis:
- name: AWS Device Farm API Create Remote Access Session
  x-api-slug: aws-device-farm-api
  description: Specifies and starts a remote access session.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Mobile-Services_AWSDeviceFarm.png
  humanURL: https://aws.amazon.com/device-farm/
  baseURL: ://///?Action=CreateRemoteAccessSession
  tags: Remote Access Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/aws-device-farm/actioncreateremoteaccesssession-get-openapi.md
- name: AWS Device Farm API Delete Remote Access Session
  x-api-slug: aws-device-farm-api
  description: Deletes a completed remote access session and its results.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Mobile-Services_AWSDeviceFarm.png
  humanURL: https://aws.amazon.com/device-farm/
  baseURL: ://///?Action=DeleteRemoteAccessSession
  tags: Remote Access Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/aws-device-farm/actiondeleteremoteaccesssession-get-openapi.md
- name: AWS Device Farm API Get Remote Access Session
  x-api-slug: aws-device-farm-api
  description: Returns a link to a currently running remote access session.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Mobile-Services_AWSDeviceFarm.png
  humanURL: https://aws.amazon.com/device-farm/
  baseURL: ://///?Action=GetRemoteAccessSession
  tags: Remote Access Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/aws-device-farm/actiongetremoteaccesssession-get-openapi.md
- name: AWS Device Farm API Install To Remote Access Session
  x-api-slug: aws-device-farm-api
  description: Installs an application to the device in a remote access session.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Mobile-Services_AWSDeviceFarm.png
  humanURL: https://aws.amazon.com/device-farm/
  baseURL: ://///?Action=InstallToRemoteAccessSession
  tags: Remote Access Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/aws-device-farm/actioninstalltoremoteaccesssession-get-openapi.md
- name: AWS Device Farm API List Remote Access Sessions
  x-api-slug: aws-device-farm-api
  description: Returns a list of all currently running remote access sessions.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Mobile-Services_AWSDeviceFarm.png
  humanURL: https://aws.amazon.com/device-farm/
  baseURL: ://///?Action=ListRemoteAccessSessions
  tags: Remote Access Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/aws-device-farm/actionlistremoteaccesssessions-get-openapi.md
- name: AWS Device Farm API Stop Remote Access Session
  x-api-slug: aws-device-farm-api
  description: Ends a specified remote access session.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Mobile-Services_AWSDeviceFarm.png
  humanURL: https://aws.amazon.com/device-farm/
  baseURL: ://///?Action=StopRemoteAccessSession
  tags: Remote Access Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/aws-device-farm/actionstopremoteaccesssession-get-openapi.md
- name: AWS Device Farm API
  x-api-slug: aws-device-farm-api
  description: AWS Device Farm is an app testing service that lets you test and interact
    with your Android, iOS, and web apps on many devices at once, or reproduce issues
    on a device in real time. View video, screenshots, logs, and performance data
    to pinpoint and fix issues before shipping your app.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Mobile-Services_AWSDeviceFarm.png
  humanURL: https://aws.amazon.com/device-farm/
  baseURL: :///
  tags: Sessions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/aws-device-farm/openapi.md
x-common:
- type: x-blog
  url: https://aws.amazon.com/blogs/mobile/tag/aws-device-farm/
- type: x-concepts
  url: https://docs.aws.amazon.com/devicefarm/latest/developerguide/concepts.html
- type: x-documentation
  url: https://docs.aws.amazon.com/devicefarm/latest/developerguide/api-ref.html
- type: x-documentation
  url: https://docs.aws.amazon.com/devicefarm/latest/developerguide/cli-ref.html
- type: x-limits
  url: https://docs.aws.amazon.com/devicefarm/latest/developerguide/limits.html
- type: x-logging
  url: https://docs.aws.amazon.com/devicefarm/latest/developerguide/cloudtrail.html
- type: x-plugins
  url: https://github.com/awslabs?q=aws-device-farm
- type: x-faq
  url: https://aws.amazon.com/device-farm/faq
- type: x-pricing
  url: https://aws.amazon.com/device-farm/pricing
- type: x-website
  url: https://aws.amazon.com/device-farm/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---