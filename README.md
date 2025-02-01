# Expo Image Component - Silent Failure to Load Local Images with Incorrect URIs

This repository demonstrates a common but difficult-to-debug issue with Expo's `Image` component:  the silent failure to load local images when the URI is incorrectly formatted.  The problem is that there are no obvious console errors, making it harder to identify the root cause.

## Problem

The `Image` component fails to render images when provided with an incorrectly formatted local file URI.  This typically occurs when the `file://` prefix is missing.

## Solution

Ensure that the URI you provide to the `Image` component's `source` prop begins with `file:///` and accurately reflects the path to your image on the device.

## Setup

1. Clone this repository.
2. Install the dependencies: `npm install` or `yarn install`.
3. Run the app: `expo start`