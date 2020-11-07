---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 5f019f413e7ae0efa2013412499fcf34bd94a248
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936468"
---
# Get-AzADApplication

## SYNOPSIS
Var olan Azure Active Directory uygulamalarını listeler.

## INDEKI

### EmptyParameterSet (varsayılan)
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### Applicationobjectivseçparameterset
```
Get-AzADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### Applicationıdparameterset
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### SearchStringParameterSet
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### Applicationıdentifieruriparameterset
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## Tanım
Var olan Azure Active Directory uygulamalarını listeler.
Uygulama araması objectID, ApplicationId, ıdentifieruri veya DisplayName tarafından yapılabilir.
Parametre sağlanmadıysa, kiracı altındaki tüm uygulamaları getirir.

## ÖRNEKLERDEN

### Örnek 1-tüm uygulamaları listeler

```
PS C:\> Get-AzADApplication
```

Kiracı 'nın altındaki tüm uygulamaları listeler.

### Örnek 2-sayfalama kullanarak uygulamaları listeleyin

```
PS C:\> Get-AzADApplication -First 100
```

Kiracı 'nın altındaki ilk 100 uygulamalarını listeler.

### Örnek 3-tanımlayıcı URI 'ye göre uygulama alın

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

URI değerini "" olarak alır http://mySecretApp1 .

### Örnek 4-nesne kimliğini kullanarak uygulamayı alın

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

Uygulama kimliği ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' olan uygulamayı alır.

## PARAMETRELERINE

### -ApplicationId
Getirilecek uygulamanın uygulama kimliği.

```yaml
Type: System.Guid
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

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
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayNameStartWith
Görünen adla başlayan tüm uygulamaları getirir.

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Önce
Döndürülecek en fazla nesne sayısı.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identifieruri
Getirilecek uygulamanın benzersiz tanımlayıcı URI 'Si.

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Includetoplamsayısı
Veri kümesindeki nesnelerin sayısını raporlar. Şu anda bu parametre hiçbir şey yapmaz.

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

### -ObjectID
Getirilecek uygulamanın nesne kimliği.

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Atla
İlk N nesneyi yoksayar ve kalan nesneleri alır.

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. Guid

### System. String

## ÇıKıŞLAR

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Remove-AzADAppCredential](./Remove-AzADAppCredential.md)

[New-AzADAppCredential](./New-AzADAppCredential.md)

[Get-AzADAppCredential](./Get-AzADAppCredential.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)

[Set-AzADApplication](./Set-AzADApplication.md)

[New-AzADApplication](./New-AzADApplication.md)

