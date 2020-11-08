---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 9436E1AB-870F-4717-ABE0-55A90C07F7E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 555ce014bbbf7174b3f7142cf7e2f217317eadc6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106291"
---
# Get-AzureStorSimpleDeviceConnectedInitiator

## SYNOPSIS
StorSimple aygıtı için sağlanan Iscsı bağlantılarını alır.

## INDEKI

### Identifybyıd
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Identifybyname
```
Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Tanım
**Get-AzureStorSimpleDeviceConnectedInitiator** cmdlet 'ı StorSimple aygıtı Için sağlanan iSCSI bağlantılarının listesini alır.
Bu cmdlet 'in döndürdüğü Iscsı bağlantı nesneleri aşağıdaki özellikleri içerir:

- **Acrınstanceıd**
- **AcrName**
- **AllowedVolumeNames**
- **Initiatoraddress**
- **Arayüzler**
- **'Si**
- **IscsiConnectionId**

Bu cmdlet yalnızca cihazda Iscsı bağlantıları açıksa bağlantı nesnesini alır.
Varsayılan olarak, bağlantılar kapalıdır.

## ÖRNEKLERDEN

### Örnek 1: bir cihaz için tüm bağlantıları alma
```
PS C:\>Get-AzureStorSimpleDeviceConnectedInitiator -DeviceName "Contoso63-AppVm"
VERBOSE: ClientRequestId: bec615b9-79ab-4671-88b0-287adeb6bf68_PS
VERBOSE: ClientRequestId: ef976c58-2660-41c8-aa15-c84e70c9d01c_PS
VERBOSE: ClientRequestId: 9b306b96-8e76-47ed-beda-d3bd2fb2bb82_PS
VERBOSE: ClientRequestId: 0f4fc743-0b60-45da-a45a-27f4b0f32bd2_PS

AcrInstanceId      : 55f24643-ab3a-4098-ade2-aa2b1a3ab18c
AcrName            : Contoso63-AppVm
AllowedVolumeNames : {Policyvolume1_Default}
InitiatorAddress   : 
Interfaces         : {Data0}
Iqn                : iqn10
IscsiConnectionId  : cfc144cb-00f1-44b1-9655-80b431f2161b

VERBOSE: 1 Iscsi Connection found!
```

Bu komut, Contoso63-AppVm adlı aygıtın tüm Iscsı bağlantılarını alır.
Bu komut yalnızca cihazda bağlantılar açıksa bağlantı döndürür.

## PARAMETRELERINE

### -DeviceID
Iscsı başlatıcılarının alınacağı StorSimple aygıtının örnek KIMLIĞINI belirtir.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Aygıtadı
Iscsı başlatıcılarının alınacağı StorSimple aygıtının adını belirtir.

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

### Listeniz\<IscsiConnection\>
Bu cmdlet, aşağıdaki özellikleri içeren bir Iscsı bağlantı nesnesi döndürür: 

- **Acrınstanceıd**
- **AcrName**
- **AllowedVolumeNames**
- **Initiatoraddress**
- **Arayüzler**
- **'Si**
- **IscsiConnectionId**

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)


