---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbConfiguration.md
ms.openlocfilehash: 4ee32822f6fb4872a9fa01d020ed0f0bf92b0456
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273526"
---
# Update-AzMariaDbConfiguration

## SYNOPSIS
Sunucunun yapılandırmasını güncelleştirir.
Update-AzMariaDbServer, \ \ Loginpassword, STB vb. güncelleştirme istiyorsanız kullanın.

## INDEKI

### Updategenişletilmiş (varsayılan)
```
Update-AzMariaDbConfiguration -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Source <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### Updateviaıdentitygenişletilmiş
```
Update-AzMariaDbConfiguration -InputObject <IMariaDbIdentity> [-Source <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Tanım
Sunucunun yapılandırmasını güncelleştirir.
Update-AzMariaDberver, \ \ Loginpassword, STB vb. güncelleştirme istiyorsanız kullanın.

## ÖRNEKLERDEN

### Örnek 1: MariaDB yapılandırmasını güncelleştirme
```powershell
PS C:\> Update-AzMariaDbConfiguration -Name delayed_insert_timeout -Value 200 -ServerName mariadb-test-h3pame -ResourceGroupName mariadb-test-qu5ov0 

Name                   Type
----                   ----
delayed_insert_timeout Microsoft.DBforMariaDB/servers/configurations
```

Bu komut bir MariaDB yapılandırmasını güncelleştirir.

## PARAMETRELERINE

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

### -InputObject
Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Sunucu yapılandırmasının adı.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ConfigurationName

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
Kaynağı içeren kaynak grubunun adı.
Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
Sunucunun adı.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kaynak
Yapılandırmanın kaynağı.

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
Bir Azure aboneliğini tanımlayan abonelik KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Değer
Yapılandırmanın değeri.

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

### Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Sanarladbıdentity

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. MariaDb. modeller. Api20180601Preview. Iconation

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


INPUTOBJECT <IMariaDbIdentity> : IDENTITY parametresi
  - `[ConfigurationName <String>]`: Sunucu yapılandırmasının adı.
  - `[DatabaseName <String>]`: Veritabanının adı.
  - `[FirewallRuleName <String>]`: Sunucu güvenlik duvarı kuralının adı.
  - `[Id <String>]`: Kaynak kimliği yolu
  - `[LocationName <String>]`: Konumun adı.
  - `[ResourceGroupName <String>]`: Kaynağı içeren kaynak grubunun adı. Bu değeri Azure Resource Manager API 'dan veya portalınızdan edinebilirsiniz.
  - `[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Güvenlik uyarısı ilkesinin adı.
  - `[ServerName <String>]`: Sunucunun adı.
  - `[SubscriptionId <String>]`: Azure aboneliğini tanımlayan abonelik KIMLIĞI.
  - `[VirtualNetworkRuleName <String>]`: Sanal ağ kuralının adı.

## ILGILI BAĞLANTıLAR

