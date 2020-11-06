---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVM.md
ms.openlocfilehash: a5a15ed27b5a862513b15667b343e932dc2571e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594786"
---
# New-AzureRmVM

## SYNOPSIS
Sanal makine oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tags <Hashtable>] [-LicenseType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzureRmVM** cmdlet 'i Azure 'da sanal makine oluşturur.
Bu cmdlet, giriş olarak bir sanal makine nesnesini alır.
Sanal makine nesnesi oluşturmak için New-AzureRmVMConfig cmdlet 'ini kullanın.
Diğer cmdlet 'ler, set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-Azurermvmnetworkınterface ve set-Azurermvmosdısk gibi sanal makineyi yapılandırmak için kullanılabilir.

## ÖRNEKLERDEN

### Örnek 1: sanal makine oluşturma
```
PS C:\> # Variables    
## Global
$ResourceGroupName = "ResourceGroup11"
$Location = "WestEurope"

## Storage
$StorageName = "generalstorage6cc"
$StorageType = "Standard_GRS"

## Network
$InterfaceName = "ServerInterface06"
$Subnet1Name = "Subnet1"
$VNetName = "VNet09"
$VNetAddressPrefix = "10.0.0.0/16"
$VNetSubnetAddressPrefix = "10.0.0.0/24"

## Compute
$VMName = "VirtualMachine12"
$ComputerName = "Server22"
$VMSize = "Standard_A2"
$OSDiskName = $VMName + "OSDisk"

# Resource Group
New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Type $StorageType -Location $Location

# Network
$PIp = New-AzureRmPublicIpAddress -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -AllocationMethod Dynamic
$SubnetConfig = New-AzureRmVirtualNetworkSubnetConfig -Name $Subnet1Name -AddressPrefix $VNetSubnetAddressPrefix
$VNet = New-AzureRmVirtualNetwork -Name $VNetName -ResourceGroupName $ResourceGroupName -Location $Location -AddressPrefix $VNetAddressPrefix -Subnet $SubnetConfig
$Interface = New-AzureRmNetworkInterface -Name $InterfaceName -ResourceGroupName $ResourceGroupName -Location $Location -SubnetId $VNet.Subnets[0].Id -PublicIpAddressId $PIp.Id

# Compute

## Setup local VM object
$Credential = Get-Credential
$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Set-AzureRmVMSourceImage -VM $VirtualMachine -PublisherName MicrosoftWindowsServer -Offer WindowsServer -Skus 2012-R2-Datacenter -Version "latest"
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $Interface.Id
$OSDiskUri = $StorageAccount.PrimaryEndpoints.Blob.ToString() + "vhds/" + $OSDiskName + ".vhd"
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -CreateOption FromImage

## Create the VM in Azure
New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $Location -VM $VirtualMachine
```

Bu örnek komut dosyası, sanal makinenin nasıl oluşturulduğunu gösterir.
Bu komut dosyası birkaç başka cmdlet kullanır.

### Örnek 2: özel Kullanıcı görüntüsünden sanal makine oluşturma
```
PS C:\> ## VM Account
# Credentials for Local Admin account you created in the sysprepped (generalized) vhd image
$VMLocalAdminUser = "LocalAdminUser"
$VMLocalAdminSecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force 
## Azure Account
$LocationName = "westus"
$ResourceGroupName = "MyResourceGroup"
# This a Premium_LRS storage account. 
# It is required in order to run a client VM with efficiency and high performance.
$StorageAccount = "Mydisk"

## VM
$OSDiskName = "MyClient"
$ComputerName = "MyClientVM"
$OSDiskUri = "https://Mydisk.blob.core.windows.net/disks/MyOSDisk.vhd"
$SourceImageUri = "https://Mydisk.blob.core.windows.net/vhds/MyOSImage.vhd"
$VMName = "MyVM"
# Modern hardware environment with fast disk, high IOPs performance. 
# Required to run a client VM with efficiency and performance
$VMSize = "Standard_DS3" 
$OSDiskCaching = "ReadWrite"
$OSCreateOption = "FromImage"

## Networking
$DNSNameLabel = "mydnsname" # mydnsname.westus.cloudapp.azure.com
$NetworkName = "MyNet"
$NICName = "MyNIC"
$PublicIPAddressName = "MyPIP"
$SubnetName = "MySubnet"
$SubnetAddressPrefix = "10.0.0.0/24"
$VnetAddressPrefix = "10.0.0.0/16"

$SingleSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name $SubnetName -AddressPrefix $SubnetAddressPrefix
$Vnet = New-AzureRmVirtualNetwork -Name $NetworkName -ResourceGroupName $ResourceGroupName -Location $LocationName -AddressPrefix $VnetAddressPrefix -Subnet $SingleSubnet
$PIP = New-AzureRmPublicIpAddress -Name $PublicIPAddressName -DomainNameLabel $DNSNameLabel -ResourceGroupName $ResourceGroupName -Location $LocationName -AllocationMethod Dynamic
$NIC = New-AzureRmNetworkInterface -Name $NICName -ResourceGroupName $ResourceGroupName -Location $LocationName -SubnetId $Vnet.Subnets[0].Id -PublicIpAddressId $PIP.Id

$Crededntial = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword); 

$VirtualMachine = New-AzureRmVMConfig -VMName $VMName -VMSize $VMSize
$VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -ProvisionVMAgent -EnableAutoUpdate
$VirtualMachine = Add-AzureRmVMNetworkInterface -VM $VirtualMachine -Id $NIC.Id
$VirtualMachine = Set-AzureRmVMOSDisk -VM $VirtualMachine -Name $OSDiskName -VhdUri $OSDiskUri -SourceImageUri $SourceImageUri -Caching $OSDiskCaching -CreateOption $OSCreateOption -Windows

New-AzureRmVM -ResourceGroupName $ResourceGroupName -Location $LocationName -VM $VirtualMachine -Verbose
```

Bu örnekte, mevcut bir sys önceden yazılmış, genelleştirilmiş özel işletim sistemi görüntüsü yer alır ve bir veri disketi eklenir; yeni bir ağ sağlar, VHD 'yi dağıtır ve çalıştırır.

Bu komut dosyası, Kullanıcı etkileşimi gerektiren **Get-Credential** ' i aramak yerine, yerel sanal makine yöneticisi kimlik bilgilerini satır içi kullandığı için otomatik sağlama için kullanılabilir.

Bu komut dosyası Azure hesabınızda oturum açtığınız varsayılır.
**Get-azuyeniden gönderme scripscripts** cmdlet 'ini kullanarak oturum açma durumunuzu doğrulayabilirsiniz.

## PARAMETRELERINE

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableBginfoExtension
Bu cmdlet 'in sanal makinedeki **bg Info** uzantısını yüklemediğini gösterir.

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

### -LicenseType
Sanal makinenin resmi veya diskinin şirket içi lisanslı olduğunu belirten bir lisans türü belirtir.
Bu değer yalnızca Windows Server işletim sistemi içeren resimler için kullanılır.
Bu parametre için kabul edilebilir değerler şunlardır:

- Windows_Client 
- Windows_Server

Bu değer güncelleştirilemez.
Güncelleştirme için bu parametreyi belirtirseniz, değer sanal makinenin başlangıç değeriyle eşleşmelidir.

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

### -Konum
Sanal makinenin konumunu belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Etiketler
Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.
Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.
Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Oluşturulacak yerel sanal makineyi belirtir.
Sanal makine nesnesi edinmek için New-AzureRmVMConfig cmdlet 'ini kullanın.
AzureRmVMOperatingSystem, set-AzureRmVMSourceImage ve Add-Azurermvmnetworkınterface gibi sanal makineyi yapılandırmak için kullanılabilir.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Bölge
Sanal makinenin bölge listesini belirtir.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet çalışırsa ne olacağını gösterir.

Cmdlet çalışmaz.

```yaml
Type: System.Management.Automation.SwitchParameter
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

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Remove-AzureRmVM](./Remove-AzureRmVM.md)

[Restart-AzureRmVM](./Restart-AzureRmVM.md)

[Başlangıç-AzureRmVM](./Start-AzureRmVM.md)

[Stop-AzureRmVM](./Stop-AzureRmVM.md)

[Güncelleştirme-AzureRmVM](./Update-AzureRmVM.md)

[Add-AzureRmVMDataDisk](./Add-AzureRmVMDataDisk.md)

[Add-Azurermvmnetworkınterface](./Add-AzureRmVMNetworkInterface.md)

[Yeni-AzureRmVMConfig](./New-AzureRmVMConfig.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)

[Set-AzureRmVMSourceImage](./Set-AzureRmVMSourceImage.md)

[Set-AzureRmVMOSDisk](./Set-AzureRmVMOSDisk.md)


