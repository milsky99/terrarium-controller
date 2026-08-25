# Terrarium Controller

ESP32 terrarium controller with misting, lighting, ventilation and a
capacitive water level probe. Runs standalone with its own web page, and
works with Home Assistant if you have it.

## First time setup

1. Power the unit on.
2. On a phone, join the WiFi network called **Terrarium Setup**. It has no
   password.
3. A setup page appears. Pick your home network and enter its password.
4. The unit reconnects on its own. Find it at `http://terrarium-xxxxxx.local`
   where the last part is printed on the unit, or look it up on your router.
5. If you run Home Assistant, it will offer to add the device automatically.

If the unit ever loses your WiFi, the Terrarium Setup network comes back so
you can point it at a new one.

## Updates

The unit checks this project for new firmware every six hours. When a new
version is available it appears as an update, either in Home Assistant or on
the unit's own web page.

## Releasing a new version

1. Edit `terrarium.yaml` and change `project_version` near the top.
2. Commit and push to `main`.
3. GitHub builds the firmware and publishes it. Existing units pick it up on
   their next check.

## One time repository setup

In the repository settings, under Pages, set the source to **GitHub Actions**.
Without this the build succeeds but nothing is published.
