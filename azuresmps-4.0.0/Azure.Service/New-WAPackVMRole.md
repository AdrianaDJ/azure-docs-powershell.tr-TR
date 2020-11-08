---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6617AA59-CDD1-4BA9-84A7-F3914BF1D4B7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14e201dc916f15b63b0e825f4ca2e37015aaa9bc
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107390"
---
# New-WAPackVMRole

## SYNOPSIS
Sanal makine rolü oluşturur.

## INDEKI

### Hızlı oluştur (varsayılan)
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Fromchoparlör hizmeti
```
New-WAPackVMRole -Name <String> -Label <String> -ResourceDefinition <VMRoleResourceDefinition>
 -CloudService <CloudService> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Yeni-WAPackVMRole** cmdlet 'i sanal makine rolü oluşturur.

## ÖRNEKLERDEN

### Örnek 1: sanal makine rolü oluşturma (WAP)
```
PS C:\> New-WAPackVMRole -Name "ContosoVMRole01" -Label "ContosoVMRoleLabel01" -ResourceDefinition $resdef
```

Herhangi bir bulut hizmeti belirttiğimiz (WAP, WAP davranışı), komut, sanal makine rolüyle aynı ada sahip olacak bir bulut hizmeti oluşturur.
Bu durumda aşağıdaki komut, ContosoVMRole01 adında bir sanal makine rolü oluşturur.
Burada kullanılan kaynak tanımının PowerShell 'den el ile oluşturulması gerektiğini unutmayın.

## PARAMETRELERINE

### -CloudService
Sanal makine rolü için bir bulut hizmeti belirtir.

```yaml
Type: CloudService
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Sanal makine rolü için bir etiket belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Sanal makine rolü için bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceDefinition
Sanal makine rolü için bir kaynak tanımı belirtir.

```yaml
Type: VMRoleResourceDefinition
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-WAPackVMRole](./Get-WAPackVMRole.md)

[Remove-WAPackVMRole](./Remove-WAPackVMRole.md)

[Set-WAPackVMRole](./Set-WAPackVMRole.md)


