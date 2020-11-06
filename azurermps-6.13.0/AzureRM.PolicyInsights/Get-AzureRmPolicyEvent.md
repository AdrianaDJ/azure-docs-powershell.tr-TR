---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyEvent.md
ms.openlocfilehash: 0c4e4f531dac3f75f0eff69ba1dcfc644473ea06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591302"
---
# Get-AzureRmPolicyEvent

## SYNOPSIS
Kaynaklar oluşturulurken veya güncelleştirildiğinde oluşturulan ilke değerlendirme olaylarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### SubscriptionScope (varsayılan)
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzureRmPolicyEvent -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzureRmPolicyEvent [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzureRmPolicyEvent -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Kaynaklar oluşturulurken veya güncelleştirildiğinde oluşturulan ilke değerlendirme olaylarını alır. İlke olay kayıtları, belirtilen zaman aralığına göre (varsayılan olarak son güne Sonuçlar filtrelenebilir, gruplandırılır ve grup toplamaları hesaplanır.

## ÖRNEKLERDEN

### Örnek 1: geçerli abonelik kapsamındaki ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır.

### Örnek 2: belirtilen abonelik kapsamındaki ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Belirtilen abonelikteki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır.

### Örnek 3: yönetim grubu kapsamındaki ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -ManagementGroupName "myManagementGroup"
```

Belirtilen yönetim grubundaki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır.

### Örnek 4: geçerli abonelikteki kaynak grubu kapsamındaki ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup"
```

Belirtilen kaynak grubundaki tüm kaynaklar için (geçerli oturum bağlamındaki abonelikte) oluşturulan ilke olayı kayıtlarını alır.

### Örnek 5: belirtilen abonelikteki kaynak grubu kapsamındaki ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Belirtilen kaynak grubundaki tüm kaynakların (belirtilen abonelikteki) son gününde oluşturulan ilke olay kayıtlarını alır.

### Örnek 6: kaynağın ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Belirtilen kaynağın son günü oluşturulan ilke olayı kayıtlarını alır.

### Örnek 7: geçerli abonelikteki bir ilke kümesi tanımı için ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Belirtilen ilke kümesi tanımıyla (geçerli oturum bağlamında bulunan abonelikte bulunan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da var) oluşturulan ilke olayı kayıtlarını alır.

### Örnek 8: belirtilen abonelikteki ilke kümesi tanımı için ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Belirtilen ilke kümesi tanımıyla (belirtilen abonelikte var olan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan ilke olayı kayıtlarını alır.

### Örnek 9: geçerli abonelikteki ilke tanımı için ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Belirtilen ilke tanımında (geçerli oturum bağlamında bulunan abonelikte var), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı içinde var) oluşturulan ilke olayı kayıtlarını alır.

### Örnek 10: belirtilen abonelikteki ilke tanımı için ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Belirtilen ilke tanımı (belirtilen abonelikte var olan) ile belirtilen tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan ilke olayı kayıtlarını alır.

### Örnek 11: geçerli abonelikteki bir ilke atamasının ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Belirtilen ilke atamasında (geçerli oturum bağlamındaki abonelikte var), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı içinde var) oluşturulan ilke olayı kayıtlarını alır.

### Örnek 12: belirtilen abonelikteki ilke atamasının ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Belirtilen ilke atamasında (belirtilen abonelikte var olan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan ilke olayı kayıtlarını alır.

### Örnek 13: geçerli abonelikteki belirtilen kaynak grubundaki ilke atamasının ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Belirtilen ilke atamasında (geçerli oturum bağlamında, aboneliğin kaynak grubunda var), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı içinde var) oluşturulan ilke olayı kayıtlarını alır.

### Örnek 14: OrderBy, top ve Select sorgu seçenekleriyle geçerli abonelik kapsamındaki ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır. Komut sonuçları zaman damgası ve ilke atama adı özelliklerine göre sıralar ve yalnızca bu sırada listelenen ilk 5 ' i alır.
Ayrıca, her kayıt için sütunların yalnızca bir alt kümesini listelemek için de seçilir.

### Örnek 15: başlangıç ve son sorgulama seçenekleriyle ilke olaylarını geçerli abonelik kapsamına alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için belirtilen tarih aralığında oluşturulan ilke olayı kayıtlarını alır.

### Örnek 16: filtre sorgusu seçeneğiyle geçerli abonelik kapsamındaki ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır.
Komut, filtreleme tarafından döndürülen sonuçları ilke tanımı eylemine dayalı olarak sınırlar (reddetme veya Denetim eylemleri içerir) ve kaynak konumu (eastus konumunu dışlar).

### Örnek 17: geçerli abonelik kapsamındaki ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -Apply "aggregate(`$count as NumberOfRecords)"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarının sayısını alır.
Komut, AdditionalProperties özelliği içinde döndürülen ilke olay kayıtlarının sayısını döndürür.

### Örnek 18: geçerli abonelik kapsamındaki ilke olaylarını toplama ile gruplandırma
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, PolicyDefinitionAction, ResourceId), aggregate(`$count as NumEvents))" -OrderBy "NumEvents desc" -Top 5
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır. Komut, filtreleme tarafından döndürülen sonuçları ilke tanımı eylemine göre sınırlar (yalnızca denetleme ve reddetme olaylarını içerir).
Bu, ilke atamasını, ilke tanımını, ilke tanımı eylemini ve kaynak kimliğini temel alarak sonuçları gruplandırır ve her gruptaki, AdditionalProperties özelliğinin içinde döndürülen kayıtların sayısını hesaplar.
Sonuçları azalan düzende sayma toplamı olarak sıralar ve yalnızca bu sırada listelenen ilk 5 ' i alır.

### Örnek 19: toplama olmadan gruplandırma belirtme
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'audit' or PolicyDefinitionAction eq 'deny'" -Apply "groupby((ResourceId))"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır. Komut, filtreleme tarafından döndürülen sonuçları ilke tanımı eylemine göre sınırlar (yalnızca denetleme ve reddetme olaylarını içerir).
Bu, sonuçları kaynak koduna göre gruplandırır. Bu, en az bir denetleme veya reddetme ilkesi için ilke olayı üreten abonelikteki tüm kaynakların listesini oluşturur.

### Örnek 20: geçerli abonelik kapsamındaki ilke olaylarını alma
```powershell
PS C:\> Get-AzureRmPolicyEvent -Filter "PolicyDefinitionAction eq 'deny'" -Apply "groupby((PolicyAssignmentId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicyDefinitionId), aggregate(`$count as NumDeniedResources))" -OrderBy "NumDeniedResources desc" -Top 5
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan ilke olay kayıtlarını alır. Komut, filtreleme tarafından döndürülen sonuçları ilke tanımı eylemine göre sınırlar (yalnızca reddetme olaylarını içerir).
İlk önce, ilke atamasını, ilke tanımını ve kaynak kimliğini temel alarak sonuçları gruplar. Ardından, bu gruplandırmanın sonuçlarını kaynak kimliği dışında aynı özelliklere göre gruplandırır ve bu gruplardan her birinde, AdditionalProperties özelliğinin içinde döndürülen kayıtların sayısını hesaplar.
Sonuçları azalan düzende sayma toplamı olarak sıralar ve yalnızca bu sırada listelenen ilk 5 ' i alır.
Bu, en fazla reddedilen kaynağa sahip ilk 5 reddetme politikalarını oluşturur.

## PARAMETRELERINE

### -Uygulama
OData gösterimini kullanarak toplamalar için ifade uygulayın.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filtre
OData gösterimini kullanan filtre ifadesi.

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

### 'Den
Sorgulanacak aralığın başlangıç saatini belirten ISO 8601 biçimli zaman damgası.
Belirtilmediğinde, varsayılan olarak ' to ' parametre değeri eksi 1 gün olur.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupName
Yönetim grubu adı.

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrderBy
OData gösterimini kullanan sıralama ifadesi.
İsteğe bağlı bir ' DESC ' (varsayılan) veya ' ASC ' içeren bir veya daha fazla virgülle ayrılmış sütun adı.

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

### -PolicyAssignmentName
İlke atama adı.

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionName
İlke tanımı adı.

```yaml
Type: System.String
Parameter Sets: PolicyDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicySetDefinitionName
İlke kümesi tanım adı.

```yaml
Type: System.String
Parameter Sets: PolicySetDefinitionScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
Kaynak KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Select
OData gösterimini kullanarak ifade seçin.
Bir veya daha fazla virgülle ayrılmış sütun adı.
Her kayıttaki sütunları yalnızca bu kişilere sınırlar.

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
Abonelik KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, ResourceGroupScope, PolicySetDefinitionScope, PolicyDefinitionScope, SubscriptionLevelPolicyAssignmentScope, ResourceGroupLevelPolicyAssignmentScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -To
ISO 8601 biçimlendirilmiş aralığın bitiş zamanını belirten biçimlendirilmiş zaman damgası.
Belirtilmediğinde, isteğin süresi varsayılan olur.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Üst
Döndürülecek en fazla kayıt sayısı.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Policınsi. model. PolicyEvent

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
