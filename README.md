# EazyFlutter - Flutter Widget Wrappers & Snippets

EazyFlutter is a VS Code extension that enhances Flutter development by providing quick actions (bulb menu) and snippets to streamline common widget-wrapping tasks.

## Features

- **Wrap with Consumer<T>** - Quickly wrap a widget with `Consumer<T>` without manually typing the structure.
- **Auto Variable Naming** - Converts `ProviderType` to a lower camel case variable (e.g., `AppUserManagementProvider` → `appUserManagementProvider`).
- **Works via Quick Fix & Snippets** - Use **Cmd + .** (Mac) / **Ctrl + .** (Windows) or snippets for fast wrapping.
- **Snippets for Speed** - Type `wrapConsumer` + `Tab` to insert a `Consumer<T>` block instantly.

## Installation

1. Open **VS Code**.
2. Go to the **Extensions Marketplace** (`Cmd + Shift + X` / `Ctrl + Shift + X`).
3. Search for **"EazyFlutter"** and click **Install**.
4. You're ready to go.

## How to Use?

### Wrap Any Widget with `Consumer<T>` (Quick Fix)

- Hover over a widget.
- Press **`Cmd + .`** (Mac) / **`Ctrl + .`** (Windows).
- Click **"Wrap with Consumer<T>"** in the Quick Fix menu.
- Enter the **Provider Type**, and it automatically wraps the widget.

#### Example:
Before wrapping:
```dart
Text('Hello World')
```
After wrapping with **EazyFlutter**:
```dart
Consumer<AppUserManagementProvider>(
  builder: (context, appUserManagementProvider, _) {
    return Text('Hello World');
  },
)
```

### Use Snippets for Faster Wrapping

1. Type **`wrapConsumer`** inside your Dart file.
2. Press **Tab**, and it will generate:
```dart
Consumer<ProviderType>(
  builder: (context, provider, _) {
    return ChildWidget();
  },
)
```
3. Replace `ProviderType` with your actual provider (e.g., `AuthProvider`).

## Extension Settings

This extension currently does not require any additional settings.

## Known Issues

- None reported yet. If you find any issues, please report them in the repository.

## Release Notes

### 1.0.0

- Initial release with **"Wrap with Consumer<T>"** feature.
- **Quick Fix action** added to wrap widgets with a provider.
- **Auto camel case conversion** for provider variables.

## Additional Resources

- [Flutter Consumer Documentation](https://pub.dev/documentation/provider/latest/provider/Consumer-class.html)
- [VS Code Extension API](https://code.visualstudio.com/api)

