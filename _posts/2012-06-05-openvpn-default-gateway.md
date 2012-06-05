---
layout: post
title: "openvpn default gateway"
description: "how to set your openvpn connection as the default gateway"
category: howto
tags: [vpn]
---
{% include JB/setup %}

This is absurdly simple and yet I couldn't find a straight answer right away.

Problem: How-to route all my traffic through my openvpn connection ?

Stupid simple solution: Open your *client* connection config file and append:

    redirect-gateway def1

If you control the *server* you could also put that as a default for all client connections using:

    push "redirect-gateway def1"


ps: don't ask me wth is "def1".
