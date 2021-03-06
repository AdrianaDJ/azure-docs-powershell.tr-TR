---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesynccompatibilitycheck
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncCompatibilityCheck.md
ms.openlocfilehash: b3c6b69b628c7461616a42ecbaaf37d017e06b46
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934298"
---
# Invoke-AzStorageSyncCompatibilityCheck

## SYNOPSIS
Sisteminiz ile Azure dosya eşitlemesi arasındaki olası uyumluluk sorunlarını denetler.

## INDEKI

### Yol tabanlı (varsayılan)
```
Invoke-AzStorageSyncCompatibilityCheck [-Path] <String> [-Credential <PSCredential>] [-SkipSystemChecks]
 [-SkipNamespaceChecks] [<CommonParameters>]
```

### Bilgisayar adı tabanlı
```
Invoke-AzStorageSyncCompatibilityCheck [-Credential <PSCredential>] [-ComputerName] <String>
 [-SkipSystemChecks] [<CommonParameters>]
```

## Tanım
**Invoke-AzStorageSyncCompatibilityCheck** cmdlet 'i, sisteminiz Ile Azure dosya eşitlemesi arasındaki olası uyumluluk sorunlarını denetler. Yerel veya uzak yol verildiğinde, sistem ve dosya ad boşluğunda bir dizi doğrulama gerçekleştirir ve bulduğu tüm uyumluluk sorunlarını döndürür.
Sistem denetimleri:
- İşletim sistemi Uyumluluk dosyası ad alanı denetimleri:
- Desteklenmeyen karakterler
- En büyük dosya boyutu
- Maksimum yol uzunluğu
- Maksimum dosya uzunluğu
- En büyük veri kümesi boyutu
- En fazla Dizin derinliği

## ÖRNEKLERDEN

### Örnek 1
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA
```

Bu komut, sistemin ve C:\DATA'TEKI dosya ve klasörlerin uyumluluğunu denetler.

### Örnek 2
```powershell
PS C:\> Invoke-AzStorageSyncCompatibilityCheck C:\DATA -SkipSystemChecks
```

Bu komut C:\VERILERDEKI dosyaların ve klasörlerin uyumluluğunu denetler, ancak sistem uyumluluğu denetimi gerçekleştirmez.

### Örnek 3
```powershell
PS C:\> $validation = Invoke-AzStorageSyncCompatibilityCheck C:\DATA
PS C:\> $validation.Results | Select-Object -Property Type, Path, Level, Description, Result | Export-Csv -Path C:\results.csv -Encoding utf8
```

Bu komut, c: \ verilerdeki dosyaların ve klasörlerin uyumluluğunu denetler ve ardından sonuçları C:\resultsdizinine CSV dosyası olarak aktarır.

## PARAMETRELERINE

### -ComputerName
Bu bilgisayarı denetleme.

```yaml
Type: System.String
Parameter Sets: ComputerNameBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Doğrulama için kimlik bilgileriniz.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Yol
Doğruladığımız paylaşımın UNC yolu.

```yaml
Type: System.String
Parameter Sets: PathBased
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skipnamespacedenetimlerini
Dosya ad alanı doğrulamalarını atlamak için bu bayrağı ayarlayın ve yalnızca sistem doğrulamaları gerçekleştirin.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PathBased
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skipsystemdenetimleri
Sistem doğrulamalarını atlayıp yalnızca dosya ad alanı doğrulamaları gerçekleştirmek için bu bayrağı ayarlayın.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Microsoft. Azure. Commands. Storagesehd. Evaluation. model. PSValidationResult

## NOTLARıNDA
* Anahtar sözcükler: Azure, az, ARM, kaynak, yönetim, storageseşit

## ILGILI BAĞLANTıLAR
