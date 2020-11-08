---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 9e52131bd5f53d48b4c958c26a0ef37b5ebd23ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277632"
---
# <span data-ttu-id="031ee-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="031ee-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="031ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="031ee-102">SYNOPSIS</span></span>
<span data-ttu-id="031ee-103">VMSS 'ye ağ arabirimi yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="031ee-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="031ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="031ee-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="031ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="031ee-105">DESCRIPTION</span></span>
<span data-ttu-id="031ee-106">**Add-Azvmssnetworkınterfaceconfiguration** cmdlet 'ı sanal makine ölçek kümesine (VMSS) bir ağ arabirim yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="031ee-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="031ee-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="031ee-107">EXAMPLES</span></span>

### <span data-ttu-id="031ee-108">Örnek 1: VMSS 'ye ağ arabirimi yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="031ee-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="031ee-109">Bu komut, VMSS 'ye bir ağ arabirimi yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="031ee-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="031ee-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="031ee-110">PARAMETERS</span></span>

### <span data-ttu-id="031ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="031ee-111">-DefaultProfile</span></span>
<span data-ttu-id="031ee-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="031ee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="031ee-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="031ee-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="031ee-114">DNS ayarları için DNS sunucusu IP adreslerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="031ee-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031ee-115">-Enableiv</span><span class="sxs-lookup"><span data-stu-id="031ee-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="031ee-116">Ağ arabiriminin hızlandırılmış ağ özellikli olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="031ee-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="031ee-117">-Enableipiletme</span><span class="sxs-lookup"><span data-stu-id="031ee-117">-EnableIPForwarding</span></span>
<span data-ttu-id="031ee-118">Bu NIC 'de IP iletiminin etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="031ee-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="031ee-119">-ID</span><span class="sxs-lookup"><span data-stu-id="031ee-119">-Id</span></span>
<span data-ttu-id="031ee-120">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="031ee-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="031ee-121">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="031ee-121">-IpConfiguration</span></span>
<span data-ttu-id="031ee-122">Ağ arabiriminin IP yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="031ee-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031ee-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="031ee-123">-Name</span></span>
<span data-ttu-id="031ee-124">Ağ arabirimi yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="031ee-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="031ee-125">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="031ee-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="031ee-126">Ağ güvenlik grubunun kimliği.</span><span class="sxs-lookup"><span data-stu-id="031ee-126">Id of the network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031ee-127">-Birincil</span><span class="sxs-lookup"><span data-stu-id="031ee-127">-Primary</span></span>
<span data-ttu-id="031ee-128">Ağ arabirimi yapılandırmasından oluşturulan ağ arabirimlerinin sanal makinenin birincil ağ bilgi merkezi (NIC) olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="031ee-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="031ee-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="031ee-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="031ee-130">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="031ee-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="031ee-131">Nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="031ee-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="031ee-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="031ee-132">-Confirm</span></span>
<span data-ttu-id="031ee-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="031ee-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="031ee-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="031ee-134">-WhatIf</span></span>
<span data-ttu-id="031ee-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="031ee-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="031ee-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="031ee-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="031ee-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="031ee-137">CommonParameters</span></span>
<span data-ttu-id="031ee-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="031ee-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="031ee-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="031ee-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="031ee-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="031ee-140">INPUTS</span></span>

### <span data-ttu-id="031ee-141">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="031ee-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="031ee-142">System. String</span><span class="sxs-lookup"><span data-stu-id="031ee-142">System.String</span></span>

### <span data-ttu-id="031ee-143">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="031ee-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="031ee-144">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="031ee-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="031ee-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="031ee-145">System.String[]</span></span>

## <span data-ttu-id="031ee-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="031ee-146">OUTPUTS</span></span>

### <span data-ttu-id="031ee-147">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="031ee-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="031ee-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="031ee-148">NOTES</span></span>

## <span data-ttu-id="031ee-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="031ee-149">RELATED LINKS</span></span>

[<span data-ttu-id="031ee-150">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="031ee-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
