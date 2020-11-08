---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106096"
---
# Remove-AzureStorSimpleAccessControlRecord

## SYNOPSIS
Hizmet yapılandırmasından bir erişim denetimi kaydını siler.

## INDEKI

### Identifybyname
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Identifybyobject
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Remove-AzureStorSimpleAccessControlRecord** cmdlet 'i, hizmet yapılandırmasından bir erişim denetimi kaydını siler.

## ÖRNEKLERDEN

### Örnek 1: bir Access denetimini kaldırma recordaccess denetimi
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

Bu komut, Acr10 adlı erişim denetimi kaydını siler.
Bu komut, *waitforcomplete* parametresini belirtir ve bu nedenle, komut işlem tamamlanana kadar bekler ve ardından **taskstatusınfo** nesnesini döndürür.

### Örnek 2: pipelineAccess Controlaccess denetimini kullanarak erişim Controlaccess denetim kaydının kaldırılması
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

Bu komut, Acr10 adlı **Accesscontrolrecord** öğesini almak için **Get-AzureStorSimpleAccessControlRecord** kullanır ve ardından bu nesneyi ardışık düzen işlecini kullanarak geçerli cmdlet 'e geçirir.
Komut, **Accesscontrolrecord** nesnesini kaldıran işlemi başlatır ve ardından bir **taskresponse** nesnesi döndürür.
Görevin durumunu görmek için **Get-AzureStorSimpleTask** cmdlet 'ini kullanın.

## PARAMETRELERINE

### -ACR
Silinecek **Accesscontrolrecord** nesnesini belirtir.
**Accesscontrolrecord** nesnesi almak Için, **Get-AzureStorSimpleAccessControlRecord** cmdlet 'ini kullanın.

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ACRName
Silinecek erişim denetimi kaydının adını belirtir.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Bu cmdlet 'in sizden onay istemez olmadığını gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profil
Bir Azure profili belirtir.

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

### -WaitForComplete
Bu cmdlet 'in, denetimi Windows PowerShell konsoluna geri göndermeden önce tamamlamasını beklediğini gösterir.

```yaml
Type: SwitchParameter
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

### AccessControlRecord
Bu cmdlet bir **Accesscontrolrecord** nesnesini kabul eder.
**Accesscontrolrecord** nesnesi aşağıdaki alanları içerir: 

- **Globalid** ( **dize** ) 
- **Initiatorname** ( **dize** ) 
- **InstanceId** ( **dize** ) 
- **Ad** ( **dize** ) 
- **Operationınprogress** ( **operationınprogress** ) 
- **Birimsayısı** ( **int** )

## ÇıKıŞLAR

### Taskstatusınfo, TaskResponse
*Waitforcomplete* parametresini belirtirseniz, bu cmdlet bir **taskstatusınfo** nesnesi döndürür.
Bu parametreyi belirtmezseniz, bir **Taskresponse** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)

[New-AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


