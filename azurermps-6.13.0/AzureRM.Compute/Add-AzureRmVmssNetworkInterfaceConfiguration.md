---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 6789b2a0f3309e8011cc6e87a27dbf9f28579d05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590371"
---
# <span data-ttu-id="994b9-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="994b9-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="994b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="994b9-102">SYNOPSIS</span></span>
<span data-ttu-id="994b9-103">VMSS 'ye ağ arabirimi yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="994b9-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="994b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="994b9-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="994b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="994b9-105">DESCRIPTION</span></span>
<span data-ttu-id="994b9-106">**Add-Azurermvmssnetworkınterfaceconfiguration** cmdlet 'ı sanal makine ölçek kümesine (VMSS) bir ağ arabirim yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="994b9-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="994b9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="994b9-107">EXAMPLES</span></span>

### <span data-ttu-id="994b9-108">Örnek 1: VMSS 'ye ağ arabirimi yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="994b9-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="994b9-109">Bu komut, VMSS 'ye bir ağ arabirimi yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="994b9-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="994b9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="994b9-110">PARAMETERS</span></span>

### <span data-ttu-id="994b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="994b9-111">-DefaultProfile</span></span>
<span data-ttu-id="994b9-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="994b9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="994b9-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="994b9-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="994b9-114">DNS ayarları için DNS sunucusu IP adreslerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="994b9-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="994b9-115">-Enableiv</span><span class="sxs-lookup"><span data-stu-id="994b9-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="994b9-116">Ağ arabiriminin hızlandırılmış ağ özellikli olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994b9-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="994b9-117">-Enableipiletme</span><span class="sxs-lookup"><span data-stu-id="994b9-117">-EnableIPForwarding</span></span>
<span data-ttu-id="994b9-118">Bu NIC 'de IP iletiminin etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="994b9-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="994b9-119">-ID</span><span class="sxs-lookup"><span data-stu-id="994b9-119">-Id</span></span>
<span data-ttu-id="994b9-120">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="994b9-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="994b9-121">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="994b9-121">-IpConfiguration</span></span>
<span data-ttu-id="994b9-122">Ağ arabiriminin IP yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994b9-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="994b9-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="994b9-123">-Name</span></span>
<span data-ttu-id="994b9-124">Ağ arabirimi yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="994b9-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="994b9-125">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="994b9-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="994b9-126">Ağ güvenlik grubunun kimliği.</span><span class="sxs-lookup"><span data-stu-id="994b9-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="994b9-127">-Birincil</span><span class="sxs-lookup"><span data-stu-id="994b9-127">-Primary</span></span>
<span data-ttu-id="994b9-128">Ağ arabirimi yapılandırmasından oluşturulan ağ arabirimlerinin sanal makinenin birincil ağ bilgi merkezi (NIC) olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="994b9-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="994b9-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="994b9-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="994b9-130">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="994b9-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="994b9-131">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="994b9-131">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="994b9-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="994b9-132">-Confirm</span></span>
<span data-ttu-id="994b9-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="994b9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="994b9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="994b9-134">-WhatIf</span></span>
<span data-ttu-id="994b9-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="994b9-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="994b9-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="994b9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="994b9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="994b9-137">CommonParameters</span></span>
<span data-ttu-id="994b9-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="994b9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="994b9-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="994b9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="994b9-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="994b9-140">INPUTS</span></span>

### <span data-ttu-id="994b9-141">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="994b9-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="994b9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="994b9-142">System.String</span></span>

### <span data-ttu-id="994b9-143">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="994b9-143">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="994b9-144">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="994b9-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="994b9-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="994b9-145">System.String[]</span></span>

## <span data-ttu-id="994b9-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="994b9-146">OUTPUTS</span></span>

### <span data-ttu-id="994b9-147">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="994b9-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="994b9-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="994b9-148">NOTES</span></span>

## <span data-ttu-id="994b9-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="994b9-149">RELATED LINKS</span></span>

[<span data-ttu-id="994b9-150">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="994b9-150">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
