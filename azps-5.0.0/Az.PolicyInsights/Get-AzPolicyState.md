---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyState.md
ms.openlocfilehash: 04600529ded8b95da578d59f0b2f46cd396594ba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276869"
---
# Get-AzPolicyState

## SYNOPSIS
Kaynaklar için ilke uyumluluk durumlarını alır.

## INDEKI

### SubscriptionScope (varsayılan)
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzPolicyState [-All] -ManagementGroupName <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzPolicyState [-All] -ResourceId <String> [-Top <Int32>] [-OrderBy <String>] [-Select <String>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-Apply <String>] [-Expand <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzPolicyState [-All] [-SubscriptionId <String>] -ResourceGroupName <String> -PolicyAssignmentName <String>
 [-Top <Int32>] [-OrderBy <String>] [-Select <String>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-Apply <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
Kaynaklar için ilke uyumluluk durumlarını alır. İlke durumu kayıtları çeşitli kapsamlarda sorgulanamaz. Belirtilen zaman aralığına dayalı (varsayılan son güne göre), en son ilke durumları veya tüm ilke durumu geçişleri sorgulanabilir. Sonuçlar filtrelenebilir, gruplandırılır ve grup toplamaları hesaplanır.

## ÖRNEKLERDEN

### Örnek 1: geçerli abonelik kapsamındaki en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır.

### Örnek 2: belirtilen abonelik kapsamındaki en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Belirtilen abonelikteki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır.

### Örnek 3: geçerli abonelik kapsamındaki tüm ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -All
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün içinde oluşturulan tüm geçmiş ilke durumu kayıtlarını (en son dahil) alır.

### Örnek 4: yönetim grubu kapsamındaki en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -ManagementGroupName "myManagementGroup"
```

Belirtilen yönetim grubundaki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır.

### Örnek 5: geçerli abonelikteki kaynak grubu kapsamındaki en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup"
```

Belirtilen kaynak grubundaki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır (geçerli oturum bağlamındaki abonelikte).

### Örnek 6: belirtilen abonelikteki kaynak grubu kapsamındaki en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Belirtilen kaynak grubundaki (belirtilen abonelikteki) tüm kaynakların son gününde oluşturulan en son ilke durumu kayıtlarını alır.

### Örnek 7: kaynağın en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Belirtilen kaynağın son günü oluşturulan en son ilke durumu kayıtlarını alır.

### Örnek 8: geçerli abonelikteki bir ilke kümesi tanımı için en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Belirtilen ilke kümesi tanımıyla (geçerli oturum bağlamında bulunan abonelikte bulunan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı içinde var) oluşturulan en son ilke durumu kayıtlarını alır.

### Örnek 9: belirtilen abonelikteki ilke kümesi tanımı için en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Belirtilen ilke kümesi tanımıyla (belirtilen abonelikte var olan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan en son ilke durumu kayıtlarını alır.

### Örnek 10: geçerli abonelikteki ilke tanımı için en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Belirtilen ilke tanımı (geçerli oturum bağlamında bulunan abonelikte var) olan tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır (geçerli oturum bağlamındaki kiracı içinde).

### Örnek 11: belirtilen abonelikteki ilke tanımı için en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Belirtilen ilke tanımı (belirtilen abonelikte var olan) ile belirtilen tüm kaynaklar için (geçerli oturum bağlamında kiracı içinde) oluşturulan en son ilke durumu kayıtlarını alır.

### Örnek 12: geçerli abonelikteki ilke atamasının en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Belirtilen ilke atamasında (geçerli oturum bağlamında bulunan abonelikte var), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı içinde var) oluşturulan en son ilke durumu kayıtlarını alır.

### Örnek 13: belirtilen abonelikteki ilke atamasının en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Belirtilen ilke atamasında (belirtilen abonelikte var olan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan en son ilke durumu kayıtlarını alır.

### Örnek 14: geçerli abonelikteki belirtilen kaynak grubundaki ilke atamasının en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Belirtilen ilke atamasında (geçerli oturum bağlamında, geçerli oturum bağlamındaki kiracı içinde var), belirtilen ilke atamasındaki tüm kaynaklar (geçerli oturum bağlamındaki kiracı içinde var) ile oluşturulan en son ilke durumu kayıtlarını alır.

### Örnek 15: OrderBy, top ve Select sorgu seçenekleri
```powershell
PS C:\> Get-AzPolicyState -OrderBy "Timestamp desc, PolicyAssignmentName asc" -Top 5 -Select "Timestamp, ResourceId, PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionId, IsCompliant"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır. Komut sonuçları zaman damgası ve ilke atama adı özelliklerine göre sıralar ve yalnızca bu sırada listelenen ilk 5 ' i alır.
Ayrıca, her kayıt için sütunların yalnızca bir alt kümesini listelemek için de seçilir.

### Örnek 16: başlangıç ve kime sorgulama seçenekleriyle geçerli abonelik kapsamındaki en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için belirtilen tarih aralığında oluşturulan en son ilke durumu kayıtlarını alır.

### Örnek 17: filtre sorgusu seçeneğiyle geçerli abonelik kapsamındaki en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ComplianceState eq 'NonCompliant' and ResourceLocation ne 'eastus'"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır.
Komut, filtreleme tarafından döndürülen sonuçları ilke tanımı eylemine göre (reddetme veya Denetim eylemleri içerir), uyumluluk durumunu (yalnızca uyumlu olmayan durum içerir) ve kaynak konumunu (dışlar eastus Location) sınırlar.

### Örnek 18: geçerli abonelik kapsamındaki en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -Apply "aggregate(`$count as NumberOfRecords)"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarının sayısını alır.
Komut, AdditionalProperties özelliği içinde döndürülen ilke durumu kayıtlarının sayısını döndürür.

### Örnek 19: toplama ile gruplandırma belirtmeye Uygula
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumStates))" -OrderBy "NumStates desc" -Top 5
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır. Komut, uyumluluk durumuna bağlı olarak filtreleme tarafından döndürülen sonuçları sınırlar (yalnızca uyumlu olmayan durumu içerir).
Bu, ilke atamasını, ilke kümesi tanımını ve ilke tanımına dayalı olarak sonuçları gruplandırır ve her gruptaki, AdditionalProperties özelliğinin içinde döndürülen kayıtların sayısını hesaplar.
Sonuçları azalan düzende sayma toplamı olarak sıralar ve yalnızca bu sırada listelenen ilk 5 ' i alır.

