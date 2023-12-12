<div align="center">
  <img alt="Statping-ng" src="https://raw.githubusercontent.com/dockur/statping-ng/dev/frontend/public/img/banner.png" style="max-width:100%;" width="256" />
</div>
<div align="center">

[![Build]][build_url]
[![Version]][tag_url]
[![Size]][tag_url]
[![Pulls]][hub_url]

</div>
</h1>

# Statping-ng
<p>An easy to use Status Page for your websites and applications. Statping will automatically fetch the application and render a beautiful status page with tons of features for you to build an even better status page. This Status Page generator allows you to use MySQL, Postgres, or SQLite on multiple operating systems.
</p>

## How to use

Via `docker-compose`

```yaml
version: "3"
services:
  statping:
    container_name: statping
    image: dockurr/statping:latest
    ports:
      - 8080:8080
    volumes:
      - /opt/statping:/app
    restart: always
    stop_grace_period: 1m
```

<hr/>
<h2 align="center" style="text-align:center">About Statping-ng</h2>

<img style="margin-right:10px;float:left;width:320px;height:235px;" align="left"  width="320" height="235" src="https://statping-ng.github.io/assets/external/statupsiterun.gif" />
<h3>A Future-Proof Status Page</h3>
<p>
  Statping-ng strives to remain future-proof and remain intact if a failure is created. Your Statping-ng service should not be running on the same instance you're trying to monitor. If your server crashes your Status Page should still remaining online to notify your users of downtime.
</p>
<div style="clear:both;"><br/><br/></div>


<h3>No Requirements - Run on Any Server</h3>
<p>
Statping-ng is built in Go Language so all you need is the pre-compiled binary based on your operating system. You won't need to install anything extra once you have the Statping binary installed. Windows, Linux or Mac, We compile to all the popular systems, including Raspberry Pi!
</p>
<p align="center" style="text-align:center">
<a href="https://github.com/statping-ng/statping-ng/wiki/Linux"><img alt="Linux" src="https://statping-ng.github.io/assets/external/linux.png" style="width:5%;margin-right:5px;" width=5% /></a>
<a href="https://github.com/statping-ng/statping-ng/wiki/Windows"><img alt="Windows" src="https://statping-ng.github.io/assets/external/windows.png" style="width:5%;margin-right:5px;" width=5% /></a>
<a href="https://github.com/statping-ng/statping-ng/wiki/Mac"><img alt="Apple Mac" src="https://statping-ng.github.io/assets/external/apple.png" style="width:5%;margin-right:5px;" width=5% /></a>
<a href="https://github.com/statping-ng/statping-ng/wiki/Docker"><img alt="Containers" src="https://statping-ng.github.io/assets/external/dockericon.png" style="width:5%;margin-right:5px;" width=5% /></a>
<a href="https://statping-ng.github.io/assets/external/android.png)](https://play.google.com/store/apps/details?id=com.statping"><img alt="Android Play Store" src="https://statping-ng.github.io/assets/external/android.png" style="width:5%;margin-right:5px;" width=5% /></a>
<a href="https://itunes.apple.com/us/app/apple-store/id1445513219"><img alt="Apple Apps Store" src="https://statping-ng.github.io/assets/external/appstore.png" style="width:5%;margin-right:5px;" width=5% /></a>
</p>
<br/>
<div style="clear:both;"><br/><br/></div>


<img style="margin-left:10px;float:right;width:320px;height:235px;" align="right" width="320" height="235" src="https://statping-ng.github.io/assets/external/slack-notifer.png" />
<h3>Lightweight and Fast</h3>
<p>
Statping-ng is a very lightweight application and is available for Linux, Mac, and Windows. The Docker image is only ~20Mb so you know that this application won't be filling up your hard drive space.
The Status binary for all other OS's is ~17Mb at most.
</p>
<div style="clear:both;"><br/><br/><br/></div>


