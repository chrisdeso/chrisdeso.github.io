---
title: rtpscope
pitch: A WebRTC video call built end to end that steps its own quality down as the network degrades, and explains whose fault each drop was.
status: active
year: 2026
course: CS 4372
featured: true
order: 1
stack: [WebRTC, RTP, Python, JavaScript]
links:
  brief: /rtpscope/
---
A browser client plus a small Python signaling server. When the network gets
worse, rtpscope lowers video quality (1080p → 720p → 480p) and attributes each
drop to the sender's link, the receiver's link, jitter, or one of the machines.

**Milestones:** progress report Oct 28 · presentation Nov 23 · code + final report Dec 5.

