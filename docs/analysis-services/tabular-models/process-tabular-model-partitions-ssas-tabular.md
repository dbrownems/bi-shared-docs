---
title: "Process Analysis Services tabular model partitions | Microsoft Docs"
ms.date: 01/29/2020
ms.prod: sql
ms.technology: analysis-services
ms.custom: tabular-models
ms.topic: conceptual
ms.author: owend
ms.reviewer: owend
author: minewiskan
monikerRange: "asallproducts-allversions || azure-analysis-services-current || power-bi-premium-current || >= sql-analysis-services-2016"
---
# Process tabular model partitions

[!INCLUDE[ssas-appliesto-sqlas-all-aas-pbip](../../includes/ssas-appliesto-sqlas-all-aas-pbip.md)]
  Partitions divide a table into logical parts. Each partition can then be processed (Refreshed) independent of other partitions. The tasks in this topic describe how to process partitions in a model database by using the **Process Partitions** dialog box in [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)].  

## To process a partition  
  
1. In [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)], right-click on the table that has the partitions you want to process, and then click **Partitions**.  
  
1. In the **Partitions** dialog box, in **Partitions**, click on the Process button.  
  
1. In the **Process Partition(s)** dialog box, in the **Mode** listbox, select one of the following process modes:  

    |Mode|Description|  
    |----------|-----------------|  
    |**Process Default**|Detects the process state of a partition object, and performs processing necessary to deliver unprocessed or partially processed partition objects to a fully processed state. Data for empty tables and partitions is loaded; hierarchies, calculated columns, and relationships are built or rebuilt.|  
    |**Process Full**|Processes a partition object and all the objects that it contains. When Process Full is run for an object that has already been processed, [!INCLUDE[ssASnoversion](../../includes/ssasnoversion-md.md)] drops all data in the object, and then processes the object. This kind of processing is required when a structural change has been made to an object.|  
    |**Process Data**|Load data into a partition or a table without rebuilding hierarchies or relationships or recalculating calculated columns and measures.|  
    |**Process Clear**|Removes all data from a partition.|  
    |**Process Add**|Incrementally update partition with new data.|  
  
1. In the **Process** checkbox column, select the partitions you want to process with the selected mode, and then click **Ok**.  
  
## See also

[Tabular Model Partitions](../../analysis-services/tabular-models/tabular-model-partitions-ssas-tabular.md)   
[Create and Manage Tabular Model Partitions](../../analysis-services/tabular-models/create-and-manage-tabular-model-partitions-ssas-tabular.md)  