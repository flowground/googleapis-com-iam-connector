# ![LOGO](logo.png) Identity and Access Management (IAM) **flow**ground Connector

## Description

A generated **flow**ground connector for the Identity and Access Management (IAM) API (version v1).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/iam/v1/swagger.json<br/>
Generated at: 2019-05-23T12:13:26+03:00

## API Description

Manages identity and access control for Google Cloud Platform resources, including the creation of service accounts, which you can use to authenticate to Google and make API calls.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Lints a Cloud IAM policy object or its sub fields. Currently supports<br/>
> google.iam.v1.Policy, google.iam.v1.Binding and<br/>
> google.iam.v1.Binding.condition.<br/>
> <br/>
> Each lint operation consists of multiple lint validation units.<br/>
> Validation units have the following properties:<br/>
> <br/>
> - Each unit inspects the input object in regard to a particular<br/>
>   linting aspect and issues a google.iam.admin.v1.LintResult<br/>
>   disclosing the result.<br/>
> - Domain of discourse of each unit can be either<br/>
>   google.iam.v1.Policy, google.iam.v1.Binding, or<br/>
>   google.iam.v1.Binding.condition depending on the purpose of the<br/>
>   validation.<br/>
> - A unit may require additional data (like the list of all possible<br/>
>   enumerable values of a particular attribute used in the policy instance)<br/>
>   which shall be provided by the caller. Refer to the comments of<br/>
>   google.iam.admin.v1.LintPolicyRequest.context for more details.<br/>
> <br/>
> The set of applicable validation units is determined by the Cloud IAM<br/>
> server and is not configurable.<br/>
> <br/>
> Regardless of any lint issues or their severities, successful calls to<br/>
> `lintPolicy` return an HTTP 200 OK status code.

*Tags:* `iamPolicies`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns a list of services that support service level audit logging<br/>
> configuration for the given resource.

*Tags:* `iamPolicies`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists the permissions testable on a resource.<br/>
> A permission is testable if it can be tested for an identity on a resource.

*Tags:* `permissions`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists the Roles defined on a resource.

*Tags:* `roles`

#### Input Parameters
* `pageSize` - _optional_ - Optional limit on the number of roles to include in the response.
* `pageToken` - _optional_ - Optional pagination token returned in an earlier ListRolesResponse.
* `parent` - _optional_ - The resource name of the parent resource in one of the following formats:
`` (empty string) -- this refers to curated roles.
`organizations/{ORGANIZATION_ID}`
`projects/{PROJECT_ID}`
* `showDeleted` - _optional_ - Include Roles that have been deleted.
* `view` - _optional_ - Optional view for the returned Role objects. When `FULL` is specified,
the `includedPermissions` field is returned, which includes a list of all
permissions in the role. The default value is `BASIC`, which does not
return the `includedPermissions` field.
    Possible values: BASIC, FULL.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Queries roles that can be granted on a particular resource.<br/>
> A role is grantable if it can be used as the role in a binding for a policy<br/>
> for that resource.

*Tags:* `roles`

#### Input Parameters
* `$.xgafv` - _optional_ - V1 error format.
    Possible values: 1, 2.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Soft deletes a role. The role is suspended and cannot be used to create new<br/>
> IAM Policy Bindings.<br/>
> The Role will not be included in `ListRoles()` unless `show_deleted` is set<br/>
> in the `ListRolesRequest`. The Role contains the deleted boolean set.<br/>
> Existing Bindings remains, but are inactive. The Role can be undeleted<br/>
> within 7 days. After 7 days the Role is deleted and all Bindings associated<br/>
> with the role are removed.

*Tags:* `projects`

#### Input Parameters
* `etag` - _optional_ - Used to perform a consistent read-modify-write.
* `name` - _required_ - The resource name of the role in one of the following formats:
`organizations/{ORGANIZATION_ID}/roles/{ROLE_NAME}`
`projects/{PROJECT_ID}/roles/{ROLE_NAME}`
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets a Role definition.

*Tags:* `roles`

#### Input Parameters
* `name` - _required_ - The resource name of the role in one of the following formats:
`roles/{ROLE_NAME}`
`organizations/{ORGANIZATION_ID}/roles/{ROLE_NAME}`
`projects/{PROJECT_ID}/roles/{ROLE_NAME}`
* `publicKeyType` - _optional_ - The output format of the public key requested.
X509_PEM is the default output format.
    Possible values: TYPE_NONE, TYPE_X509_PEM_FILE, TYPE_RAW_PUBLIC_KEY.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates a Role definition.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The resource name of the role in one of the following formats:
`roles/{ROLE_NAME}`
`organizations/{ORGANIZATION_ID}/roles/{ROLE_NAME}`
`projects/{PROJECT_ID}/roles/{ROLE_NAME}`
* `updateMask` - _optional_ - A mask describing which fields in the Role have changed.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Note: This method is in the process of being deprecated. Use<br/>
> PatchServiceAccount instead.<br/>
> <br/>
> Updates a ServiceAccount.<br/>
> <br/>
> Currently, only the following fields are updatable:<br/>
> `display_name` .<br/>
> The `etag` is mandatory.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The resource name of the service account in the following format:
`projects/{PROJECT_ID}/serviceAccounts/{ACCOUNT}`.

Requests using `-` as a wildcard for the `PROJECT_ID` will infer the
project from the `account` and the `ACCOUNT` value can be the `email`
address or the `unique_id` of the service account.

In responses the resource name will always be in the format
`projects/{PROJECT_ID}/serviceAccounts/{ACCOUNT}`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists ServiceAccountKeys.

*Tags:* `projects`

