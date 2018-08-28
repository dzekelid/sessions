swagger: "2.0"
x-collection-name: Coord
x-complete: 1
info:
  title: Users API
  description: the-users-api-allows-you-to-manage-user-data-on-the-coord-platform--sending-user-data-to-coordallows-you-to-perform-transactions-with-mobility-systems-like-renting-a-bike-parking-ina-parking-lot-or-booking-a-ridehail-trip-on-behalf-of-that-user-using-the-coord-platform-the-requirements-for-performing-a-transaction-for-a-given-user-vary-depending-on-the-systemyoure-connecting-with--some-systems-require-particular-data-about-a-user-in-order-for-thetransaction-to-take-place-and-some-systems-require-you-to-link-a-users-account--alltransactions-require-you-to-authenticate-the-user-using-a-jwt-every-coord-api-that-supports-transactions-has-an-endpoint-for-getting-information-aboutthat-apis-systems-along-with-what-you-need-to-provide-for-a-user-in-order-to-perform-atransaction-for-them--the-users-api-provides-tools-that-help-you-enable-users-to-performtransactions-as-well-as-tools-for-learning-about-the-transactions-that-a-user-can-alreadyperform-read-on-for-more-information-about-authenticating-users-linking-accounts-and-managing-userdata--authenticating-users-with-jwtsall-coord-api-endpoints-that-either-manipulate-data-or-perform-a-transaction-on-behalf-of-alogged-in-user-require-http-calls-to-include-an-authorization-bearer-jwt-token-so-thatthe-current-user-can-be-identified--all-endpoints-in-the-users-api-fall-into-this-categoryexcept-for-the-test-jwt-creation-endpoint-which-is-designed-to-allow-you-to-create-test-tokensfor-use-in-such-requests-for-information-on-how-to-create-nontest-user-authorization-tokensplease-contact-a-hrefmailtosalescoord-co-target-blanksalescoord-coaas-this-is-available-only-for-transaction-enabled-partners-see-post-v1userstestinguser-and-jwtreference0testjwtcreation-for-information-onhow-to-create-jwts-for-testing--linking-accountsmany-systems-require-you-to-link-a-user-in-order-to-perform-a-transaction--you-can-do-this-byredirecting-the-users-browser-or-webview-to-theget-v1userslink-accountreference0linkauseraccounttoenabletransactions-endpoint-this-will-allow-the-user-to-link-to-an-existing-account-with-that-system-if-they-have-one-orwill-create-a-new-one-for-them--if-you-call-this-endpoint-with-a-test-jwt-we-will-simulateaccount-linking-by-redirecting-the-user-to-a-demo-permission-page-you-can-also-simulate-linking-or-unlinking-test-users-accounts-serverside-by-calling-thepost-v1userstestingusercurrenttransactable-systemsreference0simulateaccountlinkingfortestingendpoint-remember-that-not-all-systems-are-transactable-and-not-all-transactable-systems-requireaccount-linking--getting-and-setting-user-infowe-automatically-ingest-user-information-like-email-addresses-and-names-from-the-jwtauthorization-token-you-send-us--information-about-a-users-vehicle-like-their-license-plateneeds-to-be-set-through-our-api--we-require-this-in-order-for-the-user-to-transact-with-certainparking-operators-you-can-call-get-v1usersusercurrentreference0getuserinfo-to-get-all-theinformation-we-have-about-a-user-including-the-fields-we-deduce-from-their-jwt-and-those-thatyou-have-already-set-through-our-api-you-can-call-v1usersusercurrentupdate-vehiclereference0updateuservehicle-toupdate-the-vehicle-thats-associated-with-a-users-account-
  version: 1.0.0
host: api.coord.co
basePath: /v1/users
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{location_id}/session:
    get:
      summary: Retrieve a location's sessions
      description: |-
        Retrieve information about all existing sessions at a location.

        On success, the response will be a list of existing sessions. At most one will still be
        active:
        ```
          [
            {
              "id":1,
              "start_time":"2018-04-12T00:14:20.292Z",
              "end_time":"2018-04-12T04:10:13.456Z",
              "user_id":"00000000-0000-0000-0000-000000000000"
            },
            {
              "id":2,
              "start_time":"2018-04-12T00:14:20.292Z",
              "user_id":"00000000-0000-0000-0000-000000000000"
            }
          ]
        ```
      operationId: get_location_sessions
      x-api-path-slug: location-idsession-get
      parameters:
      - in: query
        name: access_key
        description: The API access key for the request
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Locations
      - Sessions
    post:
      summary: Create a new session
      description: |-
        Create a new session for the specified user at this location_id. Returns it with either
        the start_time set, or a follow-on token (barcode, number, etc.) that the end user must use
        to initiate the session at the location.

        On success, the response will be the newly created session:
        ```
          {
            "id":1,
            "start_time":"2018-04-12T00:14:20.292Z",
            "user_id":"00000000-0000-0000-0000-000000000000"
          }
        ```
      operationId: post_session
      x-api-path-slug: location-idsession-post
      parameters:
      - in: query
        name: access_key
        description: The API access key for the request
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - New
      - Session
  /session:
    get:
      summary: Retrieve a user's sessions
      description: |-
        Retrieve information about all of a user's existing sessions.

        On success, the response will be a list of existing sessions. At most one will still be
        active:
        ```
          [
            {
              "id":1,
              "start_time":"2018-04-12T00:14:20.292Z",
              "end_time":"2018-04-12T04:10:13.456Z",
              "user_id":"00000000-0000-0000-0000-000000000000"
            },
            {
              "id":2,
              "start_time":"2018-04-12T00:14:20.292Z",
              "user_id":"00000000-0000-0000-0000-000000000000"
            }
          ]
        ```
      operationId: get_user_sessions
      x-api-path-slug: session-get
      parameters:
      - in: query
        name: access_key
        description: The API access key for the request
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Users
      - Sessions
  /{location_id}/session/{session_id}:
    get:
      summary: Retrieve an existing session
      description: |-
        Retrieve information about an existing session. This is useful to determine if/when an
        existing session has been started or ended (via external, barcode mechanism, for example).
        It may be polled to provide live feedback to an end user.

        On success, the response will be the existing session:
        ```
          {
            "id":1,
            "start_time":"2018-04-12T00:14:20.292Z",
            "user_id":"00000000-0000-0000-0000-000000000000"
          }
        ```
      operationId: get_session
      x-api-path-slug: location-idsessionsession-id-get
      parameters:
      - in: query
        name: access_key
        description: The API access key for the request
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Retrieve
      - Existing
      - Session
  /{location_id}/session/{session_id}/end:
    put:
      summary: End a previously started session
      description: |-
        End a previously started session. Note that it is invalid to call this method for sessions
        where checkout is controlled physically (those returned with a `redemption_info` field).

        On success, the response will be the existing session with billing info:
        ```
          {
            "billing_info": {
              "cost": {
                "amount": 100,
                "currency": "USD"
              }
            },
            "end_time": "2018-04-12T00:17:50.161Z",
            "id":1,
            "start_time":"2018-04-12T00:14:20.292Z",
            "user_id":"00000000-0000-0000-0000-000000000000"
          }
        ```
      operationId: end_session
      x-api-path-slug: location-idsessionsession-idend-put
      parameters:
      - in: query
        name: access_key
        description: The API access key for the request
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - End
      - Previously
      - Started
      - Session