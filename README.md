# cuckoo-hashtable

This is an implementation of the Cuckoo hashtable data structure designed by Pagh and Rodler in 2001, see--

http://www.it-c.dk/people/pagh/papers/cuckoo-undergrad.pdf

This hash algorithm guarantees worst-case constant time, since any one key hashes to only one of two buckets

I designed this implementation for use database-like use, which is why I included the following features--

  1.  The toString() override returns a string that is the ENTIRE hash table, formatted nicely, sort of mimicking DROP in SQL

  2.  getEntry() - returns a single entry in the table, kind of like DROP x CONTAINS n. The method takes the key of the object        you want, returns a STRING using the object's toString. It also uses the same lookup logic as contains().

  3.  HashEntry - this class is public, and it is intended to be used. But you cannot create your own instances of it--you can        only get info from an instance.

Thoughts and criticisms welcome -- its a work in progress -- free to any who wants it.
