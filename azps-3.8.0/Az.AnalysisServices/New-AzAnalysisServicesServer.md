---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/new-azanalysisservicesserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/New-AzAnalysisServicesServer.md
ms.openlocfilehash: 7e6b41a081b5170a34863ff29bf26431224490fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097450"
---
# New-AzAnalysisServicesServer

## SYNOPSIS
Yeni bir Analysis Services sunucusu oluşturur

## INDEKI

```
New-AzAnalysisServicesServer [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [[-Tag] <Hashtable>] [[-Administrator] <String>] [[-BackupBlobContainerUri] <String>]
 [-ReadonlyReplicaCount <Int32>] [-DefaultConnectionMode <String>]
 [-FirewallConfig <PsAzureAnalysisServicesFirewallConfig>] [-GatewayResourceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
New-AzAnalysisServicesServer cmdlet 'i yeni bir Analysis Services sunucusu oluşturur

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> New-AzAnalysisServicesServer -ResourceGroupName "testresourcegroup" -Name "testserver" -Location "West-US" -Sku "S1"
```

A-US ve kaynak grubu testresourcegroup içinde TestServer adlı bir sunucu oluşturur. Sunucu için SKU düzeyi S1 olacaktır.

## PARAMETRELERINE

### -Yönetici
Sunucuda yönetici olarak ayarlanacak Kullanıcı veya grupların virgülle ayrılmış listesini temsil eden dize. Kullanıcıların veya grupların UPN biçiminde ( user@contoso.com veya groups@contoso.com

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackupBlobContainerUri
Çözümleme Hizmetleri sunucusunu yedeklemek için blob kapsayıcı URI 'Si

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultConnectionMode
Çözümleme hizmeti sunucusunun varsayılan bağlantı modu

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: All, Readonly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -FirewallConfig
Çözümleme sunucusunun güvenlik duvarı yapılandırması

```yaml
Type: Microsoft.Azure.Commands.AnalysisServices.Models.PsAzureAnalysisServicesFirewallConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Gatewayresourceıd
Çözümleme sunucusuyla ilişkilendirilecek ağ geçidi kaynak kimliği

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Konum
Analysis Services sunucusunun barındırıldığı Azure bölgesi

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

### -Ad
Analysis Services sunucusunun adı

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

### -ReadonlyReplicaCount
Çözümleme hizmeti sunucusunun salt okunur kopya sayısı

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Sunucunun ait olduğu Azure Kaynak grubunun adı

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

### -SKU
Sunucunun SKU adı.
Desteklenen değerler, Standart katman için 0 ' ın 1 ' i 1 ' in 2 ' nin 4 ' ü; ' B1 ', temel katman için ' B2 ' ve geliştirme katmanı için 1 '.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Sunucuda etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister

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
Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. topluluklar. Hashtable

### System. Int32

### Microsoft. Azure. Commands. AnalysisServices. modeller. Psazureanalysisservices, Allconfig

## ÇıKıŞLAR

### Microsoft. Azure. Commands. AnalysisServices. modeller. AzureAnalysisServicesServer

## NOTLARıNDA
Diğer ad: New-AzAs

## ILGILI BAĞLANTıLAR

[Get-AzAnalysisServicesServer](./Get-AzAnalysisServicesServer.md)

[Remove-AzAnalysisServicesServer](./Remove-AzAnalysisServicesServer.md)
