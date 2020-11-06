---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: bfda87b4a0810dc440da63949d17f52cf611fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593442"
---
# Remove-AzureRmADSpCredential

## SYNOPSIS
Hizmet sorumlusunun kimlik bilgilerini kaldırır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### NesneKimliği (varsayılan)
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NesneKimliği
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithKeyIdParameterSet
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithAllParameterSet
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Remove-AzureRmADSpCredential cmdlet 'i, tehlikeye karşı veya kimlik bilgisi anahtarı geçişi süre sonunun bir parçası olarak bir hizmet sorumlusunun kimlik bilgilerini kaldırmak için kullanılabilir.
Hizmet sorumlusu, nesne KIMLIĞI veya hizmet asıl adı (SPN) sunarak tanımlanır.

Kaldırılacak kimlik bilgileri, tek bir kimlik bilgisinin kaldırılması veya bir ' tümü ' anahtarıyla, hizmet sorumlusu ile ilişkili tüm kimlik bilgilerinin silinmesi durumunda, bu kişinin anahtar KIMLIĞI tarafından tanımlanır.

## ÖRNEKLERDEN

### Örnek 1
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

Bu komut, hizmet sorumlusunun kimlik bilgilerini kaldırır.
Bu örnekte, "9044423a-60a3-45ac-9ab1-09534157ebb" kimliğine sahip anahtar hizmet sorumlusunun kaldırılacaktır.

### Örnek 2
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

Bu komut, hizmet sorumlusunun kimlik bilgilerini kaldırır.
Bu örnekte, tüm kimlik bilgileri, hizmet asıl adı "" ile ilişkilendirilmiş hizmet sorumlusunun altında kaldırılacaktır http://test123 .

## PARAMETRELERINE

### -Tümü
Hizmet sorumlusu ile ilişkili tüm kimlik bilgilerini kaldırmak için geçiş yapın.

```yaml
Type: SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Onay yapmadan kimlik bilgisini silmeye geçin.

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

### -KeyId
Kaldırılacak kimlik bilgileri anahtarını belirtir.
Hizmet sorumlusunun anahtar kimlikleri Get-AzureRmADSpCredential cmdlet kullanılarak elde edilebilir.

```yaml
Type: Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectID
Kimlik bilgilerini kaldırmak için hizmet sorumlusunun nesne kimliği.

```yaml
Type: String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
Kimlik bilgilerinin kaldırılacağı hizmet sorumlusunun adı (SPN).

```yaml
Type: String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmADSpCredential](./Get-AzureRmADSpCredential.md)

[Yeni-AzureRmADSpCredential](./New-AzureRmADSpCredential.md)

[Get-AzureRmADServicePrincipal](./Get-AzureRmADServicePrincipal.md)

