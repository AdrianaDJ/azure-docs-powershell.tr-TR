---
title: Azure PowerShell Değişiklik Günlüğü | Microsoft Docs
description: Azure PowerShell'in en son sürümünde yapılan değişikliklerin geçmişi aşağıda verilmiştir.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: c57ba563b5a4d4d19944fe8eca2cb4244ee5ed9e
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819720"
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