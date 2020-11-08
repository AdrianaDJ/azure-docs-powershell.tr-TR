---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 1b5f447e95e137ba9199ba596029f2088a977c91
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266940"
---
# Set-AzRecoveryServicesAsrReplicationProtectedItem

## SYNOPSIS
Belirtilen çoğaltma korumalı öğesi için hedef ağ ve sanal makine boyutu gibi kurtarma özelliklerini ayarlar.

## INDEKI

```
Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject <ASRReplicationProtectedItem> [-Name <String>]
 [-Size <String>] [-UpdateNic <String>] [-RecoveryNetworkId <String>] [-PrimaryNic <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>]
 [-NicSelectionType <String>] [-RecoveryResourceGroupId <String>] [-LicenseType <String>]
 [-RecoveryAvailabilitySet <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-EnableAcceleratedNetworkingOnRecovery] [-RecoveryBootDiagStorageAccountId <String>]
 [-AzureToAzureUpdateReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-UseManagedDisk <String>]
 [-DiskIdToDiskEncryptionSetMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-RecoveryPublicIPAddressId <String>] [-RecoveryNetworkSecurityGroupId <String>]
 [-RecoveryLBBackendAddressPoolId <String[]>] [-TfoAzureVMName <String>]
 [-ASRVMNicConfiguration <ASRVMNicConfig[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Tanım
**Set-Azrecoveryservicesasrreplicationkoruttıtem** cmdlet 'ı, çoğaltma korumalı bir öğenin kurtarma özelliklerini ayarlar.

## ÖRNEKLERDEN

### Örnek 1
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -ReplicationProtectedItem $RPI -UpdateNic $NicId -RecoveryNetworkId $AzureNetworkID -RecoveryNicSubnetName $subnetName
```

Belirtilen parametreleri kullanarak çoğaltma korumalı öğe ayarlarını güncelleştirme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.

### Örnek 2
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -UpdateNic "00:50:56:8F:3F:7B" -RecoveryNetworkId $recoveryNetwork -RecoveryNicSubnetName $recoverySubnet -NicSelectionType NotSelected
```

Belirtilen parametreleri kullanarak çoğaltma korumalı öğe ağı arabirim kartı (NIC azaltma) ayarlarını güncelleştirme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.

### Örnek 3
```
PS C:\> $currentJob = Set-AzRecoveryServicesAsrReplicationProtectedItem -InputObject $rpi -PrimaryNic "00:50:56:8F:3F:7B"
```

Belirtilen parametreleri kullanarak çoğaltma korumalı öğesini (kurtarılan VM için kullanılacak) ayarlar 'ı güncelleştirme işlemini başlatır ve işlemi izlemek için kullanılan ASR işini döndürür.

### Örnek 4
```
PS C:\>Set-ASRReplicationProtectedItem -InputObject $rpi -UpdateNic $updateNic -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName�-NicSelectionType SelectedByUser
```

Belirtilen parametreleri kullanarak çoğaltma korumalı öğe NIC 'ı (kurtarılan VM için kullanılacak) ayarlar ve işlemi izlemek için kullanılan ASR işini döndüren işlemi başlatır.

### Örnek 5
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -UpdateNic $updateNic `
        -RecoveryNetworkId $recoveryNetworkId -RecoveryNicSubnetName $recoveryNicSubnetName -EnableAcceleratedNetworkingOnRecovery
```

Çoğaltma korumalı öğesini güncelleştirme işlemini başlatır kurtarma VM 'de (Azure 'dan Azure için olağanüstü durum kurtarması için)
EnableAcceleratedNetworkingOnRecovery-hızlandırılmış ağı devre dışı bırakma.

### Örnek 6
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi `
    -DiskEncryptionVaultId  $DiskEncryptionVaultId   �-DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
     -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

Belirtilen şifreli çoğaltma korumalı öğesinin güncelleştirme işlemini başlatıp yük devretme VM için sağlanan şifreleme ayrıntılarını kullanma.

### Örnek 7
```
PS C:\> $currentJob = Set-AzureRmRecoveryServicesAsrReplicationProtectedItem -InputObject $ rpi -RecoveryProximityPlacementGroupId $ppg
```

Belirtilen çoğaltma korumalı öğe için güncelleştirme işlemini başlatıp yük devretme VM için sağlanan yakınlık Yerleşim grubunu kullanın.


## PARAMETRELERINE

