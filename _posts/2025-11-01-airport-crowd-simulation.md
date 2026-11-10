---
layout: post
title: "Building Realistic Airport Crowd Simulation"
date: 2025-11-01
---

At Outsight, I worked on simulating realistic crowd behavior for airport environments. Unity's built-in pathfinding alone wasn't enough to capture the complexity of how people actually move and wait in airports.

## The Challenge

Real airport crowds don't just navigate from point A to point B—they form queues, switch between queues, wait for varying amounts of time, and organize themselves in different patterns depending on the situation. Standard pathfinding couldn't model this behavior.

## Building Agent Goals and Scenarios

To make the simulation realistic, I built a system of agent goals and scenarios based on real-life data. Each simulated person had goals that dictated their behavior: waiting times at specific locations, queue formation patterns (straight lines, zigzag configurations), and queue-switching logic when conditions changed.

The scenarios were informed by observations of actual airport behavior, which helped make the agents feel believable rather than mechanical.

## Real-Time Point-Cloud Capture

The simulation included real-time point-cloud capture that generated multiple frames, allowing us to visualize crowd density and movement patterns as they evolved. This was crucial for validating that the behavior matched expectations and for identifying issues early.

## LiDAR Sensor Validation

In a separate project on the LiDAR simulation tool, I worked on simulating sensor laser equations even when the manufacturer's exact equations weren't available. The approach involved validating simulated results against real LiDAR scans iteratively and tracking accuracy metrics to ensure the simulation stayed reliable.

For performance, I focused on importing large point clouds without causing heap spikes—using lazy loading, chunking data without losing precision, downloading over frames, and reducing bundle size to free runtime memory.

## Lessons Learned

The biggest takeaway was that realistic simulation requires understanding the real-world behavior you're modeling. No amount of pathfinding sophistication could replace the need to encode actual patterns like queue formation and switching behavior. Grounding the work in real-life data made all the difference.
