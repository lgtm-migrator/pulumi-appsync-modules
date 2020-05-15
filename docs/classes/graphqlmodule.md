[pulumi-appsync-modules](../README.md) › [GraphQLModule](graphqlmodule.md)

# Class: GraphQLModule <**TData**>

## Type parameters

▪ **TData**

## Hierarchy

* ComponentResource

  ↳ **GraphQLModule**

## Index

### Constructors

* [constructor](graphqlmodule.md#constructor)

### Properties

* [datasources](graphqlmodule.md#datasources)
* [resolvers](graphqlmodule.md#resolvers)
* [typeDefs](graphqlmodule.md#optional-typedefs)
* [urn](graphqlmodule.md#readonly-urn)

### Methods

* [getData](graphqlmodule.md#protected-getdata)
* [getProvider](graphqlmodule.md#getprovider)
* [initialize](graphqlmodule.md#protected-initialize)
* [registerOutputs](graphqlmodule.md#protected-registeroutputs)
* [isInstance](graphqlmodule.md#static-isinstance)

## Constructors

###  constructor

\+ **new GraphQLModule**(`name`: string, `args`: [GraphQLModuleArgs](../interfaces/graphqlmoduleargs.md), `opts`: ComponentResourceOptions): *[GraphQLModule](graphqlmodule.md)*

*Overrides void*

Create a GraphQLModule resource with the given unique name, arguments, and options.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`name` | string | - | The _unique_ name of the resource. |
`args` | [GraphQLModuleArgs](../interfaces/graphqlmoduleargs.md) | - | The arguments to use to populate this resource's properties. |
`opts` | ComponentResourceOptions | {} | A bag of options that control this resource's behavior.  |

**Returns:** *[GraphQLModule](graphqlmodule.md)*

## Properties

###  datasources

• **datasources**: *[GraphQLDataSource](graphqldatasource.md)[]*

___

###  resolvers

• **resolvers**: *[GraphQLResolver](graphqlresolver.md)[]*

___

### `Optional` typeDefs

• **typeDefs**? : *undefined | string*

___

### `Readonly` urn

• **urn**: *Output‹URN›*

*Inherited from [GraphQLResolver](graphqlresolver.md).[urn](graphqlresolver.md#readonly-urn)*

urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

## Methods

### `Protected` getData

▸ **getData**(): *Promise‹TData›*

*Inherited from [GraphQLResolver](graphqlresolver.md).[getData](graphqlresolver.md#protected-getdata)*

Retrieves the data produces by [initialize].  The data is immediately available in a
derived class's constructor after the `super(...)` call to `ComponentResource`.

**Returns:** *Promise‹TData›*

___

###  getProvider

▸ **getProvider**(`moduleMember`: string): *ProviderResource | undefined*

*Inherited from [GraphQLResolver](graphqlresolver.md).[getProvider](graphqlresolver.md#getprovider)*

**Parameters:**

Name | Type |
------ | ------ |
`moduleMember` | string |

**Returns:** *ProviderResource | undefined*

___

### `Protected` initialize

▸ **initialize**(`args`: Inputs): *Promise‹TData›*

*Inherited from [GraphQLResolver](graphqlresolver.md).[initialize](graphqlresolver.md#protected-initialize)*

Can be overridden by a subclass to asynchronously initialize data for this Component
automatically when constructed.  The data will be available immediately for subclass
constructors to use.  To access the data use `.getData`.

**Parameters:**

Name | Type |
------ | ------ |
`args` | Inputs |

**Returns:** *Promise‹TData›*

___

### `Protected` registerOutputs

▸ **registerOutputs**(`outputs?`: Inputs | Promise‹Inputs› | Output‹Inputs›): *void*

*Inherited from [GraphQLResolver](graphqlresolver.md).[registerOutputs](graphqlresolver.md#protected-registeroutputs)*

registerOutputs registers synthetic outputs that a component has initialized, usually by
allocating other child sub-resources and propagating their resulting property values.

ComponentResources can call this at the end of their constructor to indicate that they are
done creating child resources.  This is not strictly necessary as this will automatically be
called after the `initialize` method completes.

**Parameters:**

Name | Type |
------ | ------ |
`outputs?` | Inputs &#124; Promise‹Inputs› &#124; Output‹Inputs› |

**Returns:** *void*

___

### `Static` isInstance

▸ **isInstance**(`obj`: any): *obj is ComponentResource*

*Inherited from [GraphQLResolver](graphqlresolver.md).[isInstance](graphqlresolver.md#static-isinstance)*

*Overrides void*

Returns true if the given object is an instance of CustomResource.  This is designed to work even when
multiple copies of the Pulumi SDK have been loaded into the same process.

**Parameters:**

Name | Type |
------ | ------ |
`obj` | any |

**Returns:** *obj is ComponentResource*