#### Input Parameters
* `keyTypes` - _optional_ - Filters the types of keys the user wants to include in the list
response. Duplicate key types are not allowed. If no key type
is provided, all keys are returned.
* `name` - _required_ - The resource name of the service account in the following format:
`projects/{PROJECT_ID}/serviceAccounts/{ACCOUNT}`.

Using `-` as a wildcard for the `PROJECT_ID`, will infer the project from
the account. The `ACCOUNT` value can be the `email` address or the
`unique_id` of the service account.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a ServiceAccountKey<br/>
> and returns it.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The resource name of the service account in the following format:
`projects/{PROJECT_ID}/serviceAccounts/{ACCOUNT}`.
Using `-` as a wildcard for the `PROJECT_ID` will infer the project from
the account. The `ACCOUNT` value can be the `email` address or the
`unique_id` of the service account.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists ServiceAccounts for a project.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Required. The resource name of the project associated with the service
accounts, such as `projects/my-project-123`.
* `pageSize` - _optional_ - Optional limit on the number of service accounts to include in the
response. Further accounts can subsequently be obtained by including the
ListServiceAccountsResponse.next_page_token
in a subsequent request.
* `pageToken` - _optional_ - Optional pagination token returned in an earlier
ListServiceAccountsResponse.next_page_token.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a ServiceAccount<br/>
> and returns it.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Required. The resource name of the project associated with the service
accounts, such as `projects/my-project-123`.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### **Note**: This method is in the process of being deprecated. Call the<br/>
> [`signBlob()`](/iam/credentials/reference/rest/v1/projects.serviceAccounts/signBlob)<br/>
> method of the Cloud IAM Service Account Credentials API instead.<br/>
> <br/>
> Signs a blob using a service account's system-managed private key.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The resource name of the service account in the following format:
`projects/{PROJECT_ID}/serviceAccounts/{ACCOUNT}`.
Using `-` as a wildcard for the `PROJECT_ID` will infer the project from
the account. The `ACCOUNT` value can be the `email` address or the
`unique_id` of the service account.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### **Note**: This method is in the process of being deprecated. Call the<br/>
> [`signJwt()`](/iam/credentials/reference/rest/v1/projects.serviceAccounts/signJwt)<br/>
> method of the Cloud IAM Service Account Credentials API instead.<br/>
> <br/>
> Signs a JWT using a service account's system-managed private key.<br/>
> <br/>
> If no expiry time (`exp`) is provided in the `SignJwtRequest`, IAM sets an<br/>
> an expiry time of one hour by default. If you request an expiry time of<br/>
> more than one hour, the request will fail.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The resource name of the service account in the following format:
`projects/{PROJECT_ID}/serviceAccounts/{ACCOUNT}`.
Using `-` as a wildcard for the `PROJECT_ID` will infer the project from
the account. The `ACCOUNT` value can be the `email` address or the
`unique_id` of the service account.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Undelete a Role, bringing it back in its previous state.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - The resource name of the role in one of the following formats:
`organizations/{ORGANIZATION_ID}/roles/{ROLE_NAME}`
`projects/{PROJECT_ID}/roles/{ROLE_NAME}`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists the Roles defined on a resource.

*Tags:* `projects`

#### Input Parameters
* `pageSize` - _optional_ - Optional limit on the number of roles to include in the response.
* `pageToken` - _optional_ - Optional pagination token returned in an earlier ListRolesResponse.
* `parent` - _required_ - The resource name of the parent resource in one of the following formats:
`` (empty string) -- this refers to curated roles.
`organizations/{ORGANIZATION_ID}`
`projects/{PROJECT_ID}`
* `showDeleted` - _optional_ - Include Roles that have been deleted.
* `view` - _optional_ - Optional view for the returned Role objects. When `FULL` is specified,
the `includedPermissions` field is returned, which includes a list of all
permissions in the role. The default value is `BASIC`, which does not
return the `includedPermissions` field.
    Possible values: BASIC, FULL.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a new Role.

*Tags:* `projects`

#### Input Parameters
* `parent` - _required_ - The resource name of the parent resource in one of the following formats:
`organizations/{ORGANIZATION_ID}`
`projects/{PROJECT_ID}`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns the Cloud IAM access control policy for a<br/>
> ServiceAccount.<br/>
> <br/>
> Note: Service accounts are both<br/>
> [resources and identities](/iam/docs/service-accounts#service_account_permissions).<br/>
> This method treats the service account as a resource. It returns the Cloud<br/>
> IAM policy that reflects what members have access to the service account.<br/>
> <br/>
> This method does not return what resources the service account has access<br/>
> to. To see if a service account has access to a resource, call the<br/>
> `getIamPolicy` method on the target resource. For example, to view grants<br/>
> for a project, call the<br/>
> [projects.getIamPolicy](/resource-manager/reference/rest/v1/projects/getIamPolicy)<br/>
> method.

*Tags:* `projects`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy is being requested.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Sets the Cloud IAM access control policy for a<br/>
> ServiceAccount.<br/>
> <br/>
> Note: Service accounts are both<br/>
> [resources and identities](/iam/docs/service-accounts#service_account_permissions).<br/>
> This method treats the service account as a resource. Use it to grant<br/>
> members access to the service account, such as when they need to<br/>
> impersonate it.<br/>
> <br/>
> This method does not grant the service account access to other resources,<br/>
> such as projects. To grant a service account access to resources, include<br/>
> the service account in the Cloud IAM policy for the desired resource, then<br/>
> call the appropriate `setIamPolicy` method on the target resource. For<br/>
> example, to grant a service account access to a project, call the<br/>
> [projects.setIamPolicy](/resource-manager/reference/rest/v1/projects/setIamPolicy)<br/>
> method.

*Tags:* `projects`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy is being specified.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Tests the specified permissions against the IAM access control policy<br/>
> for a ServiceAccount.

*Tags:* `projects`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy detail is being requested.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-iam-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
