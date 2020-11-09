---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322903"
---
# Get-AzTemplateSpec

## SYNOPSIS
Şablon özelliklerinin alır veya listeler

## INDEKI

### ListTemplateSpecsParameterSet (varsayılan)
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetTemplateSpecByNameParameterSet
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Gettemplatespecbyıdparameterset
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Bu cmdlet, bir abonelik/kaynak grubundaki şablon özelliklerinin listesini oluşturmak veya ad veya kimlik ile belirli bir şablon belirtimi almak için kullanılabilir. Ad/kimlik ile belirli bir şablon belirtimini alırken, belirli bir sürüm isteğe bağlı olarak, **-Version** parametresi aracılığıyla bir sürüm adı belirtilerek alınabilir. **-Version** kullanıldığında * içinde yalnızca belirli sürüm ayrıntıları olacaktır *.* Döndürülen şablon belirtimi nesnesindeki sürümler. Bir şablon spec 'i Name/ID ile alırken belirli bir sürüm belirtilmemişse, tüm sürümler * içinde yer alır *.* Döndürülen nesnenin sürümler özelliği.

**Not** : bir abonelik veya kaynak grubundaki tüm şablon özelliklerinin listesi *Sürümler "* özelliği *boş* olur. Sürüm bilgileri yalnızca-Name veya-RESOURCEID parametreleri sağlandığında sunulur (örneğin: belirli bir şablon belirtimi/sürümü isteniyor).

## ÖRNEKLERDEN

### Örnek 1: geçerli abonelikteki liste şablonu özellikleri
```powershell
PS C:\> Get-AzTemplateSpec
```

Geçerli abonelikteki tüm şablon özelliklerinin listesini listeler.

### Örnek 2: kaynak grubundaki şablon özelliklerinin listesi
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Geçerli aboneliğin tüm şablon özelliklerinin ' myRG ' kaynak grubunda listelenir.

### Örnek 3: ada göre şablon belirtimi (tüm sürümlerle birlikte) alma
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

' MyRG ' kaynak grubunun içindeki ' MyTemplateSpec ' adlı şablon belirtimi hakkında bilgi alır.

**Not** : şablon belirtiminin tüm sürümleri " *.* , Return nesnesinin sürümü.

### Örnek 4: ada göre şablon belirtimi (belirli bir sürüm) alma
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

' MyRG ' kaynak grubunda ' MyTemplateSpec ' adlı şablon belirtiminin sürümü hakkında bilgi alır.

**Not** : *".* Döndürülen nesnenin sürümleri, yalnızca belirli bir sürümü içerir.

### Örnek 5: kaynak kimliğiyle şablon belirtimi (tüm sürümlerle birlikte) alma
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Abonelik alt kimliğindeki ' myRG ' kaynak grubunun içindeki ' MyTemplateSpec ' adlı şablon belirtimi hakkında bilgi alır \{ \} .

**Not** : şablon belirtiminin tüm sürümleri " *.* , Return nesnesinin sürümü.

### Örnek 6: kaynak kimliğiyle şablon belirtimi (belirli bir sürüm) alma
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Abonelik alt kimliğindeki ' myRG ' kaynak grubunda ' MyTemplateSpec ' adlı şablon belirtiminin sürümü hakkında bilgi alır \{ \} .

**Not** : *".* Döndürülen nesnenin sürümleri, yalnızca belirli bir sürümü içerir.

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

### -Ad
Şablon belirtiminin adı.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adı.

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RESOURCEID
Şablon belirtiminin tam kaynak kimliği. örnek:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Şablon belirtiminin sürümü.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. ResourceManager. cmdlet. Sdkmodeller. PSTemplateSpec

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
