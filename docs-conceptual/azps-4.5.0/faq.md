---
title: Sık Sorulan Sorular (SSS)
description: Azure PowerShell hakkında Sık Sorulan Sorular.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: 2f1e3c275626fba1c4275cae8ef1d13b11f55735
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/04/2020
ms.locfileid: "89449951"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a><span data-ttu-id="5a370-103">Azure PowerShell hakkında sık sorulan sorular</span><span class="sxs-lookup"><span data-stu-id="5a370-103">Frequently asked questions about Azure PowerShell</span></span>

## <a name="what-is-azure-powershell"></a><span data-ttu-id="5a370-104">Azure PowerShell nedir?</span><span class="sxs-lookup"><span data-stu-id="5a370-104">What is Azure PowerShell?</span></span>

<span data-ttu-id="5a370-105">Azure PowerShell, Azure kaynaklarını doğrudan PowerShell ile yönetmenizi sağlayan cmdlet’lerden oluşan bir kümedir.</span><span class="sxs-lookup"><span data-stu-id="5a370-105">Azure PowerShell is a set of cmdlets that allows you to manage Azure resources directly with PowerShell.</span></span> <span data-ttu-id="5a370-106">Aralık 2018’de Az PowerShell modülü genel kullanıma sunuldu.</span><span class="sxs-lookup"><span data-stu-id="5a370-106">In December 2018, the Az PowerShell module became generally available.</span></span> <span data-ttu-id="5a370-107">Günümüzde, Azure ile etkileşim kurmak için önerilen PowerShell modülüdür.</span><span class="sxs-lookup"><span data-stu-id="5a370-107">It's now the recommended PowerShell module for interacting with Azure.</span></span> <span data-ttu-id="5a370-108">Az PowerShell modülü hakkında daha fazla bilgi edinmek için bkz. [Yeni Azure PowerShell Az modülüne giriş](/powershell/azure/new-azureps-module-az).</span><span class="sxs-lookup"><span data-stu-id="5a370-108">To learn more about the Az PowerShell module, see [Introducing the new Azure PowerShell Az module](/powershell/azure/new-azureps-module-az).</span></span>

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a><span data-ttu-id="5a370-109">Azure PowerShell’de hataya neden olan değişiklik uyarı iletilerini nasıl devre dışı bırakabilirim?</span><span class="sxs-lookup"><span data-stu-id="5a370-109">How do I disable breaking change warning messages in Azure PowerShell?</span></span>

<span data-ttu-id="5a370-110">Azure PowerShell’de hataya neden olan değişiklik uyarı iletilerini engellemek için `SuppressAzurePowerShellBreakingChangeWarnings` olan ortam değişkenini `true` olarak ayarlamanız gerekir.</span><span class="sxs-lookup"><span data-stu-id="5a370-110">To suppress the breaking change warning messages in Azure PowerShell, you'll need to set the environment variable `SuppressAzurePowerShellBreakingChangeWarnings` to `true`.</span></span>

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
