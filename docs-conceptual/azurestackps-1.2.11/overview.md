---
title: Azure Stack PowerShell’e genel bakış | Microsoft Docs
description: Azure Stack PowerShell yükleme ve yapılandırmasına genel bakış.
author: SnehaGunda
manager: Byronr
ms.product: azure-stack
ms.service: powershell
ms.devlang: powershell
ms.topic: reference
ms.author: sngun
ms.manager: byronr
ms.openlocfilehash: f895992b4200f260189b3dbc541452e73a377b00
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/08/2018
---
# <a name="azure-stack-powershell"></a><span data-ttu-id="548fb-103">Azure Stack PowerShell</span><span class="sxs-lookup"><span data-stu-id="548fb-103">Azure Stack PowerShell</span></span>

<span data-ttu-id="548fb-104">Azure Stack aşağıdaki iki PowerShell modülünü gerektirir:</span><span class="sxs-lookup"><span data-stu-id="548fb-104">Azure Stack requires the following two PowerShell modules:</span></span>  

1. <span data-ttu-id="548fb-105">**2017-03-09-profile** API Sürüm Profili yüklenerek elde edilen Azure Stack ile uyumlu **AzureRM** modülü.</span><span class="sxs-lookup"><span data-stu-id="548fb-105">The Azure Stack compatible **AzureRM** module which is available by installing the **2017-03-09-profile** API Version Profile.</span></span> <span data-ttu-id="548fb-106">Bu profil kullanılarak yüklenen cmdlet’ler yalnızca Azure Stack operatörleri ve kullanıcıları tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="548fb-106">The cmdlets installed by using this profile can be used by Azure Stack operators and users.</span></span>

2. <span data-ttu-id="548fb-107">En güncel sürüm **AzureStack** modülünün **1.2.11** kurulumudur.</span><span class="sxs-lookup"><span data-stu-id="548fb-107">The most current version is the **1.2.11** install of the **AzureStack** module.</span></span> <span data-ttu-id="548fb-108">Bu modül kullanılarak yüklenen cmdlet’ler yalnızca Azure Stack operatörleri tarafından kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="548fb-108">The cmdlets installed by using this module can be used by Azure Stack operators only.</span></span> <span data-ttu-id="548fb-109">Operatörler teklif, plan, hizmet, fiyat teklifi, vb. yönetme gibi işlemleri bu modülün sağladığı PowerShell cmdlet’lerini kullanarak gerçekleştirebilir.</span><span class="sxs-lookup"><span data-stu-id="548fb-109">Operators can perform operations such as manage offers, plans, services, quotas, etc. by using the PowerShell cmdlets provided by this module.</span></span> <span data-ttu-id="548fb-110">Bu modülde mevcut olan PowerShell cmdlet’leri hakkında bilgi almak için [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) ve [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) Başvurusu içeriğine bakın.</span><span class="sxs-lookup"><span data-stu-id="548fb-110">To learn about the PowerShell cmdlets available in this module, see the [AzureStackAdmin](https://docs.microsoft.com/powershell/module/azurerm.azurestackadmin/?view=azurestackps-1.2.11#azurerm.azurestackadmin) and [AzureStackStorage](https://docs.microsoft.com/powershell/module/azurerm.azurestackstorage/?view=azurestackps-1.2.11#azurerm.azurestackstorage) Reference content.</span></span>

## <a name="next-steps"></a><span data-ttu-id="548fb-111">Sonraki Adımlar</span><span class="sxs-lookup"><span data-stu-id="548fb-111">Next Steps</span></span>

* [<span data-ttu-id="548fb-112">Azure Stack için PowerShell yükleme</span><span class="sxs-lookup"><span data-stu-id="548fb-112">Install PowerShell for Azure Stack</span></span>](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
* [<span data-ttu-id="548fb-113">PowerShell’i Azure Stack ile kullanmak üzere yapılandırma</span><span class="sxs-lookup"><span data-stu-id="548fb-113">Configure PowerShell for use with Azure Stack</span></span>](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-configure?view=azurestackps-1.2.9&toc=%2fpowershell%2fmodule%2ftoc.json%3fview%3dazurestackps-1.2.9&view=azurestackps-1.2.9)
