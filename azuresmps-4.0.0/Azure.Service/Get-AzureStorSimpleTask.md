---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105552"
---
# Get-AzureStorSimpleTask

## SYNOPSIS
StorSimple aygıtındaki bir görevin durumunu alır.

## INDEKI

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureStorSimpleTask** cmdlet 'ı Azure StorSimple cihazında eş zamanlı olmayan çalışan bir görevin durumunu alır.

StorSimple aygıtını yönetirken, çoğu oluşturma, okuma, güncelleştirme ve silme eylemleri zaman uyumsuz olarak çalıştırılabilir.
Windows PowerShell bir **TaskID** döndürür.
Görevin geçerli durumunu almak için KIMLIĞI kullanın.

## ÖRNEKLERDEN

### Örnek 1: görevin durumunu alma
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

Bu komut, belirtilen KIMLIĞE sahip görevin durumunu alır.
Sonuçlar görevin tamamlandı durumunu ve başarılı bir sonucu olduğunu gösterir.

## PARAMETRELERINE

### -InstanceId
Bu cmdlet 'in durumu izlediği görevin KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### Jobstatusınfo
Bu cmdlet, aşağıdaki alanları içeren bir **Taskstatusınfo** nesnesi döndürür: 

- **Hatası**.
**Kod** ve **Ileti** içeren **ErrorDetails**.
- **TaskID**.
**Dizedir**.
Durumu döndürülecek görevin KIMLIĞI.
- **Görevadımları**.
**IList \<TaskStep\>**.
Her **Taskstep** nesnesi **ayrıntı** , **HataKodu** , **ileti** , **sonuç** ve **durum** içerir.
- **Sonuç**.
Görev **sonucu** , görevin genel sonucunu içerir.
Geçerli değerler: başarısız, başarılı, PartialSuccess, Iptal edildi ve geçersiz.
- **Durumu**.
Görevin genel çalışma durumunu içeren görev **durumu**.
Geçerli değerler: InProgress, geçersiz ve tamamlandı.
- **Görevsonucu**.
**TaskResult** , **sonuç** ve **durumuna** göre hesaplanan bir değer.
Geçerli değerler: başarısız, başarılı, sürüyor, PartialSuccess, Iptal edildi ve geçersiz.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

