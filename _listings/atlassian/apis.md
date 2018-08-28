---
name: Atlassian
x-slug: atlassian
description: Millions of users globally rely on Atlassian products every day for improving
  software development, project management, collaboration, and code quality.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
x-kinRank: "8"
x-alexaRank: "1656"
tags: Sessions
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/apis.md
specificationVersion: "0.14"
apis:
- name: Jira Cloud REST API - Get session
  x-api-slug: auth1session-get
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Returns information about the session. If there is no session, the calling users
    details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-openapi.md
- name: Jira Cloud REST API - Create session
  x-api-slug: auth1session-post
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Creates a session for the user in Jira. Use the session to access Jira's remote
    APIs and web UI by passing the `cloud.session.token` HTTP cookie. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=). The response contains
    the `Set-Cookie` HTTP headers that **must** be honored by the caller. If you're
    using a cookie-aware HTTP client it will handle the `Set-Cookie` headers automatically.
    Setting up the `cloud.session.token` cookie is important because setting the token
    from the response body alone may not be sufficient for the authentication to work.
    **Note:** Use of this resource isn't recommended, use HTTP BASIC authentication
    with the REST API instead. However, this resource may be used to mimic the behavior
    of Jira's log-in page so that you can, for example, display log-in errors to the
    user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-openapi.md
- name: Jira Cloud REST API - Delete session
  x-api-slug: auth1session-delete
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Destroys the user's Jira session. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-openapi.md
- name: Jira Cloud REST API - Get session
  x-api-slug: auth1session-get
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Returns information about the session. If there is no session, the calling users
    details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-openapi.md
- name: Jira Cloud REST API - Create session
  x-api-slug: auth1session-post
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Creates a session for the user in Jira. Use the session to access Jira's remote
    APIs and web UI by passing the `cloud.session.token` HTTP cookie. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=). The response contains
    the `Set-Cookie` HTTP headers that **must** be honored by the caller. If you're
    using a cookie-aware HTTP client it will handle the `Set-Cookie` headers automatically.
    Setting up the `cloud.session.token` cookie is important because setting the token
    from the response body alone may not be sufficient for the authentication to work.
    **Note:** Use of this resource isn't recommended, use HTTP BASIC authentication
    with the REST API instead. However, this resource may be used to mimic the behavior
    of Jira's log-in page so that you can, for example, display log-in errors to the
    user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-openapi.md
- name: Jira Cloud REST API - Delete session
  x-api-slug: auth1session-delete
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Destroys the user's Jira session. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-openapi.md
- name: Jira Cloud REST API - Delete session
  x-api-slug: auth1session-delete
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Destroys the user's Jira session. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-openapi.md
- name: Jira Cloud REST API - Delete session
  x-api-slug: auth1session-delete
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Destroys the user's Jira session. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-openapi.md
- name: Jira Cloud REST API - Delete session
  x-api-slug: auth1session-delete
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Destroys the user's Jira session. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-openapi.md
- name: Jira Cloud REST API - Delete session
  x-api-slug: auth1session-delete
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Destroys the user's Jira session. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-openapi.md
- name: Jira Cloud REST API - Delete session
  x-api-slug: auth1session-delete
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Destroys the user's Jira session. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** None.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-delete-openapi.md
- name: Jira Cloud REST API - Create session
  x-api-slug: auth1session-post
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Creates a session for the user in Jira. Use the session to access Jira's remote
    APIs and web UI by passing the `cloud.session.token` HTTP cookie. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=). The response contains
    the `Set-Cookie` HTTP headers that **must** be honored by the caller. If you're
    using a cookie-aware HTTP client it will handle the `Set-Cookie` headers automatically.
    Setting up the `cloud.session.token` cookie is important because setting the token
    from the response body alone may not be sufficient for the authentication to work.
    **Note:** Use of this resource isn't recommended, use HTTP BASIC authentication
    with the REST API instead. However, this resource may be used to mimic the behavior
    of Jira's log-in page so that you can, for example, display log-in errors to the
    user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-openapi.md
- name: Jira Cloud REST API - Create session
  x-api-slug: auth1session-post
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Creates a session for the user in Jira. Use the session to access Jira's remote
    APIs and web UI by passing the `cloud.session.token` HTTP cookie. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=). The response contains
    the `Set-Cookie` HTTP headers that **must** be honored by the caller. If you're
    using a cookie-aware HTTP client it will handle the `Set-Cookie` headers automatically.
    Setting up the `cloud.session.token` cookie is important because setting the token
    from the response body alone may not be sufficient for the authentication to work.
    **Note:** Use of this resource isn't recommended, use HTTP BASIC authentication
    with the REST API instead. However, this resource may be used to mimic the behavior
    of Jira's log-in page so that you can, for example, display log-in errors to the
    user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-openapi.md
