Audit trigger for postgres. Fork from [this repo](https://github.com/2ndQuadrant/audit-trigger) including a bunch of changes:

* converted from hstore to jsonb
* Add a function to stop auditing a table.
* Added option to not track insert statements.
* remove unused variables
* add pk to the table schema

Fork by hallvard-indgjerd:
* Moving deaudit_table to the audit schema
* Adding fields for actor (based on value in target_table.updated_by) as UUID
* Changing row_id to row_uuid with type UUID
* Adding jsonb fields old_data and new_data for use in a diff function