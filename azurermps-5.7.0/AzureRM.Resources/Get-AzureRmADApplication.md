---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: b44d3bbf7c594f5f9114488b536d28fd17fe56c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592915"
---
# Get-AzureRmADApplication

## SYNOPSIS
Var olan Azure Active Directory uygulamalarını listeler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### EmptyParameterSet (varsayılan)
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Applicationobjectivseçparameterset
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Applicationıdparameterset
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ApplicationDisplayNameParameterSet
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Applicationıdentifieruriparameterset
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
Var olan Azure Active Directory uygulamalarını listeler.
Uygulama araması objectID, ApplicationId, ıdentifieruri veya DisplayName tarafından yapılabilir.
Parametre sağlanmadıysa, kiracı altındaki tüm uygulamaları getirir.

## ÖRNEKLERDEN

### Örnek 1
```
PS E:\> Get-AzureRmADApplication
```

Kiracı 'nın altındaki tüm uygulamaları listeler.

### Örnek 2
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

URI değerini "" olarak alır http://mySecretApp1 .

## PARAMETRELERINE

### -ApplicationId
Getirilecek uygulamanın uygulama kimliği.

```yaml
Type: Guid
Parameter Sets: ApplicationIdParameterSet
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

### -DisplayNameStartWith
Görünen adla başlayan tüm uygulamaları getirir.

```yaml
Type: String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Identifieruri
Getirilecek uygulamanın benzersiz tanımlayıcı URI 'Si.

```yaml
Type: String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectID
Getirilecek uygulamanın nesne kimliği.

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdParameterSet
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

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

### System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication]

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-AzureRmADAppCredential](./Remove-AzureRmADAppCredential.md)

[Yeni-AzureRmADAppCredential](./New-AzureRmADAppCredential.md)

[Get-AzureRmADAppCredential](./Get-AzureRmADAppCredential.md)

[Remove-AzureRmADApplication](./Remove-AzureRmADApplication.md)

[Set-AzureRmADApplication](./Set-AzureRmADApplication.md)

[Yeni-AzureRmADApplication](./New-AzureRmADApplication.md)

