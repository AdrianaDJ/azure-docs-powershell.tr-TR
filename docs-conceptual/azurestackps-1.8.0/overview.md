---
title: Azure Stack Yönetici için PowerShell’e genel bakış | Microsoft Docs
description: Yükleme ve yapılandırma yönergeleriyle birlikte Azure Stack Yönetici için PowerShell’e genel bakış.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: ec406c80de6b457f7e340a23fe8caf2ab83be46a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 03/04/2020
ms.locfileid: "78264419"
---
# <a name="azure-stack-module-180"></a><span data-ttu-id="f5884-103">Azure Stack Modülü 1.8.0</span><span class="sxs-lookup"><span data-stu-id="f5884-103">Azure Stack Module 1.8.0</span></span>

## <a name="requirements"></a><span data-ttu-id="f5884-104">Gereksinimler:</span><span class="sxs-lookup"><span data-stu-id="f5884-104">Requirements:</span></span>

<span data-ttu-id="f5884-105">Desteklenen en düşük Azure Stack sürümü 1910’dur.</span><span class="sxs-lookup"><span data-stu-id="f5884-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="f5884-106">Not: Azure Stack'in önceki sürümleri için [Azure Stack PowerShell'i yükleme](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell) konusunu gözden geçirin</span><span class="sxs-lookup"><span data-stu-id="f5884-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="f5884-107">Yükleme</span><span class="sxs-lookup"><span data-stu-id="f5884-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a><span data-ttu-id="f5884-108">Sürüm Notları</span><span class="sxs-lookup"><span data-stu-id="f5884-108">Release Notes</span></span>

* <span data-ttu-id="f5884-109">1910 güncelleştirmesiyle desteklenir</span><span class="sxs-lookup"><span data-stu-id="f5884-109">Supported with 1910 update</span></span>
* <span data-ttu-id="f5884-110">Değişiklikler şunları içerir:</span><span class="sxs-lookup"><span data-stu-id="f5884-110">Changes include:</span></span>

    - <span data-ttu-id="f5884-111">**Yeni DRP Yönetici modülü**: Dağıtım Kaynak Sağlayıcısı (DRP), kaynak sağlayıcılarının Azure Stack Hub’a düzenlenmiş olarak dağıtılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="f5884-111">**New DRP Admin module**: The Deployment Resource Provider (DRP) enables orchestrated deployments of resource providers to Azure Stack Hub.</span></span> <span data-ttu-id="f5884-112">Bu komutlar, DRP ile etkileşimde bulunmak için Azure Resource Manager katmanıyla etkileşime geçer.</span><span class="sxs-lookup"><span data-stu-id="f5884-112">These commands interact with the Azure Resource Manager layer to interact with DRP.</span></span>

    - <span data-ttu-id="f5884-113">**BRP**:</span><span class="sxs-lookup"><span data-stu-id="f5884-113">**BRP**:</span></span>
        - <span data-ttu-id="f5884-114">Azure’ın yığın altyapısı yedeklemesine yönelik tek rolü geri yükleme desteği.</span><span class="sxs-lookup"><span data-stu-id="f5884-114">Support single role restore for Azures stack infrastructure backup.</span></span>
        - <span data-ttu-id="f5884-115">R`estore-AzsBackup` cmdlet’ine `RoleName` parametresi eklendi.</span><span class="sxs-lookup"><span data-stu-id="f5884-115">Add parameter `RoleName` to cmdlet R`estore-AzsBackup`.</span></span>

    - <span data-ttu-id="f5884-116">**FRP**: API sürümü 2019-05-01 ile **Sürücü** ve **Birim** kaynaklana yönelik önemli değişiklikler.</span><span class="sxs-lookup"><span data-stu-id="f5884-116">**FRP**: Breaking changes for **Drive** and **Volume** resources with API version 2019-05-01.</span></span> <span data-ttu-id="f5884-117">Bu özellikler Azure Stack Hub 1910 ve sonraki sürümlerinde desteklenir:</span><span class="sxs-lookup"><span data-stu-id="f5884-117">The features are supported by Azure Stack Hub 1910 and later:</span></span>
        - <span data-ttu-id="f5884-118">Kimlik, `Name`, `HealthStatus`ve `OperationalStatus` değerleri değiştirildi.</span><span class="sxs-lookup"><span data-stu-id="f5884-118">The value of ID, `Name`, `HealthStatus`, and `OperationalStatus` have been changed.</span></span>
        - <span data-ttu-id="f5884-119">**Sürücü** kaynakları için yeni `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` ve `StoragePool` özellikleri desteklenir.</span><span class="sxs-lookup"><span data-stu-id="f5884-119">Supported new properties `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer`, and `StoragePool` for **Drive** resources.</span></span>
        - <span data-ttu-id="f5884-120">**Sürücü** kaynakları için `CanPool` ve `CannotPoolReason` özellikleri kullanımdan kaldırıldı. Bunların yerine `OperationalStatus` kullanın.</span><span class="sxs-lookup"><span data-stu-id="f5884-120">The properties `CanPool` and `CannotPoolReason` of **Drive** resources have been deprecated; use `OperationalStatus` instead.</span></span>
