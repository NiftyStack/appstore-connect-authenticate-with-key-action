# appstore-connect-authenticate-with-key-action

To generate the base64 key content for the `base64-key-content`

> $ cat path_to_p8_file | base64 -b 0


```xml
jobs:

  build:
    runs-on: macos-11

    steps:
      - uses: actions/checkout@v2
      - uses: NiftyStack/appstore-connect-authenticate-with-key-action@1.0.0
        with:
          key-id: ${{ secrets.APPSTORE_CONNECT_KEY_ID }}
          issuer-id: ${{ secrets.APPSTORE_CONNECT_ISSUER_ID }}
          base64-key-content: ${{ secrets.APPSTORE_CONNECT_BASE64_KEY_CONTENT }}
```
