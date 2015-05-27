.. _c:serviceentity:

6. Service Entity (cfSrv)
=========================

The CERIF entity cfService *cfSrv* in the context of OpenAIRE can be used (a) to provide information for the CERIF-compliant system that exposes data to OpenAIRE in CERIF XML and (b) in relation to federated identifiers (e.g. for persons, projects, organisations), in particular to identify the service that has generated each federated identifier. Federated identifiers are linked with the corresponding service using cfSrv.FedId_Srv. Services are linked with organisations through cfSrv.cfOrgUnit_Srv.

Attributes
----------

Internal Identifier
^^^^^^^^^^^^^^^^^^^

(occurences: 1)

*cfSrv.cfSrvId*

Name
^^^^

(occurences: 1)

*cfSrv.cfName*

Relationship(s) with
--------------------

Organisation
^^^^^^^^^^^^

(occurences: 1)

*cfSrv.cfOrgUnit_Srv*

Applicable Vocabularies
"""""""""""""""""""""""

The range of allowed values is limited to the following controlled vocabulary:

* **Owner**

as defined in CERIF Semantics “Organisation Research Infrastructure Roles” scheme.

