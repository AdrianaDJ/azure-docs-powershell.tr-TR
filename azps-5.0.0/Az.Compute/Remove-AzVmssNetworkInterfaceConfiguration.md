---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 1b8f9b7843cccf2475e17e1c5d8866972b5b9ee4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277511"
---
# <span data-ttu-id="99088-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="99088-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="99088-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99088-102">SYNOPSIS</span></span>
<span data-ttu-id="99088-103">Bir VMSS 'den ağ arabirim yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="99088-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="99088-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="99088-104">SYNTAX</span></span>

### <span data-ttu-id="99088-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="99088-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99088-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="99088-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99088-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="99088-107">DESCRIPTION</span></span>
<span data-ttu-id="99088-108">**Remove-Azvmssnetworkınterfaceconfiguration** cmdlet 'ı sanal makine ölçek kümesinden (VMSS) ağ arabirim yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="99088-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="99088-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="99088-109">EXAMPLES</span></span>

### <span data-ttu-id="99088-110">Örnek 1: arabirim yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="99088-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="99088-111">İlk komut Get-AzVmss cmdlet 'ini kullanarak bir VMSS alır ve $VMSS değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="99088-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="99088-112">İkinci komut, $VMSS ContosoVmssInterface02 adındaki ağ arabirimi yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="99088-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="99088-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="99088-113">PARAMETERS</span></span>

### <span data-ttu-id="99088-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99088-114">-DefaultProfile</span></span>
<span data-ttu-id="99088-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="99088-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99088-116">-ID</span><span class="sxs-lookup"><span data-stu-id="99088-116">-Id</span></span>
<span data-ttu-id="99088-117">Bu cmdlet 'in kaldırıldığı ağ arabirimi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="99088-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99088-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="99088-118">-Name</span></span>
<span data-ttu-id="99088-119">Bu cmdlet 'in kaldırıldığı ağ arabirimi yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="99088-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99088-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="99088-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="99088-121">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="99088-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="99088-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="99088-122">-Confirm</span></span>
<span data-ttu-id="99088-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="99088-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99088-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99088-124">-WhatIf</span></span>
<span data-ttu-id="99088-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="99088-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99088-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="99088-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99088-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99088-127">CommonParameters</span></span>
<span data-ttu-id="99088-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="99088-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99088-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="99088-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99088-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="99088-130">INPUTS</span></span>

### <span data-ttu-id="99088-131">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="99088-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="99088-132">System. String</span><span class="sxs-lookup"><span data-stu-id="99088-132">System.String</span></span>

## <span data-ttu-id="99088-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="99088-133">OUTPUTS</span></span>

### <span data-ttu-id="99088-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="99088-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="99088-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="99088-135">NOTES</span></span>

## <span data-ttu-id="99088-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="99088-136">RELATED LINKS</span></span>

[<span data-ttu-id="99088-137">Add-Azvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="99088-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="99088-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="99088-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


