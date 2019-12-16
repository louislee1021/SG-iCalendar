# SG-iCalendar

Quick and Simple.        
When the INPUT with .ics extension is ready, PROCESS it with parser, and OUTPUT events one by one.

## Differentiation and ChangeLog 

20191216 10:23 - Updated Installation Command to include dev-master, get rid of stable minimum stability.        
20191216 08:38 - Added Installation.        
20191216 08:35 - The package name louis1021/SG-iCalendar is invalid, it should not contain uppercase characters. We suggest using louis1021/sg-i-calendar instead.        
20191216 08:34 - Packagist require the submission first.        
20191216 08:31 - Forget the FIRST Github webhook failure message for the connection to Packagist.        
20191216 07:55 - Updated the ultimate and the only uses of this package. End of this SG-iCalendar world.        
20191216 07:52 - Changed README into README.md.        
20191216 07:49 - Added composer.json with designated package name for conventional use.        
20191216 07:47 - PHP 5.6.38 compatible.        
20191216 07:45 - What? Yes. I forked.

## Installation

```bash
composer require louis1021/sg-i-calendar dev-master
```

## Overview

A simple and fast iCal parser.
-------------------------------------------------------------------------------

http://github.com/fangel/SG-iCalendar
With massive help from http://github.com/tpruvot/PHP-iCal
and http://github.com/xonev/SG-iCalendar
-------------------------------------------------------------------------------

A simple example :
 $ical = new SG_iCalReader( "./basic.ics" );
 //or
 $ical = new SG_iCalReader( "http://example.com/calendar.ics" );
 foreach( $ical->getEvents() As $event ) {
   // Do stuff with the event $event
 }

To check unit tests with phpunit, goto tests/ directory and :
 phpunit AllTests
 phpunit helpers/FreqTest

-------------------------------------------------------------------------------
CHANGELOG :
-------------------------------------------------------------------------------

current (31 oct 2010)
 + ical RDATE support (added dates in a range)
 + RDATE and EXDATE arrays support

0.7.0 (30 oct 2010)
 + ical EXDATE support (excluded dates in a range)
 + $event->isWholeDay()
 + getAllOccurrences() for repeated events
 + implemented a cache for repeated events

0.6.0 (29 oct 2010)
 + Added demo based on fullcalendar
 + Added duration unit tests
 + Support of Recurrent events in query Between()
 * various fixes on actual (5) issues

-------------------------------------------------------------------------------
TODO :
-------------------------------------------------------------------------------

These iCal keywords are not supported for the moment :
 - RECURRENCE-ID : to move one event from a recurrence
 - EXRULE : to exclude multiple days by a complex rule

Also, multiple RRULE could be specified for an event,
but that is not the case for most calendar applications

-------------------------------------------------------------------------------
To get more information about ical format and rules :
see http://www.ietf.org/rfc/rfc2445.txt
