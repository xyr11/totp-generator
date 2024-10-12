# TOTP Generator for Apps
*A time-based one-time password (TOTP) generator implementation in JavaScript*

[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)
[![GitHub Release](https://img.shields.io/github/v/release/xyr11/totp-generator)](https://github.com/xyr11/totp-generator/releases)
[![GitHub License](https://img.shields.io/github/license/xyr11/totp-generator)](https://github.com/xyr11/totp-generator/blob/main/LICENSE)

This project is a modified version of [russau's](https://jsfiddle.net/user/russau/fiddles/) [TOTP One-time password JSFiddle](https://jsfiddle.net/russau/ch8PK/) which fully works in the browser. It uses [QRious](https://github.com/neocotic/qrious) for QR code encoding and [jsSHA](https://github.com/Caligatio/jsSHA) for SHA-1 generation ([sha1.js v3.3.1](https://github.com/Caligatio/jsSHA/blob/8eac02756df4a86831bfb3f6a7a113fd36007aac/dist/sha1.js)).

## Usage
See it live: <https://xyr11.github.io/totp-generator/>

You can also download the latest version from the [Releases page](https://github.com/xyr11/totp-generator/releases) and open `index.html`.

### Query Strings

You can add query strings to automatically fill in the fields. They are based on the [OTP Key URI format](https://github.com/google/google-authenticator/wiki/Key-Uri-Format). The fields are:
Query field | Description | Example value
--- | --- | ---
label | String used to identify the account a key is associated with | `GitHub: email@site.com`
secret | Arbitrary key value encoded in Base32 | `ABCDE`
issuer | (Optional) The provider or service the key is associated with | `GitHub`

It also accepts [QRious options](https://github.com/neocotic/qrious/blob/master/README.md#api) (except `element` and `value`) to customize the QR code:

Query field | Description | Default value
--- | --- | ---
background | Background color of the QR code | `white`
backgroundAlpha | Background alpha of the QR code | `1.0`
foreground | Foreground color of the QR code | `black`
foregroundAlpha | Foreground alpha of the QR code | `1.0`
level | Error correction level of the QR code (L, M, Q, H) | `L`
mime | MIME type used to render the image for the QR code | `Image/png`
padding | Padding for the QR code (pixels) | None (auto)
size | Size of the QR code (pixels) | `200`

## License
The original code from JSFiddle doesn't have a license. QRious is licensed under the [GPL v3 License](https://www.gnu.org/licenses/gpl-3.0.en.html) and jsSHA is licensedd under the [3-Clause BSD license](https://github.com/Caligatio/jsSHA/blob/master/LICENSE).

This project is licensed under the [MIT License](https://github.com/xyr11/totp-generator/blob/main/LICENSE).
