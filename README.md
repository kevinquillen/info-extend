info-extend
===========

Info Extend module for Drupal 7 is an initial port of the Module Supports module for Drupal 6 by Dave Reid. 
Since the 7 port will implement/support more than a 'supports' directive, I am adapting the name of Info Extend for now so it's more clear.

Purpose
=======

info-extend allows developers to add new directives to their module info file to display on the module list page of the Drupal admin.

For example, in your module .info file:

suggests[] = override_node_options

Would add "Suggests: Override node options" under your module in the module list, similar to Requires: directive. Modules are linked to drupal.org project page.

Currently supported directives
==============================

* compliments[]
* suggests[]
* recommends[]
* breaks[]
* conflicts[]
* replaces[]
* enhances[]

Additional formats (planned)
==================

Special directives, like conflicts[] or breaks[], can also contain a pipe delimiter with a link after it. 

For example:

conflicts[] = views | http://drupal.org/node/1234567

Would show up as:

Conflicts with: Views (See Issue #1234567)

with the issue and issue number linked to the specific issue filed for the conflict.