<h3>Want easy containers?</h3>
<p>
No Worries, we provide docker containers for many different system architectures, with multiple docker-compose files to suit your needs, you can even bring your own SSL Certificate or automatically leverage <a href="https://letsencrypt.org/">Lets Encrypt</a> to keep things secure. But it's can be as simple as a docker run!
</p>
<div style="clear:both;"><br/><br/></div>


<img style="margin-left:10px;float:right;width:320px;height:235px;" align="right" width="320" height="235" src="https://statping-ng.github.io/assets/external/statping_theme.gif" />
<h3>Custom SASS Styling</h3>
Statping-ng will allow you to completely customize your Status Page using SASS styling with easy to use variables. The container image actually contains a pre-built SASS binary so you won't even need to setup anything!
<div style="clear:both;"><br/><br/><br/></div>


<img style="margin-right:10px;float:left;width:320px;height:235px;" align="left" width="320" height="235" src="https://statping-ng.github.io/assets/external/statping_iphone_bk.png" />
<h3>Compatible with the Statping App</h3>
<p>
Statping-ng is 100% compatible with the statping app which is available on the Apple App Store and Google Play for free. The app will allow you to view services, receive notifications when a service is offline, update groups, users, services, messages, and more! Start your own Statping-ng server and then connect it to the app by scanning the QR code in settings.</p>
<p align="center" style="text-align:center">
<a href="https://play.google.com/store/apps/details?id=com.statping"><img src="https://statping-ng.github.io/assets/external/google-play.svg"></a>
<a href="https://itunes.apple.com/us/app/apple-store/id1445513219"><img src="https://statping-ng.github.io/assets/external/app-store-badge.svg"></a>
</p>
<p align="center" style="text-align:center"><small>The mobile app is not maintained by statping-ng and includes in-app purchases to the developer of statping.</small></p>
<div style="clear:both;"><br/><br/></div>

<h3>Notifications - Slack, Email, Twilio and more</h3>
<p>Statping-ng includes email notification via SMTP and Slack integration using <a href="https://api.slack.com/incoming-webhooks">Incoming Webhook</a>. Insert the webhook URL into the Settings page in Statping-ng and enable the Slack integration. Anytime a service fails, the channel that you specified on Slack will receive a message.</p>
<p>View the <a href="https://github.com/statping-ng/statping-ng/wiki/Statping-Plugins">Plugin Wiki</a> to see detailed information about Golang Plugins. Statping-ng isn't just another Status Page for your applications, it's a framework that allows you to create your own plugins to interact with every element of your status page. <a href="https://github.com/statping-ng/statping-ng/wiki/Notifiers">Notifier's</a> can also be create with only 1 golang file.</p>
<div style="clear:both;"><br/><br/><br/></div>


<img style="margin-left:10px;float:right;width:320px;height:235px;" width="320" height="235" align="right" src="https://statping-ng.github.io/assets/external/statping_settings.gif" />
<h2>Easy to use Dashboard</h2>
<p>
Having a straight forward dashboard makes Statping-ng that much better. Quickly and Easy view statuses. Monitor your websites and applications with a basic HTTP GET request, or add a POST request with your own JSON to post to the endpoint.</p>
<div style="clear:both;"><br/><br/><br/><br/></div>


<img style="margin:35px 0;width:100%;height:250px;" align="center" width="100%" height="250" src="https://statping-ng.github.io/assets/external/statupsc2.png" />

[build_url]: https://github.com/dockur/statping/
[hub_url]: https://hub.docker.com/r/dockurr/statping/
[tag_url]: https://hub.docker.com/r/dockurr/statping/tags

[Build]: https://github.com/dockur/statping/actions/workflows/builder.yml/badge.svg
[Size]: https://img.shields.io/docker/image-size/dockurr/statping/latest?color=066da5&label=size
[Pulls]: https://img.shields.io/docker/pulls/dockurr/statping.svg?style=flat&label=pulls&logo=docker
[Version]: https://img.shields.io/docker/v/dockurr/statping/latest?arch=amd64&sort=semver&color=066da5
