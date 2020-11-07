---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 43d7040543beb049f46fce45cab69d9128a8954e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937077"
---
# <span data-ttu-id="e9794-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e9794-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="e9794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9794-102">SYNOPSIS</span></span>
<span data-ttu-id="e9794-103">VMSS 'ye ağ arabirimi yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="e9794-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="e9794-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9794-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9794-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9794-105">DESCRIPTION</span></span>
<span data-ttu-id="e9794-106">**Add-Azvmssnetworkınterfaceconfiguration** cmdlet 'ı sanal makine ölçek kümesine (VMSS) bir ağ arabirim yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="e9794-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e9794-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9794-107">EXAMPLES</span></span>

### <span data-ttu-id="e9794-108">Örnek 1: VMSS 'ye ağ arabirimi yapılandırması ekleme</span><span class="sxs-lookup"><span data-stu-id="e9794-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="e9794-109">Bu komut, VMSS 'ye bir ağ arabirimi yapılandırması ekler.</span><span class="sxs-lookup"><span data-stu-id="e9794-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="e9794-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9794-110">PARAMETERS</span></span>

### <span data-ttu-id="e9794-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9794-111">-DefaultProfile</span></span>
<span data-ttu-id="e9794-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9794-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9794-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="e9794-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="e9794-114">DNS ayarları için DNS sunucusu IP adreslerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="e9794-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9794-115">-Enableiv</span><span class="sxs-lookup"><span data-stu-id="e9794-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="e9794-116">Ağ arabiriminin hızlandırılmış ağ özellikli olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9794-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="e9794-117">-Enableipiletme</span><span class="sxs-lookup"><span data-stu-id="e9794-117">-EnableIPForwarding</span></span>
<span data-ttu-id="e9794-118">Bu NIC 'de IP iletiminin etkinleştirilip etkinleştirilmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9794-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="e9794-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e9794-119">-Id</span></span>
<span data-ttu-id="e9794-120">Sanal makinenin kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9794-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="e9794-121">-IP yapılandırması</span><span class="sxs-lookup"><span data-stu-id="e9794-121">-IpConfiguration</span></span>
<span data-ttu-id="e9794-122">Ağ arabiriminin IP yapılandırmalarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9794-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="e9794-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9794-123">-Name</span></span>
<span data-ttu-id="e9794-124">Ağ arabirimi yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9794-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="e9794-125">-Networksecuritygroupıd</span><span class="sxs-lookup"><span data-stu-id="e9794-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e9794-126">Ağ güvenlik grubunun kimliği.</span><span class="sxs-lookup"><span data-stu-id="e9794-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="e9794-127">-Birincil</span><span class="sxs-lookup"><span data-stu-id="e9794-127">-Primary</span></span>
<span data-ttu-id="e9794-128">Ağ arabirimi yapılandırmasından oluşturulan ağ arabirimlerinin sanal makinenin birincil ağ bilgi merkezi (NIC) olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9794-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="e9794-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e9794-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e9794-130">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9794-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="e9794-131">Nesneyi oluşturmak için [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e9794-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9794-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9794-132">-Confirm</span></span>
<span data-ttu-id="e9794-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9794-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9794-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9794-134">-WhatIf</span></span>
<span data-ttu-id="e9794-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9794-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9794-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9794-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9794-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9794-137">CommonParameters</span></span>
<span data-ttu-id="e9794-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9794-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9794-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9794-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9794-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9794-140">INPUTS</span></span>

### <span data-ttu-id="e9794-141">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e9794-141">VirtualMachineScaleSet</span></span>
<span data-ttu-id="e9794-142">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="e9794-142">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="e9794-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9794-143">OUTPUTS</span></span>

###  
<span data-ttu-id="e9794-144">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e9794-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e9794-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9794-145">NOTES</span></span>

## <span data-ttu-id="e9794-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9794-146">RELATED LINKS</span></span>

[<span data-ttu-id="e9794-147">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e9794-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
