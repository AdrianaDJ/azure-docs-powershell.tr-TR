---
title: Azure kaynaklarını sorgulama ve sonuçları biçimlendirme | Microsoft Docs
description: Azure’daki kaynakları sorgulama ve sonuçları biçimlendirme.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: dde1702f512be70ece137059797e29c75926e231
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34820315"
---
# <a name="querying-for-azure-resources"></a>Azure kaynaklarını sorgulama

PowerShell’de sorgu işlemleri yerleşik cmdlet’ler kullanılarak gerçekleştirilebilir. PowerShell’de cmdlet adları **_Fiil-İsim_** biçiminde olur. **_Get_** fiilini kullanan cmdlet’ler sorgu cmdlet’leridir. Cmdlet isimleri, cmdlet fiilleri tarafından üzerinde eylem gerçekleştirilen Azure kaynağı türleridir.

## <a name="selecting-simple-properties"></a>Basit özellikleri seçerek

Azure PowerShell’de her cmdlet için tanımlı bir varsayılan biçimlendirme vardır. Her kaynak türünün en yaygın özellikleri, otomatik olarak bir tablo ya da liste biçiminde görüntülenir. Çıktı biçimlendirme hakkında daha fazla bilgi edinmek için bkz. [Sorgu sonuçlarını biçimlendirme](formatting-output.md).

Hesabınızdaki VM’lerin listesini sorgulamak için `Get-AzureRmVM` cmdlet’ini kullanın.

```azurepowershell-interactive
Get-AzureRmVM
```

Varsayılan çıktı otomatik olarak bir tablo şeklinde biçimlendirilir.

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

`Select-Object` cmdlet’ini kullanarak ilginizi çeken belirli özellikleri seçebilirsiniz.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,ResourceGroupName,Location
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

## <a name="selecting-complex-nested-properties"></a>Karmaşık iç içe özellikler seçme

Seçmek istediğiniz özellik JSON çıktısında derin olarak iç içe yerleştirilmişse, bu iç içe özelliğin tam yolunu sağlamanız gerekir. Aşağıdaki örnekte `Get-AzureRmVM` cmdlet’inden VM Adı ve işletim sistemi türünün nasıl seçileceği gösterilir.

```azurepowershell-interactive
Get-AzureRmVM | Select Name,@{Name='OSType'; Expression={$_.StorageProfile.OSDisk.OSType}}
```

```output
Name           OSType
----           ------
MyUnbuntu1610   Linux
MyWin2016VM   Windows
```

## <a name="filter-result-using-the-where-object-cmdlet"></a>Where-Object cmdlet’ini kullanarak sonucu filtreleme

`Where-Object` cmdlet’i, sonucu herhangi bir özellik değerine göre filtrelemenize imkan tanır. Aşağıdaki örnekte, filtre yalnızca adında "RGD" metni geçen VM’leri seçer.

```azurepowershell-interactive
Get-AzureRmVM | Where ResourceGroupName -like RGD* | Select ResourceGroupName,Name
```

```output
ResourceGroupName  Name
-----------------  ----
RGDEMO001          KBDemo001VM
RGDEMO001          KBDemo020
```

Bir sonraki örnekte sonuçlar, boyutu 'Standart_DS1_V2' olan VM’leri döndürür.

```azurepowershell-interactive
Get-AzureRmVM | Where vmSize -eq Standard_DS1_V2
```

```output
ResourceGroupName          Name     Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----     --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610   westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM   westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```