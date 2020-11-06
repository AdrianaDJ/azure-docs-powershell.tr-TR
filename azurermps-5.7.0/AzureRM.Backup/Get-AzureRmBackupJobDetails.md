---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6187F603-5298-4854-94F3-0C38FCF3125F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJobDetails.md
ms.openlocfilehash: 109a02ac04fe9926ef4510d295c978e01026ade2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595109"
---
# Get-AzureRmBackupJobDetails

## SYNOPSIS
Yedekleme işinin ayrıntılarını alır.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### İş (varsayılan)
```
Get-AzureRmBackupJobDetails -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### Idfiltersset
```
Get-AzureRmBackupJobDetails -Vault <AzureRMBackupVault> -JobId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Get-AzureRmBackupJobDetails** cmdlet 'i, bir Azure yedekleme işinin ayrıntılarını alır.
Başarısız olan bir iş hakkında bilgi toplamak için bu cmdlet 'i kullanabilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: başarısız işin ayrıntılarını görüntüleme
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Jobs = Get-AzureRmBackupJob -Vault $Vault -Status Failed
PS C:\> $JobDetails = Get-AzureRmBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
ErrorCode ErrorMessage                            Recommendations
--------- ------------                            ---------------
   400001 Command execution failed.               {Another operation is currently in p...
```

İlk komut **Get-Azurermbackupkasa** cmdlet 'Ini kullanarak Vault03 adlı kasayı alır.
Komut bu nesneyi $Vault değişkeninde depolar.

İkinci komut $Vault kasadan başarısız işleri alır ve $Jobs dizi değişkeninde depolar.

Üçüncü iş, $Jobs değişkenindeki ilk işin ayrıntılarını alır ve $JobDetails değişkeninde bu ayrıntıları depolar.

Final komutu, standart nokta söz dizimini kullanarak $JobDetails 'un **ErrorDetails** özelliğini görüntüler.

### Örnek 2: başarısız iş için önerilen eylemi görüntüleme
```
PS C:\>$JobDetails.ErrorDetails.Recommendations
Another operation is currently in progress on this item. Please wait until the previous operation is completed, and then retry.
```

Bu komut, ilk örnekte oluşturulan $JobDetails değişkeninden önerilen eylemi görüntüler.

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

### -Job
Bu cmdlet 'in ayrıntıları aldığı işi belirtir.
**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob cmdlet 'ini kullanın.

```yaml
Type: AzureRMBackupJob
Parameter Sets: JobsFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Bu cmdlet 'in ayrıntıları aldığı iş KIMLIĞINI belirtir.
ID, **Azurermbackupjob** nesnesinin **InstanceId** özelliğidir.
**Azurermbackupjob** nesnesi almak için Get-AzureRmBackupJob seçeneğini kullanın.

```yaml
Type: String
Parameter Sets: IdFiltersSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Kasa
Bu cmdlet 'in iş ayrıntılarını aldığı yedek kasayı belirtir.
**Azurermbackupkasa** nesnesi almak için Get-AzureRmBackupVault cmdlet 'ini kullanın.

```yaml
Type: AzureRMBackupVault
Parameter Sets: IdFiltersSet
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

### Yabilirsiniz

## ÇıKıŞLAR

### AzureRmBackupJobDetails

## NOTLARıNDA
* Yabilirsiniz

## ILGILI BAĞLANTıLAR

[Get-AzureRmBackupJob](./Get-AzureRmBackupJob.md)

[Get-Azurermbackupkasası](./Get-AzureRmBackupVault.md)


