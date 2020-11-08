---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/get-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Get-AzAppConfigurationStore.md
ms.openlocfilehash: 88847cbb128f5545a235eb2c5c02043231ff1078
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107985"
---
# Get-AzAppConfigurationStore

## SYNOPSIS
Uygulama yapılandırma depolarını alma veya listeleme.

## INDEKI

### Liste (varsayılan)
```
Get-AzAppConfigurationStore [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Al
```
Get-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Getviaıdentity
```
Get-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### List1
```
Get-AzAppConfigurationStore -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## Tanım
Uygulama yapılandırma depolarını alma veya listeleme.

## ÖRNEKLERDEN

### Örnek 1: aboneliğin altındaki tüm uygulama yapılandırma depolarını listeler
```powershell
PS C:\> Get-AzAppConfigurationStore

Location Name               Type
-------- ----               ----
eastus   appconfig-test01   Microsoft.AppConfiguration/configurationStores
eastus   contoso-app-config Microsoft.AppConfiguration/configurationStores
```

Bu komut, bir aboneliğin altındaki tüm uygulama yapılandırma depolarını listeler.

### Örnek 2: kaynak grubu altındaki tüm uygulama yapılandırma depolarını listeler
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
eastus   appconfig-test02 Microsoft.AppConfiguration/configurationStores
```

Bu komut, kaynak grubu altındaki tüm uygulama yapılandırma depolarını listeler.

### Örnek 3: ada göre bir uygulama yapılandırma deposu alma
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

Bu komut, uygulama yapılandırma deposunu adıyla alır.

### Örnek 4: ardışık düzene göre uygulama yapılandırma deposunu alma
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test01 | Get-AzAppConfigurationStore

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

Bu komut, bir uygulama yapılandırma deposunu ardışık düzene göre alır.

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

### -InputObject
Yapı Için IDENTITY parametresi, ıNPUTOBJECT özellikleri için Notlar bölümüne bakın ve karma tablo oluşturur.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Ad
Yapılandırma deposu adı.

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kapsayıcı kayıt defterinin ait olduğu kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionID
Microsoft Azure abonelik KIMLIĞI.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
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

### Microsoft. Azure. PowerShell. cmdlet. AppConfiguration. modeller. ıappconfigurationıdentity

## ÇıKıŞLAR

### Microsoft. Azure. PowerShell. cmdlet. AppConfiguration. modeller. Api20200601. Iconationstore

## NOTLARıNDA

DIĞER adları

KARMAŞıK PARAMETRE ÖZELLIKLERI

Aşağıda açıklanan parametreleri oluşturmak için uygun özellikleri içeren bir karma tablo oluşturun. Karma tablolar hakkında bilgi için Get-Help about_Hash_Tables.


INPUTOBJECT <IAppConfigurationIdentity> : IDENTITY parametresi
  - `[ConfigStoreName <String>]`: Yapılandırma deposu adı.
  - `[GroupName <String>]`: Özel bağlantı kaynak grubunun adı.
  - `[Id <String>]`: Kaynak kimliği yolu
  - `[PrivateEndpointConnectionName <String>]`: Özel uç noktası bağlantı adı
  - `[ResourceGroupName <String>]`: Kapsayıcı kayıt defterinin ait olduğu kaynak grubunun adı.
  - `[SubscriptionId <String>]`: Microsoft Azure abonelik KIMLIĞI.

## ILGILI BAĞLANTıLAR

