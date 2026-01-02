# Java Addon

This addon allows you to run a Java JAR file inside Home Assistant. Simply place your JAR in the `apps` folder inside the addon config directory, and name it `app.jar`.

## Usage

1. **Prepare your app:**
    - Build or obtain a JAR file compatible with **Java 17**.
    - Name the file `app.jar`.
2. **Place the file:**
    - Copy `app.jar` to the `apps` folder in the addon configuration directory.
3. **Start the addon:**
    - When started, the addon will automatically run `app.jar` using Java 17.
4. **Replace the jar and restart the addon:**
    - When your project has changed, you just put your new version of the jar and restart the addon.

> **Note:** Only Java 17 is supported. Your Java app will only run once unless it keeps itself alive. No custom parameters can be passed from the addon configuration; use `SUPERVISOR_TOKEN` for Supervisor API access.

## Motivation

This addon was created because there was no existing solution for running Java applications in Home Assistant. For users who rely on Java for various tasks, this provides a simple way to integrate Java apps.

## Compliance & Contributions

- The addon is compliant with Home Assistant addon standards, but minimal time is invested in its development.
- Suggestions and improvements are welcome! Feel free to fork or submit a pull request.

## Supported platforms

![aarch64-shield]
![amd64-shield]

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
