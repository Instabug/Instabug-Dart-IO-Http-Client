An add-on package to [`instabug_flutter`](https://pub.dev/packages/instabug_flutter).

This package intercepts any requests performed using the dart:io package `HttpClient`  
and attaches them to the report that will be sent to Instabug dashboard.

## Usage

To enable network logging, use the custom Instabug client:

```dart
final client = InstabugCustomHttpClient();
```

and continue to use the package normally to make your network requests:

```dart
final request = await client.getUrl(Uri.parse(URL));
final response = await request.close();
```
