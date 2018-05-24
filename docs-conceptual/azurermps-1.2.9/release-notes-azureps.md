---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: b42ad6f22f47e10c9190cf5a919f781375ff26f2
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/23/2018
---
# <a name="release-notes"></a>Sürüm notları

Azure PowerShell'in bu sürümünde yapılan değişikliklerin listesi aşağıda verilmiştir.

## <a name="version-129"></a>Sürüm 1.2.9

Bu Sürümdeki Değişiklikler

* AzureRm.AzureStackAdmin Modülü
    + Add-AzureRmResourceProviderRegistration cmdlet’inde Yönetici Azure resource manager ve kiracı azure resource manager bölünmesini desteklemek üzere değişiklik yapıldı. -ResourceManagerType adlı yeni bir parametre eklendi.
    + -AdminUri, -ApiVersion, -SubscriptionId ve -Token parametreleri her bir cmdlet’ten kaldırıldı. Bu parametrelerinin kullanımdan kaldırılacağı ile ilgili uyarılar yayınlanmıştı ve şimdi kaldırıldı.
* AzureStackStorage modülü
    + Kapsayıcı geçiş senaryolarını destekleyen yeni cmdlet’ler eklendi.
    + İç bileşenlere ve temel alınan özelliklere başvuran cmdlet'ler kaldırıldı.
* AzureRM.BootStrapper
    + Sürüm profilleri kullanılarak Azure PowerShell cmdlet’lerinin sürümlerini yönetmek için yeni modül oluşturuldu