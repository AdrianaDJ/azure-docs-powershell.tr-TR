---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 71302FB6-7E2B-4972-A743-AB537AC7CD79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79e194e0f8dda4392dec191881702c680bf172ac
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106552"
---
# Get-AzureStorSimpleAccessControlRecord

## SYNOPSIS
Hizmet yapılandırmasındaki erişim denetimi kayıtlarını alır.

## INDEKI

```
Get-AzureStorSimpleAccessControlRecord [-ACRName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureStorSimpleAccessControlRecord** cmdlet 'ı StorSimple Manager hizmet yapılandırmasındaki erişim denetimi kayıtlarını alır.
Bu cmdlet tüm kayıtları veya adlandırılmış kaydı alır.

Access denetim kayıtları, Iscsı başlatıcı parametrelerinin kapsayıcılarıdır.
Bu parametreler hangi başlatıcıların birime erişebileceğini belirtir.
Bir Iscsı başlatıcısı bir birime bağlanmaya çalıştığında, bu birime atanmış erişim denetimi kayıtlarını kontrol eder.
Iscsı başlatıcı parametreleri, bu birimle eşlenmiş bir erişim denetimi kaydındaki girdilerden biriyle eşleşirse, Iscsı Başlatıcısı bağlanabilir.

## ÖRNEKLERDEN

### Örnek 1: tüm erişim denetimi kayıtlarını alma
```
PS C:\>Get-AzureStorSimpleAccessControlRecord
InstanceId                           Name                        InitiatorName               VolumeCount
----------                           ----                        -------------               -----------
01a31aa5-14de-4b77-b926-2842577f540e Windows_XYUSFL718-RV_ACR    iqn.1991-05.com.microsof... 3
071c282d-0cd2-4c5f-b687-48966037ba48 Linux_XYUSFL719_ACR         iqn.1994-05.com.redhat:a... 3
4600eade-71f8-4d04-baec-0e7cf1d1e8fb Windows_XYUSFL720_ACR       iqn.1991-05.com.microsof... 9
d508d6f0-fcda-4624-b223-c0b307d6113e Linux_XYUSFL350_ACR         iqn.1991-05.com.microsof... 9
```

Bu komut, tüm erişim denetimi kayıtlarını alır.

### Örnek 2: belirli bir erişim denetimi kaydı alma
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr11"
VERBOSE: ClientRequestId: 61f261c7-acd3-4bcc-922a-ddfd85eb767b_PS
VERBOSE: ClientRequestId: 49c6a4c7-d299-46fd-a553-034c52b47487_PS

GlobalId            : 
InitiatorName       : iqn-contoso63
InstanceId          : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
Name                : Acr11
OperationInProgress : None
VolumeCount         : 6

VERBOSE: Access Control Record with given name Acr11 is found!
```

Bu komut, Acr11 adlı erişim denetimi kaydını alır.

## PARAMETRELERINE

### -ACRName
Alınacak bir erişim denetimi kaydının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### AccessControlRecord, IList\<AccessControlRecord\>
Bu cmdlet bir **Accesscontrolrecord** nesnesi veya **\<AccessControlRecord\> IList** nesnesi döndürür.
**Accesscontrolrecord** nesnesi aşağıdaki alanları içerir: 

- **Globalid** ( **dize** ) 
- **Initiatorname** ( **dize** ) 
- **InstanceId** ( **dize** ) 
- **Ad** ( **dize** ) 
- **Operationınprogress** ( **operationınprogress** ) 
- **Birimsayısı** ( **int** )

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Remove-AzureStorSimpleAccessControlRecord](./Remove-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)


