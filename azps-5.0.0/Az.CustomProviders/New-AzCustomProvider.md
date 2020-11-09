---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321298"
---
# New-AzCustomProvider

## SYNOPSIS
Özel kaynak sağlayıcısını oluşturur veya güncelleştirir.

## INDEKI

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım
Özel kaynak sağlayıcısını oluşturur veya güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1: özel sağlayıcı oluşturma
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

Özel kaynak sağlayıcısı oluşturma

### Örnek 2: ilişkilendirmelere sahip özel bir sağlayıcı oluşturma
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

Özel sağlayıcı ilişkilendirmeleri için yol içeren özel bir sağlayıcı oluşturun.

## PARAMETRELERINE

### -Eylem
Özel kaynak sağlayıcısının uyguladığı eylemlerin listesi.
Oluşturmak için, eylem özelliklerinin Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Iş
Komutu iş olarak çalıştırmak

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

### -Konum
Kaynak konumu

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Kaynak sağlayıcının adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWait
Komutu zaman uyumsuz olarak çalıştırır

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
Kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Özel kaynak sağlayıcısının uyguladığı kaynak türlerinin listesi.
Oluşturmak için, RESOURCETYPE özelliklerinin notlar bölümü 'ne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
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
Bu GUID biçimli bir dizedir (örneğin, 00000000-0000-0000-0000-000000000000)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
Kaynak etiketleri

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

### -Doğrulama
Özel kaynak sağlayıcısının isteklerinde çalışacak doğrulama listesi.
Oluşturmak için, doğrulama özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
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

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. CustomProviders. modeller. Api20180901Preview. ICustomRpManifest

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


EYLEM <ıcustomrpactionroutedefinition [] >: özel kaynak sağlayıcısının uyguladığı eylemlerin listesi.
  - `Endpoint <String>`: Özel kaynak sağlayıcısının proxy tarafından istek aldığı yol tanımı uç noktası URI 'SI. Bu, düz bir URI biçiminde (örneğin, ' https://testendpoint/ ') veya bir yol üzerinden yönlendirme için belirtilebilir (örneğin, ' https://testendpoint/{requestPath} ')
  - `Name <String>`: Yol tanımının adı. Bu, ARM uzantısının adı olur (örneğin, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name} ')
  - `[RoutingType <ActionRouting?>]`: Eylem istekleri için desteklenen yönlendirme türleri.

RESOURCETYPE <ıcustomrpresourcetyperoutedefinition [] >: özel kaynak sağlayıcısının uyguladığı kaynak türlerinin listesi.
  - `Endpoint <String>`: Özel kaynak sağlayıcısının proxy tarafından istek aldığı yol tanımı uç noktası URI 'SI. Bu, düz bir URI biçiminde (örneğin, ' https://testendpoint/ ') veya bir yol üzerinden yönlendirme için belirtilebilir (örneğin, ' https://testendpoint/{requestPath} ')
  - `Name <String>`: Yol tanımının adı. Bu, ARM uzantısının adı olur (örneğin, '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name} ')
  - `[RoutingType <ResourceTypeRouting?>]`: Kaynak istekleri için desteklenen yönlendirme türleri.

DOĞRULAMA <ıcustomrpdoğrulamaları [] >: özel kaynak sağlayıcısının isteklerinde çalışacak doğrulama listesi.
  - `Specification <String>`: Doğrulama belirtiminin bağlantısı. Belirtim raw.githubusercontent.com üzerinde barındırılmalıdır.
  - `[ValidationType <ValidationType?>]`: Eşleşen bir istekte çalışacak doğrulama türü.

## ILGILI BAĞLANTıLAR