- name: Jira Cloud REST API - Create session
  x-api-slug: auth1session-post
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Creates a session for the user in Jira. Use the session to access Jira's remote
    APIs and web UI by passing the `cloud.session.token` HTTP cookie. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=). The response contains
    the `Set-Cookie` HTTP headers that **must** be honored by the caller. If you're
    using a cookie-aware HTTP client it will handle the `Set-Cookie` headers automatically.
    Setting up the `cloud.session.token` cookie is important because setting the token
    from the response body alone may not be sufficient for the authentication to work.
    **Note:** Use of this resource isn't recommended, use HTTP BASIC authentication
    with the REST API instead. However, this resource may be used to mimic the behavior
    of Jira's log-in page so that you can, for example, display log-in errors to the
    user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-openapi.md
- name: Jira Cloud REST API - Create session
  x-api-slug: auth1session-post
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Creates a session for the user in Jira. Use the session to access Jira's remote
    APIs and web UI by passing the `cloud.session.token` HTTP cookie. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=). The response contains
    the `Set-Cookie` HTTP headers that **must** be honored by the caller. If you're
    using a cookie-aware HTTP client it will handle the `Set-Cookie` headers automatically.
    Setting up the `cloud.session.token` cookie is important because setting the token
    from the response body alone may not be sufficient for the authentication to work.
    **Note:** Use of this resource isn't recommended, use HTTP BASIC authentication
    with the REST API instead. However, this resource may be used to mimic the behavior
    of Jira's log-in page so that you can, for example, display log-in errors to the
    user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-openapi.md
- name: Jira Cloud REST API - Create session
  x-api-slug: auth1session-post
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Creates a session for the user in Jira. Use the session to access Jira's remote
    APIs and web UI by passing the `cloud.session.token` HTTP cookie. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** _Administer Jira_ [global permission](href=). The response contains
    the `Set-Cookie` HTTP headers that **must** be honored by the caller. If you're
    using a cookie-aware HTTP client it will handle the `Set-Cookie` headers automatically.
    Setting up the `cloud.session.token` cookie is important because setting the token
    from the response body alone may not be sufficient for the authentication to work.
    **Note:** Use of this resource isn't recommended, use HTTP BASIC authentication
    with the REST API instead. However, this resource may be used to mimic the behavior
    of Jira's log-in page so that you can, for example, display log-in errors to the
    user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-post-openapi.md
- name: Jira Cloud REST API - Get session
  x-api-slug: auth1session-get
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Returns information about the session. If there is no session, the calling users
    details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-openapi.md
- name: Jira Cloud REST API - Get session
  x-api-slug: auth1session-get
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Returns information about the session. If there is no session, the calling users
    details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-openapi.md
- name: Jira Cloud REST API - Get session
  x-api-slug: auth1session-get
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Returns information about the session. If there is no session, the calling users
    details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-openapi.md
- name: Jira Cloud REST API - Get session
  x-api-slug: auth1session-get
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Returns information about the session. If there is no session, the calling users
    details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-openapi.md
- name: Jira Cloud REST API - Get session
  x-api-slug: auth1session-get
  description: This resource is deprecated and will be removed December 1, 2018. For
    more information, see [Deprecation notice - Basic authentication with passwords
    and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
    Returns information about the session. If there is no session, the calling users
    details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
    required:** Permission to access Jira.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/691-atlassian.jpg
  humanURL: http://atlassian.com/
  baseURL: https:////
  tags: Coding, Programming, Wiki, Issues, Code Issues, Stack Network, SaaS, Technology,
    Enterprise, API Provider, API Service Provider, Profiles, Relative Data, Service
    API
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/sessions/master/_listings/atlassian/auth1session-get-openapi.md
x-common:
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/platform/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/confluence/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/software/swagger.v3.json
- type: x-openapi
  url: https://developer.atlassian.com/cloud/jira/service-desk/swagger.v3.json
- type: x-website
  url: http://atlassian.com/
- type: x-website
  url: http://www.atlassian.com
- type: x-api-gallery
  url: http://att.dev.program.api.gallery.streamdata.io
- type: x-api-stack
  url: http://atlassian.stack.network
- type: x-blog
  url: http://blogs.atlassian.com/
- type: x-crunchbase
  url: https://crunchbase.com/organization/atlassian
- type: x-crunchbase
  url: http://www.crunchbase.com/company/atlassian
- type: x-email
  url: copyright@atlassian.com
- type: x-email
  url: trademarks@atlassian.com
- type: x-email
  url: sales@atlassian.com
- type: x-email
  url: ar_enterprise@atlassian.com
- type: x-email
  url: privacy@atlassian.com
- type: x-email
  url: eudatarep@atlassian.com
- type: x-email
  url: experts@atlassian.com
- type: x-email
  url: remittance@atlassian.com
- type: x-email
  url: ap@atlassian.com
- type: x-email
  url: procurement@atlassian.com
- type: x-github
  url: https://github.com/atlassian
- type: x-privacy-policy
  url: https://www.atlassian.com/legal/privacy-policy?_ga=2.188884514.868776184.1519225620-845241124.1519225620
- type: x-twitter
  url: https://twitter.com/atlassian
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---