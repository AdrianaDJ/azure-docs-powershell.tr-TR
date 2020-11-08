---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppPlan.md
ms.openlocfilehash: e0831e95a5601d3558af7089825684cc48e7838c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275404"
---
# Update-AzFunctionAppPlan

## SYNOPSIS
Bir işlev App Service planını güncelleştirir.

## INDEKI

### ByName (varsayılan)
```
Update-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Update-AzFunctionAppPlan -InputObject <IAppServicePlan> [-MaximumWorkerCount <Int32>]
 [-MinimumWorkerCount <Int32>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım
Bir işlev App Service planını güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1: bir App Service planını yirmimaksimum çalışanı olan SKU 'yu EP2.
```powershell
PS C:\> Update-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                                 -Name MyPremiumPlan `
                                 -MaximumWorkerCount 20 `
                                 -Sku EP2

```

Bu komut, bir App Service planını yirmimaksimum çalışan SKU 'yu EP2.

## PARAMETRELERINE

### -Iş
Komutu iş olarak çalıştırır.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Oluşturmak için, ıNPUTOBJECT özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumWorkerCount
App Service planı için en fazla çalışan sayısı.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumWorkerCount
App Service planı için en az çalışan sayısı.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
App Service planının adı.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Komutu zaman uyumsuz olarak çalıştırır.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynağın ait olduğu kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SKU
Plan SKU 'su.
Geçerli girdiler: EP1, EP2, EP3

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionID
Azure aboneliği KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
Kaynak etiketleri.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ıappserviceplan

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. Functions. modeller. Api20190801. ıappserviceplan

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


INPUTOBJECT <IAppServicePlan> : 
  - `Location <String>`: Kaynak konumu.
  - `[Kind <String>]`: Kaynak türü.
  - `[Tag <IResourceTags>]`: Kaynak etiketleri.
    - `[(Any) <String>]`: Bu, hiçbir özelliğin bu nesneye ekleneolabileceğini gösterir.
  - `[Capacity <Int32?>]`: Kaynağa atanmış geçerli örnek sayısı.
  - `[FreeOfferExpirationTime <DateTime?>]`: Sunucu grubunun ücretsiz teklifinin süresi dolduğunda geçen saat.
  - `[HostingEnvironmentProfileId <String>]`: App Service ortamının kaynak KIMLIĞI.
  - `[HyperV <Boolean?>]`: Hyper-V kapsayıcı uygulama hizmeti planı Eğer <code>true</code> değilse <code>false</code> .
  - `[IsSpot <Boolean?>]`: <code>true</code> Bu App Service planı, nokta örneklerinin sahibi.
  - `[IsXenon <Boolean?>]`: Geçersiz: Hyper-V kapsayıcı uygulama hizmeti planı varsa <code>true</code> , <code>false</code> Aksi halde.
  - `[MaximumElasticWorkerCount <Int32?>]`: Bu Eladascaleenabled App Service planı için izin verilen toplam çalışan sayısı üst sınırı
  - `[PerSiteScaling <Boolean?>]`: <code>true</code> Bu App Service planına atanmış uygulamalar bağımsız olarak ölçeklendirilemez.         <code>false</code>Bu App Service planına atanmış uygulamalar planın tüm örneklerine ölçeklendirecektir.
  - `[Reserved <Boolean?>]`: Linux App Service planı yoksa <code>true</code> <code>false</code> .
  - `[SkuCapability <ICapability[]>]`: SKU 'nun özellikleri, örneğin Traffic Manager 'ı etkinleştirmi?
    - `[Name <String>]`: SKU özelliğinin adı.
    - `[Reason <String>]`: SKU özelliğinin nedeni.
    - `[Value <String>]`: SKU özelliğinin değeri.
  - `[SkuCapacityDefault <Int32?>]`: Bu App Service planı SKU 'SU için varsayılan çalışan sayısı.
  - `[SkuCapacityMaximum <Int32?>]`: Bu App Service planı SKU 'sunda maksimum çalışan sayısı.
  - `[SkuCapacityMinimum <Int32?>]`: Bu App Service planı SKU 'sunda en az çalışan sayısı.
  - `[SkuCapacityScaleType <String>]`: Bir App Service planı için kullanılabilir ölçeklendirme yapılandırmaları.
  - `[SkuFamily <String>]`: Kaynak SKU 'nun aile kodu.
  - `[SkuLocation <String[]>]`: SKU 'nun konumları.
  - `[SkuName <String>]`: Kaynak SKU 'nun adı.
  - `[SkuSize <String>]`: Kaynak SKU 'nun boyut belirticisi.
  - `[SkuTier <String>]`: Kaynak SKU 'nun hizmet katmanı.
  - `[SpotExpirationTime <DateTime?>]`: Sunucu grubunun süresi dolduğunda saat. Yalnızca bir nokta sunucusu grubuysa geçerlidir.
  - `[TargetWorkerCount <Int32?>]`: Çalışan sayısını ölçeklendirme.
  - `[TargetWorkerSizeId <Int32?>]`: Çalışan boyutu
  - `[WorkerTierName <String>]`: App Service planına atanan hedef çalışan katmanı.

## ILGILI BAĞLANTıLAR

