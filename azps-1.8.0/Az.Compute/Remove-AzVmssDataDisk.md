---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 3f70df791964f6b60385b6c12be46ce15f63a469
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761272"
---
# <span data-ttu-id="f0eda-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="f0eda-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="f0eda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0eda-102">SYNOPSIS</span></span>
<span data-ttu-id="f0eda-103">Bir veri diskini VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f0eda-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="f0eda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0eda-104">SYNTAX</span></span>

### <span data-ttu-id="f0eda-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0eda-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0eda-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0eda-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0eda-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0eda-107">DESCRIPTION</span></span>
<span data-ttu-id="f0eda-108">**Remove-Azvmssdatadısk** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) örneğinden bir veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f0eda-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="f0eda-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0eda-109">EXAMPLES</span></span>

### <span data-ttu-id="f0eda-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f0eda-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="f0eda-111">Bu komut, VMSS nesnesinden ' DataDisk1 ' adlı veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f0eda-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="f0eda-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="f0eda-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="f0eda-113">Bu komut, LUN 0 veri diskini VMSS nesnesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f0eda-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="f0eda-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0eda-114">PARAMETERS</span></span>

### <span data-ttu-id="f0eda-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0eda-115">-DefaultProfile</span></span>
<span data-ttu-id="f0eda-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0eda-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0eda-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="f0eda-117">-Lun</span></span>
<span data-ttu-id="f0eda-118">Diskin mantıksal birim numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0eda-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="f0eda-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0eda-119">-Name</span></span>
<span data-ttu-id="f0eda-120">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0eda-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="f0eda-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f0eda-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f0eda-122">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f0eda-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="f0eda-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0eda-123">-Confirm</span></span>
<span data-ttu-id="f0eda-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f0eda-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0eda-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0eda-125">-WhatIf</span></span>
<span data-ttu-id="f0eda-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f0eda-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0eda-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f0eda-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0eda-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0eda-128">CommonParameters</span></span>
<span data-ttu-id="f0eda-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0eda-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0eda-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0eda-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0eda-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0eda-131">INPUTS</span></span>

### <span data-ttu-id="f0eda-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f0eda-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="f0eda-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f0eda-133">System.String</span></span>

### <span data-ttu-id="f0eda-134">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="f0eda-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f0eda-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0eda-135">OUTPUTS</span></span>

### <span data-ttu-id="f0eda-136">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f0eda-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f0eda-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0eda-137">NOTES</span></span>

## <span data-ttu-id="f0eda-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0eda-138">RELATED LINKS</span></span>
