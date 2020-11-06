---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 31F2AF24-488D-4CAF-A9C8-C8DAE76E031F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyDefinition.md
ms.openlocfilehash: 5140219c5392a7fb9c727998ae248d600edfde23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593020"
---
# New-AzureRmPolicyDefinition

## SYNOPSIS
İlke tanımı oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmPolicyDefinition -Name <String> [-DisplayName <String>] [-Description <String>] -Policy <String>
 [-Metadata <String>] [-Parameter <String>] [-Mode <PolicyDefinitionMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Tanım
**New-AzureRmPolicyDefinition** cmdlet 'ı JavaScript nesne GÖSTERIMI (JSON) biçiminde ilke kuralı içeren bir ilke tanımı oluşturur.

## ÖRNEKLERDEN

### Örnek 1: ilke dosyası kullanarak ilke tanımı oluşturma
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -Policy C:\VMPolicy.json
```

Bu komut, C:\VMPolicy.jsüzerinde belirtilen ilke kuralını içeren VMPolicyDefinition adlı bir ilke tanımı oluşturur.

### Örnek 2: satır içi ilke tanımı oluşturma
```
PS C:\>New-AzureRmPolicyDefinition -Name "VMPolicyDefinition" -DisplayName "Virtual Machine policy definition" -Policy "{""if"":{""source"":""action"",""equals"":""Microsoft.Compute/virtualMachines/write""},""then"":{""effect"":""deny""}}"
```

Bu komut VMPolicyDefinition adlı bir ilke tanımı oluşturur.
Komut ilkeyi geçerli JSON biçiminde bir dize olarak belirtir.

## PARAMETRELERINE

### -Apıversion
Kaynak sağlayıcı API 'sının kullanılacağı sürümü belirtir.
Bir sürüm belirtmezseniz, bu cmdlet en son sürümü kullanır.

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

### -Açıklama
İlke tanımının açıklamasını belirtir.

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

### -DisplayName
İlke tanımı için bir görünen ad belirtir.

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

### -Informationaction
Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

- 'A
- Manıza
- Sorgulamak
- Sustlıkdevam
- Durdurduğunuzda
- Biliriz

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationvariable
Bir bilgi değişkeni belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
İlke tanımı için bir ad belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parametre
İlke tanımı için parametreler bildirimi. Bu, Parameters bildirimini veya Parameters bildirimini içeren bir dosya adına yol olabilir.

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

### -İlke
İlke tanımı için bir ilke kuralı belirtir.
. Json dosyasının veya JSON biçimindeki ilkeyi içeren dizenin yolunu belirtebilirsiniz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre-
Bu cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlediği durumlarda sürüm API sürümlerini kabul ettiğini gösterir.

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

### -Metadata
İlke tanımı için meta veriler. Bu, meta veri veya meta veri içeren bir dosya adının yolu olabilir.

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

### -Mod
İlke tanımının modu.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyDefinitionMode]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### System. Management. Automation. PSObject

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmPolicyDefinition](./Get-AzureRmPolicyDefinition.md)

[Remove-AzureRmPolicyDefinition](./Remove-AzureRmPolicyDefinition.md)

[Set-AzureRmPolicyDefinition](./Set-AzureRmPolicyDefinition.md)


