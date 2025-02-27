---
displayed_sidebar: jsClientSidebar
---

# Class: Client

[internal](../modules/internal.md).Client

## Properties

### axiosClient

• `Private` **axiosClient**: [`AxiosInstance`](../interfaces/internal.AxiosInstance.md)

#### Defined in

[medusa-js/src/request.ts:29](https://github.com/medusajs/medusa/blob/0b0d50b47/packages/medusa-js/src/request.ts#L29)

___

### config

• `Private` **config**: [`Config`](../interfaces/internal.Config.md)

#### Defined in

[medusa-js/src/request.ts:30](https://github.com/medusajs/medusa/blob/0b0d50b47/packages/medusa-js/src/request.ts#L30)

## Methods

### createClient

▸ **createClient**(`config`): [`AxiosInstance`](../interfaces/internal.AxiosInstance.md)

Creates the axios client used for requests
As part of the creation, we configure the retry conditions
and the exponential backoff approach.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `config` | [`Config`](../interfaces/internal.Config.md) | user supplied configurations |

#### Returns

[`AxiosInstance`](../interfaces/internal.AxiosInstance.md)

#### Defined in

[medusa-js/src/request.ts:146](https://github.com/medusajs/medusa/blob/0b0d50b47/packages/medusa-js/src/request.ts#L146)

___

### normalizeHeader

▸ **normalizeHeader**(`header`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `header` | `string` |

#### Returns

`string`

#### Defined in

[medusa-js/src/request.ts:83](https://github.com/medusajs/medusa/blob/0b0d50b47/packages/medusa-js/src/request.ts#L83)

___

### normalizeHeaders

▸ **normalizeHeaders**(`obj`): `Record`<`string`, `any`\>

#### Parameters

| Name | Type |
| :------ | :------ |
| `obj` | `object` |

#### Returns

`Record`<`string`, `any`\>

#### Defined in

[medusa-js/src/request.ts:71](https://github.com/medusajs/medusa/blob/0b0d50b47/packages/medusa-js/src/request.ts#L71)

___

### request

▸ **request**(`method`, `path`, `payload?`, `options?`, `customHeaders?`): `Promise`<`any`\>

Axios request

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `method` | [`RequestMethod`](../modules/internal.md#requestmethod) | request method |
| `path` | `string` | request path |
| `payload` | `Record`<`string`, `any`\> | request payload |
| `options` | [`RequestOptions`](../interfaces/internal.RequestOptions.md) | axios configuration |
| `customHeaders` | `Record`<`string`, `any`\> | custom request headers |

#### Returns

`Promise`<`any`\>

#### Defined in

[medusa-js/src/request.ts:183](https://github.com/medusajs/medusa/blob/0b0d50b47/packages/medusa-js/src/request.ts#L183)

___

### requiresAuthentication

▸ **requiresAuthentication**(`path`, `method`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `path` | `any` |
| `method` | `any` |

#### Returns

`boolean`

#### Defined in

[medusa-js/src/request.ts:92](https://github.com/medusajs/medusa/blob/0b0d50b47/packages/medusa-js/src/request.ts#L92)

___

### setHeaders

▸ **setHeaders**(`userHeaders`, `method`, `path`, `customHeaders?`): [`AxiosRequestHeaders`](../modules/internal.md#axiosrequestheaders)

Creates all the initial headers.
We add the idempotency key, if the request is configured to retry.

#### Parameters

| Name | Type | Description |
| :------ | :------ | :------ |
| `userHeaders` | [`RequestOptions`](../interfaces/internal.RequestOptions.md) | user supplied headers |
| `method` | [`RequestMethod`](../modules/internal.md#requestmethod) | request method |
| `path` | `string` | request path |
| `customHeaders` | `Record`<`string`, `any`\> | user supplied headers |

#### Returns

[`AxiosRequestHeaders`](../modules/internal.md#axiosrequestheaders)

#### Defined in

[medusa-js/src/request.ts:108](https://github.com/medusajs/medusa/blob/0b0d50b47/packages/medusa-js/src/request.ts#L108)

___

### shouldRetryCondition

▸ **shouldRetryCondition**(`err`, `numRetries`, `maxRetries`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `err` | [`AxiosError`](../interfaces/internal.AxiosError.md)<`any`, `any`\> |
| `numRetries` | `number` |
| `maxRetries` | `number` |

#### Returns

`boolean`

#### Defined in

[medusa-js/src/request.ts:40](https://github.com/medusajs/medusa/blob/0b0d50b47/packages/medusa-js/src/request.ts#L40)
