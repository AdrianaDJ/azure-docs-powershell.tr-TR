---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 293bb0f314b82ed2318684996f9b18c79a3b81d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762033"
---
# <span data-ttu-id="1b015-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="1b015-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="1b015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b015-102">SYNOPSIS</span></span>
<span data-ttu-id="1b015-103">Bir veri diskini VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b015-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b015-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b015-104">SYNTAX</span></span>

### <span data-ttu-id="1b015-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b015-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b015-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b015-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Lun] <Int32> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b015-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b015-107">DESCRIPTION</span></span>
<span data-ttu-id="1b015-108">**Remove-Azurermvmssdatadısk** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) örneğinden bir veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b015-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="1b015-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b015-109">EXAMPLES</span></span>

### <span data-ttu-id="1b015-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b015-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="1b015-111">Bu komut, VMSS nesnesinden ' DataDisk1 ' adlı veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b015-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="1b015-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="1b015-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="1b015-113">Bu komut, LUN 0 veri diskini VMSS nesnesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1b015-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="1b015-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b015-114">PARAMETERS</span></span>

### <span data-ttu-id="1b015-115">-LUN</span><span class="sxs-lookup"><span data-stu-id="1b015-115">-Lun</span></span>
<span data-ttu-id="1b015-116">Diskin mantıksal birim numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b015-116">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b015-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="1b015-117">-Name</span></span>
<span data-ttu-id="1b015-118">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1b015-118">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="1b015-119">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1b015-119">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1b015-120">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="1b015-120">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="1b015-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b015-121">-Confirm</span></span>
<span data-ttu-id="1b015-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b015-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b015-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b015-123">-WhatIf</span></span>
<span data-ttu-id="1b015-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b015-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b015-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b015-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b015-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b015-126">CommonParameters</span></span>
<span data-ttu-id="1b015-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b015-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b015-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b015-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b015-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b015-129">INPUTS</span></span>

### <span data-ttu-id="1b015-130">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1b015-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="1b015-131">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1b015-131">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="1b015-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b015-132">OUTPUTS</span></span>

### <span data-ttu-id="1b015-133">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1b015-133">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="1b015-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b015-134">NOTES</span></span>

## <span data-ttu-id="1b015-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b015-135">RELATED LINKS</span></span>

