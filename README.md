# sap-hana-notes

Notes on SAP HANA. Short and to the point!

**Table of contents**

- [Changing Existing Tables](#changing-existing-tables)
- [Sample Procedures](#sample-procedures)

# Changing existing tables

[Complete Alter Table documentation](https://help.sap.com/viewer/4fe29514fd584807ac9f2a04f6754767/2.0.03/en-US/20d329a6751910149d5fdbc4800f92ff.html)

## Adding column to existing table

```
ALTER TABLE "SCHEMA_NAME"."TABLE_NAME" ADD (COLUMN_NAME VARCHAR(10));
```

# Sample procedures

## Sample delete procedure

```
PROCEDURE "SCHEMA_NAME"."PACKAGE_NAME::PROCEDURE_NAME" ( )
   LANGUAGE SQLSCRIPT
   SQL SECURITY INVOKER
   DEFAULT SCHEMA "SCHEMA_NAME"
   AS
BEGIN
   /*************************************
       COMMENT
   *************************************/
   declare variable_name integer := 1;
   
   DELETE FROM "TABLE" WHERE "COLUMN" < ADD_DAYS(CURRENT_TIMESTAMP, 1);
END
```
