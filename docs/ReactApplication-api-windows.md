---
id: reactapplication-api
title: ReactApplication
---

`ReactApplication` provides a base application class for use in applications that are entirely written in React Native. `ReactApplication` will load the React instance on launch of your app for you and provide accessors to your application's [`ReactInstanceSettings`](ReactInstanceSettings-api-windows.md) and [`ReactNativeHost`](ReactNativeHost-api-windows.md) to customize your React instance.

# Reference

## Properties

### `InstanceSettings`

```csharp
ReactInstanceSettings InstanceSettings { get; set; }
```

Provides access to your application's [`ReactInstanceSettings`](ReactInstanceSettings-api-windows.md).  Generally, changes to these settings will not take effect if the React instance is already loaded, unless the React instance is reloaded, so most settings should be set in your applications constructor.

### `PackageProviders`

```csharp
IVector<IReactPackageProvider> PackageProviders { get; }
```

Provides access to the list of `IReactPackageProvider`'s that the instance will use to provide native modules to the application. This can be used to register additional package providers, such as package providers from community modules. See [`ReactNativeHost`](ReactNativeHost-api-windows.md) for more information.

### `Host`

```csharp
ReactNativeHost Host { get; }
```

Access to the [`ReactNativeHost`](ReactNativeHost-api-windows.md) of your application.

### `UseDeveloperSupport`

```csharp
bool UseDeveloperSupport { get; set; }
```

Should the developer experience features such as the developer menu and `RedBox` be enabled.  See [`ReactInstanceSettings.UseDeveloperSupport`](ReactInstanceSettings-api-windows.md#usedevelopersupport).


### `JavaScriptMainModuleName`

```csharp
string JavaScriptMainModuleName { get; set; }
```

See [`ReactInstanceSettings.JavaScriptMainModuleName`](ReactInstanceSettings-api-windows.md#javascriptmainmodulename).


### `JavaScriptBundleFile`

```csharp
string JavaScriptBundleFile { get; set; }
```

See [`ReactInstanceSettings.JavaScriptBundleFile`](ReactInstanceSettings-api-windows.md#javascriptbundlefile).

<!-- // Copyright (c) Microsoft Corporation. All rights reserved.
// Licensed under the MIT License.

import "ReactNativeHost.idl";
import "ReactApplicationDelegate.idl";


namespace Microsoft.ReactNative {

  [webhosthidden]
  [default_interface]
  unsealed runtimeclass ReactApplication : XAML_NAMESPACE.Application {
    ReactApplication();

    ReactInstanceSettings InstanceSettings { get; set; };
    IVector<IReactPackageProvider> PackageProviders { get; };
    ReactNativeHost Host { get; };

    Boolean UseDeveloperSupport { get; set; };
    String JavaScriptMainModuleName { get; set; };
    String JavaScriptBundleFile { get; set; };
  }
} // namespace Microsoft.ReactNative
-->


