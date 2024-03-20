# CPOSC 2024: Getting Started with Meshtastic

## About

This repository contains the information and details related to
the CPOSC 2024 talk:

**Getting Started with Meshtastic**

This talk is targeted at beginners and long-time licensed ham radio operator
audiences alike, aimed to provide a high-level overview of the relatively new
ecosystem of devices which can be used to inexpensively, easily, and securely
communicate over long distances.
The talk will focus on Meshtastic, a free and open source Long Range
communication protocol used by inexpensive devices, considered the
next-generation of LoRaWAN communication, making it easy to send data and text
over long distances.


This code is hosted on both [GitHub](https://github.com/tomswartz07/CPOSC2024)
and [GitLab](https://gitlab.com/tom.swartz07/CPOSC2024).

## Learning Objectives

The ideal audience member is someone who is interested in LoRa/mesh networks,
has the desire to send data over long distances, or is interested in collaborating
with a long range local area mesh network.

The talk covers a number of topics and common confusion points for those
who are getting started with Meshtastic.

- Infrastructure-less communications
- Digital Security Concerns
- Creation of your own, custom sensor devices
- Central management of multiple Meshtastic devices/platforms

## Session Outline
- Introduction
  - Brief explanation on current state of various LoRa protocols
  - Overview of Meshtastic devices/software
- Meshtastic Software in Detail
  - Architecture and Design of Home Assistant
  - Overview of sub-protocols, long range modes vs short range modes
  - Network Security/Encryption vs Amateur Radio modes
- Meshtastic Hardware in Detail
  - Various Open Source Hardware examples
- Making Custom Meshtastic Sensors
  - Custom Temperature Sensors
  - Integration with existing Internet-of-Things devices and Services

## Expectations for Attendees

Attendees will gain knowledge necessary to install/deploy Meshtastic devices and
learn how to use these devices to connect to a local area mesh network.
Attendees will leave confident that they could deploy a device capable of connecting
to a Lancaster-area Meshtastic network.

## Files in this Repository:

- `presentation/cposc2024.tex`: LaTeX Beamer presentation files

## Making the presentation

### Option 1: Docker
Assuming you have Docker installed, you can simply run the following:

```sh
cd presentation
docker build -t latex:latest .
docker run --rm -v $(pwd):/data latex:latest make all
```

The PDF will be generated by the docker container and placed in the local directory

### Option 2: Direct LaTeX
Assuming you have `pdflatex` installed, or TeXLive
simply run the following command:

```sh
cd presentation
pdflatex cposc2024.tex
```

The PDF document will be generated and viewable for you.


## External Resources

There are a number of projects and external resources which were referenced in this
presentation.
They can be found here:

- [Home Assistant](https://www.home-assistant.io/)
- [ESPHome](https://www.esphome.io/)
