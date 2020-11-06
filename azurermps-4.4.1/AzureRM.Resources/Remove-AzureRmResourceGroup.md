---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: 6938cf80f3fa6fb20252e1e4a212133ecd1c62a9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592557"
---
# Remove-AzureRmResourceGroup

## SYNOPSIS
Kaynak grubunu kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Ad temelinde kaynak grubunu listeler. Varsayýlan
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Kimliği temel alan kaynak grubunu listeler.
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Remove-AzureRmResourceGroup** cmdlet 'i, bir Azure kaynak grubunu ve kaynaklarını geçerli abonelikten kaldırır.
Kaynak grubundan çıkmak için Remove-AzureRmResource cmdlet 'ini kullanın.

## ÖRNEKLERDEN

### Örnek 1: kaynak grubunu kaldırma
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

Bu komut, ContosoRG01 kaynak grubunu abonelikten çıkarır.
Cmdlet sizden onay ister ve çıkış döndürmez.

### Örnek 2: onaysız kaynak grubunu kaldırma
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

Bu komut, ContosoRG01 kaynak grubunu almak için Get-AzureRmResourceGroup cmdlet 'ini kullanır ve ardından ardışık düzen işlecini kullanarak **-AzureRmResourceGroup öğesini kaldıracak** şekilde geçirir.
*Ayrıntılı* ortak parametre işlemle ilgili durum bilgilerini alır ve *Force* parametresi onay istemini bastırır.

### Örnek 3: tüm kaynak gruplarını kaldırma
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

Bu komut **Get-azurermresourcegroup** cmdlet 'ini kullanarak tüm kaynak gruplarını alır ve ardından bunları ardışık düzen işlecini kullanarak **-Azurermresourcegroup öğesini kaldıracak** şekilde geçirir.

## PARAMETRELERINE

### -Apıversion
Kaynak sağlayıcısı tarafından desteklenen API sürümünü belirtir.
Varsayılan sürümden farklı bir sürüm belirtebilirsiniz.

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

### -Force
Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.

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

### -ID
Kaldırılacak kaynak grubu KIMLIĞINI belirtir.
Joker karakterler kullanılamaz.

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the Id.
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Kaldırılacak kaynak gruplarının adlarını belirtir.
Joker karakterler kullanılamaz.

```yaml
Type: System.String
Parameter Sets: Lists the resource group based in the name.
Aliases: ResourceGroupName

Required: True
Position: 0
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

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Yabilirsiniz

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[Yeni-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)


