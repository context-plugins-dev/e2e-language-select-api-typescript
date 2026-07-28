# API

```ts
const apiController = new ApiController(client);
```

## Class Name

`ApiController`


# List Contacts

```ts
async listContacts(
  requestOptions?: RequestOptions
): Promise<ApiResponse<CrmV3ObjectsContactsResponse>>
```

## Authentication

This endpoint requires [OAuth2](../../doc/auth/oauth-2-authorization-code-grant.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**: OK

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`CrmV3ObjectsContactsResponse`](../../doc/models/crm-v3-objects-contacts-response.md).

## Example Usage

```ts
try {
  const response = await apiController.listContacts();

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

