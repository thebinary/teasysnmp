teasysnmp
=========

Extended easysnmp with helpers to work with snmp tables

teasysnmp Table
---------------

The teasysnmp extensions vastly depends on a custom teasysnmp data
structure that is referred to as the **"teasysnmp table"** in all
documentations and documentation strings as well as in the extended
function calls.

| To keep things simple and optimized, the datastructure is a simple
  tuple with 2 elements - the snmp table entry oid - dictionary with
  definition of fields
|  - field\_name: tuple of (field\_index str, easysnmp typestr)

An example is given below:

.. code:: python

    ifTableEntry = (
        ".1.3.6.1.2.1.2.2.1",
        {
            'Index': ('1', 'INTEGER'),
            'Descr': ('2', 'OCTETSTR'),
            'Type': ('3', 'INTEGER'),
            'MTU': ('4', 'INTEGER'),
        }
    )

The possible easysnmp typestr are:

+--------------------+
| Easysnmp Typestr   |
+====================+
| OBJECTID           |
+--------------------+
| OCTETSTR           |
+--------------------+
| INTEGER            |
+--------------------+
| INTEGER32          |
+--------------------+
| UNSIGNED32         |
+--------------------+
| NETADDR            |
+--------------------+
| IPADDR             |
+--------------------+
| COUNTER            |
+--------------------+
| GAUGE              |
+--------------------+
| TICKS              |
+--------------------+
| OPAQUE             |
+--------------------+
| COUNTER64          |
+--------------------+
| NULL               |
+--------------------+
| UINTEGER           |
+--------------------+
| NOTIF              |
+--------------------+
| BITS               |
+--------------------+
| TRAP               |
+--------------------+

Special Thanks To
=================

-  Contributors of
   `easysnmp <https://github.com/kamakazikamikaze/easysnmp.git>`__