[avalanche](../README.md) › [Common-Transactions](../modules/common_transactions.md) › [StandardTx](common_transactions.standardtx.md)

# Class: StandardTx ‹**KPClass, KCClass, SUBTx**›

Class representing a signed transaction.

## Type parameters

▪ **KPClass**: *[StandardKeyPair](common_keychain.standardkeypair.md)*

▪ **KCClass**: *[StandardKeyChain](common_keychain.standardkeychain.md)‹KPClass›*

▪ **SUBTx**: *[StandardUnsignedTx](common_transactions.standardunsignedtx.md)‹KPClass, KCClass, [StandardBaseTx](common_transactions.standardbasetx.md)‹KPClass, KCClass››*

## Hierarchy

* [Serializable](utils_serialization.serializable.md)

  ↳ **StandardTx**

  ↳ [Tx](api_platformvm_transactions.tx.md)

  ↳ [Tx](api_avm_transactions.tx.md)

## Index

### Constructors

* [constructor](common_transactions.standardtx.md#constructor)

### Properties

* [_codecID](common_transactions.standardtx.md#protected-_codecid)
* [_typeID](common_transactions.standardtx.md#protected-_typeid)
* [_typeName](common_transactions.standardtx.md#protected-_typename)
* [credentials](common_transactions.standardtx.md#protected-credentials)
* [unsignedTx](common_transactions.standardtx.md#protected-unsignedtx)

### Methods

* [deserialize](common_transactions.standardtx.md#deserialize)
* [fromBuffer](common_transactions.standardtx.md#abstract-frombuffer)
* [fromString](common_transactions.standardtx.md#fromstring)
* [getCodecID](common_transactions.standardtx.md#getcodecid)
* [getCredentials](common_transactions.standardtx.md#getcredentials)
* [getTypeID](common_transactions.standardtx.md#gettypeid)
* [getTypeName](common_transactions.standardtx.md#gettypename)
* [getUnsignedTx](common_transactions.standardtx.md#getunsignedtx)
* [serialize](common_transactions.standardtx.md#serialize)
* [toBuffer](common_transactions.standardtx.md#tobuffer)
* [toString](common_transactions.standardtx.md#tostring)

## Constructors

###  constructor

\+ **new StandardTx**(`unsignedTx`: SUBTx, `credentials`: [Credential](common_signature.credential.md)[]): *[StandardTx](common_transactions.standardtx.md)*

*Defined in [src/common/tx.ts:388](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L388)*

Class representing a signed transaction.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`unsignedTx` | SUBTx | undefined | Optional [StandardUnsignedTx](common_transactions.standardunsignedtx.md) |
`credentials` | [Credential](common_signature.credential.md)[] | undefined | - |

**Returns:** *[StandardTx](common_transactions.standardtx.md)*

## Properties

### `Protected` _codecID

• **_codecID**: *number* = undefined

*Inherited from [SigIdx](common_signature.sigidx.md).[_codecID](common_signature.sigidx.md#protected-_codecid)*

*Defined in [src/utils/serialization.ts:40](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/utils/serialization.ts#L40)*

___

### `Protected` _typeID

• **_typeID**: *any* = undefined

*Overrides [Serializable](utils_serialization.serializable.md).[_typeID](utils_serialization.serializable.md#protected-_typeid)*

*Defined in [src/common/tx.ts:310](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L310)*

___

### `Protected` _typeName

• **_typeName**: *string* = "StandardTx"

*Overrides [Serializable](utils_serialization.serializable.md).[_typeName](utils_serialization.serializable.md#protected-_typename)*

*Defined in [src/common/tx.ts:309](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L309)*

___

### `Protected` credentials

• **credentials**: *[Credential](common_signature.credential.md)[]* = []

*Defined in [src/common/tx.ts:322](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L322)*

___

### `Protected` unsignedTx

• **unsignedTx**: *SUBTx* = undefined

*Defined in [src/common/tx.ts:321](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L321)*

## Methods

###  deserialize

▸ **deserialize**(`fields`: object, `encoding?`: [SerializedEncoding](../modules/src_utils.md#serializedencoding)): *void*

*Inherited from [StandardParseableInput](common_inputs.standardparseableinput.md).[deserialize](common_inputs.standardparseableinput.md#deserialize)*

*Defined in [src/utils/serialization.ts:72](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/utils/serialization.ts#L72)*

**Parameters:**

Name | Type |
------ | ------ |
`fields` | object |
`encoding?` | [SerializedEncoding](../modules/src_utils.md#serializedencoding) |

**Returns:** *void*

___

### `Abstract` fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset?`: number): *number*

*Defined in [src/common/tx.ts:338](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L338)*

**Parameters:**

Name | Type |
------ | ------ |
`bytes` | Buffer |
`offset?` | number |

**Returns:** *number*

___

###  fromString

▸ **fromString**(`serialized`: string): *number*

*Defined in [src/common/tx.ts:376](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L376)*

Takes a base-58 string containing an [StandardTx](common_transactions.standardtx.md), parses it, populates the class, and returns the length of the Tx in bytes.

**`remarks`** 
unlike most fromStrings, it expects the string to be serialized in cb58 format

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`serialized` | string | A base-58 string containing a raw [StandardTx](common_transactions.standardtx.md)  |

**Returns:** *number*

The length of the raw [StandardTx](common_transactions.standardtx.md)

___

###  getCodecID

▸ **getCodecID**(): *number*

*Inherited from [SigIdx](common_signature.sigidx.md).[getCodecID](common_signature.sigidx.md#getcodecid)*

*Defined in [src/utils/serialization.ts:59](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/utils/serialization.ts#L59)*

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** *number*

___

###  getCredentials

▸ **getCredentials**(): *[Credential](common_signature.credential.md)[]*

*Defined in [src/common/tx.ts:327](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L327)*

Returns the [[Credential[]]]

**Returns:** *[Credential](common_signature.credential.md)[]*

___

###  getTypeID

▸ **getTypeID**(): *number*

*Inherited from [SigIdx](common_signature.sigidx.md).[getTypeID](common_signature.sigidx.md#gettypeid)*

*Defined in [src/utils/serialization.ts:52](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/utils/serialization.ts#L52)*

Used in serialization. Optional. TypeID is a number for the typeID of object being output.

**Returns:** *number*

___

###  getTypeName

▸ **getTypeName**(): *string*

*Inherited from [SigIdx](common_signature.sigidx.md).[getTypeName](common_signature.sigidx.md#gettypename)*

*Defined in [src/utils/serialization.ts:45](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/utils/serialization.ts#L45)*

Used in serialization. TypeName is a string name for the type of object being output.

**Returns:** *string*

___

###  getUnsignedTx

▸ **getUnsignedTx**(): *SUBTx*

*Defined in [src/common/tx.ts:334](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L334)*

Returns the [StandardUnsignedTx](common_transactions.standardunsignedtx.md)

**Returns:** *SUBTx*

___

###  serialize

▸ **serialize**(`encoding`: [SerializedEncoding](../modules/src_utils.md#serializedencoding)): *object*

*Overrides [Serializable](utils_serialization.serializable.md).[serialize](utils_serialization.serializable.md#serialize)*

*Defined in [src/common/tx.ts:312](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L312)*

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`encoding` | [SerializedEncoding](../modules/src_utils.md#serializedencoding) | "hex" |

**Returns:** *object*

___

###  toBuffer

▸ **toBuffer**(): *Buffer*

*Defined in [src/common/tx.ts:343](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L343)*

Returns a [Buffer](https://github.com/feross/buffer) representation of the [StandardTx](common_transactions.standardtx.md).

**Returns:** *Buffer*

___

###  toString

▸ **toString**(): *string*

*Defined in [src/common/tx.ts:386](https://github.com/ava-labs/avalanchejs/blob/ae78dee/src/common/tx.ts#L386)*

Returns a cb58 representation of the [StandardTx](common_transactions.standardtx.md).

**`remarks`** 
unlike most toStrings, this returns in cb58 serialization format

**Returns:** *string*
