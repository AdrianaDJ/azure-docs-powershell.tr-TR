---
title: Sık Sorulan Sorular (SSS)
description: Azure PowerShell hakkında Sık Sorulan Sorular.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.openlocfilehash: ac7a15121a19fa9c208163dad41b1aeed1981080
ms.sourcegitcommit: bd7edc4d48b6a8a8bec864edc876e16af0a49505
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/18/2020
ms.locfileid: "88513006"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Azure PowerShell hakkında sık sorulan sorular

## <a name="what-is-azure-powershell"></a>Azure PowerShell nedir?

Azure PowerShell, Azure kaynaklarını doğrudan PowerShell ile yönetmenizi sağlayan cmdlet’lerden oluşan bir kümedir. Aralık 2018’de Az PowerShell modülü genel kullanıma sunuldu. Günümüzde, Azure ile etkileşim kurmak için önerilen PowerShell modülüdür. Az PowerShell modülü hakkında daha fazla bilgi edinmek için bkz. [Yeni Azure PowerShell Az modülüne giriş](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Azure PowerShell’de hataya neden olan değişiklik uyarı iletilerini nasıl devre dışı bırakabilirim?

Azure PowerShell’de hataya neden olan değişiklik uyarı iletilerini engellemek için `SuppressAzurePowerShellBreakingChangeWarnings` olan ortam değişkenini `true` olarak ayarlamanız gerekir.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```