---
layout: post
title:  The beginning
date:   2017-05-04
categories: netjsonconfig
---

This year I got interested in a community network project called [Ninux][ninux-firenze] in Firenze. A community network is a networking project owned and run by a group of individuals instead of a company or association. The project goal is to be able to run networked applications (as the world wide web) on your network, extend the capabilities of software and make new friends.

The ideas behind are those of free software and the only way to realize them is by running your own hardware as there is no ISP that allows the kind of transparency that we are striving for.

So sometimes we climb on a roof and we try to install a ninux-node to get connectivity to Firenze's ninux island to some other participant. Using a mix of off the shelves hardware and open source tools we can bring connectivity as fast as 1Gbs, not bad!

Anyway this is how I got in touch with [Gabriele][gabri] who later convinced me to apply for a GSOC project with OpenWISP.

I had two projects I could choose from and I got interested more in adding a backend to [netjsonconfig][netjsonconfig].

Netjsonconfig provides a library and a command line interface to transform [NetJSON](https://netjson.org/rfc.html) into other format such as UCI blocks for OpenWRT/LEDE.

{% highlight json %}
{
  "interfaces": [
    {
      "name": "eth0",
      "addresses": [
        {
          "address": "192.168.1.1",
          "mask": 24,
          "family": "ipv4",
          "proto": "static",
        }
      ]
    }
  ]
}
{% endhighlight %}

So eventually this is how I got to work during summer on this project to add the first AirOS backend. But what is AirOS?

AirOS is the firmware distributed by Ubiquity on their long range WiFI devices and it comes with a web interface to configure things such as WiFi authentication, VLAN, networking and other services.

Is it also possible to upload a file containing the configuration from the web interface and this is where things become interesting.

This configuration file is easily readable and with some networking knowledges is possible to infer what state the device is in.

Here is an example to set the `eth0` interface to the static ip `192.168.1.1/24`

{% highlight ini %}
netconf.1.devname=eth0
netconf.1.ip=192.168.1.1
netconf.1.mask=255.255.255.0
{% endhighlight %}

The project goal is to be able to output this configuration file from an initial NetJSON configuration and then upload it to the device skipping the web interface.

This is important because community network projects rely on this kind of hardware to connect distant users, being able to control not only the routers but also the antennas would greatly simplify the management of this kind of network where users (and owners) have different level of abilities.

With this in mind the journey started and I had to find a device to test and sample configurations.

[ninux-firenze]: http://www.firenze.ninux.org/
[gabri]: https://github.com/gabri94
[netjsonconfig]: http://netjsonconfig.openwisp.org/en/stable/
