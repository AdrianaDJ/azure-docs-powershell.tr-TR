---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: e2eca141678c5455df0e443c155693c3c1445e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762871"
---
# <span data-ttu-id="6ce0b-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="6ce0b-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="6ce0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ce0b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce0b-103">VMSS 'ye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ce0b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ce0b-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-CreateOption <DiskCreateOptionTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ce0b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ce0b-105">DESCRIPTION</span></span>
<span data-ttu-id="6ce0b-106">**Add-Azurermvmssdatadısk** cmdlet 'ı, sanal makine ölçek KÜMESI (VMSS) örneğine veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="6ce0b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ce0b-107">EXAMPLES</span></span>

### <span data-ttu-id="6ce0b-108">Örnek 1: veri disketi ekleme</span><span class="sxs-lookup"><span data-stu-id="6ce0b-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="6ce0b-109">Bu komut, VMSS nesnesine boş bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="6ce0b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ce0b-110">PARAMETERS</span></span>

### <span data-ttu-id="6ce0b-111">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="6ce0b-111">-Caching</span></span>
<span data-ttu-id="6ce0b-112">Diskin önbelleğe alma türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce0b-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="6ce0b-113">-CreateOption</span></span>
<span data-ttu-id="6ce0b-114">Diskin oluştur seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-114">Specifies the create option of the disk.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce0b-115">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="6ce0b-115">-DiskSizeGB</span></span>
<span data-ttu-id="6ce0b-116">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-116">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce0b-117">-LUN</span><span class="sxs-lookup"><span data-stu-id="6ce0b-117">-Lun</span></span>
<span data-ttu-id="6ce0b-118">Diskin mantıksal birim numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce0b-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ce0b-119">-Name</span></span>
<span data-ttu-id="6ce0b-120">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="6ce0b-121">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="6ce0b-121">-StorageAccountType</span></span>
<span data-ttu-id="6ce0b-122">Diskin depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-122">Specifies the storage account type of the disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce0b-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6ce0b-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6ce0b-124">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-124">Specify the VMSS object.</span></span>
<span data-ttu-id="6ce0b-125">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="6ce0b-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ce0b-126">-Confirm</span></span>
<span data-ttu-id="6ce0b-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ce0b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ce0b-128">-WhatIf</span></span>
<span data-ttu-id="6ce0b-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ce0b-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ce0b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce0b-131">CommonParameters</span></span>
<span data-ttu-id="6ce0b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ce0b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce0b-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce0b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce0b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ce0b-134">INPUTS</span></span>

### <span data-ttu-id="6ce0b-135">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6ce0b-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="6ce0b-136">System. String System. Int32 System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. modeller. DiskCreateOptionTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] sistem. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. modeller. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="6ce0b-136">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="6ce0b-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ce0b-137">OUTPUTS</span></span>

### <span data-ttu-id="6ce0b-138">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6ce0b-138">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="6ce0b-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ce0b-139">NOTES</span></span>

## <span data-ttu-id="6ce0b-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ce0b-140">RELATED LINKS</span></span>
