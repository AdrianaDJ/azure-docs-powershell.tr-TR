---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: bb5b570f9cc4699e9b2e6b612345d1deb2dae4de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752756"
---
# <span data-ttu-id="156b0-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="156b0-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="156b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="156b0-102">SYNOPSIS</span></span>
<span data-ttu-id="156b0-103">Bir veri diskini VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="156b0-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="156b0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="156b0-104">SYNTAX</span></span>

### <span data-ttu-id="156b0-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="156b0-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="156b0-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="156b0-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="156b0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="156b0-107">DESCRIPTION</span></span>
<span data-ttu-id="156b0-108">**Remove-Azvmssdatadısk** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) örneğinden bir veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="156b0-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="156b0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="156b0-109">EXAMPLES</span></span>

### <span data-ttu-id="156b0-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="156b0-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="156b0-111">Bu komut, VMSS nesnesinden ' DataDisk1 ' adlı veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="156b0-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="156b0-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="156b0-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="156b0-113">Bu komut, LUN 0 veri diskini VMSS nesnesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="156b0-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="156b0-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="156b0-114">PARAMETERS</span></span>

### <span data-ttu-id="156b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="156b0-115">-DefaultProfile</span></span>
<span data-ttu-id="156b0-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="156b0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="156b0-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="156b0-117">-Lun</span></span>
<span data-ttu-id="156b0-118">Diskin mantıksal birim numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="156b0-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="156b0-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="156b0-119">-Name</span></span>
<span data-ttu-id="156b0-120">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="156b0-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="156b0-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="156b0-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="156b0-122">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="156b0-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="156b0-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="156b0-123">-Confirm</span></span>
<span data-ttu-id="156b0-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="156b0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="156b0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="156b0-125">-WhatIf</span></span>
<span data-ttu-id="156b0-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="156b0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="156b0-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="156b0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="156b0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="156b0-128">CommonParameters</span></span>
<span data-ttu-id="156b0-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="156b0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="156b0-130">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="156b0-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="156b0-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="156b0-131">INPUTS</span></span>

### <span data-ttu-id="156b0-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="156b0-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="156b0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="156b0-133">System.String</span></span>

### <span data-ttu-id="156b0-134">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="156b0-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="156b0-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="156b0-135">OUTPUTS</span></span>

### <span data-ttu-id="156b0-136">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="156b0-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="156b0-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="156b0-137">NOTES</span></span>

## <span data-ttu-id="156b0-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="156b0-138">RELATED LINKS</span></span>
