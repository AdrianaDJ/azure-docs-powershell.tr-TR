---
title: Azure PowerShell cmdlet'lerinin çıkışını sorgulama
description: Azure’daki kaynakları sorgulama ve sonuçları biçimlendirme.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/10/2019
ms.openlocfilehash: 9141f5640467722608cb7748f425ce3942668fb8
ms.sourcegitcommit: 0c012450805bef75472f48c74fe488baf6ba53bb
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/04/2019
ms.locfileid: "66498650"
---
# <a name="query-output-of-azure-powershell"></a>Azure PowerShell'in çıkışını sorgulama 

Tüm Azure PowerShell cmdlet'lerinin sonuçları birer Azure PowerShell nesnesidir. Açıkça `Get-` işlemleri olmayan cmdlet'ler bile, oluşturulmuş veya değiştirilmiş olan kaynak hakkında bilgi vermek için incelenebilecek bir değer döndürür. Cmdlet'lerin çoğu tek bir nesne döndürse de, bazıları yinelenmesi gereken bir dizi döndürür.

Çoğu durumda sorgunuz Azure PowerShell'den [Select-Object](/powershell/module/Microsoft.PowerShell.Utility/Select-Object) cmdlet'iyle (çoğunlukla `select` olarak kısaltılmıştır) çıkış sağlar. Çıkış [Where-Object](/powershell/module/Microsoft.PowerShell.Core/Where-Object) ile veya bunun `where` diğer adıyla filtrelenebilir.

## <a name="select-simple-properties"></a>Basit özellikleri seçme

Varsayılan tablo biçiminde, Azure PowerShell cmdlet'leri tüm kullanılabilir özelliklerini görüntülemez. Tüm özellikleri almak için [Format-List](/powershell/module/microsoft.powershell.utility/format-list) cmdlet'ini kullanabilir veya çıkışı `Select-Object *` cmdlet'ine yönlendirebilirsiniz:

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

İlgilendiğiniz özelliklerin adını öğrendikten sonra, bu özellik adlarını `Select-Object` ile kullanarak bunları doğrudan alabilirsiniz:

```azurepowershell-interactive
Get-AzVM -Name TestVM -ResourceGroupName TestGroup | Select-Object Name,VmId,ProvisioningState
```

```output
Name   VmId                                 ProvisioningState
----   ----                                 -----------------
TestVM 711d8ed1-b888-4c52-8ab9-66f07b87eb6b Succeeded
```

`Select-Object` kullanılarak alınan çıkış her zaman istenen bilgileri görüntüleyecek şekilde biçimlendirilir. Cmdlet sonuçlarını sorgulama kapsamında biçimlendirmeyi kullanmayı öğrenmek için bkz. [Azure PowerShell cmdlet'inin çıkışını biçimlendirme](formatting-output.md).

## <a name="select-nested-properties"></a>İç içe özellikleri seçme

Azure PowerShell cmdlet'inin çıkışındaki bazı özellikler (`Get-AzVM` çıkışının `StorageProfile` özelliği gibi) iç içe nesneler kullanır. İç içe özellikten bir değer almak için, `Select-Object` cmdlet'inde dictionary bağımsız değişkeninin parçası olarak incelemek istediğiniz değerin görünen adını ve tam yolunu sağlayın:

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

Her dictionary bağımsız değişkeni nesneden bir özellik seçer. Ayıklanacak olan özellik ifadenin bir parçası olmalıdır.

## <a name="filter-results"></a>Sonuçları filtreleme 

`Where-Object` cmdlet’i, sonucu iç içe özellikler de dahil olmak üzere herhangi bir özellik değerine göre filtrelemenize imkan tanır. Sonraki örnekte, kaynak grubunda Linux VM'lerini bulmak için `Where-Object` öğesinin nasıl kullanıldığı gösterilir.

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

`Select-Object` ile `Where-Object` işlemlerinin sonuçlarını birbirine yönlendirebilirsiniz. Performans açısından, her zaman `Where-Object` işleminin `Select-Object` işleminden önce kullanılması önerilir:

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