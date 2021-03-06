---
title: "PredictVariance (DMX) | Microsoft Docs"
ms.custom: ""
ms.date: "03/02/2016"
ms.prod: analysis-services
ms.prod_service: "analysis-services"
ms.component: ""
ms.reviewer: ""
ms.suite: "pro-bi"
ms.technology: 
  
ms.component: data-mining
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
f1_keywords: 
  - "PredictVariance"
dev_langs: 
  - "DMX"
helpviewer_keywords: 
  - "PredictVariance function"
ms.assetid: 3c535237-083a-4102-bdfe-9f3c929e7b2c
caps.latest.revision: 34
author: "Minewiskan"
ms.author: "owend"
manager: "erikre"
---
# PredictVariance (DMX)
[!INCLUDE[ssas-appliesto-sqlas](../includes/ssas-appliesto-sqlas.md)]

  Returns the variance of a specified column.  
  
## Syntax  
  
```  
  
PredictVariance(<scalar column reference>)  
```  
  
## Applies To  
 A scalar column.  
  
## Return Type  
 A scalar value of the type that is specified by *\<scalar column reference>*.  
  
## Remarks  
 If the column reference is discrete, **PredictVariance** returns 0 because the variance cannot be calculated from discrete values.  
  
## Examples  
 The following example uses a natural prediction join to determine if an individual is likely to be a bike buyer based on the TM Decision Tree mining model, and also determines the variance for the prediction.  
  
```  
SELECT  
  [Bike Buyer],  
  PredictVariance([Bike Buyer]) AS [Variance]  
FROM  
  [TM Decision Tree]  
NATURAL PREDICTION JOIN  
(SELECT 28 AS [Age],  
  '2-5 Miles' AS [Commute Distance],  
  'Graduate Degree' AS [Education],  
  0 AS [Number Cars Owned],  
  0 AS [Number Children At Home]) AS t  
```  
  
## See Also  
 [Data Mining Extensions &#40;DMX&#41; Function Reference](../dmx/data-mining-extensions-dmx-function-reference.md)   
 [Functions &#40;DMX&#41;](../dmx/functions-dmx.md)   
 [General Prediction Functions &#40;DMX&#41;](../dmx/general-prediction-functions-dmx.md)  
  
  
