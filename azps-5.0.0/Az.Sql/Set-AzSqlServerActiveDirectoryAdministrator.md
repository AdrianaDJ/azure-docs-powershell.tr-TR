---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveractivedirectoryadministrator
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: d450fa7795a530106a72180210d9cb133c7d3047
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322309"
---
# Set-AzSqlServerActiveDirectoryAdministrator

## SYNOPSIS
SQL Server için Azure AD yöneticisi sağlar.

## INDEKI

```
Set-AzSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Set-AzSqlServerActiveDirectoryAdministrator** cmdlet 'i, geçerli abonelikteki AzureSQL Server Için Azure Active Directory (Azure AD) Yöneticisi sağlar.
Aynı anda yalnızca bir yönetici temin edebilirsiniz.
Aşağıdaki Azure AD üyeleri SQL Server Yöneticisi olarak sağlanabilir:
- Yerel Azure AD üyeleri 
- Şirket içindeki Federasyon üyeleri 
- Yerel veya Federasyon üyesi olan diğer Azure reklamlardan alınan Üyeler 
- Güvenlik grupları olarak oluşturulan Azure AD grupları, Outlook.com, Hotmail.com veya Live.com etki alanlarında olduğu gibi, yöneticiler tarafından desteklenmez.
Gmail.com veya Yahoo.com etki alanlarında olduğu gibi diğer Konuk hesapları yöneticiler tarafından desteklenmez.
Adanmış bir Azure AD grubunu yönetici olarak sağlamanızı öneririz.

## ÖRNEKLERDEN

### Örnek 1: sunucu için yönetici grubu hazırlama
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- ---------------------------
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

Bu komut, server01 adlı sunucu için Vseçbas adlı bir Azure AD Yöneticisi grubu sağlar.
Bu sunucu, kaynak grubu ResourceGroup01 ile ilişkilendirilmiştir.

### Örnek 2: sunucu için Yönetici Kullanıcı sağlama
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9 False
```

Bu komut, server01 adlı sunucunun yöneticisi olarak bir Azure AD kullanıcısı sağlar.

### Örnek 3: KIMLIĞINI belirterek yönetici grubu hazırlama
```
PS C:\>Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId IsAzureADOnlyAuthentication 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b False
```

Bu komut, server01 adlı sunucu için Vseçbas adlı bir Azure AD Yöneticisi grubu sağlar.
Komut, *ObjectID* parametresi IÇIN bir kimlik belirtir.
Bu, grubun görünen adı benzersiz olmasa bile komutun başarılı olmasını sağlar.

## PARAMETRELERINE

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
Bu cmdlet 'in sağlamasını sağlayan Azure AD yöneticisinin görünen adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectID
Bu cmdlet 'in sağlamasını sağlayan Azure AD yöneticisinin benzersiz KIMLIĞINI belirtir.
Görünen ad benzersiz değilse, bu parametre için bir değer belirtmeniz gerekir.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Sunucunun atandığı kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Bu cmdlet 'in yönetici tarafından belirttiği SQL Server 'ın adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. Guid

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Sql. ServerActiveDirectoryAdministrator. model. Azureskreserveractivedirectoryadministratormodel

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzSqlServerActiveDirectoryAdministrator](./Get-AzSqlServerActiveDirectoryAdministrator.md)

[Remove-AzSqlServerActiveDirectoryAdministrator](./Remove-AzSqlServerActiveDirectoryAdministrator.md)

[Disable-AzSqlServerActiveDirectoryOnlyAuthentication](./Disable-AzSqlServerActiveDirectoryOnlyAuthentication.md)

[SQL veritabanı belgeleri](https://docs.microsoft.com/azure/sql-database/)


