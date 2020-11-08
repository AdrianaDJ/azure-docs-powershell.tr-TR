---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278701"
---
# New-AzEventGridTopic

## SYNOPSIS
Yeni bir Azure olay Kılavuzu konusu oluşturur.

## INDEKI

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Yeni bir Azure olay Kılavuzu konusu oluşturur. Konu oluşturulduğunda, bir uygulama etkinlikleri konu noktasında yayımlayabilir.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

\` \` \` \` Myresourcegroupname kaynak grubunda belirtilen coğrafi konum Westus2 konu1 \` bir etkinlik Kılavuzu konusu oluşturur \` .

### Örnek 2
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

\` \` \` Belirtilen ( \` \` \` "Bölüm" ve "ortam" etiketli kaynak grubundaki belirtilen coğrafi konum westus2 konu1 bir etkinlik Kılavuzu konusu oluşturur.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -InboundIpRule
Gelen IP kuralları listesini temsil eden Hashtable. Her kural, CıDR gösteriminde IP adresini, örneğin, IPMask ile eşleşmesiz veya eşleşmesiz eşleşme Olası eylem değerleri yalnızca Izin ver

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Inputmappingdefaultvalue
Alan ayrılmış anahtar = değer biçimindeki varsayılan değer ile giriş eşleme alanlarını temsil eden Hashtable. İzin verilen anahtar adları: Subject, EventType ve dataversion. Bu, ınputschemahelp yalnızca customeventschema olduğunda kullanılır.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Inputmappingfield
Karma değer eşleme alanlarını boşlukla ayrılmış anahtar = değer biçiminde temsil eder. İzin verilen anahtar adları: id, konu, EventTime, konu, EventType ve dataversion. Bu, ınputschemahelp yalnızca customeventschema olduğunda kullanılır.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Inputschema
Konu için giriş olaylarının şeması. İzin verilen değerler: eventgridschema, customeventschema veya cloudeventv01Schema. Varsayılan değer eventgridschema değeridir. Customeventschema belirtildiyse, ınputmappingfield veya/ve ınputmappingdefaultvalue parametrelerinin da belirtilmesi gerektiğini unutmayın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Konum
Konunun konumu

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
Konunun adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicNetworkAccess
Bu, trafiğin ortak ağ üzerinden izin verilip verilmediğini belirler. Varsayılan olarak etkindir. Inboundiprule parametrelerini yapılandırarak belirli IP 'lere daha fazla kısıtlama uygulayabilirsiniz. İzin verilen değerler devre dışı bırakılır ve etkinleştirilir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Konunun oluşturulması gereken kaynak grubu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Kaynak etiketlerini temsil eden hashtables 'lar.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. topluluklar. Hashtable

## ÇıKıŞLAR

### Microsoft. Azure. Commands. EventGrid. modeller. PSTopic

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
