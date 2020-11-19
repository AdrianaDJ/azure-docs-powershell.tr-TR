---
title: Sık Sorulan Sorular (SSS)
description: Azure PowerShell hakkında Sık Sorulan Sorular.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 10ed859f04fa29d866530af71c32819b256c882a
ms.sourcegitcommit: d81c3b0f0f7289104be03869eb675128b61db7d3
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 11/17/2020
ms.locfileid: "94715711"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="2a516-103">Azure PowerShell hakkında sık sorulan sorular</span><span class="sxs-lookup"><span data-stu-id="2a516-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="2a516-104">Azure PowerShell nedir?</span><span class="sxs-lookup"><span data-stu-id="2a516-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="2a516-105">Azure PowerShell, Azure kaynaklarını doğrudan PowerShell ile yönetmenizi sağlayan cmdlet’lerden oluşan bir kümedir.</span><span class="sxs-lookup"><span data-stu-id="2a516-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="2a516-106">Aralık 2018’de Az PowerShell modülü genel kullanıma sunuldu.</span><span class="sxs-lookup"><span data-stu-id="2a516-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="2a516-107">Günümüzde, Azure ile etkileşim kurmak için önerilen PowerShell modülüdür.</span><span class="sxs-lookup"><span data-stu-id="2a516-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="2a516-108">Az PowerShell modülü hakkında daha fazla bilgi edinmek için bkz. [Yeni Azure PowerShell Az modülüne giriş](/powershell/azure/new-azureps-module-az).</span><span class="sxs-lookup"><span data-stu-id="2a516-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="2a516-109">Azure PowerShell’de hataya neden olan değişiklik uyarı iletilerini nasıl devre dışı bırakabilirim?</span><span class="sxs-lookup"><span data-stu-id="2a516-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="2a516-110">Azure PowerShell’de hataya neden olan değişiklik uyarı iletilerini engellemek için `SuppressAzurePowerShellBreakingChangeWarnings` olan ortam değişkenini `true` olarak ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="2a516-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
