Sonic Go-CD Monitor
----------------------------------------
##### A Customised fork of Karmats Go-CD monitor
----------------------------------------

| Color        | State           |
| ------------- |-------------|
| Red | Failed |
| Green | Passing |
| Cyan with spinner | Running on a green build |
| Red with spinner | Running on a red build |
| BlueGrey | Paused, Cancelled |

![View](https://user-images.githubusercontent.com/17930002/61585251-1e433d80-ab4f-11e9-98e9-fff1e52cb672.png)

To Run
```
npm install
npm start
```
Go to `http://localhost:8080?admin` to configure or `http://localhost:8080`

To Push to CF:
```
npm install
cf push -f manifest-dev.yml -t 180
```

Change `app-config` for any changes
See Karmats Go-cd for info to configure

## Added Features/ Differences with Karmats Go-CD
- Indicative spinner for running builds
- Colorscheme is easy on the eyes
- Previous failed build distinguised with Red even if running
- No clutter
-- No Blame last commit
-- No passes infor for passed builds
-- Font size changes for big screens
-- No Sunny icons, only cloudy

## Configuration
Go to `http://localhost:8080?admin` and click the settings button in the bottom-right corner to open the configuration dialog.
* Sort Order - Sort pipelines by status or latest build time
* Filter Pipelines - Disable/enable pipelines to retrieve from go server. It's also possible to write a regex with the pipelines you want.

Maintainer: Joviano Dias ( jovez 10 at gmail dot com )