---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicystatesummary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyStateSummary.md
ms.openlocfilehash: 4b4d45414a9a27561c3be4be195a1e5f77076e6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588422"
---
# Get-AzureRmPolicyStateSummary

## SYNOPSIS
Kaynaklar için en son ilke uyumluluk durumları özetini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### SubscriptionScope (varsayılan)
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ManagementGroupScope
```
Get-AzureRmPolicyStateSummary -ManagementGroupName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicySetDefinitionScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicySetDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### PolicyDefinitionScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyDefinitionName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### SubscriptionLevelPolicyAssignmentScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -PolicyAssignmentName <String> [-Top <Int32>]
 [-From <DateTime>] [-To <DateTime>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelPolicyAssignmentScope
```
Get-AzureRmPolicyStateSummary [-SubscriptionId <String>] -ResourceGroupName <String>
 -PolicyAssignmentName <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceScope
```
Get-AzureRmPolicyStateSummary -ResourceId <String> [-Top <Int32>] [-From <DateTime>] [-To <DateTime>]
 [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
En son ilke uyumluluk durumu numaralarının, ilke atamalarına ve ilke tanımlarına ayrılmış olan bir Özet görünümünü alır. Yalnızca uyumlu olmayan ilke durumlarını içerir.

## ÖRNEKLERDEN

### Örnek 1: geçerli abonelik kapsamındaki en son uyumlu olmayan ilke durumlarını alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.

### Örnek 2: belirtilen abonelik kapsamındaki en son uyumlu olmayan ilke durumlarını alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5"
```

Belirtilen abonelikteki tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.

### Örnek 3: yönetim grubu kapsamındaki en son uyumlu olmayan ilke durumlarını alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ManagementGroupName "myManagementGroup"
```

Belirtilen yönetim grubundaki tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.

### Örnek 4: geçerli abonelikteki kaynak grubu kapsamındaki en son uyumlu olmayan ilke durumlarını alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup"
```

Belirtilen kaynak grubundaki tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır (geçerli oturum bağlamındaki abonelikte).

### Örnek 5: belirtilen abonelikteki en son uyumlu olmayan ilke durumlarını kaynak grubu kapsamında alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -ResourceGroupName "myResourceGroup"
```

Belirtilen kaynak grubundaki (belirtilen abonelikteki) tüm kaynakların son gününde oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.

### Örnek 6: bir kaynağın en son uyumlu olmayan ilke durumlarını alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceId "/subscriptions/fff10b27-fff3-fff5-fff8-fffbe01e86a5/resourceGroups/myResourceGroup/providers/Microsoft.EventHub/namespaces/myns1/eventhubs/eh1/consumergroups/cg1"
```

Belirtilen kaynağın son günü oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.

### Örnek 7: geçerli abonelikteki ilke kümesi tanımı için uyumlu olmayan en son ilke durumlarının özetini alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Belirtilen ilke kümesi tanımıyla (geçerli oturum bağlamında bulunan abonelikte bulunan), tüm kaynaklar için son gün içinde oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.

### Örnek 8: belirtilen abonelikteki ilke kümesi tanımı için uyumlu olmayan en son ilke durumlarının özetini alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicySetDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Belirtilen ilke kümesi tanımıyla (belirtilen abonelikte var olan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.

### Örnek 9: geçerli abonelikteki ilke tanımının en son uyumlu olmayan ilke durumlarını alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Belirtilen ilke tanımı (geçerli oturum bağlamında bulunan abonelikte var) olan tüm kaynaklar için son gün içinde oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır (geçerli oturum bağlamındaki kiracı içinde).

### Örnek 10: belirtilen abonelikteki en son uyumlu olmayan ilke durumlarının bir ilke tanımı için özetini alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyDefinitionName "fff58873-fff8-fff5-fffc-fffbe7c9d697"
```

Belirtilen ilke tanımı (belirtilen abonelikte var olan) ile belirtilen tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.

### Örnek 11: geçerli abonelikteki ilke atamasının en son uyumlu olmayan ilke durumlarını alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Belirtilen ilke atamasında (geçerli oturum bağlamında bulunan abonelikte var), tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır (geçerli oturum bağlamındaki kiracı içinde).

### Örnek 12: belirtilen abonelikteki en son uyumlu olmayan ilke durumlarını alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -SubscriptionId "fff10b27-fff3-fff5-fff8-fffbe01e86a5" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Belirtilen ilke atamasında (belirtilen abonelikte var olan), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı 'da) oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.

### Örnek 13: geçerli abonelikteki belirtilen kaynak grubundaki ilke atamasının en son uyumlu olmayan ilke durumlarını alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -ResourceGroupName "myResourceGroup" -PolicyAssignmentName "ddd8ef92e3714a5ea3d208c1"
```

Belirtilen ilke atamasında (geçerli oturum bağlamındaki abonelikteki kaynak grubunda var), tüm kaynaklar için (geçerli oturum bağlamındaki kiracı içinde var) oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.

### Örnek 14: üst sorgu seçeneğiyle, geçerli abonelik kapsamındaki en son uyumlu olmayan ilke durumlarını alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Top 5
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır. Komut, sonuçlarda ilke ataması özetlerini uyumlu olmayan kaynak sayısına göre azalan şekilde sıralar ve bu ilke atama özetleri yalnızca ilk 5 ' i alır.

### Örnek 15: başlangıç ve kime sorgulama seçenekleriyle geçerli abonelik kapsamındaki en son uyumlu olmayan ilke durumlarını alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -From "2018-03-08 00:00:00Z" -To "2018-03-15 00:00:00Z"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için belirtilen tarih aralığında oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.

### Örnek 16: filtre sorgusu seçeneğiyle geçerli abonelik kapsamındaki en son uyumlu olmayan ilke durumlarını alma
```powershell
PS C:\> Get-AzureRmPolicyStateSummary -Filter "(PolicyDefinitionAction eq 'deny' or PolicyDefinitionAction eq 'audit') and ResourceLocation ne 'eastus'"
```

Geçerli oturum bağlamında, aboneliğin içindeki tüm kaynaklar için son gün oluşturulan en son ilke uyumluluk durumlarının Özet görünümünü alır.
Komut, filtreleme tarafından döndürülen sonuçları ilke tanımı eylemine (reddetme veya Denetim eylemleri içerir) ve kaynak konumuna (eastus konumunu dışlar) göre sınırlandırır.

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

### Microsoft. Azure. Commands. Policınsi. model. PolicyStateSummary

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmPolicyState](./Get-AzureRmPolicyState.md)
