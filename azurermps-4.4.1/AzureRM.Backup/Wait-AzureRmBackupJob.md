---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: 6ee1319881b200b3fcae56e433f81460bfc90274
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593595"
---
# Wait-AzureRmBackupJob

## SYNOPSIS
Yedekleme işinin bitmesini bekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Tanım
**Wait-AzureRmBackupJob** cmdlet 'ı bir Azure yedekleme işinin bitmesini bekler.
Yedekleme işleri uzun zaman alabilir.
Bir yedekleme işini bir komut dosyasının parçası olarak çalıştırırsanız, diğer görevlere devam etmeden önce bu komut dosyasının işin bitmesini beklemeye zorlamak isteyebilirsiniz.

Bu cmdlet 'i içeren bir komut dosyası, iş durumu için yedekleme hizmetini yoklayıp birden kolay olabilir.

## ÖRNEKLERDEN

## PARAMETRELERINE

### -Job
Bu cmdlet 'in iptal olduğu bir iş belirtir.
**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TimeOut
Bu cmdlet işin bitmesini beklediği en uzun süreyi saniye cinsinden belirtir.
Zaman aşımı değeri belirtmenizi öneririz.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### AzureRmBackupJob

## ÇıKıŞLAR

### AzureRmBackupJob []

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[Stop-AzureRmBackupJob](./Stop-AzureRmBackupJob.md)


