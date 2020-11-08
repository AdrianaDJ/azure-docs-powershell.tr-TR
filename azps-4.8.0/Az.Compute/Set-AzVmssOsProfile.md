---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110006"
---
# Set-AzVmssOsProfile

## SYNOPSIS
VMSS işletim sistemi profili özelliklerini ayarlar.

## INDEKI

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**Set-AzVmssOsProfile** cmdlet 'ı, sanal makine ölçeğini ayarlama işletim sistemi profili özelliklerini ayarlar.

## ÖRNEKLERDEN

### Örnek 1: bir VMSS için işletim sistemi profili özelliklerini ayarlama
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

Bu komut, ContosoVMSS adlı VMSS 'ye ait sanal makinelerin işletim sistemi profili özelliklerini ayarlar.
Bu komut, VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini, yöneticinin kullanıcı adını ve parolasını test etmek üzere ayarlar.

## PARAMETRELERINE

### -Additionalunattenvseçcontent
Bir katılımsız içerik nesnesi belirtir.
Nesneyi oluşturmak için Add-AzVMAdditionalUnattendContent kullanabilirsiniz.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminPassword
VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici parolasını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminUsername
VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici hesap adını belirtir. <br>
**Yalnızca Windows sınırlaması:** Bitemez \" .\" <br>
**Izin verilmeyen değerler:** \" yönetici \" , \" yönetici \" , \" Kullanıcı \" , \" kullanıcı1 \" , \" Test \" , \" kullanıcı2 \" , \" test1 \" , \" User3 \" , \" admin1 \" , \" 1 \" , \" 123 \" , \" a \" , \" ACTUser \" , \" ADM \" , \" Admin2 \" , \" ASPNET \" , \" Yedekleme \" , \" konsol \" , \" David \" , \" Guest \" , \" barış \" , \" Owner \" , \" root \" , \" Server \" , \" SQL \" , \" Destek \" , \" SUPPORT_388945a0 \" , \" sys \" , \" test2 \" , \" test3 \" , \" User4 \" , \" user5 \" . <br>
**Minimum uzunluk (Linux):** 1 karakter <br>
**En büyük uzunluk (Linux):** 64 karakterler <br>
**En büyük uzunluk (Windows):** 20 karakter  <br>
<li> Linux VM 'ye kök erişimi için, [Azure 'Daki Linux sanal makinelerde kök ayrıcalıklarını kullanma](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)konusuna bakın.<br>
<li> Linux 'taki, bu alanda kullanılması gereken yerleşik sistem kullanıcıları listesi için, [bkz.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ComputerNamePrefix
VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini belirtir.
Bilgisayar adları 1-15 karakter uzunluğunda olmalıdır.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
Özel verilerin Base-64 kodlu dizesini belirtir.
Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.
İkili dizinin en fazla uzunluğu 65535 bayttır. <br>
VM 'unuzda bulut-init kullanmak için, [oluşturma sırasında bir LINUX VM 'yi özelleştirmek amacıyla Cloud-Init kullanma](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)konusuna bakın.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -LinuxConfigurationDisablePasswordAuthentication
Bu cmdlet 'in parola kimlik doğrulamasını devre dışı bırakacağını gösterir.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Listener
Windows Uzaktan Yönetim (WinRM) dinleyicilerini belirtir.
Bu, uzak Windows PowerShell 'i etkinleştirmiştir.
Dinleyiciyi oluşturmak için Add-AzVmssWinRMListener cmdlet 'ini kullanabilirsiniz.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicKey
Güvenli Kabuk (SSH) ortak anahtar nesnesini belirtir.
Nesneyi oluşturmak için Add-AzVMSshPublicKey cmdlet 'ini kullanabilirsiniz.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Parola
Sanal makineye yerleştirilecek sertifika başvurularını içeren gizli nesne türünü belirtir.
Gizli nesneleri oluşturmak için Add-AzVmssSecret cmdlet 'ini kullanabilirsiniz.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Sanal makinenin saat dilimini belirtir. Örneğin \" Pasifik standart saati \" . <br>
Olası değerler, [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)tarafından döndürülen saat dilimlerinde [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) değeri olabilir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
VMSS nesnesini belirtir.
Nesneyi oluşturmak için New-AzVmssConfig cmdlet 'ini kullanabilirsiniz.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WindowsConfigurationEnableAutomaticUpdate
VMSS 'deki sanal makinelerin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowsConfigurationProvisionVMAgent
VMSS 'deki sanal makinelerde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet

### System. String

### System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]

### Microsoft. Azure. Management. COMPUTE. modeller. Addiunattenvseçcontent []

### Microsoft. Azure. Management. COMPUTE. model. WinRMListener []

### Microsoft. Azure. Management. COMPUTE. model. SshPublicKey []

### Microsoft. Azure. Management. COMPUTE. modeller. VaultSecretGroup []

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Add-AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[Add-AzVmssWinRMListener](./Add-AzVmssWinRMListener.md)

[Add-AzVMSshPublicKey](./Add-AzVMSshPublicKey.md)

[Add-AzVmssSecret](./Add-AzVmssSecret.md)

[Yeni-AzVmssConfig](./New-AzVmssConfig.md)


