---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregionhealth
schema: 2.0.0
ms.openlocfilehash: 6f5fa25f1b35ac03d27688eced71919cb409d1cb
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94105288"
---
# Get-AzsRegionHealth

## SYNOPSIS
Bir bölgenin istenen sistem durumunu döndürür.

## INDEKI

### Get (varsayılan)
```
Get-AzsRegionHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Getviaıdentity
```
Get-AzsRegionHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Listeniz
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Tanım
Bir bölgenin istenen sistem durumunu döndürür.

## ÖRNEKLERDEN

### Örnek 1:
```powershell
PS C:\> Get-AzsRegionHealth
```

Bölgenin uygunluk durumu listesini döndürür.

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

### -Filtre
OData filtre parametresi.

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -InputObject
Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Konum
Bölgenin adı

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -ResourceGroupName
Kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionID
Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri.
Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. IInfrastructureInsightsAdminIdentity

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. InfrastructureInsightsAdmin. modeller. Api20160501. ıregionhealth



## NOTLARıNDA

KARMAŞıK parametre ÖZELLIKLERI aşağıda açıklanan parametreleri oluşturmak Için uygun özellikleri içeren karma bir tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.

INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : IDENTITY parametresi
  - `[AlertName <String>]`: Uyarının adı.
  - `[Id <String>]`: Kaynak kimliği yolu
  - `[Location <String>]`: Bölgenin adı
  - `[ResourceGroupName <String>]`: Kaynak grubunun adı.
  - `[ResourceRegistrationId <String>]`: Kaynak kayıt KIMLIĞI.
  - `[ServiceHealth <String>]`: Hizmet durumu adı.
  - `[ServiceRegistrationId <String>]`: Hizmet kayıt KIMLIĞI.
  - `[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgileri. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.

## ILGILI BAĞLANTıLAR

