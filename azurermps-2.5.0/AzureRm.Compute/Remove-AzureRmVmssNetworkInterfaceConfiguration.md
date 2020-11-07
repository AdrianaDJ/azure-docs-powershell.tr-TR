---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
ms.openlocfilehash: 46058901188b99eb30d088e2ea784fdc0df8d782
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939948"
---
# <span data-ttu-id="54195-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="54195-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="54195-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54195-102">SYNOPSIS</span></span>
<span data-ttu-id="54195-103">Bir VMSS 'den ağ arabirim yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="54195-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54195-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54195-104">SYNTAX</span></span>

### <span data-ttu-id="54195-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="54195-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54195-106">Idparameterset</span><span class="sxs-lookup"><span data-stu-id="54195-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54195-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="54195-107">DESCRIPTION</span></span>
<span data-ttu-id="54195-108">**Remove-Azurermvmssnetworkınterfaceconfiguration** cmdlet 'ı sanal makine ölçek kümesinden (VMSS) ağ arabirim yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="54195-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="54195-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54195-109">EXAMPLES</span></span>

### <span data-ttu-id="54195-110">Örnek 1: arabirim yapılandırmasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="54195-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="54195-111">İlk komut Get-AzureRmVmss cmdlet 'ini kullanarak bir VMSS alır ve $VMSS değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="54195-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="54195-112">İkinci komut, $VMSS ContosoVmssInterface02 adındaki ağ arabirimi yapılandırmasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="54195-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="54195-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54195-113">PARAMETERS</span></span>

### <span data-ttu-id="54195-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54195-114">-DefaultProfile</span></span>
<span data-ttu-id="54195-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54195-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54195-116">-ID</span><span class="sxs-lookup"><span data-stu-id="54195-116">-Id</span></span>
<span data-ttu-id="54195-117">Bu cmdlet 'in kaldırıldığı ağ arabirimi yapılandırmasının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="54195-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54195-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="54195-118">-Name</span></span>
<span data-ttu-id="54195-119">Bu cmdlet 'in kaldırıldığı ağ arabirimi yapılandırmasının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54195-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54195-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="54195-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="54195-121">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="54195-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="54195-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="54195-122">-Confirm</span></span>
<span data-ttu-id="54195-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="54195-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54195-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54195-124">-WhatIf</span></span>
<span data-ttu-id="54195-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="54195-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54195-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="54195-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54195-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54195-127">CommonParameters</span></span>
<span data-ttu-id="54195-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54195-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54195-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54195-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54195-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54195-130">INPUTS</span></span>

### <span data-ttu-id="54195-131">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="54195-131">VirtualMachineScaleSet</span></span>
<span data-ttu-id="54195-132">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="54195-132">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="54195-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54195-133">OUTPUTS</span></span>

### <span data-ttu-id="54195-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="54195-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="54195-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54195-135">NOTES</span></span>

## <span data-ttu-id="54195-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54195-136">RELATED LINKS</span></span>

[<span data-ttu-id="54195-137">Add-Azurermvmssnetworkınterfaceconfiguration</span><span class="sxs-lookup"><span data-stu-id="54195-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="54195-138">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="54195-138">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


