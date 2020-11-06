---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 05E6155D-4F0E-406B-9312-77AD97EF66EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86a3c32dd8ee191e5a40d95b2d6cded761944c06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587617"
---
# New-AzureRmVM

## SYNOPSIS
Sanal makine oluşturur.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

### SimpleParameterSet (varsayılan)
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String> -Credential <PSCredential>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] [-ImageName <String>]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DefaultParameterSet
```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tag <Hashtable>] [-LicenseType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DiskFileParameterSet
```
New-AzureRmVM [[-ResourceGroupName] <String>] [[-Location] <String>] -Name <String>
 [-VirtualNetworkName <String>] [-AddressPrefix <String>] [-SubnetName <String>]
 [-SubnetAddressPrefix <String>] [-PublicIpAddressName <String>] [-DomainNameLabel <String>]
 [-AllocationMethod <String>] [-SecurityGroupName <String>] [-OpenPorts <Int32[]>] -DiskFile <String> [-Linux]
 [-Size <String>] [-AvailabilitySetName <String>] [-AsJob] [-DataDiskSizeInGb <Int32[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Tanım
**New-AzureRmVM** cmdlet 'i Azure 'da sanal makine oluşturur.
Bu cmdlet, giriş olarak bir sanal makine nesnesini alır.
Sanal makine nesnesi oluşturmak için New-AzureRmVMConfig cmdlet 'ini kullanın.
Diğer cmdlet 'ler, set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-Azurermvmnetworkınterface ve set-Azurermvmosdısk gibi sanal makineyi yapılandırmak için kullanılabilir.

, `SimpleParameterSet` Ortak VM oluşturma bağımsız değişkenlerini isteğe bağlı olarak yaparak VM oluşturmak için uygun bir yöntem sağlar.

## ÖRNEKLERDEN

### Örnek 1: sanal makine oluşturma
```
PS C:\> New-AzureRmVM -Name MyVm -Credential (Get-Credential)

VERBOSE: Use 'mstsc /v:myvm-222222.eastus.cloudapp.azure.com' to connect to the VM.

ResourceGroupName        : MyVm
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyVm/provi
ders/Microsoft.Compute/virtualMachines/MyVm
VmId                     : 11111111-1111-1111-1111-111111111111
Name                     : MyVm
Type                     : Microsoft.Compute/virtualMachines
Location                 : eastus
Tags                     : {}
HardwareProfile          : {VmSize}
NetworkProfile           : {NetworkInterfaces}
OSProfile                : {ComputerName, AdminUsername, WindowsConfiguration, Secrets}
ProvisioningState        : Succeeded
StorageProfile           : {ImageReference, OsDisk, DataDisks}
FullyQualifiedDomainName : myvm-222222.eastus.cloudapp.azure.com
```

Bu örnek komut dosyası, sanal makinenin nasıl oluşturulduğunu gösterir.
Komut dosyası, VM için Kullanıcı adı ve parola sorar.
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

$Credential = New-Object System.Management.Automation.PSCredential ($VMLocalAdminUser, $VMLocalAdminSecurePassword);

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

### -AddressPrefix
VM için oluşturulacak sanal ağın adres öneki.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.0.0/16
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllocationMethod
VM için oluşturulacak ortak IP için IP ayırma yöntemi.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:
Accepted values: Static, Dynamic

Required: False
Position: Named
Default value: Static
Accept pipeline input: False
Accept wildcard characters: False
```

### -Iş
Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.

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

### -Kullanılabilirlik
Kullanılabilirlik kümesi için bir ad belirtir.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
VM için yönetici kimlik bilgileri.

```yaml
Type: PSCredential
Parameter Sets: SimpleParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataDiskSizeInGb
Veri disklerinin boyutunu GB cinsinden belirtir.

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
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
Type: IAzureContextContainer
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
Type: SwitchParameter
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Diskfıle
Buluta yüklenecek sanal sabit disk dosyasının yerel yolu ve VM 'i oluşturmak için, soneki olarak '. vhd ' bulunmalıdır.

```yaml
Type: String
Parameter Sets: DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainNameLabel
VM 'nin tam etki alanı adı (FQDN) için alt etki alanı etiketi.  Bu, formu alır `{domainNameLabel}.{location}.cloudapp.azure.com` .

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GörüntüAdı
VM 'nin dayandığı kolay yansıma adı.  Bunlar şunlardır: Win2016Datacenter, Win2012R2Datacenter, Win2012Datacenter, Win2008R2SP1, UbuntuLTS, CentOS, CoreOS, de, openSUSE-

```yaml
Type: String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: Win2016Datacenter
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
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
Belirtildiyse, disk dosyasının Linux VM için olup olmadığını gösterir; Varsayılan olarak belirtilmezse, pencereler.

```yaml
Type: SwitchParameter
Parameter Sets: DiskFileParameterSet
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
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ad
VM kaynağının adı.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OpenPorts
Oluşturulan VM için ağ güvenlik grubunda (NSG) açılacak bağlantı noktalarının listesi.  Varsayılan değer, seçilen resim türüne (yani, Windows: 3389, 5985 ve Linux: 22) bağlıdır.

```yaml
Type: Int32[]
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Publicıpaddressname
Oluşturulan VM 'nin kullanması için yeni (veya mevcut) genel IP adresinin adı.  Belirtilmezse, bir ad oluşturulur.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adını belirtir.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityGroupName
Oluşturulan VM 'nin kullanması için yeni (veya mevcut) bir ağ güvenlik grubunun (NSG) adı.  Belirtilmezse, bir ad oluşturulur.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Boyut
Sanal makine boyutu.  Varsayılan değer: Standard_DS1_v2.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: Standard_DS1_v2
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetAddressPrefix
VM için oluşturulacak alt ağın adres öneki.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: 192.168.1.0/24
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
Oluşturulan VM 'nin kullanması için yeni (veya mevcut) bir alt ağın adı.  Belirtilmezse, bir ad oluşturulur.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### Etiketli
Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.
Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.
Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.

```yaml
Type: Hashtable
Parameter Sets: DefaultParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetworkName
Oluşturulan VM 'nin kullanması için yeni (veya mevcut) sanal ağının adı.  Belirtilmezse, bir ad oluşturulur.

```yaml
Type: String
Parameter Sets: SimpleParameterSet, DiskFileParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Oluşturulacak yerel sanal makineyi belirtir.
Sanal makine nesnesi edinmek için New-AzureRmVMConfig cmdlet 'ini kullanın.
AzureRmVMOperatingSystem, set-AzureRmVMSourceImage ve Add-Azurermvmnetworkınterface gibi sanal makineyi yapılandırmak için kullanılabilir.

```yaml
Type: PSVirtualMachine
Parameter Sets: DefaultParameterSet
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
Type: String[]
Parameter Sets: DefaultParameterSet
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

### PSVirtualMachine
' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse

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


