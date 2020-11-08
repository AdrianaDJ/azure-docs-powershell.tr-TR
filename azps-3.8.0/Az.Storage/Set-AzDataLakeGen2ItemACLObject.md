---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2itemaclobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2ItemACLObject.md
ms.openlocfilehash: d16a476bea988afb53ddff7b34a83658e0f274e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096705"
---
# Set-AzDataLakeGen2ItemAclObject

## SYNOPSIS
Update-AzDataLakeGen2Item cmdlet 'te kullanılabilen bir DataLake Gen2 Item ACL nesnesi oluşturur/güncelleştirir.

## INDEKI

```
Set-AzDataLakeGen2ItemAclObject [-EntityId <String>] [-DefaultScope] -Permission <String>
 [-InputObject <PSPathAccessControlEntry[]>] -AccessControlType <AccessControlType> [<CommonParameters>]
```

## Tanım
**Set-AzDataLakeGen2ItemAclObject** cmdlet 'i, Update-AzDataLakeGen2Item cmdlet 'te kullanılabilen bir datalake Gen2 Item ACL nesnesi oluşturur/güncelleştirir.
Giriş ACL 'de aynı AccessControlType/EntityId/DefaultScope içeren yeni ACL girişi yoksa, yeni bir ACL girişi oluşturur, başka bir ACL girdisi oluşturur.

## ÖRNEKLERDEN

### Örnek 1:3 ACL girişi olan bir ACL nesnesi oluşturma ve bir dizindeki ACL 'yi güncelleştirme
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/dir3" -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

Bu komut, 3 ACL girişi içeren bir ACL nesnesi oluşturur (var olan ACL nesnesine ACL girişi eklemek için-InputObject parametresini kullanın) ve bir dizindeki ACL 'yi günceller.

### Örnek 2:4 ACL girişi olan bir ACL nesnesi oluşturma ve var olan ACL girdisinin izinlerini güncelleştirme
```
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx -DefaultScope
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rwx -InputObject $acl 
PS C:\>$acl

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ rwx        

PS C:\>$acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission r-x -InputObject $acl 
PS C:\>$acl  

DefaultScope AccessControlType EntityId                             Permissions
------------ ----------------- --------                             -----------
True         User                                                   rwx        
False        Group                                                  rw-        
False        Other                                                  rw-        
False        User              ********-****-****-****-************ r-x
```

Bu komut ilk olarak 4 ACL girişi olan bir ACL nesnesi oluşturur, ardından cmdlet 'i farklı izinlerle, var olan bir ACL girdisinin aynı AccessControlType/EntityId/DefaultScope değeriyle yeniden çalıştırır.
Ardından ACL girdisinin izni güncellenir, ancak yeni bir ACL girdisi eklenmez.

## PARAMETRELERINE

### -AccessControlType
Dört tür vardır: "Kullanıcı" sahibi veya adlandırılmış bir kullanıcıya hak veriyor, "Grup" sahibi olan gruba veya adlandırılmış bir gruba hak veriyor, "maske" adlandırılmış kullanıcılara ve grupların üyelerine verilen hakları kısıtlar ve "diğer" diğer girdilerde bulunmayan tüm kullanıcılara hak veriyor.

```yaml
Type: Azure.Storage.Files.DataLake.Models.AccessControlType
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultScope
ACE 'nin bir dizinin varsayılan ACL 'ye ait olduğunu belirtmek için bu parametreyi ayarlayın; Yoksa kapsam örtük ve ACE Access ACL 'ye aittir.

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

### -EntityId
Kullanıcı veya grup tanımlayıcısı.
AccessControlType "Mask" ve "diğer" girdileri için kullanılmaz.
Kullanıcı veya grup kimliği sahibi ve sahip olan grup için de atlandı.

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

### -InputObject
PSPathAccessControlEntry \[ \] nesnesiyle karşılaşırsanız yeni ACL 'Yi, PSPathAccessControlEntry nesnesinin yeni bir öğesi olarak ekler \[ \] .

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -İzin
İzin alanı, ilk karakterin ' r ' olduğu bir 3 karakterlik dizi olduğundan, okuma erişimi vermek için ikinci karakter ' w ' olur ve yürütme izni vermek için üçüncü karakter ' x ' olur.
Erişim verilmezse, iznin reddedildiğini belirtmek için '-' karakteri kullanılır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Windowsazde. Commands. Storage. model. ResourceModel. PSPathAccessControlEntry

## NOTLARıNDA

## ILGILI BAĞLANTıLAR
