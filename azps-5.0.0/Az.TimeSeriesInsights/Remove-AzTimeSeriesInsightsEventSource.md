---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/remove-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/Remove-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 7f647da2543a4675dad53f88e2494aa7f6c39419
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322591"
---
# Remove-AzTimeSeriesInsightsEventSource

## SYNOPSIS
Belirtilen abonelikteki, kaynak grubundaki ve ortamdaki olay kaynağını siler

## INDEKI

### Sil (varsayılan)
```
Remove-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Deleteviaıdentity
```
Remove-AzTimeSeriesInsightsEventSource -InputObject <ITimeSeriesInsightsIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım
Belirtilen abonelikteki, kaynak grubundaki ve ortamdaki olay kaynağını siler

## ÖRNEKLERDEN

### Örnek 1: belirtilen olay kaynağını ada göre kaldırma
```powershell
PS C:\> Remove-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -Name iots001 -ResourceGroupName testgroup

```

Bu, belirli bir olay kaynağını kaldırır.

### Örnek 2: belirli bir olay kaynağını nesne ile kaldırma
```powershell
PS C:\> $es = Get-AzTimeSeriesInsightsEventSource -EnvironmentName tsitest001 -ResourceGroupName testgroup -Name iots001
PS C:\> Remove-AzTimeSeriesInsightsEventSource -InputObject $es

```

Bu, belirli bir olay kaynağını kaldırır.

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

### -EnvironmentName
Belirtilen kaynak grubuyla ilişkili saat serisi öngörüleri ortamının adı.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.ITimeSeriesInsightsIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geçiş
Komut başarılı olduğunda doğru verir

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
Azure Kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionID
Azure abonelik KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: Delete
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

### Microsoft. Azure. PowerShell. cmdlet. W32.

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


INPUTOBJECT <ITimeSeriesInsightsIdentity> : IDENTITY parametresi
  - `[AccessPolicyName <String>]`: Erişim ilkesinin adı.
  - `[EnvironmentName <String>]`: Ortamın adı
  - `[EventSourceName <String>]`: Belirtilen ortamla ilişkili saat serisi öngörüleri olay kaynağının adı.
  - `[Id <String>]`: Kaynak kimliği yolu
  - `[ReferenceDataSetName <String>]`: Başvuru veri kümesinin adı.
  - `[ResourceGroupName <String>]`: Azure Kaynak grubunun adı.
  - `[SubscriptionId <String>]`: Azure abonelik KIMLIĞI.

## ILGILI BAĞLANTıLAR

