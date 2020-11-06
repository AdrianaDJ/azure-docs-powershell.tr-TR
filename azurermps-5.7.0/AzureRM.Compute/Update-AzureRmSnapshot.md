---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmSnapshot.md
ms.openlocfilehash: ff70d3879685b0cdc9fcc42732a68e6b85bbd580
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586762"
---
# Update-AzureRmSnapshot

## SYNOPSIS
Anlık görüntüyü güncelleştirir.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### DefaultParameter (varsayılan)
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String>
 [-SnapshotUpdate] <SnapshotUpdate> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Kolay Yöntem
```
Update-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Snapshot] <Snapshot> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Update-AzureRmSnapshot** cmdlet 'ini güncelleştirir.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $snapshotupdateconfig = New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateDiskEncryptionKey -SnapshotUpdate $snapshotupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $snapshotupdateconfig = Set-AzureRmSnapshotUpdateKeyEncryptionKey -SnapshotUpdate $snapshotupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -SnapshotUpdate $snapshotupdateconfig;
```

İlk komut Premium_LRS depolama hesabı türünde, boyutu 10 olan yerel bir boş anlık görüntü güncelleştirme nesnesi oluşturur.  Ayrıca, Windows işletim sistemi türünü de ayarlar ve şifreleme ayarlarını belirler.
İkinci ve üçüncü komutlar, anlık görüntü güncelleştirme nesnesi için disk şifrelemesi anahtarını ve anahtar şifreleme anahtarı ayarlarını ayarlar.
Son komut, anlık görüntü güncelleştirme nesnesini alır ve ' ResourceGroup01 ' kaynak grubunda ' Snapshot01 ' adlı anlık görüntüyü güncelleştirir.

### Örnek 2
```
PS C:\> New-AzureRmSnapshotUpdateConfig -DiskSizeGB 10 | Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
```

Bu komut, ' ResourceGroup01 ' kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüyü 10 GB disk boyutuna güncelleştirir.

### Örnek 3
```
PS C:\> $snapshot = Get-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01';
PS C:\> $snapshot.DiskSizeGB = 10;
PS C:\> Update-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshot;
```

Bu komutlar, ' ResourceGroup01 ' kaynak grubundaki ' Snapshot01 ' adlı anlık görüntüyü 10 GB disk boyutuna de güncelleştirir.

## PARAMETRELERINE

### -ResourceGroupName
Kaynak grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Anlık görüntü
Yerel bir anlık görüntü nesnesi belirtir.

```yaml
Type: Snapshot
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SnapshotName
Anlık görüntünün adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SnapshotUpdate
Yerel anlık görüntü güncelleştirme nesnesini belirtir.

```yaml
Type: SnapshotUpdate
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
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
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

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

### System. String
Microsoft. Azure. Management. COMPUTE. modeller. SnapshotUpdate Microsoft. Azure. Management. COMPUTE. modeller. anlık görüntüsü

## ÇıKıŞLAR

### System. Object

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

