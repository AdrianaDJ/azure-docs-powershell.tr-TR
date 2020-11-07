---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 30836628d6be41e06eaf8982fcc59646fb5b5e89
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936897"
---
# <span data-ttu-id="e71f6-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="e71f6-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="e71f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e71f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e71f6-103">Bir veri diskini VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e71f6-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="e71f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e71f6-104">SYNTAX</span></span>

### <span data-ttu-id="e71f6-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e71f6-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e71f6-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="e71f6-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e71f6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e71f6-107">DESCRIPTION</span></span>
<span data-ttu-id="e71f6-108">**Remove-Azvmssdatadısk** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) örneğinden bir veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e71f6-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="e71f6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e71f6-109">EXAMPLES</span></span>

### <span data-ttu-id="e71f6-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e71f6-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="e71f6-111">Bu komut, VMSS nesnesinden ' DataDisk1 ' adlı veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e71f6-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="e71f6-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="e71f6-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="e71f6-113">Bu komut, LUN 0 veri diskini VMSS nesnesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e71f6-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="e71f6-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e71f6-114">PARAMETERS</span></span>

### <span data-ttu-id="e71f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71f6-115">-DefaultProfile</span></span>
<span data-ttu-id="e71f6-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e71f6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e71f6-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="e71f6-117">-Lun</span></span>
<span data-ttu-id="e71f6-118">Diskin mantıksal birim numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e71f6-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="e71f6-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e71f6-119">-Name</span></span>
<span data-ttu-id="e71f6-120">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e71f6-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="e71f6-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e71f6-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e71f6-122">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e71f6-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="e71f6-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="e71f6-123">-Confirm</span></span>
<span data-ttu-id="e71f6-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e71f6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e71f6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e71f6-125">-WhatIf</span></span>
<span data-ttu-id="e71f6-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e71f6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e71f6-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e71f6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e71f6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71f6-128">CommonParameters</span></span>
<span data-ttu-id="e71f6-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e71f6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71f6-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e71f6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71f6-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e71f6-131">INPUTS</span></span>

### <span data-ttu-id="e71f6-132">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e71f6-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="e71f6-133">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e71f6-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="e71f6-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e71f6-134">OUTPUTS</span></span>

### <span data-ttu-id="e71f6-135">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e71f6-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="e71f6-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e71f6-136">NOTES</span></span>

## <span data-ttu-id="e71f6-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e71f6-137">RELATED LINKS</span></span>

