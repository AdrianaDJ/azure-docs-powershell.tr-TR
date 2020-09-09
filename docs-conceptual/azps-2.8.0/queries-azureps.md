---
title: Azure PowerShell cmdlet'lerinin çıkışını sorgulama
description: Azure’daki kaynakları sorgulama ve sonuçları biçimlendirme.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2754df5132ca9d528217fa5caad95b7f59cc8215
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89240905"
---
# <a name="query-output-of-azure-powershell"></a><span data-ttu-id="c952d-103">Azure PowerShell'in çıkışını sorgulama</span><span class="sxs-lookup"><span data-stu-id="c952d-103">Query output of Azure PowerShell</span></span> 

<span data-ttu-id="c952d-104">Tüm Azure PowerShell cmdlet'lerinin sonuçları birer Azure PowerShell nesnesidir.</span><span class="sxs-lookup"><span data-stu-id="c952d-104">The results of each Azure PowerShell cmdlet are an Azure PowerShell object.</span></span> <span data-ttu-id="c952d-105">Açıkça `Get-` işlemleri olmayan cmdlet'ler bile, oluşturulmuş veya değiştirilmiş olan kaynak hakkında bilgi vermek için incelenebilecek bir değer döndürür.</span><span class="sxs-lookup"><span data-stu-id="c952d-105">Even cmdlets that aren't explicitly `Get-` operations might return a value that can be inspected, to give information about a resource that was created or modified.</span></span> <span data-ttu-id="c952d-106">Cmdlet'lerin çoğu tek bir nesne döndürse de, bazıları yinelenmesi gereken bir dizi döndürür.</span><span class="sxs-lookup"><span data-stu-id="c952d-106">While most cmdlets return a single object, some return an array that should be iterated through.</span></span>

