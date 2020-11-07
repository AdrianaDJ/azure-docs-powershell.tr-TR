---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: b12369fb0a4140bea1693fd9074a601cd73fa9cd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752019"
---
# Get-AzEventGridDomainTopic

## SYNOPSIS
Bir olay Kılavuzu etki alanı konusunun ayrıntılarını alır veya geçerli Azure aboneliğindeki belirli bir olay Kılavuzu etki alanı altındaki tüm olay Kılavuzu etki alanı konularının listesini alır.

## INDEKI

### DomainTopicNameParameterSet (varsayılan)
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Resourceıddomaintopicparameterset
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Get-AzEventGridDomainTopic cmdlet 'i, belirli bir olay Kılavuzu etki alanı konusunun ayrıntılarını veya geçerli Azure aboneliğindeki belirli bir etki alanının altındaki tüm olay Kılavuzu etki alanı konularının listesini alır.
Etki alanı konu adı sağlanmışsa, tek bir olay Kılavuzu etki alanı konusunun ayrıntıları verilir.
Etki alanı konu adı sağlanmadıysa, belirtilen etki alanı adı altındaki etki alanı konularının listesi döndürülür. Bu listede döndürülen öğelerin sayısı üst parametre tarafından denetlenir. Üst değer belirtilmemişse veya $null, liste tüm etki alanı konuları öğelerini içerir. Aksi takdirde, en çok listede döndürülecek en fazla öğe sayısını belirtir.
Daha fazla etki alanı konusu hala kullanılabiliyorsa, sonraki çağrıda, etki alanı konularının sonraki sayfasını elde etmek için, NextLink 'teki değer kullanılmalıdır.
Son olarak, ODataQuery parametresi arama sonuçlarının filtrelenmesini gerçekleştirmek için kullanılır. Filtreleme sorgusu yalnızca Name özelliğini kullanarak OData söz dizimini takip eder. Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.

## ÖRNEKLERDEN

### Örnek 1

\` \` \` \` Myresourcegroupname kaynak grubundaki DomainTopic1 etki alanı domain1 altındaki olay \` Kılavuzu etki alanı konusunun ayrıntılarını alır \` .

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Örnek 2

\` \` \` \` \` RESOURCEID seçeneğini kullanarak myresourcegroupname kaynak grubundaki DomainTopic1 etki alanı konu başlığı altındaki olay Kılavuzu etki alanı konusunun ayrıntılarını \` .

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Örnek 3

\` \` \` Sayfalama olmadan myresourcegroupname kaynak grubunda domain1 \` (tüm sonuçlar tek bir görüntü içinde döndürülür)

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Örnek 4

Tüm olay Kılavuzu etki alanı domain1 'in altındaki \` \` \` myresourcegroupname kaynak grubundaki \` tüm olay Kılavuzu etki alanı başlıklarını listeleme

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Örnek 5

$OdataFilter etki alanı domain1 'in altındaki etki alanı altında, \` \` \` \` bir kerede 10 etki alanı Daha fazla sonuç kullanılabiliyorsa $result. NextLink $null olmaz. Etki alanı konularının sonraki sayfaları alabilmek için, kullanıcının Get-AzEventGridDomainTopic yeniden araması ve sonucu kullanması beklenir. Önceki çağrıdan edinilmiş bir bağlantı. Çağrı yapıldığında arayan durur. NextLink $null olur.

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## PARAMETRELERINE

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

### -EtkiAlanıAdı
EventGrid etki alanı adı.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
EventGrid etki alanı konu adı.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODataQuery
Liste sonuçlarının filtrelenmesini sağlayan OData sorgusu. Şu anda yalnızca Name özelliğinde filtreleme izni vardır. Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
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
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RESOURCEID
Olay Kılavuzu etki alanı veya kılavuz etki alanı konusunu temsil eden kaynak tanıtıcısı.

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Üst
Liste sonuçlarının filtrelenmesini sağlayan OData sorgusu. Şu anda yalnızca Name özelliğinde filtreleme izni vardır. Desteklenen işlemler şunları içerir: CONTAINS, EQ (eşittir), ne (eşit değildir için) ve veya DEĞIL.

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. Int32

## ÇıKıŞLAR

### Microsoft.Azure.Commands.EventGrid.Models.PSDOmainkonu başlığı

### Microsoft.Azure.Commands.EventGrid.Models.PSDOmaintopiclistınstance

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
