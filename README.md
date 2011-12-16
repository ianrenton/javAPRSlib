javAPRSlib
==========

javAPRSlib is a Java library to parse and create [APRS](http://www.aprs.org/)
packets. APRS (Automatic Packet Reporting System) is a digital amateur radio
mode used for broadcasting local tactical information, position tracking and
much more.

javAPRSlib is licensed under the GNU Lesser General Public License. The aim of
the library is to become an easy-to-use APRS backend both for open and for
closed APRS applications. If you are using javAPRSlib in your project, please
let us know and contribute patches, fixes and improvements.

Usage instructions
------------------

### When using `ant`

Just run `ant` from the project directory. The compiled library is located as
`bin/javAPRSlib.jar`.

### When using Eclipse

To be done.

### Examples

You can invoke the parser from the command line:

	$ PKT="DO1GL-5>APDR11,TCPIP*,qAC,T2SP:=5206.  N/01138.  E$ Georg APRSdroid http://aprsdroid.org/"
	$ java -classpath bin/javAPRSlib.jar net.ab0oo.aprs.parser.Parser $PKT
	Packet parsed as a T_UNSPECIFIED
	From:  DO1GL-5
	To:  APDR11
	Via: ,TCPIP*,qAC,T2SP
	DTI: =
	Valid?  true
	=5206.  N/01138.  E$Georg APRSdroid http://aprsdroid.org/


Features
--------

So far, the following APRS packet types can be decoded and encoded:

 * Position (standard, Mic-E, NMEA)
 * Object
 * Message

Further, it is possible to encode and decode the AX.25 MAC format.

Acknowledgement
---------------

The following people have contributed to javAPRSlib:

 * Matti Aarnio, OH2MQK (original java-aprs-fap code)
 * John Gorkos, AB0OO
 * Georg Lukas, DO1GL