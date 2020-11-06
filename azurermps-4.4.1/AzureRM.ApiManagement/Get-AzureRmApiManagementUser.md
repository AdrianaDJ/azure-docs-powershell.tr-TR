---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementUser.md
ms.openlocfilehash: be6c9ee6c0db12e324786052348209703b79601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587040"
---
# Get-AzureRmApiManagementUser

## SYNOPSIS
Bir kullanıcıyı veya kullanıcıları alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Tüm kullanıcıları al (varsayılan)
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### KIMLIĞE göre Kullanıcı alma
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Kullanıcıları bulma
```
Get-AzureRmApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azurermapsananagementuser** cmdlet 'i belirtilen kullanıcıyı veya herhangi bir Kullanıcı belirtilmemişse tüm kullanıcıları alır.

## ÖRNEKLERDEN

### Örnek 1: tüm kullanıcıları alma
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext
```

Bu komut tüm kullanıcıları alır.

### Örnek 2: KIMLIĞE göre bir Kullanıcı alma
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789"
```

Bu komut bir kullanıcıyı KIMLIĞE göre alır.

### Örnek: kullanıcıları soyadına göre alma
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -LastName "Fuller"
```

Bu komut, belirli bir soyadınız olan kullanıcıları alır.

### Örnek 4: e-posta adresine göre Kullanıcı alma
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -Email 
"user@contoso.com"
```

Bu komut, belirtilen e-posta adresine sahip kullanıcıyı alır.

### Örnek 5: Grup içindeki tüm kullanıcıları alma
```
PS C:\>Get-AzureRmApiManagementUser -Context $apimContext -GroupId "0001"
```

Bu komut belirtilen gruptaki tüm kullanıcıları alır.

## PARAMETRELERINE

### -Context
**Psapsananagementcontext** örneğini belirtir.

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -E-posta
Kullanıcının e-posta adresini belirtir.
Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı e-posta ile bulur.
Bu parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Ad
Kullanıcının adını belirtir.
Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı adıyla bulur.
Bu parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GroupID
Grup tanımlayıcısını belirtir.
Belirtilmişse, bu cmdlet belirtilen gruptaki tüm kullanıcıları bulur.
Bu parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LastName
Kullanıcının soyadını belirtir.
Belirtilmişse, bu cmdlet kullanıcıları soyadına göre bulur.
Bu parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: Find users
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Durumlu
Kullanıcı durumunu belirtir.
Belirtilmişse bu cmdlet bu durumda kullanıcıları bulur.
Bu parametre isteğe bağlıdır.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementUserState]
Parameter Sets: Find users
Aliases: 
Accepted values: Active, Blocked

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserID
Bir kullanıcı KIMLIĞI belirtir.
Belirtilmişse, bu cmdlet kullanıcıyı bu tanımlayıcıyla bulur.
Bu parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: Get user by ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## ÇıKıŞLAR

### IList<Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser>

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azurermapımanagementuser](./New-AzureRmApiManagementUser.md)

[Remove-Azurermapsananagementuser](./Remove-AzureRmApiManagementUser.md)

[Set-Azurermapımanagementuser](./Set-AzureRmApiManagementUser.md)


