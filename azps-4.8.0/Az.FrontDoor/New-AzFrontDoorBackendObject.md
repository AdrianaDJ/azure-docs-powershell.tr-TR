---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorbackendobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorBackendObject.md
ms.openlocfilehash: 8eee112840fa7d7af81838927017b38988c9649b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273579"
---
# New-AzFrontDoorBackendObject

## SYNOPSIS
Psarka uç nesnesi oluşturma

## INDEKI

```
New-AzFrontDoorBackendObject -Address <String> [-HttpPort <Int32>] [-HttpsPort <Int32>] [-Priority <Int32>]
 [-Weight <Int32>] [-EnabledState <PSEnabledState>] [-BackendHostHeader <String>] [-PrivateLinkAlias <String>]
 [-PrivateLinkResourceId <String>] [-PrivateLinkLocation <String>] [-PrivateLinkApprovalMessage <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Ön kapı oluşturmak için Psarka uç nesnesi oluşturma

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\>New-AzFrontDoorBackendObject -Address "contoso1.azurewebsites.net"


Address           : contoso1.azurewebsites.net
HttpPort          : 80
HttpsPort         : 443
Priority          : 1
Weight            : 50
BackendHostHeader :
EnabledState      : Enabled
```

Ön kapı oluşturmak için Psarka uç nesnesi oluşturma

## PARAMETRELERINE

### -Adres
Arka ucun konumu (IP adresi veya FQDN)

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

### -BackendHostHeader
Arka uca gönderilen ana bilgisayar üst bilgisi olarak kullanılacak değer. Varsayılan değer, arka uç adresidir.

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

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledState
Bu arka ucun kullanımını etkinleştirip etkinleştirmeyeceğinizi. Varsayılan değer etkindir

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpPort
HTTP TCP bağlantı noktası numarası.
1 ile 65535 arasında olmalıdır.
Varsayılan değer 80 ' dır.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpsPort
HTTPS TCP bağlantı noktası numarası.
1 ile 65535 arasında olmalıdır.
Varsayılan değer 443

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Öncelik
Yük Dengelemesi için kullanılacak öncelik.
1 ile 5 arasında olmalıdır.
Varsayılan değer 1 ' dir

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Privatelinkalıas
Özel bağlantı kaynağının diğer adı. Bu isteğe bağlı alan doldurulurken, bu uç ucun ' özel ' olduğunu gösterir

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

### -PrivateLinkApprovalMessage
Özel bağlantısına bağlanmak için onay isteğine dahil edilecek özel bir ileti

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

### -PrivateLinkLocation
Özel bağlantı kaynağının konumu. Privatelinkresourceıd ayarlandığında konum gereklidir

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

### -Privatelinkresourceıd
Özel bağlantının kaynak KIMLIĞI. Bu isteğe bağlı alan doldurulurken, bu uç ucun ' özel ' olduğunu gösterir

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

### -Kalınlık
Bu uç noktanın yük dengelemesi amaçları için ağırlığı.
1 ile 1000 arasında olmalıdır.
Varsayılan değer 50

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Frontkapısı. modeller. Psarka uç

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)
