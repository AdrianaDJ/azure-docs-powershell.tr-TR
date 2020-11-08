---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/remove-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Remove-AzFunctionAppPlan.md
ms.openlocfilehash: 6668952ba07327482da7ed3c274eb003ac61c73c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275417"
---
# Remove-AzFunctionAppPlan

## SYNOPSIS
İşlev uygulaması planını siler.

## INDEKI

### ByName (varsayılan)
```
Remove-AzFunctionAppPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Force]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### ByObjectInput
```
Remove-AzFunctionAppPlan -InputObject <IAppServicePlan> [-Force] [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım
İşlev uygulaması planını siler.

## ÖRNEKLERDEN

### Örnek 1: ada göre bir işlev uygulaması planı alın ve silin.
```powershell
PS C:\> Get-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName | Remove-AzFunctionAppPlan -Force
```

Bu komut bir işlev uygulaması planını ada göre alır ve siler.

### Örnek 2: ada göre bir işlev uygulaması planını silme.
```powershell
PS C:\> Remove-AzFunctionAppPlan -Name MyAppName -ResourceGroupName MyResourceGroupName -Force
```

Bu komut bir işlev uygulaması planını ada göre siler.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

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

### -Force
Cmdlet 'i, onay istemeden işlev uygulaması planını kaldırmaya zorlar.

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

### -Ad
İşlev uygulamasının adı.

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

### -Geçiş
Komut başarılı olduğunda doğru döndürür.

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

### System. Boolean

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

