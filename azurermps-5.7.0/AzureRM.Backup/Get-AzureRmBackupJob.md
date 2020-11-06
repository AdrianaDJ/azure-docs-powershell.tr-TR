---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: 3402dc7018f094a5f95a967385d9bae8d70c68f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588988"
---
# Get-AzureRmBackupJob

## SYNOPSIS
Yedekleme işlerini alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### FiltersSet (varsayılan)
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### JobsListFilter
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmBackupJob** cmdlet 'i, belirli bir kasa Için Azure yedekleme işlerini alır.

## ÖRNEKLERDEN

### Örnek 1: yedekleme kasasındaki tüm işleri alma
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

İlk komut **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı kasayı alır.
Komut bu nesneyi $Vault değişkeninde depolar.

İkinci komut $Vault kasa için tüm işleri alır.

### Örnek 2: tamamlanan işleri alma
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Bu komut $Vault iş kasasından tamamlanmış işleri alır.

### Örnek 3: geçen hafta başarısız iş alma
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

Bu komut, $Vault 'daki kasadan geçen haftaki başarısız işleri alır.
*From* parametresi geçmişte yedi gün bir saat belirtir.
Komut *to* parametresi için bir değer belirtmiyor.
Bu nedenle, geçerli zamanın varsayılan değerini kullanır.

### Örnek 4: süren devam eden iş için yedekleme yoklama
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Bu komut dosyası, iş tamamlanana kadar devam eden ilk işi yoklar.

Komut dosyasının ilk satırı, sürmekte olan $Vault tüm işleri alır ve bu işleri $Jobs dizi değişkeninde depolar.

İkinci satır, $Job değişkeninde $Jobs dizisinden ilk işi depolar.

Üçüncü satır, iş tamamlanana kadar işin geçerli durumunu denetleyen **while** döngüsünü başlatır.
Eğer **anahtar sözcüğü** hakkında bilgi için şunu yazın `Get-Help about_While` .

**While** döngüsü konsola bir ileti yazar, on $Job saniye boyunca uyku
Komut dosyası, işin mevcut durumunu almak için mevcut $Job değerini ve geçerli cmdlet 'i kullanarak $Job değişkenini güncelleştirir.
Windows PowerShell cmdlet 'leri hakkında bilgi için, `Get-Help Write-Host` ve yazın `Get-Help Start-Sleep` .

Komut dosyasının son satırında, komut dosyasının bittiğini söyler.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### 'Den
Bu cmdlet 'in aldığı işler için zaman aralığının başlangıç, **DateTime** nesnesi olarak başlangıcını belirtir.
**TarihSaat** nesnesi almak için Get-Date cmdlet 'ini kullanın.
**TarihSaat** nesneleri hakkında daha fazla bilgi için, yazın `Get-Help Get-Date` .

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Job
Bu cmdlet 'in aldığı işi belirtir.
**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Bu cmdlet 'in aldığı bir işin KIMLIĞINI belirtir.
ID, **Azurermbackupjob** nesnesinin **InstanceId** özelliğidir.
**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob seçeneğini kullanın.

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -İşlem
Bu cmdlet 'in aldığı işlerin bir işlemini belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Yedeğinin 
- ConfigureBackup 
- DeleteBackupData 
- Kaydettiremedi 
- Kurtarma 
- Sayfa korumasını kaldır 
- Kaldırabilirsiniz

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Durum
Bu cmdlet 'in aldığı işlerin durumunu belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- Progress
- Erişilemedi
- İptal
- Edilirse
- Tamamladığı
- Completeduyarıları 

Tüm sürmekte olan işleri veya tüm başarısız işleri bulmak için bu parametreyi belirtebilirsiniz.

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Bu cmdlet 'in aldığı işler için zaman aralığının sonunu bir **Tarih saat** olarak belirtir.
Varsayılan değer geçerli sistem saatinin değeridir.
Bu parametreyi belirtirseniz, *from* parametresini de belirtmeniz gerekir.

```yaml
Type: DateTime
Parameter Sets: FiltersSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tür
Bu cmdlet 'in yedekleme işlerini aldığı kapsayıcının türünü belirtir.
Şu anda desteklenen tek değer AzureVM.

```yaml
Type: String
Parameter Sets: FiltersSet
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kasa
Bu cmdlet 'in işleri aldığı yedek kasayı belirtir.
**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.

```yaml
Type: AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Azurermbackupkasası

## ÇıKıŞLAR

### AzureRmBackupJob []
Bu cmdlet bir veya daha fazla yedekleme işi döndürür.

## NOTLARıNDA
* Yabilirsiniz

## ILGILI BAĞLANTıLAR

[Get-Azurermbackupkasası](./Get-AzureRmBackupVault.md)

[Stop-AzureRmBackupJob](./Stop-AzureRmBackupJob.md)

[Wait-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


