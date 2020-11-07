---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 881908cf85ff4f22fb76b7222a2c09d40a1e9e32
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917411"
---
# <span data-ttu-id="43aee-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43aee-101">Get-AzVmss</span></span>

## <span data-ttu-id="43aee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43aee-102">SYNOPSIS</span></span>
<span data-ttu-id="43aee-103">Bir VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="43aee-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="43aee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="43aee-104">SYNTAX</span></span>

### <span data-ttu-id="43aee-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="43aee-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43aee-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="43aee-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43aee-107">Osupgrade, Methodparameter</span><span class="sxs-lookup"><span data-stu-id="43aee-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43aee-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="43aee-108">DESCRIPTION</span></span>
<span data-ttu-id="43aee-109">**Get-AzVmss** cmdlet 'ı sanal makine ölçek kümesinin (VMSS) modelini ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="43aee-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="43aee-110">Model görünümü, kullanıcının belirttiği sanal makine ölçeği kümesi özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="43aee-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="43aee-111">Örnek görünümü, sanal makine ölçek kümesinin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="43aee-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="43aee-112">Yalnızca sanal makine ölçek kümesinin örnek görünümünü almak için *InstanceView* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="43aee-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="43aee-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="43aee-113">EXAMPLES</span></span>

### <span data-ttu-id="43aee-114">Örnek 1: bir VMSS özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="43aee-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"

ResourceGroupName                           : Group001
Sku                                         :
  Name                                      : Standard_DS1_v2
  Tier                                      : Standard
  Capacity                                  : 2
UpgradePolicy                               :
  Mode                                      : Manual
VirtualMachineProfile                       :
  OsProfile                                 :
    ComputerNamePrefix                      : test
    AdminUsername                           : contoso
    WindowsConfiguration                    :
      ProvisionVMAgent                      : True
      EnableAutomaticUpdates                : True
  StorageProfile                            :
    ImageReference                          :
      Publisher                             : MicrosoftWindowsServer
      Offer                                 : WindowsServer
      Sku                                   : 2016-Datacenter
      Version                               : latest
    OsDisk                                  :
      Caching                               : None
      CreateOption                          : FromImage
      ManagedDisk                           :
        StorageAccountType                  : Premium_LRS
  NetworkProfile                            :
    NetworkInterfaceConfigurations[0]       :
      Name                                  : Group001
      Primary                               : True
      EnableAcceleratedNetworking           : False
      NetworkSecurityGroup                  :
        Id                                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001
/providers/Microsoft.Network/networkSecurityGroups/Group001
      DnsSettings                           :
      IpConfigurations[0]                   :
        Name                                : Group001
        Subnet                              :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/virtualNetworks/Group001/subnets/Group001
        PrivateIPAddressVersion             : IPv4
        LoadBalancerBackendAddressPools[0]  :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/backendAddressPools/Group001
        LoadBalancerInboundNatPools[0]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
        LoadBalancerInboundNatPools[1]      :
          Id                                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/group001
/providers/Microsoft.Network/loadBalancers/Group001/inboundNatPools/Group001
      EnableIPForwarding                    : False
ProvisioningState                           : Succeeded
Overprovision                               : True
UniqueId                                    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SinglePlacementGroup                        : False
Id                                          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/Group001/
providers/Microsoft.Compute/virtualMachineScaleSets/VMSS001
Name                                        : VMSS001
Type                                        : Microsoft.Compute/virtualMachineScaleSets
Location                                    : eastus
Tags                                        : {}
```

<span data-ttu-id="43aee-115">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="43aee-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="43aee-116">Komut, *InstanceView* anahtar parametresini belirtmediğinden, cmdlet sanal makine ölçek kümesinin model görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="43aee-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="43aee-117">Örnek 2: kaynak grubundaki tüm VMSS 'leri alma</span><span class="sxs-lookup"><span data-stu-id="43aee-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="43aee-118">"Group001" kaynak grubundaki tüm VMSS 'leri alma</span><span class="sxs-lookup"><span data-stu-id="43aee-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="43aee-119">Örnek 3: abonelikteki tüm VMSS 'leri alma</span><span class="sxs-lookup"><span data-stu-id="43aee-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="43aee-120">Tüm VMSS 'leri abonelikle edinin.</span><span class="sxs-lookup"><span data-stu-id="43aee-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="43aee-121">Örnek 4: filtreleme kullanarak tüm VMSS 'leri alma</span><span class="sxs-lookup"><span data-stu-id="43aee-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="43aee-122">"VMSS00" ile başlayan tüm VMSS 'leri edinin.</span><span class="sxs-lookup"><span data-stu-id="43aee-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="43aee-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="43aee-123">PARAMETERS</span></span>

### <span data-ttu-id="43aee-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43aee-124">-DefaultProfile</span></span>
<span data-ttu-id="43aee-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="43aee-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43aee-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="43aee-126">-InstanceView</span></span>
<span data-ttu-id="43aee-127">Bu cmdlet 'in yalnızca sanal makine ölçek kümesinin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="43aee-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43aee-128">-Osupın geçmiş</span><span class="sxs-lookup"><span data-stu-id="43aee-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="43aee-129">Bu cmdlet 'in sanal makine ölçek kümesinin işletim sistemi yükseltme geçmişini listediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="43aee-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43aee-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43aee-130">-ResourceGroupName</span></span>
<span data-ttu-id="43aee-131">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="43aee-131">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="43aee-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="43aee-132">-VMScaleSetName</span></span>
<span data-ttu-id="43aee-133">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="43aee-133">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="43aee-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43aee-134">CommonParameters</span></span>
<span data-ttu-id="43aee-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="43aee-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43aee-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="43aee-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43aee-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="43aee-137">INPUTS</span></span>

### <span data-ttu-id="43aee-138">System. String</span><span class="sxs-lookup"><span data-stu-id="43aee-138">System.String</span></span>

## <span data-ttu-id="43aee-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="43aee-139">OUTPUTS</span></span>

### <span data-ttu-id="43aee-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="43aee-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="43aee-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="43aee-141">NOTES</span></span>

## <span data-ttu-id="43aee-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="43aee-142">RELATED LINKS</span></span>

[<span data-ttu-id="43aee-143">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43aee-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="43aee-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43aee-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="43aee-145">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43aee-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="43aee-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43aee-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="43aee-147">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43aee-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="43aee-148">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43aee-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="43aee-149">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="43aee-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


