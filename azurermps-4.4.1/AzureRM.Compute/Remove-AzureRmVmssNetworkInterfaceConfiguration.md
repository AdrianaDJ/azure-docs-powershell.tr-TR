---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 85f593c1d66b02f9982cecc4606603fbef1385d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762068"
---
# <span data-ttu-id="fe78e-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe78e-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="fe78e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe78e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe78e-103">Bir VMSS 'den ağ arabirim yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe78e-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe78e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe78e-104">SYNTAX</span></span>

### <span data-ttu-id="fe78e-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe78e-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe78e-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="fe78e-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe78e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe78e-107">DESCRIPTION</span></span>
<span data-ttu-id="fe78e-108">**Remove-Azurermvmssnetworkınterfaceconfiguration** cmdlet 'ı sanal makine ölçek kümesinden (VMSS) ağ arabirim yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe78e-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="fe78e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe78e-109">EXAMPLES</span></span>

### <span data-ttu-id="fe78e-110">Örnek 1: arabirim yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fe78e-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="fe78e-111">İlk komut Get-AzureRmVmss cmdlet 'ini kullanarak bir VMSS alır ve $VMSS değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fe78e-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="fe78e-112">İkinci komut, $VMSS ContosoVmssInterface02 adındaki ağ arabirimi yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe78e-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="fe78e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe78e-113">PARAMETERS</span></span>

### <span data-ttu-id="fe78e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe78e-114">-DefaultProfile</span></span>
<span data-ttu-id="fe78e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fe78e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe78e-116">-ID</span><span class="sxs-lookup"><span data-stu-id="fe78e-116">-Id</span></span>
<span data-ttu-id="fe78e-117">Bu cmdlet 'in kaldırıldığı ağ arabirimi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe78e-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fe78e-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="fe78e-118">-Name</span></span>
<span data-ttu-id="fe78e-119">Bu cmdlet 'in kaldırıldığı ağ arabirimi yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe78e-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fe78e-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fe78e-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fe78e-121">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe78e-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="fe78e-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="fe78e-122">-Confirm</span></span>
<span data-ttu-id="fe78e-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fe78e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe78e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe78e-124">-WhatIf</span></span>
<span data-ttu-id="fe78e-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe78e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe78e-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fe78e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe78e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe78e-127">CommonParameters</span></span>
<span data-ttu-id="fe78e-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe78e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe78e-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe78e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe78e-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe78e-130">INPUTS</span></span>

## <span data-ttu-id="fe78e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe78e-131">OUTPUTS</span></span>

## <span data-ttu-id="fe78e-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe78e-132">NOTES</span></span>

## <span data-ttu-id="fe78e-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe78e-133">RELATED LINKS</span></span>

[<span data-ttu-id="fe78e-134">Add-Azurermvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="fe78e-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="fe78e-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe78e-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


