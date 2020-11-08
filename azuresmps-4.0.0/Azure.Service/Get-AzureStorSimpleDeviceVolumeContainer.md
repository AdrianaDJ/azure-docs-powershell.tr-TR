---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105563"
---
# Get-AzureStorSimpleDeviceVolumeContainer

## SYNOPSIS
Cihazda birim kapsayıcılarını alır.

## INDEKI

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**Get-AzureStorSimpleDeviceVolumeContainer** cmdlet 'i, bir aygıttaki birim kapsayıcılarının veya belirtilen ada sahip birim kapsayıcısının listesini alır.
Döndürülen nesne aşağıdaki özellikleri içerir: 

- **BandwidthRate**
- **Şifrelemetuşu**
- **Örnek**
- **IsDefault**
- **Isencryptionenabled**
- **Adlandır**
- **Operationınprogress**
- **Aitse**
- **Primarystoragecredential**
- **Secretsencryptionparmak Izi**
- **Birimsayısı**

## ÖRNEKLERDEN

### Örnek 1: cihazdaki tüm kapsayıcıları alma
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

Bu komut, 8600-Bravo 001 adlı aygıttaki birim kapsayıcılarının listesini alır.

### Örnek 2: adını kullanarak kapsayıcı alma
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

Bu komut, Contoso63-AppVm adındaki cihazda Container08 adlı birim kapsayıcısını alır.

## PARAMETRELERINE

### -Aygıtadı
StorSimple aygıtının adını belirtir.
Bu cmdlet, bu parametrenin belirttiği cihazdan birim kapsayıcılarını alır.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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

### -VolumeContainerName
Alınacak birim kapsayıcısının adını belirtir.

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

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Yabilirsiniz

## ÇıKıŞLAR

### DataContainer, IList\<DataContainer\>
Bu cmdlet, *Volumecontainername* parametresini belirttiğinizde bir **datacontainer** nesnesi döndürür.
Bu parametreyi belirtmezseniz, bu cmdlet bir **IList \<DataContainer\>** nesnesi döndürür.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[New-AzureStorSimpleDeviceVolumeContainer](./New-AzureStorSimpleDeviceVolumeContainer.md)

[Remove-AzureStorSimpleDeviceVolumeContainer](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


