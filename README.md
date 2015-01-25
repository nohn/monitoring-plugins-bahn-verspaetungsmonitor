Monitoring Plugins Bahn Verspätungen
====================================

Check for Deutsche Bahn delays in Nagios/Icinga.

Based on https://bitbucket.org/thomasweinert/carica-status-monitor/ by
Thomas Weinert.

License:   The MIT License
           http://www.opensource.org/licenses/mit-license.php
Copyright: 2012-2013 Thomas Weinert <thomas@weinert.info>
Copyright: 2015      Sebastian Nohn <sebastian@nohn.net>

Usage
-----

check_bahn_verspaetung StationName ProductCode

    ProductCode = Trains Types to Display
       tailing zeros can  be skipped
       1 1 1 1 1 1 1 1
       | | | | | | | Trams
       | | | | | | | Metro Lines
       | | | | | | Ferries
       | | | | | Buses
       | | | | Commuter (S) Trains
       | | | Local Trains (RB + RE ...)
       | | Express (IR + D) Trains
       | InterCity (IC) Trains
       InterCityExpress (ICE) Trains

Example

    check_bahn_verspaetung "Bonn Hbf" 00111000