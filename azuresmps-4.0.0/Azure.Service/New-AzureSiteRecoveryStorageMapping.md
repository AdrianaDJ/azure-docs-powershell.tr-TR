---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105975"
---
# New-AzureSiteRecoveryStorageMapping

## SYNOPSIS
Azure depolama nesnesi ile kurtarma depolama nesnesi arasında eşleme oluşturur.

## INDEKI

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**New-AzureSiteRecoveryStorageMapping** cmdlet 'ı Azure Site Recovery yönetilen birincil Azure depolama nesnesi Ile kurtarma depolama nesnesi arasında eşleme oluşturur.

## ÖRNEKLERDEN

### Örnek 1: depolama nesnesiyle kurtarma depolama nesnesi arasında eşleme oluşturma
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

İlk komut cmdlet 'i **Get-AzureSiteRecoveryServer** cmdlet 'ini kullanarak geçerli Azure Site Recovery Kasası için sunucuları alır.
Komut, $Servers dizi değişkeninde site kurtarma sunucularını depolar.

İkinci komut $Servers dizisindeki ilk sunucunun site kurtarma depolamasını alır ve $Storages depolar.

Son komutu birincil ağla kurtarma ağı arasında bir eşleme oluşturur.
Komut birincil depolama nesnesini $Storages ilk öğesi olarak belirtir.
Komut, kurtarma depolama nesnesini $Storages ikinci öğesi olarak belirtir.

## PARAMETRELERINE

### -PrimaryStorage
Kurtarma depolama alanı ile eşlenecek birincil depolamayı belirtir.
Bir **Asrstorage** nesnesi almak için Get-AzureSiteRecoveryStorage cmdlet 'ini kullanın.

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bu cmdlet 'in okuduğu Azure profilini belirtir.
Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryStorage
Kurtarma depolama nesnesini belirtir.
Bu cmdlet birincil depolama nesnesini bu parametrenin belirttiği depolama nesnesiyle eşleştirir.
Bir **Asrstorage** nesnesi almak için **Get-AzureSiteRecoveryStorage** kullanın.

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)

[Get-AzureSiteRecoveryStorageMapping](./Get-AzureSiteRecoveryStorageMapping.md)

[Remove-AzureSiteRecoveryStorageMapping](./Remove-AzureSiteRecoveryStorageMapping.md)


