---
title: "Electronic Updates #1"
date: 2025-10-08
draft: false
---

## Software

We need to collect data from testing to improve the engine. This data will include thrust, mass flow, temperature, pressure, and vibration. To ensure safety, all this data will be collected by sensors and transmitted back to a computer, where it can be plotted in real time and exported after completion. There are several options for achieving this goal.

The electronics team confirmed that the Arduino serial plotter can have multiple data points, which means we don't need an additional ESP32 for data logging, saving costs.

![Data Record](/images/updates/103-data-record.png)

The test used the temperature sensor and successfully drew the image.

![Data Graph](/images/updates/103-data-graph.png)