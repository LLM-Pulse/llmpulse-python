# llmpulse.TeamApi

All URIs are relative to *https://api.llmpulse.ai/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_team_invitation**](TeamApi.md#create_team_invitation) | **POST** /team_invitations | Invite a team member
[**list_team_invitations**](TeamApi.md#list_team_invitations) | **GET** /team_invitations | List pending team invitations
[**list_team_members**](TeamApi.md#list_team_members) | **GET** /team_members | List team members
[**remove_team_member**](TeamApi.md#remove_team_member) | **DELETE** /team_members/{id} | Remove a team member
[**revoke_team_invitation**](TeamApi.md#revoke_team_invitation) | **DELETE** /team_invitations/{id} | Revoke a pending team invitation


# **create_team_invitation**
> CreateTeamInvitation201Response create_team_invitation(create_team_invitation_request)

Invite a team member

Invites someone to the account team with the same rules as the Team Members settings page, and sends them the invitation email (email_sent is false when the email provider refused it; the invitation still exists, so revoke it and invite again once the address is fixed). Send project_ids, or all_projects: true for every project (for a team member inviting, every project they can access). The account owner and co-owners choose the access with permission_role: full_access (default), view_only, custom (with permissions, feature key to verbs) or account_role (with account_role_id). A team member with permission to invite cannot choose access: leave those fields out and the invitation copies their own permissions. Only the account owner can set account_admin (co-owner) or billing_access. An address already registered on the platform, or with an invitation pending, is refused with ERR_INVALID_PARAM (revoke the pending one first). An account that cannot add more team members, or that reached its daily limit of invitations sent through the API and MCP (revoked ones count), answers ERR_LIMIT_REACHED; the message says which. Requires a `read_write` scope API key.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.create_team_invitation201_response import CreateTeamInvitation201Response
from llmpulse.models.create_team_invitation_request import CreateTeamInvitationRequest
from llmpulse.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.llmpulse.ai/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = llmpulse.Configuration(
    host = "https://api.llmpulse.ai/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: BearerAuth
configuration = llmpulse.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with llmpulse.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = llmpulse.TeamApi(api_client)
    create_team_invitation_request = llmpulse.CreateTeamInvitationRequest() # CreateTeamInvitationRequest | 

    try:
        # Invite a team member
        api_response = api_instance.create_team_invitation(create_team_invitation_request)
        print("The response of TeamApi->create_team_invitation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TeamApi->create_team_invitation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_team_invitation_request** | [**CreateTeamInvitationRequest**](CreateTeamInvitationRequest.md)|  | 

### Return type

[**CreateTeamInvitation201Response**](CreateTeamInvitation201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created. The invitation, as GET /team_invitations lists it, and whether the email went out. |  -  |
**401** | Authentication failed |  -  |
**403** | A key limited to some projects answers ERR_KEY_PROJECT_SCOPED, since the team belongs to the whole account. A team member without the Team Members permission, or asking for something only the owner or a co-owner can do, answers ERR_INSUFFICIENT_PERMISSION, and a write with a read-only key ERR_INSUFFICIENT_SCOPE, with the same status |  -  |
**404** | Resource not found |  -  |
**422** | Invalid parameters |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_team_invitations**
> ListTeamInvitations200Response list_team_invitations(page=page, per_page=per_page)

List pending team invitations

Lists invitations that have not been accepted yet: the address, the access and projects the person will get, when the invitation was sent and when its link expires. An accepted invitation keeps its id and moves to GET /team_members. Same access rules as GET /team_members.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.list_team_invitations200_response import ListTeamInvitations200Response
from llmpulse.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.llmpulse.ai/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = llmpulse.Configuration(
    host = "https://api.llmpulse.ai/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: BearerAuth
configuration = llmpulse.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with llmpulse.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = llmpulse.TeamApi(api_client)
    page = 56 # int |  (optional)
    per_page = 56 # int | Default 20, max 100 (optional)

    try:
        # List pending team invitations
        api_response = api_instance.list_team_invitations(page=page, per_page=per_page)
        print("The response of TeamApi->list_team_invitations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TeamApi->list_team_invitations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **per_page** | **int**| Default 20, max 100 | [optional] 

### Return type

[**ListTeamInvitations200Response**](ListTeamInvitations200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**401** | Authentication failed |  -  |
**403** | A key limited to some projects answers ERR_KEY_PROJECT_SCOPED, since the team belongs to the whole account. A team member without the Team Members permission, or asking for something only the owner or a co-owner can do, answers ERR_INSUFFICIENT_PERMISSION, and a write with a read-only key ERR_INSUFFICIENT_SCOPE, with the same status |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_team_members**
> ListTeamMembers200Response list_team_members(page=page, per_page=per_page)

List team members

Lists the account owner first, then every team member who joined, with their access level (permission_role, account role and the resulting permissions), co-owner and billing flags, project access, status (active or blocked) and last sign-in. Pending invitations are listed by GET /team_invitations; GET /account limits.team_members.used counts both. Available to the account owner, co-owners and team members with the Team Members permission. A key limited to some projects answers ERR_KEY_PROJECT_SCOPED: the team belongs to the whole account.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.list_team_members200_response import ListTeamMembers200Response
from llmpulse.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.llmpulse.ai/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = llmpulse.Configuration(
    host = "https://api.llmpulse.ai/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: BearerAuth
configuration = llmpulse.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with llmpulse.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = llmpulse.TeamApi(api_client)
    page = 56 # int |  (optional)
    per_page = 56 # int | Default 20, max 100 (optional)

    try:
        # List team members
        api_response = api_instance.list_team_members(page=page, per_page=per_page)
        print("The response of TeamApi->list_team_members:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TeamApi->list_team_members: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **per_page** | **int**| Default 20, max 100 | [optional] 

### Return type

[**ListTeamMembers200Response**](ListTeamMembers200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**401** | Authentication failed |  -  |
**403** | A key limited to some projects answers ERR_KEY_PROJECT_SCOPED, since the team belongs to the whole account. A team member without the Team Members permission, or asking for something only the owner or a co-owner can do, answers ERR_INSUFFICIENT_PERMISSION, and a write with a read-only key ERR_INSUFFICIENT_SCOPE, with the same status |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_team_member**
> RemoveTeamMember200Response remove_team_member(id)

Remove a team member

Removes a member from the team, as the settings page does: their sessions and API keys stop working at once and their user account is deleted in the background shortly after. Account owner or co-owner only; a co-owner cannot remove the owner, another co-owner or themselves. The owner cannot be removed. Pending invitations are revoked with DELETE /team_invitations/{id}; an id that is not a member of the account answers ERR_NOT_FOUND. Requires a `read_write` scope API key.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.remove_team_member200_response import RemoveTeamMember200Response
from llmpulse.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.llmpulse.ai/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = llmpulse.Configuration(
    host = "https://api.llmpulse.ai/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: BearerAuth
configuration = llmpulse.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with llmpulse.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = llmpulse.TeamApi(api_client)
    id = 56 # int | The member id from GET /team_members

    try:
        # Remove a team member
        api_response = api_instance.remove_team_member(id)
        print("The response of TeamApi->remove_team_member:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TeamApi->remove_team_member: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The member id from GET /team_members | 

### Return type

[**RemoveTeamMember200Response**](RemoveTeamMember200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**401** | Authentication failed |  -  |
**403** | A key limited to some projects answers ERR_KEY_PROJECT_SCOPED, since the team belongs to the whole account. A team member without the Team Members permission, or asking for something only the owner or a co-owner can do, answers ERR_INSUFFICIENT_PERMISSION, and a write with a read-only key ERR_INSUFFICIENT_SCOPE, with the same status |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **revoke_team_invitation**
> RevokeTeamInvitation200Response revoke_team_invitation(id)

Revoke a pending team invitation

Revokes a pending invitation: its link stops working immediately. Account owner or co-owner only, and a co-owner cannot revoke an invitation that makes someone a co-owner. Members who already joined are removed with DELETE /team_members/{id}; an id that is not a pending invitation of the account answers ERR_NOT_FOUND. Requires a `read_write` scope API key.

### Example

* Bearer Authentication (BearerAuth):

```python
import llmpulse
from llmpulse.models.revoke_team_invitation200_response import RevokeTeamInvitation200Response
from llmpulse.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.llmpulse.ai/api/v1
# See configuration.py for a list of all supported configuration parameters.
configuration = llmpulse.Configuration(
    host = "https://api.llmpulse.ai/api/v1"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization: BearerAuth
configuration = llmpulse.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with llmpulse.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = llmpulse.TeamApi(api_client)
    id = 56 # int | The invitation id from GET /team_invitations

    try:
        # Revoke a pending team invitation
        api_response = api_instance.revoke_team_invitation(id)
        print("The response of TeamApi->revoke_team_invitation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TeamApi->revoke_team_invitation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int**| The invitation id from GET /team_invitations | 

### Return type

[**RevokeTeamInvitation200Response**](RevokeTeamInvitation200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | OK |  -  |
**401** | Authentication failed |  -  |
**403** | A key limited to some projects answers ERR_KEY_PROJECT_SCOPED, since the team belongs to the whole account. A team member without the Team Members permission, or asking for something only the owner or a co-owner can do, answers ERR_INSUFFICIENT_PERMISSION, and a write with a read-only key ERR_INSUFFICIENT_SCOPE, with the same status |  -  |
**404** | Resource not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

