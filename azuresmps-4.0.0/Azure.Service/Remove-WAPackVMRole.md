---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107411"
---
# Remove-WAPackVMRole

## SYNOPSIS
Sanal makine rolü nesnelerini kaldırır.

## INDEKI

### FromVMRoleObject (varsayılan)
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Fromchoparlör hizmeti
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Bu konular kullanım dışıdır ve gelecekte kaldırılacaktır.
Bu konuda, Microsoft Azure PowerShell modülünün 0.8.1 sürümündeki cmdlet açıklanmaktadır.
Kullandığınız modülün sürümünü bulmak için, Azure PowerShell konsolundan yazın `(Get-Module -Name Azure).Version` .

**Remove-WAPackVMRole** cmdlet 'i sanal makine rol nesnelerini kaldırır.

## ÖRNEKLERDEN

### Örnek 1: sanal makine rolünü kaldırma (WAP Portalı kullanılarak oluşturulmuş)
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

İlk komut ContosoVMRole01 adındaki sanal makine rolünü **Get-WAPackVMRole** cmdlet 'ini kullanarak alır ve bu nesneyi $VMRole değişkeninde depolar.

İkinci komut, $VMRole depolanan sanal makine rolünü kaldırır.
Komut sizden onaylamanızı ister. Bu sanal makine rolünün WAP Portalı kullanılarak oluşturulduğunu varsayarsak, bulut hizmeti adını belirtmeniz gerekmez.

### Örnek 2: el ile bulut hizmeti oluşturulduktan sonra oluşturulan bir sanal makine rolünü kaldırma
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

İlk komut, **Get-WAPackVMRole** cmdlet 'ini kullanarak "ContosoVMRole02" adlı sanal makine rolünü alır ve bu nesneyi $VMRole değişkeninde depolar.

İkinci komut, $VMRole depolanan sanal makine rolünü kaldırır.
Komut sizden onaylamanızı ister.
Bu sanal makine rolünün Portal kullanılarak oluşturulmamış olduğunu varsayarsak, kullanıcının bulut hizmeti adını belirtmesi gerekmektedir.
Bu durumda, "ContosoCloudService02".

### Örnek 3: onaysız sanal makine rolünü kaldırma
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

İlk komut ContosoVMRole03 adındaki bulut hizmetini **Get-WAPackVMRole** cmdlet 'ini kullanarak alır ve bu nesneyi $VMRole değişkeninde depolar.

İkinci komut, $VMRole depolanan sanal makine rolünü kaldırır.
Bu komut *Force* parametresini içerir.
Komut sizden onay istemez.

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
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Geçiş
Çalıştığınız öğeyi temsil eden bir nesne döndürür.
Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -VMRole
Sanal makine rolünü belirtir.
Sanal makine rolünü almak için **Get-WAPackVMRole** cmdlet 'ini kullanın.

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-WAPackVMRole](./Get-WAPackVMRole.md)

[Yeni-WAPackVMRole](./New-WAPackVMRole.md)

[Set-WAPackVMRole](./Set-WAPackVMRole.md)