### -ASRVMNicConfiguration
Test yük devretmesi ve yük devretme NIC yapılandırma ayrıntılarını belirtir.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMNicConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureToAzureUpdateReplicationConfiguration
Yönetilen disk VM için motive edilecek disk yapılandırmasını belirtir (Azure 'dan Azure 'a Azure DR manzara).

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSecretUrl
Yük devretme sonrasında kurtarma VM olarak kullanılacak sürüm (Azure disk şifrelemesi) içeren disk şifrelemesi gizlilik URL 'sini belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionVaultId
Yük devretmenin ardından kurtarma VM olarak kullanılacak disk şifrelemesi gizli Anahtar Kasası KIMLIĞINI (Azure disk şifrelemesi) belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Diskivseçtodiskencryptionsetmap
Disk kaynağı kimliği 'nin disk şifrelemesi kümesi ARM kimliğine sahip sözlüğü.

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAcceleratedNetworkingOnRecovery
Yük devretme işlemi hızlandırılmış ağ kullanır

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

### -InputObject
Cmdlet 'e giriş nesnesi: Bu, güncelleştirilecek çoğaltma korumalı öğeye karşılık gelen ASR çoğaltması korumalı öğe nesnesi.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeyEncryptionKeyUrl
Yük devretmenin ardından kurtarma VM olarak kullanılacak disk şifrelemesi anahtar URL sürümünü (Azure disk şifrelemesi) belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyEncryptionVaultId
Yük devretmenin ardından kurtarma VM olarak kullanılacak Anahtar Kasası KIMLIĞI 'ni (Azure disk şifrelemesi) belirtir.


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Windows Server sanal makinelerinde kullanılacak lisans türü seçimini belirtin. Geçiş için Azure Karma Kullanım avantajını (HUB) kullanmaya hak duyuyorsanız ve bu korumalı öğenin yerine çalışırken HUB ayarının kullanılacağını belirtmek istiyorsanız, lisans türünü WindowsServer olarak ayarlayın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
Yük devretmenin ardından oluşturulacak kurtarma sanal makinesinin adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NicSelectionType
Kullanıcı tarafından ayarlanan ağ arabirim kartı (NIC) özelliklerini belirtir veya varsayılan olarak ayarlanır.
Varsayılan değerlere dönmek için NotSelected belirtebilirsiniz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Eldeki
Yük devretmenin ardından, recvcovery VM için birincil NIC olarak kullanılacak NIC 'yi belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryAvailabilitySet
Yük devretme sonrasında çoğaltma korumalı öğe için kullanılabilirlik kümesi.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Recoverybootdiagstorageaccountıd
Kurtarma Azure VM için önyükleme tanılaması depolama hesabını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Recoverycloudserviceıd
Bu sanal makinenin yük devretmesine yönelik kurtarma bulut hizmetinin kaynak KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Recoverylbbackendaddresspoıd
Kurtarma NIC ile ilişkilendirilecek hedef arka uç adres havuzlarını belirtir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Recoverynetworkıd
Korunan öğenin yük devri gerektiği Azure sanal ağının KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Recoverynetworksecuritygroupıd
Kurtarma NIC ile ilişkilendirilecek ağ güvenlik grubunun KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Recoverynicstaticıpaddress
Kurtarmada birincil NIC 'ye atanması gereken statik IP adresini belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryNicSubnetName
Korumalı öğenin bu NIC 'in yük devretmeye bağlanması gereken, kurtarma Azure sanal ağında alt ağın adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryProximityPlacementGroupId
Sanal makinenin yük devretmesine yönelik kurtarma yakınlık yerleşimi grubunun kaynak kimliğini belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryPublicIPAddressId
Kurtarma NIC ile ilişkilendirilecek genel IP adresi kaynağının KIMLIĞINI belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Recoveryresourcegroupıd
Korunan öğenin yük devretmeye kurtarılacağı kurtarma bölgesindeki Azure Kaynak grubunun KIMLIĞI.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Boyut
Kurtarma sanal makine boyutunu belirtir.
Değer, Azure sanal makinelerinin desteklediği boyutlar kümesinden olmalıdır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TfoAzureVMName
Test yük devretme VM 'sinin adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateNic
Bu cmdlet 'in kurtarma ağı özelliğini motive olarak ayarladığı sanal makinenin NIC 'ini belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseManagedDisk
Yük devretmenin üstünde oluşturulan Azure sanal makinesinin yönetilen diskleri kullanıp kullanmeyeceğini belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: True, False

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir. Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. Asrreplicationkorunabilir

## ÇıKıŞLAR

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-Azrecoveryservicesasrreplicationkorunabilir.](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[New-Azrecoveryservicesasrreplicationkorunabilir](./New-AzRecoveryServicesAsrReplicationProtectedItem.md)

[Remove-Azrecoveryservicesasrreplicationkorunabilir.](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)