<span data-ttu-id="c952d-107">Çoğu durumda sorgunuz Azure PowerShell'den [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet'iyle (çoğunlukla `select` olarak kısaltılmıştır) çıkış sağlar.</span><span class="sxs-lookup"><span data-stu-id="c952d-107">In almost all cases, you query output from Azure PowerShell with the [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet, often abbreviated to `select`.</span></span> <span data-ttu-id="c952d-108">Çıkış [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) ile veya bunun `where` diğer adıyla filtrelenebilir.</span><span class="sxs-lookup"><span data-stu-id="c952d-108">Output can be filtered with [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object), or its alias `where`.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="c952d-109">Basit özellikleri seçme</span><span class="sxs-lookup"><span data-stu-id="c952d-109">Select simple properties</span></span>

<span data-ttu-id="c952d-110">Varsayılan tablo biçiminde, Azure PowerShell cmdlet'leri tüm kullanılabilir özelliklerini görüntülemez.</span><span class="sxs-lookup"><span data-stu-id="c952d-110">In the default table format, Azure PowerShell cmdlets don't display all of their available properties.</span></span> <span data-ttu-id="c952d-111">Tüm özellikleri almak için [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet'ini kullanabilir veya çıkışı `Select-Object *` cmdlet'ine yönlendirebilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="c952d-111">You can get the full properties by using the [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet, or by piping output to `Select-Object *`:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object *
```

```output
ResourceGroupName        : TESTGROUP
Id                       : /subscriptions/711d8ed1-b888-4c52-8ab9-66f07b87eb6b/resourceGroups/TESTGROUP/providers/Micro
                           soft.Compute/virtualMachines/TestVM
VmId                     : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
Name                     : TestVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
LicenseType              :
Tags                     : {}
AvailabilitySetReference :
DiagnosticsProfile       :
Extensions               : {}
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
Plan                     :
ProvisioningState        : Succeeded
StorageProfile           : Microsoft.Azure.Management.Compute.Models.StorageProfile
DisplayHint              : Compact
Identity                 :
Zones                    : {}
FullyQualifiedDomainName :
AdditionalCapabilities   :
RequestId                : 711d8ed1-b888-4c52-8ab9-66f07b87eb6b
StatusCode               : OK
```

<span data-ttu-id="c952d-112">İlgilendiğiniz özelliklerin adını öğrendikten sonra, bu özellik adlarını `Select-Object` ile kullanarak bunları doğrudan alabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="c952d-112">Once you know the names of the properties that you're interested in, you can use those property names with `Select-Object` to get them directly:</span></span>

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

<span data-ttu-id="c952d-113">`Select-Object` kullanılarak alınan çıkış her zaman istenen bilgileri görüntüleyecek şekilde biçimlendirilir.</span><span class="sxs-lookup"><span data-stu-id="c952d-113">Output from using `Select-Object` is always formatted to display the requested information.</span></span> <span data-ttu-id="c952d-114">Cmdlet sonuçlarını sorgulama kapsamında biçimlendirmeyi kullanmayı öğrenmek için bkz. [Azure PowerShell cmdlet'inin çıkışını biçimlendirme](formatting-output.md).</span><span class="sxs-lookup"><span data-stu-id="c952d-114">To learn about using formatting as part of querying cmdlet results, see [Format Azure PowerShell cmdlet output](formatting-output.md).</span></span>

## <a name="select-nested-properties"></a><span data-ttu-id="c952d-115">İç içe özellikleri seçme</span><span class="sxs-lookup"><span data-stu-id="c952d-115">Select nested properties</span></span>

<span data-ttu-id="c952d-116">Azure PowerShell cmdlet'inin çıkışındaki bazı özellikler (`Get-AzVM` çıkışının `StorageProfile` özelliği gibi) iç içe nesneler kullanır.</span><span class="sxs-lookup"><span data-stu-id="c952d-116">Some properties in Azure PowerShell cmdlet output use nested objects, like the `StorageProfile` property of `Get-AzVM` output.</span></span> <span data-ttu-id="c952d-117">İç içe özellikten bir değer almak için, `Select-Object` cmdlet'inde dictionary bağımsız değişkeninin parçası olarak incelemek istediğiniz değerin görünen adını ve tam yolunu sağlayın:</span><span class="sxs-lookup"><span data-stu-id="c952d-117">To get a value from a nested property, provide a display name and the full path to the value you want to inspect as part of a dictionary argument to `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Select-Object Name,@{Name="OSType"; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name     OSType
----     ------
TestVM    Linux
TestVM2   Linux
WinVM   Windows
```

<span data-ttu-id="c952d-118">Her dictionary bağımsız değişkeni nesneden bir özellik seçer.</span><span class="sxs-lookup"><span data-stu-id="c952d-118">Each dictionary argument selects one property from the object.</span></span> <span data-ttu-id="c952d-119">Ayıklanacak olan özellik ifadenin bir parçası olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c952d-119">The property to extract must be part of an expression.</span></span>

## <a name="filter-results"></a><span data-ttu-id="c952d-120">Sonuçları filtreleme</span><span class="sxs-lookup"><span data-stu-id="c952d-120">Filter results</span></span> 

<span data-ttu-id="c952d-121">`Where-Object` cmdlet’i, sonucu iç içe özellikler de dahil olmak üzere herhangi bir özellik değerine göre filtrelemenize imkan tanır.</span><span class="sxs-lookup"><span data-stu-id="c952d-121">The `Where-Object` cmdlet allows you to filter the result based on any property value, including nested properties.</span></span> <span data-ttu-id="c952d-122">Sonraki örnekte, kaynak grubunda Linux VM'lerini bulmak için `Where-Object` öğesinin nasıl kullanıldığı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="c952d-122">The next example shows how to use `Where-Object` to find the Linux VMs in a resource group.</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OSDisk.OSType -eq "Linux"}
```

```output
ResourceGroupName    Name Location          VmSize OsType        NIC ProvisioningState Zone
-----------------    ---- --------          ------ ------        --- ----------------- ----
TestGroup          TestVM  westus2 Standard_D2s_v3  Linux  testvm299         Succeeded
TestGroup         TestVM2  westus2 Standard_D2s_v3  Linux testvm2669         Succeeded
```

<span data-ttu-id="c952d-123">`Select-Object` ile `Where-Object` işlemlerinin sonuçlarını birbirine yönlendirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c952d-123">You can pipe the results of `Select-Object` and `Where-Object` to each other.</span></span> <span data-ttu-id="c952d-124">Performans açısından, her zaman `Where-Object` işleminin `Select-Object` işleminden önce kullanılması önerilir:</span><span class="sxs-lookup"><span data-stu-id="c952d-124">For performance purposes, it's always recommended to put the `Where-Object` operation before `Select-Object`:</span></span>

```azurepowershell-interactive
Get-AzVM -ResourceGroupName TestGroup | `
    Where-Object {$_.StorageProfile.OsDisk.OsType -eq "Linux"} | `
    Select-Object Name,VmID,ProvisioningState
```

```output
Name    VmId                                 ProvisioningState
----    ----                                 -----------------
TestVM  711d8ed1-b888-4c52-8ab9-66f07b87eb6  Succeeded
TestVM2 cbcee769-dd78-45e3-a14d-2ad11c647d0  Succeeded
```
