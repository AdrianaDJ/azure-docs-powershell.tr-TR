---
title: Sık Sorulan Sorular (SSS)
description: Azure PowerShell hakkında Sık Sorulan Sorular.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "92754032"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Azure PowerShell hakkında sık sorulan sorular

## <a name="what-is-azure-powershell"></a>Azure PowerShell nedir?

Azure PowerShell, Azure kaynaklarını doğrudan PowerShell ile yönetmenizi sağlayan cmdlet’lerden oluşan bir kümedir. Aralık 2018’de Az PowerShell modülü genel kullanıma sunuldu. Günümüzde, Azure ile etkileşim kurmak için önerilen PowerShell modülüdür. Az PowerShell modülü hakkında daha fazla bilgi edinmek için bkz. [Yeni Azure PowerShell Az modülüne giriş](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Azure PowerShell’de hataya neden olan değişiklik uyarı iletilerini nasıl devre dışı bırakabilirim?

Azure PowerShell’de hataya neden olan değişiklik uyarı iletilerini engellemek için `SuppressAzurePowerShellBreakingChangeWarnings` olan ortam değişkenini `true` olarak ayarlamanız gerekir.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
