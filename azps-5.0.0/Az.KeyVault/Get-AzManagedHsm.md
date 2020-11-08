---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277727"
---
# Get-AzManagedHsm

## SYNOPSIS
Yönetilen HSMs alın.

## INDEKI

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzManagedHsm** cmdlet 'i, bir abonelikteki yönetilen hsms hakkında bilgi alır. Tüm yönetilen HSMs örneklerini bir abonelikte görüntüleyebilir ya da sonuçlarınızı bir kaynak grubuna veya belirli bir yönetilen HSM 'ye göre filtreleyebilirsiniz.
Tek bir yönetilen HSM aldığınızda bu cmdlet için kaynak grubu 'nun isteğe bağlı olduğunu belirten unutmayın, daha iyi performans için bunu yapmalısınız.

## ÖRNEKLERDEN

### Örnek 1: geçerli aboneliğinizde tüm yönetilen HSMs 'leri edinin
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Bu komut geçerli aboneliğinizde tüm yönetilen HSMs 'yi alır.

### Örnek 2: belirli bir yönetilen HSM alma
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Bu komut, geçerli aboneliğinizde myhsm adlı yönetilen HSM 'yi alır.

### Örnek 3: kaynak grubunda yönetilen HSMs alma
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Bu komut, myrg1 adlı kaynak grubundaki tüm yönetilen HSMs 'yi alır.

### Örnek 4: filtreleme kullanarak yönetilen HSMs alma
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

Bu komut, abonelikteki tüm yönetilen HSMs 'i "myhsm" ile başlayan bir alan alır.

## PARAMETRELERINE

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

### -Ad
HSM adı. Cmdlet, adı ve seçili durumdaki ortamı temel alan bir HSM FQDN 'SI oluşturur.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Sorgulanan yönetilen HSM ile ilişkili kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### Etiketli
Yönetilen HSMs 'in listesini filtrelemek için belirtilen etiketin anahtarını ve isteğe bağlı değerini belirtir.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### System. String

### System. topluluklar. Hashtable

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Keykasa. modeller. PSManagedHsm

### Microsoft. Azure. Commands. Keykasa. modeller. Pskeyvaultidentityıtem

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Yeni-AzManagedHsm](./New-AzManagedHsm.md)

[Remove-AzManagedHsm](./Remove-AzManagedHsm.md)

[Güncelleştirme-AzManagedHsm](./Update-AzManagedHsm.md)