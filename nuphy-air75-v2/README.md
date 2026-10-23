# Nuphy Air75 V2 Config

1. Official JSON file: https://nuphy.com/pages/json-files-for-nuphy-keyboards
2. Official Guide: https://nuphy.com/pages/via-usage-guide-for-nuphy-keyboards
3. Manual File: https://cdn.shopify.com/s/files/1/0268/7297/1373/files/NuPhy_Air75_V2_Quick_Guide.pdf?v=1696498123

## Connect but nothing happened

Check your productId via: 

```shell
lsusb | grep NuPhy
```

And I get `0x3265` and edit this value on `nuphy-air75-v2-via3.json`, you can use it directly

via: https://www.reddit.com/r/NuPhy/comments/1g4ejrn/nuphy_air_96_v2_not_connecting_on_via/


## Want to reset layout

If you change a lot of thing with keyboard, but want to go back default, If you never backup your layout, you only way is reset it by pressing `fn + [`

And you can use `nuphy_air75_v2.layout.default.json` directly


## Fn lock with Nuphy Air V2

Because VIA, Nuphy Air V2 not support Fn lcok, via: https://x.com/nuphystudio/status/1717718691440480481, Only way is change the layout.

You can use my customized layout `nuphy_air75_v2.layout.fn-lock.json` directly.
