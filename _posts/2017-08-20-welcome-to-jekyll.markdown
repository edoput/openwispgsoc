---
layout: post
title:  The beginning
date:   2017-05-04
categories: netjsonconfig
---

This year I got interested in a community network project called [Ninux][ninux-firenze] in Firenze and this is how I got in touch with [Gabriele][gabri] who later convinced me to apply for a GSOC project with OpenWISP.

I had two projects I could choose from and I got interested more in adding a backend to [netjsonconfig][netjsonconfig].

This project provides a library and a command line interface to transform [NetJSON](https://netjson.org/rfc.html) into other format such as UCI blocks for OpenWRT/LEDE.

So eventually this is how I got to work during summer on this library to add the first AirOS backend.

AirOS is the firmware distributed by Ubiquity on their long range WiFI devices and it comes with a web interface to configure things such as WiFi authentication, VLAN, networking and other services.

Is it also possible to upload a file containing the configuration from the web interface and this is where things become interesting.

This configuration file is easily readable and with some networking knowledges is possible to infer what state the device is in.

The project goal is to be able to output this configuration file from an initial NetJSON configuration and then upload it to the device skipping the web interface.

With this in mind the journey started and I had to find a device to test and sample configurations.

[ninux-firenze]: http://www.firenze.ninux.org/
[gabri]: https://github.com/gabri94
[netjsonconfig]: http://netjsonconfig.openwisp.org/en/stable/
