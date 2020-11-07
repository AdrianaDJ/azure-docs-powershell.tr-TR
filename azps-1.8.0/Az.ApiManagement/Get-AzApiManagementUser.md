---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 638B2BF6-23F8-4038-B20B-1CFABFDBF5D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementUser.md
ms.openlocfilehash: 1734eeb341d850f61fa3d5e930cabc26a4060de6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751139"
---
# Get-AzApiManagementUser

## SYNOPSIS
Bir kullanıcıyı veya kullanıcıları alır.

## INDEKI

### GeAllUsers (varsayılan)
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Getbyuserıd
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByUser
```
Get-AzApiManagementUser -Context <PsApiManagementContext> [-FirstName <String>] [-LastName <String>]
 [-State <PsApiManagementUserState>] [-Email <String>] [-GroupId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-Azapsananagementuser** cmdlet 'i belirtilen kullanıcıyı veya herhangi bir Kullanıcı belirtilmemişse tüm kullanıcıları alır.

## ÖRNEKLERDEN

### Örnek 1: tüm kullanıcıları alma
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext
```

Bu komut tüm kullanıcıları alır.

### Örnek 2: KIMLIĞE göre bir Kullanıcı alma
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -UserId "0123456789"
```

Bu komut bir kullanıcıyı KIMLIĞE göre alır.

### Örnek: kullanıcıları soyadına göre alma
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -LastName "Fuller"
```

Bu komut, belirli bir soyadınız olan kullanıcıları alır.

### Örnek 4: e-posta adresine göre Kullanıcı alma
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -Email "user@contoso.com"
```

Bu komut, belirtilen e-posta adresine sahip kullanıcıyı alır.

### Örnek 5: Grup içindeki tüm kullanıcıları alma
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementUser -Context $apimContext -GroupId "0001"
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

### -E-posta
Kullanıcının e-posta adresini belirtir.
Bu parametre belirtilmişse, bu cmdlet bir kullanıcıyı e-posta ile bulur.
Bu parametre isteğe bağlıdır.

```yaml
Type: System.String
Parameter Sets: GetByUser
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
Parameter Sets: GetByUser
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
Parameter Sets: GetByUser
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
Parameter Sets: GetByUser
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
Parameter Sets: GetByUser
Aliases:
Accepted values: Active, Blocked, Deleted, Pending

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
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementcontext

### System. String

### System. Nullable ' 1 [[Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuserstate, Microsoft. Azure. PowerShell. cmdlet

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Apsananamedi. ServiceManagement. modeller. Psapsananagementuser

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-Azsız Kullanıcı](./New-AzApiManagementUser.md)

[Remove-Azapsananagementuser](./Remove-AzApiManagementUser.md)

[Set-Azapsananagementuser](./Set-AzApiManagementUser.md)


