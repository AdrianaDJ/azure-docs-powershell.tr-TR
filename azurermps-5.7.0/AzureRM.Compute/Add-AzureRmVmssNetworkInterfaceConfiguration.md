---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 0b21b5fa3b5b605ee3092a61eaf67a2c63c4346b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762037"
---
# <span data-ttu-id="17552-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="17552-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="17552-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17552-102">SYNOPSIS</span></span>
<span data-ttu-id="17552-103">VMSS 'ye ağ arabirimi yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="17552-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17552-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17552-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17552-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="17552-105">DESCRIPTION</span></span>
<span data-ttu-id="17552-106">**Add-Azurermvmssnetworkınterfaceconfiguration** cmdlet 'ı sanal makine ölçek kümesine (VMSS) bir ağ arabirim yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="17552-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="17552-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17552-107">EXAMPLES</span></span>

### <span data-ttu-id="17552-108">Örnek 1: VMSS 'ye ağ arabirimi yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="17552-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="17552-109">Bu komut, VMSS 'ye bir ağ arabirimi yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="17552-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="17552-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17552-110">PARAMETERS</span></span>

### <span data-ttu-id="17552-111">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="17552-111">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="17552-112">DNS ayarları için DNS sunucusu IP adreslerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="17552-112">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17552-113">-ID</span><span class="sxs-lookup"><span data-stu-id="17552-113">-Id</span></span>
<span data-ttu-id="17552-114">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="17552-114">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17552-115">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="17552-115">-IpConfiguration</span></span>
<span data-ttu-id="17552-116">Ağ arabiriminin IP yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17552-116">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17552-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="17552-117">-Name</span></span>
<span data-ttu-id="17552-118">Ağ arabirimi yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="17552-118">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17552-119">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="17552-119">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="17552-120">Ağ güvenlik grubunun kimliği.</span><span class="sxs-lookup"><span data-stu-id="17552-120">Id of the network security group.</span></span>

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

### <span data-ttu-id="17552-121">-Birincil</span><span class="sxs-lookup"><span data-stu-id="17552-121">-Primary</span></span>
<span data-ttu-id="17552-122">Ağ arabirimi yapılandırmasından oluşturulan ağ arabirimlerinin sanal makinenin birincil ağ bilgi merkezi (NIC) olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="17552-122">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17552-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="17552-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="17552-124">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="17552-124">Specifies the VMSS object.</span></span>
<span data-ttu-id="17552-125">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17552-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17552-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="17552-126">-Confirm</span></span>
<span data-ttu-id="17552-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="17552-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17552-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17552-128">-WhatIf</span></span>
<span data-ttu-id="17552-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="17552-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17552-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="17552-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17552-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17552-131">CommonParameters</span></span>
<span data-ttu-id="17552-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17552-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17552-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17552-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17552-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17552-134">INPUTS</span></span>

### <span data-ttu-id="17552-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="17552-135">None</span></span>
<span data-ttu-id="17552-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="17552-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="17552-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17552-137">OUTPUTS</span></span>

###  
<span data-ttu-id="17552-138">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="17552-138">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="17552-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17552-139">NOTES</span></span>

## <span data-ttu-id="17552-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17552-140">RELATED LINKS</span></span>

[<span data-ttu-id="17552-141">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="17552-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
