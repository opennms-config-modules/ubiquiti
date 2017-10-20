# Ubiquiti

OpenNMS configuration for Ubiquiti AirMax 6

## Installation

.Download and install from GitHub
[source, bash]
----
cd $OPENNMS_HOME/etc/modules-available
git clone https://github.com/opennms-config-modules/ubiquiti.git
----

### Datacollection

.Install datacollection configuration
[source, bash]
----
cd $OPENNMS_HOME/etc/datacollection
ln -s ../modules-available/ubiquiti/datacollection/*.xml .
----

.Include in datacollection-config.xml
[source, xml]
----
<include-collection dataCollectionGroup="Ubiquiti"/>
----

### Graph report definitions

.Install graph report definitions
[source, bash]
----
cd $OPENNMS_HOME/etc/snmp-graph.properties.d
ln -s ../modules-available/ubiquiti/graphs/*.properties .
----

