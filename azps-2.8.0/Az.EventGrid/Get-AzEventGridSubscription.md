---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 987882928ee215ed2da842e924386f5dec8b862f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752014"
---
# Get-AzEventGridSubscription

## SYNOPSIS
Bir olay aboneliğinin ayrıntılarını alır veya geçerli Azure aboneliğindeki tüm olay aboneliklerinin listesini alır.

## INDEKI

### EventSubscriptionTopicNameParameterSet (varsayılan)
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Get-AzEventGridSubscription cmdlet 'i, belirli bir olay Kılavuzu aboneliğinin ayrıntılarını veya geçerli Azure aboneliğindeki veya kaynak grubundaki tüm olay Kılavuzu aboneliklerinin listesini alır.
Olay aboneliği adı sağlanmışsa, tek bir olay Kılavuzu aboneliğinin ayrıntıları döndürülür.
Olay aboneliği adı sağlanmazsa, tüm olay abonelikleri listesi döndürülür. Bu listede döndürülen öğelerin sayısı üst parametre tarafından denetlenir. Üst değer belirtilmemişse veya $null, liste tüm olay aboneliği öğelerini içerir. Aksi takdirde, en çok listede döndürülecek en fazla öğe sayısını belirtir.
Daha fazla etkinlik hala kullanılabilirse, sonraki çağrıda, bir sonraki olay abonelikleri sayfasını elde etmek için NextLink 'teki değer kullanılmalıdır.
Son olarak, ODataQuery parametresi arama sonuçlarının filtrelenmesini gerçekleştirmek için kullanılır. Filtreleme sorgusu yalnızca Name özelliğini kullanarak OData söz dizimini takip eder. Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

\` \` \` \` Myresourcegroupname kaynak grubundaki konu konu1 EventSubscription1 için oluşturulan olay \` aboneliği ayrıntılarını alır \` .

### Örnek 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

\` \` \` \` \` \` Web kancası tabanlı bir olay aboneliği olan tam uç nokta URL 'si de dahil olmak üzere, myresourcegroupname kaynak grubundaki konu konu1 için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır.

### Örnek 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

\` \` \` Sayfalandırmadan myresourcegroupname kaynak grubundaki konu1 konu için oluşturulan tüm olay aboneliklerinin listesini edinin \` .

### Örnek 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

\` \` \` $OdataFilter sorgusunu karşılayan myresourcegroupname kaynak grubundaki konu konu1 için oluşturulmuş ilk 10 olay aboneliğini (varsa) listeleyin \` . Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz. Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı. Çağrı yapıldığında arayan durur. NextLink $null olur.

### Örnek 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

\` \` Myresourcegroupname kaynak grubu için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır \` \` .

### Örnek 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

\` \` Seçili Azure aboneliği için oluşturulan olay aboneliği EventSubscription1 ayrıntılarını alır.

### Örnek 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Sayfalandırmadan myresourcegroupname kaynak grubu altında oluşturulan tüm genel olay aboneliklerinin listesini alır \` \` .

### Örnek 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

\`$OdataFilter sorgusunu karşılayan myresourcegroupname kaynak grubu altında oluşturulmuş ilk 5 olay aboneliğini listeleyin \` . Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz. Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı. Çağrı yapıldığında arayan durur. NextLink $null olur.

### Örnek 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Seçili Azure aboneliği altında, sayfalandırmadan oluşturulan tüm genel olay aboneliklerinin listesini alır.

### Örnek 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Seçili Azure aboneliği altında, $odataFilter sorgusunu karşılayan ilk 15 genel etkinlik aboneliğini (varsa) listeleyin. Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz. Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı. Çağrı yapıldığında arayan durur. NextLink $null olur.

### Örnek 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

\` \` Westus2 belirtilen konumunda, sayfalandırmadan belirtilen myresourcegroupname kaynak grubu altında oluşturulan tüm bölgesel olay aboneliklerinin listesini alır \` \` .

### Örnek 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Belirtilen konumdaki myresourcegroupname kaynak grubu altında oluşturulmuş ilk 15 bölgesel etkinlik aboneliğini (varsa), \` \` \` \` $odataFilter sorgusunu karşılayan westus2. Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz. Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı. Çağrı yapıldığında arayan durur. NextLink $null olur.

### Örnek 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Belirtilen EventHub ad alanı için oluşturulan tüm olay aboneliklerinin listesini sayfalandırmadan alır.

### Örnek 14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

$OdataFilter sorgusunu karşılayan belirtilen EventHub ad alanı için oluşturulmuş ilk 25 olay aboneliğini (varsa) listeleyin. Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz. Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı. Çağrı yapıldığında arayan durur. NextLink $null olur.

### Örnek 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Belirtilen konu türü (EventHub ad alanları) için oluşturulan tüm olay aboneliklerinin listesini sayfalandırmadan belirtilen konumda alır.

### Örnek 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Belirtilen konum türü (EventHub ad alanları) için oluşturulmuş ilk 15 olay aboneliğini, $odataFilter sorgusunu karşılayan belirtilen konumda listeleyin. Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz. Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı. Çağrı yapıldığında arayan durur. NextLink $null olur.

### Örnek 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Belirli bir kaynak grubu için oluşturulan tüm olay aboneliklerinin listesini sayfalandırmadan alır.

### Örnek 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

$OdataFilter sorgusunu karşılayan belirli bir kaynak grubu için oluşturulmuş ilk 100 olay aboneliğini (varsa) listeleyin. Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz. Olay aboneliklerinin sonraki sayfaları almak için kullanıcının Get-AzEventGridSubscription yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı. Çağrı yapıldığında arayan durur. NextLink $null olur.

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

### -Domainınputobject
Olay Kılavuzu

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -EtkiAlanıAdı
EventGrid etki alanı adı.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DomainTopicInputObject
EventGrid etki alanı konu nesnesi.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainTopicName
EventGrid etki alanı konu adı.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
Olay aboneliğinin adı

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Olay aboneliği hedefinin tam uç nokta URL 'sini ekleyin.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
EventGrid konu nesnesi.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Konum
Konumuyla

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Gönderilecek kaynakların sonraki sayfasının bağlantısı. Bu değer, daha fazla kaynak sorgulanmaya devam edildiğinde ilk Get-AzEventGrid cmdlet çağrısıyla elde edilir.

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
Liste sonuçlarının filtrelenmesini sağlayan OData sorgusu. Şu anda yalnızca Name özelliğinde filtreleme izni vardır. Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
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
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
Olay aboneliklerinin oluşturulduğu kaynağın tanıtıcısı.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Üst
Liste sonuçlarının filtrelenmesini sağlayan OData sorgusu. Şu anda yalnızca Name özelliğinde filtreleme izni vardır. Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
EventGrid konu adı.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
TopicType adı

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### Microsoft. Azure. Commands. EventGrid. modeller. PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDOmainkonu başlığı

### System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## ÇıKıŞLAR

### Microsoft. Azure. Commands. EventGrid. modeller. PSEventSubscription

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
