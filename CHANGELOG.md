## LSP4J Change Log

### v0.5.0 (Sep. 2018)

 * Implemented LSP version 3.10.0

Fixed issues: https://github.com/eclipse/lsp4j/milestone/3?closed=1

Breaking API changes:
 * Return type of `textDocument/documentSymbol` changed from `List<? extends SymbolInformation>` to `List<Either<SymbolInformation, DocumentSymbol>>`
 * Return type of `textDocument/codeAction` changed from `List<? extends Command>` to `List<Either<Command, CodeAction>>`

### v0.4.1 (May 2018)

Fixed issues: https://github.com/eclipse/lsp4j/milestone/4?closed=1

Breaking API changes:
 * Type of `ServerCapabilities.colorProvider` changed from `ColorProviderOptions` to `Either<Boolean, ColorProviderOptions>`
 * Renamed `ColorPresentationParams.colorInfo` property to `color`

### v0.4.0 (Apr. 2018)

 * Implemented the VS Code Debug Protocol
 * Implemented LSP version 3.7.0
 * Support multiple local and remote services
 * Improved error handling

Fixed issues: [#54](https://github.com/eclipse/lsp4j/issues/54), [#118](https://github.com/eclipse/lsp4j/issues/118), [#126](https://github.com/eclipse/lsp4j/issues/126), [#130](https://github.com/eclipse/lsp4j/issues/130), [#132](https://github.com/eclipse/lsp4j/issues/132), [#136](https://github.com/eclipse/lsp4j/issues/136), [#138](https://github.com/eclipse/lsp4j/issues/138), [#139](https://github.com/eclipse/lsp4j/issues/139), [#141](https://github.com/eclipse/lsp4j/issues/141), [#142](https://github.com/eclipse/lsp4j/issues/142), [#143](https://github.com/eclipse/lsp4j/issues/143), [#146](https://github.com/eclipse/lsp4j/issues/146), [#147](https://github.com/eclipse/lsp4j/issues/147), [#152](https://github.com/eclipse/lsp4j/issues/152), [#153](https://github.com/eclipse/lsp4j/issues/153), [#167](https://github.com/eclipse/lsp4j/issues/167), [#178](https://github.com/eclipse/lsp4j/issues/178), [#181](https://github.com/eclipse/lsp4j/issues/181), [#183](https://github.com/eclipse/lsp4j/issues/183), [#185](https://github.com/eclipse/lsp4j/issues/185), [#187](https://github.com/eclipse/lsp4j/issues/187)

Breaking API changes:
 * Parameter of `completion` requests changed from `TextDocumentPositionParams` to `CompletionParams` (this change **breaks all LanguageServer implementations**, but the migration is trivial)
 * Type of `CompletionItem.documentation`, `ParameterInformation.documentation` and `SignatureInformation.documentation` changed from `String` to `Either<String, MarkupContent>`
 * Type of `Hover.contents` changed from `List<Either<String, MarkedString>>` to `Either<List<Either<String, MarkedString>>, MarkupContent>`
 * All protocol properties with type `Object` are parsed to `JsonElement` (previously `Map` for objects and `List` for arrays)
 * Corrected `DocumentFilter.schema` property name to `scheme`
 * Removed `DocumentSelector` interface
 * `VersionedTextDocumentIdentifier.version` changed from type `int` to `Integer`, thus can be `null` now.
 
-----

### v0.3.1 (Apr. 2018)

Fixed issues: [#122](https://github.com/eclipse/lsp4j/issues/122), [#123](https://github.com/eclipse/lsp4j/issues/123), [#128](https://github.com/eclipse/lsp4j/issues/128), [#144](https://github.com/eclipse/lsp4j/issues/144), [#157](https://github.com/eclipse/lsp4j/issues/157)

### v0.3.0 (Sep. 2017)

 * Support union of three types with the `Either3` class

Fixed issues: https://github.com/eclipse/lsp4j/milestone/1?closed=1

-----

### v0.2.1 (Jul. 2017)

Fixed issues: https://github.com/eclipse/lsp4j/milestone/8?closed=1

### v0.2.0 (May 2017)

 * Implemented LSP version 3.0
 * Support union of two types with the `Either` class
 * Support multiple parameters in protocol methods
 * Support custom error codes

Fixed issues: https://github.com/eclipse/lsp4j/milestone/7?closed=1

Breaking API changes:
 * Type of `ServerCapabilities.textDocumentSync` changed from `TextDocumentSyncKind` to `Either<TextDocumentSyncKind, TextDocumentSyncOptions>`
 * Type of `Hover.contents` changed from `List<String>` to `List<Either<String, MarkedString>>`

-----

### v0.1.2 (Mar. 2017)

Fixed issues: https://github.com/eclipse/lsp4j/milestone/6?closed=1

### v0.1.1 (Jan. 2017)

Fixed issues: https://github.com/eclipse/lsp4j/milestone/5?closed=1