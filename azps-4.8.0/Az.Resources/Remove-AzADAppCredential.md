---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADAppCredential.md
ms.openlocfilehash: f6344590828663a0cf44d96d6fe733adff8757c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274004"
---
# Remove-AzADAppCredential

## SYNOPSIS
Uygulamadaki kimlik bilgilerini kaldırır.

## INDEKI

### Applicationobjectivseçwithkeyidparameterset (varsayılan)
```
Remove-AzADAppCredential -ObjectId <String> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Applicationıdwithkeyıdparameterset
```
Remove-AzADAppCredential -ApplicationId <Guid> [-KeyId <Guid>] [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ApplicationDisplayNameParameterSet
```
Remove-AzADAppCredential -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Applicationobjectwithkeyıdparameterset
```
Remove-AzADAppCredential [-KeyId <Guid>] -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
Remove-AzADAppCredential cmdlet 'i, tehlikeye karşı veya kimlik bilgisi anahtarı geçişi süre sonunun bir parçası olarak bir uygulamadan kimlik bilgileri kaldırmak için kullanılabilir.
Uygulama, nesne KIMLIĞI veya AppID sağlayarak tanımlanır.
Kaldırılacak kimlik bilgileri, anahtar KIMLIĞIYLE tanımlanır.

## ÖRNEKLERDEN

### Örnek 1: uygulamadan belirli bir kimlik bilgisini kaldırma

```powershell
PS C:\> Remove-AzADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

Anahtar kimliği ' 9044423a-60a3-45ac-9ab1-09534157ebb ' olan kimlik bilgisini uygulamadan nesne kimliği ' 7663d3fb-6f86-4352-9e6vseç-cf9vseç50vseç5ee82 ' ile kaldırır.

### Örnek 2: uygulamadaki tüm kimlik bilgilerini kaldırma

```powershell
PS C:\> Remove-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58
```

Uygulamadaki tüm kimlik bilgilerini ' 4589cd6b-3d79-4bb4-93b8-a0bfc58 ' uygulama kimliğiyle kaldırır.

### Örnek 3: boru kullanarak tüm kimlik bilgilerini kaldırma

```powershell
PS C:\> Get-AzADApplication -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 | Remove-AzADAppCredential
```

Uygulama kimliği ' 7663d3fb-6f86-4352-9e613-cf9vseç50vseç5ee82 ' ve Remove-AzADAppCredential kanallar ile bu uygulamadaki tüm kimlik bilgilerini kaldıran uygulamayı alır.

## PARAMETRELERINE

### -ApplicationId
Kimlik bilgilerinin kaldırılacağı uygulamanın kimliği.

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ApplicationObject
Kimlik bilgilerini kaldırmak için uygulama nesnesi.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -DisplayName
Uygulamanın görünen adı.

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Onay yapmadan kimlik bilgisini silmeye geçin.

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

### -KeyId
Kaldırılacak kimlik bilgileri anahtarını belirtir.
Uygulamanın anahtar kimlikleri, Get-AzADAppCredential cmdlet 'i kullanılarak elde edilebilir.

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectWithKeyIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectID
Kimlik bilgilerinin kaldırılacağı uygulamanın nesne kimliği.

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Geçiş
Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.

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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. Guid

### Microsoft. Azure. Commands. ActiveDirectory. PSADApplication

## ÇıKıŞLAR

### System. Boolean

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzADAppCredential](./Get-AzADAppCredential.md)

[New-AzADAppCredential](./New-AzADAppCredential.md)

[Get-AzADApplication](./Get-AzADApplication.md)
