---
title: Sık Sorulan Sorular (SSS)
description: Azure PowerShell hakkında Sık Sorulan Sorular.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/06/2020
ms.locfileid: "93407519"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Azure PowerShell hakkında sık sorulan sorular

## <a name="what-is-azure-powershell"></a>Azure PowerShell nedir?

Azure PowerShell, Azure kaynaklarını doğrudan PowerShell ile yönetmenizi sağlayan cmdlet’lerden oluşan bir kümedir. Aralık 2018’de Az PowerShell modülü genel kullanıma sunuldu. Günümüzde, Azure ile etkileşim kurmak için önerilen PowerShell modülüdür. Az PowerShell modülü hakkında daha fazla bilgi edinmek için bkz. [Yeni Azure PowerShell Az modülüne giriş](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Azure PowerShell’de hataya neden olan değişiklik uyarı iletilerini nasıl devre dışı bırakabilirim?

Azure PowerShell’de hataya neden olan değişiklik uyarı iletilerini engellemek için `SuppressAzurePowerShellBreakingChangeWarnings` olan ortam değişkenini `true` olarak ayarlamanız gerekir.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
