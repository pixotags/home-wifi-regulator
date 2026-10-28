# Home Regulator

A self-built bandwidth regulator for household devices on NBN with Google Nest mesh.
A parent node (MacBook) throttles or restores each device's speed on demand,
without changing the router.

## How it (should) work
1. Each device runs a small agent that sends all its traffic through an
   always-on WireGuard tunnel to the parent node.
2. The parent node shapes each device's tunnel with pf + dummynet.
3. A parent sets a device to full speed, throttled, or paused, and the change
   applies within seconds.

## Why?

Why not?

## Status
Early development. The parent node comes first.