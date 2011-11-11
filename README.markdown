Nagios plugins to monitor Tomcat
================================

Nagios plugins that can be used to monitor Tomcat -- currently, heap / PermGen usage 
and frequency of garbage collections in a given time period. They use jstat to obtain 
this information from the JVM.

The plugins are written in Python and are based on the [nagiosplugin module][1], version 0.4.4.

The plugins can be easily adapted for other Java processes -- just substitute "Bootstrap"
appropriately. This should probably be made configurable, but doing this without
introducing a security hole requires some thought.

The plugins still need tidying up to better deal with exceptions (service not running, 
jstat not available, ...).

[1]: http://packages.python.org/nagiosplugin/index.html
