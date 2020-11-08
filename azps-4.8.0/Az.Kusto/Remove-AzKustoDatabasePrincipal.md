---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/remove-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Remove-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 495561794485e259d81b2e611658be461233d36d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274496"
---
# Remove-AzKustoDatabasePrincipal

## SYNOPSIS
Veritabanı sorumlusu izinlerini kaldırın.

## INDEKI

### Removegenişletilmiş (varsayılan)
```
Remove-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Value <IDatabasePrincipal[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### Removeviaıdentitygenişletilen
```
Remove-AzKustoDatabasePrincipal -InputObject <IKustoIdentity> [-Value <IDatabasePrincipal[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım
Veritabanı sorumlusu izinlerini kaldırın.

## ÖRNEKLERDEN

### Örnek 1: veritabanı sorumluları izinlerini kaldırma
```powershell
PS C:\> Remove-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -Value (@{Name="Some User"; Role="Admin"; Type="User"; Email="someuser@microsoft.com"})

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

Yukarıdaki komut veritabanı sorumluları izinlerini kaldırır

## PARAMETRELERINE

### -ClusterName
Kusto kümesinin adı.

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Kusto kümesindeki veritabanının adı.

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
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

### -InputObject
Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: RemoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Kusto kümesini içeren kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionID
Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır.
Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: RemoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Değer
Kusto veritabanı sorumlularının listesi.
Oluşturmak için, değer özellikleri için Notlar bölümüne bakın ve karma tablo oluşturun.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal[]
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

### Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. ıkustoıdentity

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. kusto. modeller. Api20200614. IDatabasePrincipal

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


INPUTOBJECT <IKustoIdentity> : IDENTITY parametresi
  - `[AttachedDatabaseConfigurationName <String>]`: Ekli veritabanı yapılandırmasının adı.
  - `[ClusterName <String>]`: Kusto kümesinin adı.
  - `[DataConnectionName <String>]`: Veri bağlantısının adı.
  - `[DatabaseName <String>]`: Kusto kümesindeki veritabanının adı.
  - `[Id <String>]`: Kaynak kimliği yolu
  - `[Location <String>]`: Azure konumu.
  - `[PrincipalAssignmentName <String>]`: Kusto principalAssignment adı.
  - `[ResourceGroupName <String>]`: Kusto kümesini içeren kaynak grubunun adı.
  - `[SubscriptionId <String>]`: Microsoft Azure aboneliğini benzersiz bir şekilde tanımlayan abonelik kimlik bilgilerini alır. Her hizmet çağrısı için URI 'nin bir parçası olan abonelik KIMLIĞI.

DEĞER <IDatabasePrincipal [] >: kusto veritabanı sorumlularının listesi.
  - `Name <String>`: Veritabanı asıl adı.
  - `Role <DatabasePrincipalRole>`: Veritabanı sorumlusu rolü.
  - `Type <DatabasePrincipalType>`: Veritabanı sorumlusu türü.
  - `[AppId <String>]`: Uygulama kimliği-yalnızca uygulama sorumlusu türü için geçerlidir.
  - `[Email <String>]`: Varsa, veritabanı sorumlusu e-postası.
  - `[Fqn <String>]`: Veritabanı sorumlusu tam adı.

## ILGILI BAĞLANTıLAR

