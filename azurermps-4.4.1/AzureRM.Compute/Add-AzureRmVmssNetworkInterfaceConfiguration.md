---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 651e339de5782d288350535ba1b0527d7a3eb0de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591798"
---
# <span data-ttu-id="0d6dd-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="0d6dd-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="0d6dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d6dd-102">SYNOPSIS</span></span>
<span data-ttu-id="0d6dd-103">VMSS 'ye ağ arabirimi yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d6dd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d6dd-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d6dd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d6dd-105">DESCRIPTION</span></span>
<span data-ttu-id="0d6dd-106">**Add-Azurermvmssnetworkınterfaceconfiguration** cmdlet 'ı sanal makine ölçek kümesine (VMSS) bir ağ arabirim yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="0d6dd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d6dd-107">EXAMPLES</span></span>

### <span data-ttu-id="0d6dd-108">Örnek 1: VMSS 'ye ağ arabirimi yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="0d6dd-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="0d6dd-109">Bu komut, VMSS 'ye bir ağ arabirimi yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="0d6dd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d6dd-110">PARAMETERS</span></span>

### <span data-ttu-id="0d6dd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d6dd-111">-DefaultProfile</span></span>
<span data-ttu-id="0d6dd-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d6dd-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="0d6dd-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="0d6dd-114">DNS ayarları için DNS sunucusu IP adreslerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="0d6dd-115">-Enableiv</span><span class="sxs-lookup"><span data-stu-id="0d6dd-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="0d6dd-116">Ağ arabiriminin hızlandırılmış ağ özellikli olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d6dd-117">-ID</span><span class="sxs-lookup"><span data-stu-id="0d6dd-117">-Id</span></span>
<span data-ttu-id="0d6dd-118">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-118">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="0d6dd-119">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="0d6dd-119">-IpConfiguration</span></span>
<span data-ttu-id="0d6dd-120">Ağ arabiriminin IP yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-120">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="0d6dd-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d6dd-121">-Name</span></span>
<span data-ttu-id="0d6dd-122">Ağ arabirimi yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-122">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="0d6dd-123">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="0d6dd-123">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="0d6dd-124">Ağ güvenlik grubunun kimliği.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-124">Id of the network security group.</span></span>

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

### <span data-ttu-id="0d6dd-125">-Birincil</span><span class="sxs-lookup"><span data-stu-id="0d6dd-125">-Primary</span></span>
<span data-ttu-id="0d6dd-126">Ağ arabirimi yapılandırmasından oluşturulan ağ arabirimlerinin sanal makinenin birincil ağ bilgi merkezi (NIC) olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-126">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="0d6dd-127">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0d6dd-127">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0d6dd-128">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-128">Specifies the VMSS object.</span></span>
<span data-ttu-id="0d6dd-129">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-129">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="0d6dd-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="0d6dd-130">-Confirm</span></span>
<span data-ttu-id="0d6dd-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d6dd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d6dd-132">-WhatIf</span></span>
<span data-ttu-id="0d6dd-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d6dd-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d6dd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d6dd-135">CommonParameters</span></span>
<span data-ttu-id="0d6dd-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d6dd-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d6dd-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d6dd-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d6dd-138">INPUTS</span></span>

## <span data-ttu-id="0d6dd-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d6dd-139">OUTPUTS</span></span>

###  
<span data-ttu-id="0d6dd-140">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="0d6dd-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0d6dd-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d6dd-141">NOTES</span></span>

## <span data-ttu-id="0d6dd-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d6dd-142">RELATED LINKS</span></span>

[<span data-ttu-id="0d6dd-143">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0d6dd-143">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
