======================
 Technical Description
======================
.. _`tech-description`:

To understand how Galera Cluster works you first need to understand database replication, both what it is and how it works.  That understanding in turn provides contexts for understanding what Galera does and why.

------------
Replication
------------

.. _`replication`:

Replication refers to the frequent copying of data from one server to another, distributing the content so that all the servers in the cluster share the same level of information.

.. toctree::
   :maxdepth: 2
	      
   introduction
   certificationbasedreplication

-------------
Architecture
-------------
.. _`architecture`:

How does Galera Cluster actually work?  Galera uses eager replication, where the nodes keep all other nodes in sync by updating all replicas in a single transaction.  When a transaction commits, all nodes have the same value through write-set replication over group communication.

.. toctree::
   :maxdepth: 2

   architecture
   isolationlevels
   statetransfer

----------
Management
----------
.. _`management`:

How does Galera Cluster maintain its state across many nodes?

.. toctree::
   :maxdepth: 2

   nodestates
   recovery
   weightedquorum
