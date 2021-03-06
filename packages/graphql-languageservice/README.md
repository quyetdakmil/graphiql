# `graphql-languageservice`

> **Note**: Still mostly experimental, however it depends mostly on stable libraries.

## Purpose

This package brings together all the dependencies for building out web or desktop IDE services for the GraphQL Language.

It is named as such to match the convention of other vscode languageservices.

It also provides a new `LanguageService` class as browser/web-worker runtime friendly alternative to the one that lives in `graphql-language-service-interface`, that utilizes the same underlying functions, meaning _most_ fixes and improvements from here on out will continue to be reflected by both implementations.

## Usage

Instantiates with these optional parameters:

```ts
type GraphQLLanguageConfig = {
  parser?: typeof parse;
  schemaLoader?: typeof defaultSchemaLoader;
  schemaBuilder?: typeof defaultSchemaBuilder;
  schemaConfig: SchemaConfig;
};
```

this is the minimum configuration required:

```ts
const languageService = new LanguageService({
  schemaConfig: { uri: 'https://my/schema' },
});
```

### Methods

We are working on restoring our typedoc which will provide much more info soon.
