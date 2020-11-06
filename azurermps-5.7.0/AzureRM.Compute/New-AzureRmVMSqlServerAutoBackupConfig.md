---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 15f26b611f90f8211e8f49c45c583d8953c028a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586799"
---
# New-AzureVMSqlServerAutoBackupConfig

## SYNOPSIS
SQL Server otomatik yedekleme için yapılandırma nesnesi oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### Storageurisurserverautobackup (varsayılan)
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

### StorageContextSqlServerAutoBackup
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

## Tanım
**New-AzureVMSqlServerAutoBackupConfig** CMDLET 'ı SQL Server otomatik yedekleme için yapılandırma nesnesi oluşturur.

## ÖRNEKLERDEN

### Örnek 1: depolama URI 'sini ve hesap anahtarını kullanarak otomatik yedekleme yapılandırması oluşturma
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Bu komut, depolama URI 'sini ve hesap anahtarını belirterek otomatik bir yedekleme yapılandırma nesnesi oluşturur.
Otomatik yedekleme etkinleştirilir ve otomatik yedeklemeler 10 gün boyunca tutulur.
Komut sonucu $AutoBackupConfig değişkeninde depolar.
Bu yapılandırma öğesini, Set-AzureRmVMSqlServerExtension cmdlet gibi diğer cmdlet 'ler için belirtebilirsiniz.

### Örnek 2: depolama alanı kullanarak otomatik yedekleme yapılandırması oluşturma
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

İlk komut depolama bağlamı oluşturur ve $StorageContext değişkeninde depolar.
Daha fazla bilgi için bkz.

İkinci komut $StorageContext 'da depolama bağlamını belirterek otomatik bir yedekleme yapılandırma nesnesi oluşturur.
Otomatik yedekleme etkinleştirilir ve otomatik yedeklemeler 10 gün boyunca tutulur.

### Örnek 3: şifreleme ve parolayla depolama bağlamını kullanarak otomatik yedekleme yapılandırması oluşturma
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

Bu komut otomatik yedek yapılandırma nesnesi oluşturur ve depolar.
Komut, önceki örnekte oluşturulan depolama bağlamını belirtir.
Komut parola ile şifrelemeyi etkinleştirmiştir.
Parola daha önce $CertificatePassword değişkeninde güvenli bir dize olarak depolanmıştı.
Güvenli bir dize oluşturmak için ConvertTo-SecureString cmdlet 'ini kullanın.

## PARAMETRELERINE

### -BackupScheduleType
Yedekleme zamanlama türü, el ile veya otomatik

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackupSystemDbs
Sistem veritabanlarını yedekleme

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificatePassword
SQL Server şifreli yedeklemelerini gerçekleştirmek için kullanılan sertifikayı şifrelemek için parola belirtir.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
SQL Server sanal makinesinin otomatik yedeklemesinin etkinleştirildiğini gösterir.
Bu parametreyi belirtirseniz, otomatik yedekleme tüm geçerli ve yeni veritabanları için bir yedekleme zamanlaması ayarlar.
Bu işlem, yönetilen yedekleme ayarlarınızı bu zamanlamayı izleyecek şekilde güncelleştirir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableEncryption
Bu cmdlet 'in şifrelemeyi etkinleştirdiğini belirtir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupFrequency
Günlük veya haftalık SQL Server tam yedekleme sıklığı

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupStartHour
SQL Server tam yedekleme başlaması gereken günün saati (0-23)

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Fullbackupwindowınhours
SQL Server tam yedekleme penceresi saat cinsinden

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogBackupFrequencyInMinutes
SQL Server günlük yedekleme sıklığı, her 1-60 dakikada bir

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Sanal makinenin kaynak grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionPeriodInDays
Yedeklemenin tutulacağı gün sayısını belirtir.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
Yedekleri depolamak için kullanılacak depolama hesabını belirtir.
**Azurestoragecontext** nesnesi edinmek için New-AzureStorageContext cmdlet 'ini kullanın.
Varsayılan, SQL Server sanal makinesiyle ilişkili depolama hesabıdır.

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
BLOB depolama hesabının depolama anahtarını belirtir.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageUri
BLOB depolama hesabının Tekdüzen Kaynak tanımlayıcısını (URI) belirtir.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz
Bu cmdlet hiçbir girişi kabul etmez.

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureVMSqlServerAutoPatchingConfig](./New-AzureVMSqlServerAutoPatchingConfig.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


