# Unhandled FormatException in Dart's jsonDecode

This repository demonstrates an example of an uncommon error in Dart, specifically an unhandled `FormatException` thrown by the `jsonDecode` function.  The `jsonDecode` function from the `dart:convert` library is used to parse JSON responses from APIs or other sources. If the input string isn't valid JSON, this function throws a `FormatException`.  This example shows how to properly handle such exceptions to prevent app crashes.

## Bug Report

The `bug.dart` file contains code that attempts to decode a JSON response without proper error handling.  If the API response is malformed or contains non-JSON data, this results in an unhandled exception and a crash.

## Solution

The `bugSolution.dart` file demonstrates the correct way to handle this situation using a `try-catch` block. This ensures that the application gracefully handles the error without crashing, possibly by displaying an error message or retrying the request.