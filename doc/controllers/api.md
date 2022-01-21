# API

```ts
const apiController = new ApiController(client);
```

## Class Name

`ApiController`

## Methods

* [Test](/doc/controllers/api.md#test)
* [Test Endpoint 2](/doc/controllers/api.md#test-endpoint-2)


# Test

some desc

```ts
async test(
  testparam: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `testparam` | `string` | Query, Required | some desc |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

`void`

## Example Usage

```ts
const testparam = 'true';
try {
  const { result, ...httpResponse } = await apiController.test(testparam);
  // Get more response info...
  // const { statusCode, headers } = httpResponse;
} catch(error) {
  if (error instanceof ApiError) {
    const errors = error.result;
    // const { statusCode, headers } = error;
  }
}
```


# Test Endpoint 2

some desc

```ts
async testEndpoint2(
  test: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<void>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `test` | `string` | Query, Required | some desc |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

`void`

## Example Usage

```ts
const test = 'sup';
try {
  const { result, ...httpResponse } = await apiController.testEndpoint2(test);
  // Get more response info...
  // const { statusCode, headers } = httpResponse;
} catch(error) {
  if (error instanceof ApiError) {
    const errors = error.result;
    // const { statusCode, headers } = error;
  }
}
```

