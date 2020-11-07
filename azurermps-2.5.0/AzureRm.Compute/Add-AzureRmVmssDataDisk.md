---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: c91b9dc68bcc0cdecda9ced83a9b3c64452d6413
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939193"
---
# <span data-ttu-id="bf201-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="bf201-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="bf201-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf201-102">SYNOPSIS</span></span>
<span data-ttu-id="bf201-103">VMSS 'ye veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="bf201-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf201-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf201-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <DiskCreateOptionTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf201-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf201-105">DESCRIPTION</span></span>
<span data-ttu-id="bf201-106">**Add-Azurermvmssdatadısk** cmdlet 'ı, sanal makine ölçek KÜMESI (VMSS) örneğine veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="bf201-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="bf201-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf201-107">EXAMPLES</span></span>

### <span data-ttu-id="bf201-108">Örnek 1: veri disketi ekleme</span><span class="sxs-lookup"><span data-stu-id="bf201-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="bf201-109">Bu komut, VMSS nesnesine boş bir veri diski ekler.</span><span class="sxs-lookup"><span data-stu-id="bf201-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="bf201-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf201-110">PARAMETERS</span></span>

### <span data-ttu-id="bf201-111">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="bf201-111">-Caching</span></span>
<span data-ttu-id="bf201-112">Diskin önbelleğe alma türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf201-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="bf201-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="bf201-113">-CreateOption</span></span>
<span data-ttu-id="bf201-114">Diskin oluştur seçeneğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf201-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="bf201-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf201-115">-DefaultProfile</span></span>
<span data-ttu-id="bf201-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf201-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf201-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="bf201-117">-DiskSizeGB</span></span>
<span data-ttu-id="bf201-118">GB cinsinden diskin boyutunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf201-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="bf201-119">-LUN</span><span class="sxs-lookup"><span data-stu-id="bf201-119">-Lun</span></span>
<span data-ttu-id="bf201-120">Diskin mantıksal birim numarasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf201-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="bf201-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="bf201-121">-Name</span></span>
<span data-ttu-id="bf201-122">Diskin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf201-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="bf201-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="bf201-123">-StorageAccountType</span></span>
<span data-ttu-id="bf201-124">Diskin depolama hesabı türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf201-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="bf201-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bf201-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="bf201-126">VMSS nesnesini belirtin.</span><span class="sxs-lookup"><span data-stu-id="bf201-126">Specify the VMSS object.</span></span>
<span data-ttu-id="bf201-127">Nesneyi oluşturmak için [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="bf201-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="bf201-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="bf201-128">-WriteAccelerator</span></span>
<span data-ttu-id="bf201-129">Veri diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="bf201-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf201-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf201-130">-Confirm</span></span>
<span data-ttu-id="bf201-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf201-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf201-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf201-132">-WhatIf</span></span>
<span data-ttu-id="bf201-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf201-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf201-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf201-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf201-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf201-135">CommonParameters</span></span>
<span data-ttu-id="bf201-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf201-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf201-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf201-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf201-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf201-138">INPUTS</span></span>

### <span data-ttu-id="bf201-139">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bf201-139">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="bf201-140">System. String System. Int32 System. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. modeller. DiskCreateOptionTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]] sistem. Nullable `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 1 [[Microsoft. Azure. Management. COMPUTE. modeller. StorageAccountTypes, Microsoft. Azure. Management. COMPUTE, Version = 14.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="bf201-140">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="bf201-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf201-141">OUTPUTS</span></span>

### <span data-ttu-id="bf201-142">Microsoft. Azure. Management. COMPUTE. modeller. VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="bf201-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="bf201-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf201-143">NOTES</span></span>

## <span data-ttu-id="bf201-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf201-144">RELATED LINKS</span></span>