### Örnek 20: toplama olmadan gruplandırma belirtmeye Uygula
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((ResourceId))"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır. Komut, uyumluluk durumuna bağlı olarak filtreleme tarafından döndürülen sonuçları sınırlar (yalnızca uyumlu olmayan durumu içerir).
Bu, sonuçları kaynak koduna göre gruplandırır. Bu, abonelikteki en az bir ilke için uyumlu olmayan tüm kaynakların listesini oluşturur.

### Örnek 21: geçerli abonelik kapsamındaki en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -Filter "ComplianceState eq 'NonCompliant'" -Apply "groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId, ResourceId))/groupby((PolicyAssignmentId, PolicySetDefinitionId, PolicyDefinitionReferenceId, PolicyDefinitionId), aggregate(`$count as NumNonCompliantResources))" -OrderBy "NumNonCompliantResources desc" -Top 5
```

### Örnek 22: kaynağın ilke değerlendirme ayrıntıları dahil en son ilke durumlarını alma
```powershell
PS C:\> Get-AzPolicyState -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1" -Expand "PolicyEvaluationDetails"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke durumu kayıtlarını alır. Komut, uyumluluk durumuna bağlı olarak filtreleme tarafından döndürülen sonuçları sınırlar (yalnızca uyumlu olmayan durumu içerir).
İlk önce, ilke atamasını, ilke kümesi tanımını, ilke tanımını ve kaynak kimliğini temel alarak sonuçları gruplar. Ardından, bu gruplandırmanın sonuçlarını kaynak kimliği dışında aynı özelliklere göre gruplandırır ve bu gruplardan her birinde, AdditionalProperties özelliğinin içinde döndürülen kayıtların sayısını hesaplar.
Sonuçları azalan düzende sayma toplamı olarak sıralar ve yalnızca bu sırada listelenen ilk 5 ' i alır.
Bu, en çok uyumlu olmayan kaynakların ilk 5 ilkesini oluşturur.

## PARAMETRELERINE

### -Tümü
Belirtilen zaman aralığında, yalnızca en son yerine tüm ilke durumlarına ulaşın.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Genişletme
OData gösterimini kullanarak genişletme ifadesi.

```yaml
Type: System.String
Parameter Sets: ResourceScope
Aliases:

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Policınsi. model. PolicyState

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azilkestatesummary](./Get-AzPolicyStateSummary.md)
