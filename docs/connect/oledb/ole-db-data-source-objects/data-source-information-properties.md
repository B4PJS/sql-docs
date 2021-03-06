---
title: "Data Source Information Properties | Microsoft Docs"
description: "Data Source information properties"
ms.custom: ""
ms.date: "03/26/2018"
ms.prod: sql
ms.prod_service: "database-engine, sql-database, sql-data-warehouse, pdw"
ms.component: "ole-db-data-source-objects"
ms.reviewer: ""
ms.suite: "sql"
ms.technology: connectivity
ms.tgt_pltfrm: ""
ms.topic: "reference"
helpviewer_keywords: 
  - "OLE DB Driver for SQL Server, data source properties"
  - "properties [OLE DB]"
  - "data source properties [OLE DB]"
  - "information properties [OLE DB]"
  - "OLE DB data source properties [OLE DB Driver for SQL Server]"
author: "pmasl"
ms.author: "Pedro.Lopes"
manager: craigg
---
# Data Source Information Properties
[!INCLUDE[appliesto-ss-asdb-asdw-pdw-md](../../../includes/appliesto-ss-asdb-asdw-pdw-md.md)]

  In the provider-specific property set DBPROPSET_SQLSERVERDATASOURCEINFO, the OLE DB Driver for SQL Server defines the following data source information properties.  
  
|Property ID|Description|  
|-----------------|-----------------|  
|SSPROP_COLUMNLEVELCOLLATION|Type: VT_BOOL<br /><br /> R/W: Read<br /><br /> Default: VARIANT_TRUE<br /><br /> Description: Used to determine if column collation is supported.<br /><br /> VARIANT_TRUE: Column level collation is supported.<br /><br /> VARIANT_FALSE: Column level collation is not supported.|  
|SSPROP_UNICODELCID|Type: VT_I4 R/W: Read<br /><br /> Description: Unicode locale ID.<br /><br /> This is the locale used for Unicode data sorting.|  
|SSPROP_UNICODECOMPARISONSTYLE|Type: VT_I4 R/W: Read<br /><br /> Description: Unicode comparison style.<br /><br /> The sorting options used for Unicode data sorting.|  
  
 In the provider-specific property set DBPROPSET_SQLSERVERSTREAM, the OLE DB Driver for SQL Server defines the following additional property.  
  
|Property ID|Description|  
|-----------------|-----------------|  
|SSPROP_STREAM_XMLROOT|Type: VT_BSTR R/W: Read/Write<br /><br /> Description: The result of a FOR XML query may not be a well-formed document. When this property is specified, the result of a ‘select … for XML’ query is wrapped in the root tag provided by this property to return a well formed XML document. If the query is executed in the browser it may cause the browser to display parser errors when loading the result. To avoid the error, SQL ISAPI supports the keyword ROOT. This keyword maps to SSPROP_STREAM_XMLROOT property.|  
  
## See Also  
 [Data Source Objects &#40;OLE DB&#41;](../../oledb/ole-db-data-source-objects/data-source-objects-ole-db.md)  
  
  
