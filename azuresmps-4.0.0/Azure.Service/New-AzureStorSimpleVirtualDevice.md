---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105511"
---
# New-AzureStorSimpleVirtualDevice

## SYNOPSIS
Sanal StorSimple cihazı oluşturur.

## INDEKI

### CreateNewStorageAccount
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### UseExistingStorageAccount
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Tanım
**New-AzureStorSimpleVirtualDevice** cmdlet 'ı sanal StorSimple cihazı oluşturur.
Cihaz için bir cihaz adı belirtin.
Aynı abonelikteki sanal ağın sanal ağ ve alt ağ ayrıntılarını belirtin.
Coğrafi olarak, StorSimple kaynağının oluşturulduğu coğrafi değer eşleşmelidir.
Bu sanal cihaz için var olan bir depolama hesabını kullanmak için, adı belirtin.
Bu sanal cihaz için yeni bir depolama hesabı oluşturmak için hem *storageAccountName* hem de *createnewstorageaccount* parametrelerini belirtin.

## ÖRNEKLERDEN

### Örnek 1: yeni bir hesap ve var olan bir ağ ile sanal cihaz oluşturma
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

Bu komut yeni bir depolama hesabı ve var olan sanal ağ kullanan bir sanal cihaz oluşturur.

### Örnek 2: var olan bir hesap ve sanal ağ ile sanal cihaz oluşturma
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

Bu komut, var olan bir depolama hesabını ve var olan sanal ağı kullanan bir sanal cihaz oluşturur.

## PARAMETRELERINE

### -CreateNewStorageAccount
Bu cmdlet 'in yeni bir depolama hesabı oluşturduğunu gösterir.

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PersistAzureVMOnFailrue
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

### -StorageAccountName
Depolama hesabının adını belirtir.

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubNetName
Sanal alt ağın adını belirtir.

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

### -Sanalaygıtadı
Sanal cihaz için bir ad belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkName
Sanal ağın adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

### Dizisi
Bu cmdlet, sanal cihazı oluşturan işin KIMLIĞINI döndürür.
Get-AzureStorSimpleJob cmdlet 'ini kullanarak ilerlemeyi izlemek için bu KIMLIĞI kullanabilirsiniz.

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)

[Set-AzureStorSimpleVirtualDevice](./Set-AzureStorSimpleVirtualDevice.md)


