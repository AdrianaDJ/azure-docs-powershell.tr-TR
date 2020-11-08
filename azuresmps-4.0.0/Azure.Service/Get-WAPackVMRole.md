---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D7EB9FE4-BDEB-43A5-B6D3-FEAB16BC2711
online version: ''
schema: 2.0.0
ms.openlocfilehash: 388277115281cbbacfb634ebdac5cdd9aa86b709
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107414"
---
# Get-WAPackVMRole

## SYNOPSIS

## INDEKI

### Boş (varsayılan)
```
Get-WAPackVMRole [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### FromName
```
Get-WAPackVMRole -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Fromchoparlör hizmeti
```
Get-WAPackVMRole -Name <String> -CloudServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

## ÖRNEKLERDEN

### Örnek 1: sanal makine rolünü alma (Portal aracılığıyla oluşturulur)
```
PS C:\> Get-WAPackVMRole -Name "ContosoVMRole01"
```

Bu komut, ContosoVMRole01 adındaki Portal aracılığıyla oluşturulan bir sanal makine rolünü alır.

### Örnek 2: ad ve bulut hizmet adını kullanarak sanal makine rolü alma
```
PS C:\> Get-WAPackVMRole -CloudServiceName "ContosoCloudService01" -Name "ContosoVMRole02"
```

Bu komut, ContosoCloudService01 adlı bir bulut hizmetinde ContosoVMRole02 adlı bir sanal makine rolünü alır.

### Örnek 3: tüm sanal makine rolünü alın
```
PS C:\> Get-WAPackVMRole
```

Bu komut, var olan tüm sanal makine rolünü alır.

## PARAMETRELERINE

### -Cloudhizmetadı
Sanal makine rolünün bulut hizmeti adını belirtir.

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Sanal makine rolünün adını belirtir.

```yaml
Type: String
Parameter Sets: FromName, FromCloudService
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-WAPackVMRole](./New-WAPackVMRole.md)

[Remove-WAPackVMRole](./Remove-WAPackVMRole.md)

[Set-WAPackVMRole](./Set-WAPackVMRole.md)


