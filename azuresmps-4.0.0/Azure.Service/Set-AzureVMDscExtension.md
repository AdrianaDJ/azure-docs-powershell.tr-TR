---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94107351"
---
# Set-AzureVMDscExtension

## SYNOPSIS
Bir sanal makinede DSC uzantısını yapılandırır.

## INDEKI

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzureVMDscExtension** cmdlet 'i sanal makinede Istenen durum YAPıLANDıRMASı (DSC) uzantısını yapılandırır.

## ÖRNEKLERDEN

### Örnek 1: sanal makinede DSC uzantısını yapılandırma
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

Bu komut, bir sanal makinede DSC uzantısını yapılandırır.

MyConfiguration.ps1.zip paketi, **Publish-AzureVMDscConfiguration** komutunu kullanarak Azure depolama 'ya daha önce yüklenmiş olmalıdır ve MyConfiguration.ps1 betiğini ve bağımlı olduğu modülleri içerir.

MyConfiguration bağımsız değişkeni, komut dosyasının yürütüleceği belirli DSC yapılandırmasını gösterir.
- *Configurationargument* parametresi, yapılandırma işlevine iletilen bağımsız değişkenlerle birlikte bir Hashtable belirtir.

### Örnek 2: yapılandırma verilerine yol kullanarak sanal makinedeki DSC uzantısını yapılandırma
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

Bu komut, yapılandırma verilerine yol kullanarak sanal makinedeki DSC uzantısını yapılandırır.

## PARAMETRELERINE

### -ConfigurationArchive
Daha önce Publish-AzureVMDscConfiguration tarafından karşıya yüklenen yapılandırma paketinin (. zip dosyası) adını belirtir.
Bu parametrenin, herhangi bir yol olmadan yalnızca dosyanın adını belirtmesi gerekir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationArgument
Yapılandırma işlevinin bağımsız değişkenlerini belirten bir Hashtable belirtir.
Anahtarlar parametre adlarına ve parametre değerlerinin değerlerine karşılık gelir.

Bu parametre için kabul edilebilir değerler şunlardır:

- ilkel türler
- dizisi
- dizisinde
- Pscrential

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Yapılandırma işlevi için verileri belirten bir. psd1 dosyasının yolunu belirtir.
Bu dosyada, yapılandırma ve ortam verilerini ayırma başlığı altında açıklandığı gibi bir Hashtable bulunmalıdır https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationName
DSC Uzantısı tarafından çağrılan yapılandırma dosyasının veya modülün adını belirtir.

Bu parametrenin değeri, *Configurationarchive* 'de paketlenmiş betiklerin veya modüllerdeki bulunan yapılandırma işlevlerinden birinin adı olmalıdır.

Bu cmdlet, herhangi bir uzantıyı dışlayarak, *Configurationarchive* parametresi tarafından verilen dosyanın adını varsayılan olarak belirler.
Örneğin, *Configurationarchive* "SalesWebSite.ps1.zip" Ise, *ConfigurationName* Için varsayılan değer "satışsitesi" olur.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Kapsayıcıadı
*Configurationarchive* 'ın bulunduğu Azure depolama kapsayıcısının adını belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DataCollection
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Bu cmdlet 'in var olan blob 'ları üzerine yaztığını gösterir.

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

### -Informationaction
Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.

Bu parametre için kabul edilebilir değerler şunlardır:

- 'A
- Manıza
- Sorgulamak
- Sustlıkdevam
- Durdurduğunuzda
- Biliriz

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Informationvariable
Bir bilgi değişkeni belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

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

### -ReferenceName
Uzantıya başvurmak için kullanılabilecek Kullanıcı tanımlı bir dize belirtir.
Bu parametre, uzantı sanal makineye ilk kez eklendiğinde belirtilir.
Sonraki güncelleştirmelerde, uzantıyı güncelleştirirken önceden kullanılmış başvuru adını belirtmeniz gerekir.
Uzantıya atanan *ReferenceName* , **Get-AzureVM** cmdlet 'i kullanılarak döndürülür.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
Yapılandırma komut dosyasına erişmek için kullanılan güvenlik ayarlarını sağlayan Azure depolama bağlamını belirtir.
Bu bağlam, *ContainerName* parametresinde belirtilen kapsayıcıya okuma erişimi sağlar.

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Tüm depolama hizmetleri için DNS uç noktası sonekini (örneğin, "core.contoso.net") belirtir.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
DSC uzantısının kullanılacak sürümünü belirtir.
Bu parametre belirtilmemişse varsayılan değer "1. *" olarak ayarlanır.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Kalıcı sanal makine nesnesini belirtir.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WmfVersion
Sanal makineye yüklenecek Windows Yönetim çerçevesi (WMF) sürümünü belirtir.
DSC Uzantısı, yalnızca WMF güncelleştirmelerinde bulunan DSC özelliklerine bağlıdır.
Bu parametre, güncelleştirmenin hangi sürümünün sanal makineye yükleneceğini belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:

- 4,0.
Daha yeni bir sürüm yüklü değilse, WMF 4,0 'i yükler.
- 5,0.
WMF 5,0 'in en son sürümünü yükler.
- sürümü.
En son WMF, şu anda WMF 5,0 yükler.

Varsayılan değer en son olur.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Onay
Cmdlet 'i çalıştırmadan önce onaylamanızı ister.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.
Cmdlet çalışmaz.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

## ÇıKıŞLAR

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureVMDscExtension](./Get-AzureVMDscExtension.md)

[Remove-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[Remove-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[Get-AzureVM](./Get-AzureVM.md)

[Yayımla-AzureVMDscConfiguration](./Publish-AzureVMDscConfiguration.md)


