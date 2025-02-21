---
title: Use the one-click table batching policy wizard to change the ingestion batching policy for a table in Azure Data Explorer.
description: In this article, you learn how to change a table's ingestion batching policy using the one-click experience.
author: orspod
ms.author: orspodek
ms.reviewer: tzgitlin
ms.service: data-explorer
ms.topic: how-to
ms.date: 01/02/2022
---
# Create a table's ingestion batching policy with one-click

During the ingestion process, throughput is optimized by batching small ingress data chunks together before ingestion. The  [ingestion batching policy](kusto/management/batchingpolicy.md) defines data aggregation for batching.
In this article, you can define and assign an ingestion batching policy for a table using the one-click experience.

## Prerequisites

* An Azure subscription. Create a [free Azure account](https://azure.microsoft.com/free/).
* Create [a cluster and database](create-cluster-database-portal.md).

## Define and assign a table batching policy

1. In the left menu of the [Web UI](https://dataexplorer.azure.com/), select the **Data** tab, [or use the one-click link](https://dataexplorer.azure.com/oneclick). 

    :::image type="content" source="media/one-click-table-policies/one-click-batch-policy-start.png" alt-text="Select one-click table batching ingestion policy update in the web UI.":::

1. In the **Table batching policy** tile, select **Update**. 

    The **Table batching policy** window opens with the **Policy update** tab selected.

### Policy update
 
:::image type="content" source="media/one-click-table-policies/table-batch-policy-update.png" alt-text="Screen shot of Update table retention policy window. Cluster, Database, Table and Policy fields must be filled out before proceeding to Update.":::

1. The **Cluster** and **Database** fields are auto-populated. You may select a different cluster or database from the drop-down menus, or add a cluster connection.

1. Under **Table**, select a table from the drop-down menus.  

1. Under **Inherit values from database**, toggle **On** to apply the batching policy values from the database to the table. To create or update a separate policy for the table, toggle to **Off**.

1. If you selected **Off**, you can fill in the following fields to define the table batching policy:

    |**Setting** | **Default value** | **Field description**
    |---|---|---|
    | Number of items | *500*  | Batch file number limit. |
    | Time (seconds) |  *10* | Batching time limit.  |
    | Size (MB) |  *1024* | Batch size limit.  |

1. Select **Update**.

## Summary

In the **Summary** tab, all steps will be marked with green check marks when the update finishes successfully. The tiles below these steps give you options to explore your data with **Quick queries**, or undo changes made using **Tools**.

:::image type="content" source="media/one-click-table-policies/batch-policy-success.png" alt-text="Screenshot of final screen in the update table batching policy wizard for Azure Data Explorer with the one-click experience.":::

## Next steps

* [Query data in Azure Data Explorer Web UI](web-query-data.md)
* [Write queries for Azure Data Explorer using Kusto Query Language](write-queries.md)