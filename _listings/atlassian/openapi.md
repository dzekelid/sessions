swagger: "2.0"
x-collection-name: Atlassian
x-complete: 1
info:
  title: Stride API
  description: this-service-provides-public-api-for-the-stride-
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /auth/1/session:
    get:
      summary: Get session
      description: This resource is deprecated and will be removed December 1, 2018.
        For more information, see [Deprecation notice - Basic authentication with
        passwords and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
        Returns information about the session. If there is no session, the calling
        users details are returned. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** Permission to access Jira.
      operationId: com.atlassian.jira.rest.auth.Login.getCurrentUserLoginInformation_get
      x-api-path-slug: auth1session-get
      responses:
        200:
          description: OK
      tags:
      - Session
    post:
      summary: Create session
      description: This resource is deprecated and will be removed December 1, 2018.
        For more information, see [Deprecation notice - Basic authentication with
        passwords and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
        Creates a session for the user in Jira. Use the session to access Jira's remote
        APIs and web UI by passing the `cloud.session.token` HTTP cookie. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** _Administer Jira_ [global permission](href=). The response contains
        the `Set-Cookie` HTTP headers that **must** be honored by the caller. If you're
        using a cookie-aware HTTP client it will handle the `Set-Cookie` headers automatically.
        Setting up the `cloud.session.token` cookie is important because setting the
        token from the response body alone may not be sufficient for the authentication
        to work. **Note:** Use of this resource isn't recommended, use HTTP BASIC
        authentication with the REST API instead. However, this resource may be used
        to mimic the behavior of Jira's log-in page so that you can, for example,
        display log-in errors to the user.
      operationId: com.atlassian.jira.rest.auth.Login.logIn_post
      x-api-path-slug: auth1session-post
      responses:
        200:
          description: OK
      tags:
      - Session
    delete:
      summary: Delete session
      description: This resource is deprecated and will be removed December 1, 2018.
        For more information, see [Deprecation notice - Basic authentication with
        passwords and cookie-based authentication](https://developer.atlassian.com/cloud/jira/platform/deprecation-notice-basic-auth-and-cookie-based-auth/).
        Destroys the user's Jira session. **[Permissions](https://confluence.atlassian.com/x/FQiiLQ)
        required:** None.
      operationId: com.atlassian.jira.rest.auth.Login.logOut_delete
      x-api-path-slug: auth1session-delete
      responses:
        200:
          description: OK
      tags:
      - Session