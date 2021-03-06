..  Copyright (C)  Brad Miller, David Ranum, and Jan Pearce
    This work is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by-nc-sa/4.0/.


Search Tree Operations
----------------------

Before we look at the implementation, let’s review the interface
provided by the map ADT. You will notice that this interface is very
similar to the C++ Hash Table.

-  ``Map()`` Create a new, empty map.

-  ``put(key,val)`` Add a new key-value pair to the map. If the key is
   already in the map then replace the old value with the new value.

-  ``get(key)`` Given a key, return the value stored in the map or
   ``NULL`` otherwise.

-  ``del`` Delete the key-value pair from the map using a statement of
   the form ``del map[key]``.

-  ``length()`` Return the number of key-value pairs stored in the map.
