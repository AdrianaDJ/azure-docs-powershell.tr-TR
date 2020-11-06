---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmWcfRelay.md
ms.openlocfilehash: 3aa57c1ec70d560a0fee395b27d79372bdf4fd61
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587177"
---
# New-AzureRmWcfRelay

## SYNOPSIS
Belirtilen geçiş ad alanında WcfRelay oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### WcfRelayInputObjectSet
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <WcfRelayAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### WcfRelayPropertiesSet
```
New-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-WcfRelayType <String>] [-RequiresClientAuthorization <Boolean>] [-RequiresTransportSecurity <Boolean>]
 [-UserMetadata <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
New-AzureRmWcfRelay cmdlet 'i belirtilen geçiş ad alanında WcfRelay oluşturur.

## ÖRNEKLERDEN

### Örnek 1-InputObject
```
PS C:\> $getWcfRelay = Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -WcfRelayName TestWCFRelay1
PS C:\> $GetWcfRelay.UserMetadata = "TestWCFRelay2"
PS C:\> $GetWcfRelay.RequiresClientAuthorization = $False
PS C:\> $GetWcfRelay.RelayType = "Http"
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay2 -InputObject

RelayType                   : Http
CreatedAt                   : 4/26/2017 5:14:46 PM
UpdatedAt                   : 4/26/2017 5:14:46 PM
ListenerCount               :
RequiresClientAuthorization : False
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : TestWCFRelay2
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay2
Name                        : TestWCFRelay2
Type                        : Microsoft.Relay/WcfRelays
```

\` \` Belirtilen geçiş ad alanı \` TestNamespace-Relay Içinde Yeni bir wcfrelay TestWCFRelay2 oluşturur \` .

### Örnek 2-Özellikler
```
PS C:\> New-AzureRmWcfRelay -ResourceGroupName Default-Storage-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay -WcfRelayType "NetTcp"  -RequiresClientAuthorization $True -RequiresTransportSecurity $True -UserMetadata "User Meta data"

RelayType                   : NetTcp
CreatedAt                   : 4/26/2017 5:20:08 PM
UpdatedAt                   : 4/26/2017 5:20:08 PM
ListenerCount               :
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/55f3dcd4-cac7-43b4-990b-a139d62a1eb2/resourceGroups/Default-Storage-WestUS/providers/Microsoft.Rel
                              ay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay
Name                        : TestWCFRelay
Type                        : Microsoft.Relay/WcfRelays
```

\` \` Belirtilen geçiş ad alanı testwcfrelay-Relay1 için yeni bir wcfrelay testwcfrelay oluşturur \` \` .

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
WcfRelay nesnesi.

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes
Parameter Sets: WcfRelayInputObjectSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
WcfRelay adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Ad alanı adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Requiresclientauthorter
Bu geçiş için istemci yetkilendirmesi gerekliyse doğru; Aksi takdirde, false

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RequiresTransportSecurity
Bu geçiş için taşıma güvenliği gerekliyse doğru; Aksi takdirde, false

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserMetadata
Kullanıcı tanımlı dize verilerinin HybridConnection uç noktasına depolanması için bir yer tutucudur. ekip listesi ve kişi bilgileri gibi açıklayıcı verileri depolamak için kullanılabilir, Kullanıcı tanımlı yapılandırma ayarları da depolanabilir.

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WcfRelayType
WcfRelay türü.
Olası değerler: ' NetTcp ' veya ' http '

```yaml
Type: System.String
Parameter Sets: WcfRelayPropertiesSet
Aliases:
Accepted values: NetTcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.
Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String
Microsoft. Azure. Commands. Relay. modeller. PSWcfRelayAttributes System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]


## ÇıKıŞLAR

### Microsoft. Azure. Commands. Relay. modeller. PSWcfRelayAttributes


## NOTLARıNDA

## ILGILI BAĞLANTıLAR
