---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: 411e822153c0b95bbf30829f8da915039d01ea32
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938888"
---
# <span data-ttu-id="76078-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="76078-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="76078-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76078-102">SYNOPSIS</span></span>
<span data-ttu-id="76078-103">Bir veri diskini VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="76078-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76078-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76078-104">SYNTAX</span></span>

### <span data-ttu-id="76078-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="76078-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76078-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="76078-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76078-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="76078-107">DESCRIPTION</span></span>
<span data-ttu-id="76078-108">**Remove-Azurermvmssdatadısk** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) örneğinden bir veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="76078-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="76078-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76078-109">EXAMPLES</span></span>

### <span data-ttu-id="76078-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76078-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="76078-111">Bu komut, VMSS nesnesinden ' DataDisk1 ' adlı veri diskini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="76078-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="76078-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="76078-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="76078-113">Bu komut, LUN 0 veri diskini VMSS nesnesinden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="76078-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="76078-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76078-114">PARAMETERS</span></span>

### <span data-ttu-id="76078-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76078-115">-DefaultProfile</span></span>
<span data-ttu-id="76078-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76078-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76078-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="76078-117">-Lun</span></span>
<span data-ttu-id="76078-118">Diskin mantıksal birim numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76078-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="76078-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="76078-119">-Name</span></span>
<span data-ttu-id="76078-120">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="76078-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="76078-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="76078-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="76078-122">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="76078-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="76078-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="76078-123">-Confirm</span></span>
<span data-ttu-id="76078-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="76078-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76078-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76078-125">-WhatIf</span></span>
<span data-ttu-id="76078-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76078-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76078-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76078-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76078-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76078-128">CommonParameters</span></span>
<span data-ttu-id="76078-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76078-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76078-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76078-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76078-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76078-131">INPUTS</span></span>

### <span data-ttu-id="76078-132">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="76078-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="76078-133">System. String System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="76078-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="76078-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76078-134">OUTPUTS</span></span>

### <span data-ttu-id="76078-135">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="76078-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="76078-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76078-136">NOTES</span></span>

## <span data-ttu-id="76078-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76078-137">RELATED LINKS</span></span>

