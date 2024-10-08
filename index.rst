.. SatDump documentation master file, created by
   sphinx-quickstart on Sun Nov  5 10:35:15 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Welcome to SatDump's documentation!
===================================



What is SatDump?
================

SatDump is a general purpose satellite data processing software. It is a one-stop-shop that provides all the necessary stages to get from the satellite transmission to actual products.

Features
========

* Support of many SDRs such as RTL-SDR, Airspy, HackRF, BladeRF, LimeSDR, PlutoSDR, etc.
* Recording of radio basebands from your SDR
* Decoding and processing the data from over 90 different satellites and even space probes.
* Live decoding of supported satellite links such as APT, LRPT, HRPT, LRIT, HRIT and many more.
* Image and data decoding from satellites such as NOAA 15-18-19, Meteor-M, GOES, Elektro-L, Metop, FengYun, etc.
* Calibrated and georefrenced L1b products output on select satellites, such as Sea Surface Temperature, Microphysics, etc. ready to use for scientific applications such as numerical weather forecasts.
* Support for projecting the satellite imagery over a map, including layering with other instruments or satellites.
* Inmarsat Aero and STD-C EGC messages decoding.
* Scheduler and rotator control for automated satellite stations.
* Ingestor for automated geostationary weather satellites reception.

.. toctree::
   :caption: Documentation

   pipelines
   plugins
   sdr_options
   sat_tracker
   composites
   projections
   product_spec
   official_products
   faq_troubleshooting
   build_windows
   scripting
   autotrack

.. toctree::
   :caption: SatDump Links

   Website <https://www.satdump.org/>
   Download <https://www.satdump.org/download/>
