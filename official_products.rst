Official Products
=================

SatDump supports decoding and processing certain official products from space and meteorological agencies.

.. note::
   This module is experimental and could contain bugs; users are encouraged to test and report any issues `on the GitHub <https://github.com/SatDump/SatDump/issues>`_.

All products must be decoded with the ``Data Stores/Archives Formats (NOAA/EUMETSAT/CMA/NASA), Experimental`` pipeline. 

List of supported products
--------------------------

EUMETSAT
~~~~~~~~

 ============================================================ ============ ============ ================================================================ ======================================= 
  Product                                                      Satellite    Instrument   Link                                                             Notes                                  
 ============================================================ ============ ============ ================================================================ ======================================= 
  High Rate SEVIRI Level 1.5 Image Data - MSG - 0 degree       MSG          SEVIRI       https://data.eumetsat.int/product/EO:EUM:DAT:MSG:HRSEVIRI        Open the `.nc` (native) file           
  High Rate SEVIRI Level 1.5 Image Data - MSG - Indian Ocean   MSG          SEVIRI       https://data.eumetsat.int/product/EO:EUM:DAT:MSG:HRSEVIRI-IODC   Open the `.nc` (native) file           
  Rapid Scan High Rate SEVIRI Level 1.5 Image Data - MSG       MSG          SEVIRI       https://data.eumetsat.int/product/EO:EUM:DAT:MSG:MSG15-RSS       Open the `.nc` (native) file           
  FCI Level 1c Normal Resolution Image Data - MTG - 0 degree   MTG          FCI          https://data.eumetsat.int/product/EO:EUM:DAT:0662                Open the ZIP file as downloaded (SIP)  
  FCI Level 1c High Resolution Image Data - MTG - 0 degree     MTG          FCI          https://data.eumetsat.int/product/EO:EUM:DAT:0665                Open the ZIP file as downloaded (SIP)  
  AVHRR Level 1B - Metop - Global                              Metop        AVHRR        https://data.eumetsat.int/product/EO:EUM:DAT:METOP:AVHRRL1       Open the `.nc` (native) file           
  IASI Level 1C - All Spectral Samples - Metop - Global        Metop        IASI         https://data.eumetsat.int/product/EO:EUM:DAT:METOP:IASIL1C-ALL   Open the `.nc` (native) file           
  AMSU-A Level 1B - Metop - Global                             Metop        AMSU-A       https://data.eumetsat.int/product/EO:EUM:DAT:METOP:AMSUL1        Open the `.nc` (native) file           
  MHS Level 1B - Metop - Global                                Metop        MHS          https://data.eumetsat.int/product/EO:EUM:DAT:METOP:MHSL1         Open the `.nc` (native) file           
  OLCI Level 1B Full Resolution - Sentinel-3                   Sentinel-3   OLCI         https://data.eumetsat.int/product/EO:EUM:DAT:0409                Open the ZIP file as downloaded (SIP)                                                                                                                                                                                                 
 ============================================================ ============ ============ ================================================================ ======================================= 

