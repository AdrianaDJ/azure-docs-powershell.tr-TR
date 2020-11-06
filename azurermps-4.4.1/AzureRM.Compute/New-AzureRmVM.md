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
# <span data-ttu-id="799ea-101">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="799ea-101">New-AzureRmVM</span></span>

## <span data-ttu-id="799ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="799ea-102">SYNOPSIS</span></span>
<span data-ttu-id="799ea-103">Sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="799ea-103">Creates a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="799ea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="799ea-104">SYNTAX</span></span>

```
New-AzureRmVM [-ResourceGroupName] <String> [-Location] <String> [-VM] <PSVirtualMachine> [[-Zone] <String[]>]
 [-DisableBginfoExtension] [-Tags <Hashtable>] [-LicenseType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="799ea-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="799ea-105">DESCRIPTION</span></span>
<span data-ttu-id="799ea-106">**New-AzureRmVM** cmdlet 'i Azure 'da sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="799ea-106">The **New-AzureRmVM** cmdlet creates a virtual machine in Azure.</span></span>
<span data-ttu-id="799ea-107">Bu cmdlet, giriş olarak bir sanal makine nesnesini alır.</span><span class="sxs-lookup"><span data-stu-id="799ea-107">This cmdlet takes a virtual machine object as input.</span></span>
<span data-ttu-id="799ea-108">Sanal makine nesnesi oluşturmak için New-AzureRmVMConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="799ea-108">Use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>
<span data-ttu-id="799ea-109">Diğer cmdlet 'ler, set-AzureRmVMOperatingSystem, set-AzureRmVMSourceImage, Add-Azurermvmnetworkınterface ve set-Azurermvmosdısk gibi sanal makineyi yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="799ea-109">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, Add-AzureRmVMNetworkInterface, and Set-AzureRmVMOSDisk.</span></span>

## <span data-ttu-id="799ea-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="799ea-110">EXAMPLES</span></span>

### <span data-ttu-id="799ea-111">Örnek 1: sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="799ea-111">Example 1: Create a virtual machine</span></span>
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

<span data-ttu-id="799ea-112">Bu örnek komut dosyası, sanal makinenin nasıl oluşturulduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="799ea-112">This example script shows how to create a virtual machine.</span></span>
<span data-ttu-id="799ea-113">Bu komut dosyası birkaç başka cmdlet kullanır.</span><span class="sxs-lookup"><span data-stu-id="799ea-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="799ea-114">Örnek 2: özel Kullanıcı görüntüsünden sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="799ea-114">Example 2: Create a virtual machine from a custom user image</span></span>
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

<span data-ttu-id="799ea-115">Bu örnekte, mevcut bir sys önceden yazılmış, genelleştirilmiş özel işletim sistemi görüntüsü yer alır ve bir veri disketi eklenir; yeni bir ağ sağlar, VHD 'yi dağıtır ve çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="799ea-115">This example takes an existing sys-prepped, generalized custom operating system image and attaches a data disk to it, provisions a new network, deploys the VHD, and runs it.</span></span>

<span data-ttu-id="799ea-116">Bu komut dosyası, Kullanıcı etkileşimi gerektiren **Get-Credential** ' i aramak yerine, yerel sanal makine yöneticisi kimlik bilgilerini satır içi kullandığı için otomatik sağlama için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="799ea-116">This script can be used for automatic provisioning because it uses the local virtual machine admin credentials inline instead of calling **Get-Credential** which requires user interaction.</span></span>

<span data-ttu-id="799ea-117">Bu komut dosyası Azure hesabınızda oturum açtığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="799ea-117">This script assumes that you are already logged into your Azure account.</span></span>
<span data-ttu-id="799ea-118">**Get-azuyeniden gönderme scripscripts** cmdlet 'ini kullanarak oturum açma durumunuzu doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="799ea-118">You can confirm your login status by using the **Get-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="799ea-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="799ea-119">PARAMETERS</span></span>

### <span data-ttu-id="799ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="799ea-120">-DefaultProfile</span></span>
<span data-ttu-id="799ea-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="799ea-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="799ea-122">-DisableBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="799ea-122">-DisableBginfoExtension</span></span>
<span data-ttu-id="799ea-123">Bu cmdlet 'in sanal makinedeki **bg Info** uzantısını yüklemediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="799ea-123">Indicates that this cmdlet does not install the **BG Info** extension on the virtual machine.</span></span>

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

### <span data-ttu-id="799ea-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="799ea-124">-LicenseType</span></span>
<span data-ttu-id="799ea-125">Sanal makinenin resmi veya diskinin şirket içi lisanslı olduğunu belirten bir lisans türü belirtir.</span><span class="sxs-lookup"><span data-stu-id="799ea-125">Specifies a license type, which indicates that the image or disk for the virtual machine was licensed on-premises.</span></span>
<span data-ttu-id="799ea-126">Bu değer yalnızca Windows Server işletim sistemi içeren resimler için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="799ea-126">This value is used only for images that contain the Windows Server operating system.</span></span>
<span data-ttu-id="799ea-127">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="799ea-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="799ea-128">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="799ea-128">Windows_Client</span></span> 
- <span data-ttu-id="799ea-129">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="799ea-129">Windows_Server</span></span>

<span data-ttu-id="799ea-130">Bu değer güncelleştirilemez.</span><span class="sxs-lookup"><span data-stu-id="799ea-130">This value cannot be updated.</span></span>
<span data-ttu-id="799ea-131">Güncelleştirme için bu parametreyi belirtirseniz, değer sanal makinenin başlangıç değeriyle eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="799ea-131">If you specify this parameter for an update, the value must match the initial value for the virtual machine.</span></span>

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

### <span data-ttu-id="799ea-132">-Konum</span><span class="sxs-lookup"><span data-stu-id="799ea-132">-Location</span></span>
<span data-ttu-id="799ea-133">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="799ea-133">Specifies a location for the virtual machine.</span></span>

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

### <span data-ttu-id="799ea-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="799ea-134">-ResourceGroupName</span></span>
<span data-ttu-id="799ea-135">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="799ea-135">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="799ea-136">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="799ea-136">-Tags</span></span>
<span data-ttu-id="799ea-137">Kaynakların ve kaynak gruplarının ad-değer çiftleri kümesiyle etiketlenemeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="799ea-137">Specifies that resources and resource groups can be tagged with a set of name-value pairs.</span></span>
<span data-ttu-id="799ea-138">Kaynaklara etiket eklemek, kaynakları kaynak grupları arasında birlikte gruplandırmanızı ve kendi görünümlerinizi oluşturmanızı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="799ea-138">Adding tags to resources enables you to group resources together across resource groups and to create your own views.</span></span>
<span data-ttu-id="799ea-139">Her kaynak veya kaynak grubunda en fazla 15 etiket olabilir.</span><span class="sxs-lookup"><span data-stu-id="799ea-139">Each resource or resource group can have a maximum of 15 tags.</span></span>

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

### <span data-ttu-id="799ea-140">-VM</span><span class="sxs-lookup"><span data-stu-id="799ea-140">-VM</span></span>
<span data-ttu-id="799ea-141">Oluşturulacak yerel sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="799ea-141">Specifies a local virtual machine to create.</span></span>
<span data-ttu-id="799ea-142">Sanal makine nesnesi edinmek için New-AzureRmVMConfig cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="799ea-142">To obtain a virtual machine object, use the New-AzureRmVMConfig cmdlet.</span></span>
<span data-ttu-id="799ea-143">AzureRmVMOperatingSystem, set-AzureRmVMSourceImage ve Add-Azurermvmnetworkınterface gibi sanal makineyi yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="799ea-143">Other cmdlets can be used to configure the virtual machine, such as Set-AzureRmVMOperatingSystem, Set-AzureRmVMSourceImage, and Add-AzureRmVMNetworkInterface.</span></span>

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

### <span data-ttu-id="799ea-144">-Bölge</span><span class="sxs-lookup"><span data-stu-id="799ea-144">-Zone</span></span>
<span data-ttu-id="799ea-145">Sanal makinenin bölge listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="799ea-145">Specifies the zone list of the virtual machine.</span></span>

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

### <span data-ttu-id="799ea-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="799ea-146">-Confirm</span></span>
<span data-ttu-id="799ea-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="799ea-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="799ea-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="799ea-148">-WhatIf</span></span>
<span data-ttu-id="799ea-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="799ea-149">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="799ea-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="799ea-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="799ea-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="799ea-151">CommonParameters</span></span>
<span data-ttu-id="799ea-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="799ea-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="799ea-153">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="799ea-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="799ea-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="799ea-154">INPUTS</span></span>

## <span data-ttu-id="799ea-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="799ea-155">OUTPUTS</span></span>

## <span data-ttu-id="799ea-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="799ea-156">NOTES</span></span>

## <span data-ttu-id="799ea-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="799ea-157">RELATED LINKS</span></span>

[<span data-ttu-id="799ea-158">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="799ea-158">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="799ea-159">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="799ea-159">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="799ea-160">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="799ea-160">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="799ea-161">Başlangıç-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="799ea-161">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="799ea-162">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="799ea-162">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="799ea-163">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="799ea-163">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)

[<span data-ttu-id="799ea-164">Add-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="799ea-164">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="799ea-165">Add-Azurermvmnetworkınterface</span><span class="sxs-lookup"><span data-stu-id="799ea-165">Add-AzureRmVMNetworkInterface</span></span>](./Add-AzureRmVMNetworkInterface.md)

[<span data-ttu-id="799ea-166">Yeni-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="799ea-166">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="799ea-167">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="799ea-167">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="799ea-168">Set-AzureRmVMSourceImage</span><span class="sxs-lookup"><span data-stu-id="799ea-168">Set-AzureRmVMSourceImage</span></span>](./Set-AzureRmVMSourceImage.md)

[<span data-ttu-id="799ea-169">Set-AzureRmVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="799ea-169">Set-AzureRmVMOSDisk</span></span>](./Set-AzureRmVMOSDisk.md)


