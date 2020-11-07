---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 7985a979f9bbb89d6594416575e3fa00640784b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938395"
---
# <span data-ttu-id="acbe5-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="acbe5-101">Get-AzVmss</span></span>

## <span data-ttu-id="acbe5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acbe5-102">SYNOPSIS</span></span>
<span data-ttu-id="acbe5-103">Bir VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="acbe5-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="acbe5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="acbe5-104">SYNTAX</span></span>

### <span data-ttu-id="acbe5-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="acbe5-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acbe5-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="acbe5-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="acbe5-107">Osupgrade, Methodparameter</span><span class="sxs-lookup"><span data-stu-id="acbe5-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acbe5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="acbe5-108">DESCRIPTION</span></span>
<span data-ttu-id="acbe5-109">**Get-AzVmss** cmdlet 'ı sanal makine ölçek kümesinin (VMSS) modelini ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="acbe5-109">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="acbe5-110">Model görünümü, kullanıcının belirttiği sanal makine ölçeği kümesi özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="acbe5-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="acbe5-111">Örnek görünümü, sanal makine ölçek kümesinin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="acbe5-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="acbe5-112">Yalnızca sanal makine ölçek kümesinin örnek görünümünü almak için *InstanceView* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="acbe5-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="acbe5-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="acbe5-113">EXAMPLES</span></span>

### <span data-ttu-id="acbe5-114">Örnek 1: bir VMSS özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="acbe5-114">Example 1: Get the properties of a VMSS</span></span>
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

<span data-ttu-id="acbe5-115">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="acbe5-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="acbe5-116">Komut, *InstanceView* anahtar parametresini belirtmediğinden, cmdlet sanal makine ölçek kümesinin model görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="acbe5-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

### <span data-ttu-id="acbe5-117">Örnek 2: kaynak grubundaki tüm VMSS 'leri alma</span><span class="sxs-lookup"><span data-stu-id="acbe5-117">Example 2: Get all Vmss in a resource group</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001"

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
```

<span data-ttu-id="acbe5-118">"Group001" kaynak grubundaki tüm VMSS 'leri alma</span><span class="sxs-lookup"><span data-stu-id="acbe5-118">Get all Vmss in resource group "Group001"</span></span>

### <span data-ttu-id="acbe5-119">Örnek 3: abonelikteki tüm VMSS 'leri alma</span><span class="sxs-lookup"><span data-stu-id="acbe5-119">Example 3: Get all Vmss in a subscription</span></span>
```
PS C:\> Get-AzVmss

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="acbe5-120">Tüm VMSS 'leri abonelikle edinin.</span><span class="sxs-lookup"><span data-stu-id="acbe5-120">Get all Vmss in subscription.</span></span>

### <span data-ttu-id="acbe5-121">Örnek 4: filtreleme kullanarak tüm VMSS 'leri alma</span><span class="sxs-lookup"><span data-stu-id="acbe5-121">Example 4: Get all Vmss using filtering</span></span>
```
PS C:\> Get-AzVmss -Name VMSS00*

ResourceGroupName                               Name       Location             Sku Capacity ProvisioningState
-----------------                               ----       --------             --- -------- -----------------
Group001                                       VMSS001      eastus Standard_DS1_v2        2         Succeeded
Group001                                       VMSS002      eastus     Standard_A1        2         Succeeded
Group002                                       VMSS003      eastus     Standard_A1        1         Succeeded
Group002                                       VMSS004      eastus Standard_DS1_v2        2         Succeeded
```

<span data-ttu-id="acbe5-122">"VMSS00" ile başlayan tüm VMSS 'leri edinin.</span><span class="sxs-lookup"><span data-stu-id="acbe5-122">Get all Vmss in subscription that start with "VMSS00".</span></span>

## <span data-ttu-id="acbe5-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="acbe5-123">PARAMETERS</span></span>

### <span data-ttu-id="acbe5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acbe5-124">-DefaultProfile</span></span>
<span data-ttu-id="acbe5-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="acbe5-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acbe5-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="acbe5-126">-InstanceView</span></span>
<span data-ttu-id="acbe5-127">Bu cmdlet 'in yalnızca sanal makine ölçek kümesinin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="acbe5-127">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="acbe5-128">-Osupın geçmiş</span><span class="sxs-lookup"><span data-stu-id="acbe5-128">-OSUpgradeHistory</span></span>
<span data-ttu-id="acbe5-129">Bu cmdlet 'in sanal makine ölçek kümesinin işletim sistemi yükseltme geçmişini listediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="acbe5-129">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="acbe5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acbe5-130">-ResourceGroupName</span></span>
<span data-ttu-id="acbe5-131">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="acbe5-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="acbe5-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="acbe5-132">-VMScaleSetName</span></span>
<span data-ttu-id="acbe5-133">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="acbe5-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="acbe5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acbe5-134">CommonParameters</span></span>
<span data-ttu-id="acbe5-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="acbe5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acbe5-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="acbe5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acbe5-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="acbe5-137">INPUTS</span></span>

### <span data-ttu-id="acbe5-138">System. String</span><span class="sxs-lookup"><span data-stu-id="acbe5-138">System.String</span></span>

## <span data-ttu-id="acbe5-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="acbe5-139">OUTPUTS</span></span>

### <span data-ttu-id="acbe5-140">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="acbe5-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="acbe5-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="acbe5-141">NOTES</span></span>

## <span data-ttu-id="acbe5-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="acbe5-142">RELATED LINKS</span></span>

[<span data-ttu-id="acbe5-143">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="acbe5-143">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="acbe5-144">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="acbe5-144">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="acbe5-145">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="acbe5-145">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="acbe5-146">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="acbe5-146">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="acbe5-147">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="acbe5-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="acbe5-148">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="acbe5-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="acbe5-149">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="acbe5-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


