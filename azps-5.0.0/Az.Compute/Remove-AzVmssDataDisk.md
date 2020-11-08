---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 908405de847526682d8526ef2e576e6a07893c3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278754"
---
# <span data-ttu-id="36308-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="36308-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="36308-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36308-102">SYNOPSIS</span></span>
<span data-ttu-id="36308-103">Bir veri diskini VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36308-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="36308-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36308-104">SYNTAX</span></span>

### <span data-ttu-id="36308-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="36308-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36308-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="36308-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36308-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="36308-107">DESCRIPTION</span></span>
<span data-ttu-id="36308-108">**Remove-Azvmssdatadısk** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) örneğinden bir veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36308-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="36308-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36308-109">EXAMPLES</span></span>

### <span data-ttu-id="36308-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="36308-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="36308-111">Bu komut, VMSS nesnesinden ' DataDisk1 ' adlı veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36308-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="36308-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="36308-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="36308-113">Bu komut, LUN 0 veri diskini VMSS nesnesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="36308-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="36308-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36308-114">PARAMETERS</span></span>

### <span data-ttu-id="36308-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36308-115">-DefaultProfile</span></span>
<span data-ttu-id="36308-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36308-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36308-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="36308-117">-Lun</span></span>
<span data-ttu-id="36308-118">Diskin mantıksal birim numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36308-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="36308-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="36308-119">-Name</span></span>
<span data-ttu-id="36308-120">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36308-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="36308-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36308-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="36308-122">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="36308-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="36308-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="36308-123">-Confirm</span></span>
<span data-ttu-id="36308-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="36308-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36308-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36308-125">-WhatIf</span></span>
<span data-ttu-id="36308-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="36308-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36308-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="36308-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36308-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36308-128">CommonParameters</span></span>
<span data-ttu-id="36308-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36308-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36308-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="36308-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36308-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36308-131">INPUTS</span></span>

### <span data-ttu-id="36308-132">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36308-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="36308-133">System. String</span><span class="sxs-lookup"><span data-stu-id="36308-133">System.String</span></span>

### <span data-ttu-id="36308-134">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="36308-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="36308-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36308-135">OUTPUTS</span></span>

### <span data-ttu-id="36308-136">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="36308-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="36308-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36308-137">NOTES</span></span>

## <span data-ttu-id="36308-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36308-138">RELATED LINKS</span></span>
