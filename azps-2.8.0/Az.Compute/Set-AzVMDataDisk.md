---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: 16c15838b07ab2589f5590128f5d948ae3cd6be0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752696"
---
# <span data-ttu-id="dfc9f-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="dfc9f-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="dfc9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfc9f-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc9f-103">Sanal makine veri diskinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="dfc9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dfc9f-104">SYNTAX</span></span>

### <span data-ttu-id="dfc9f-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="dfc9f-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfc9f-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="dfc9f-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfc9f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="dfc9f-107">DESCRIPTION</span></span>
<span data-ttu-id="dfc9f-108">**Set-AzVMDataDisk** cmdlet 'i sanal makine veri diskinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="dfc9f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dfc9f-109">EXAMPLES</span></span>

### <span data-ttu-id="dfc9f-110">Örnek 1: veri diskinin önbelleğe alma modunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="dfc9f-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="dfc9f-111">İlk komut ContosoVM07 adındaki sanal makineyi **Get-AzVM** kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="dfc9f-112">Komut, $VM değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="dfc9f-113">İkinci komut $VM sanal makinesindeki DataDisk01 adlı veri diskinin önbelleğe alma modunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="dfc9f-114">Komut sonucu değişikliklerinizi uygulayan Update-AzVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="dfc9f-115">Nakit modunda yapılan değişiklik, sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="dfc9f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dfc9f-116">PARAMETERS</span></span>

### <span data-ttu-id="dfc9f-117">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="dfc9f-117">-Caching</span></span>
<span data-ttu-id="dfc9f-118">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="dfc9f-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="dfc9f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="dfc9f-120">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="dfc9f-120">ReadOnly</span></span>
- <span data-ttu-id="dfc9f-121">ReadWrite varsayılan değer ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="dfc9f-122">Bu değerin değiştirilmesi sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="dfc9f-123">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-123">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfc9f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc9f-124">-DefaultProfile</span></span>
<span data-ttu-id="dfc9f-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfc9f-126">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="dfc9f-126">-DiskSizeInGB</span></span>
<span data-ttu-id="dfc9f-127">Veri diskinin boyutunu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-127">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfc9f-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="dfc9f-128">-Lun</span></span>
<span data-ttu-id="dfc9f-129">Bu cmdlet 'in değiştirdiği veri diskinin mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-129">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfc9f-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="dfc9f-130">-Name</span></span>
<span data-ttu-id="dfc9f-131">Bu cmdlet 'in değiştirdiği veri diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-131">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfc9f-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="dfc9f-132">-StorageAccountType</span></span>
<span data-ttu-id="dfc9f-133">Sanal makine yönetilen diskinin hesap türü.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-133">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfc9f-134">-VM</span><span class="sxs-lookup"><span data-stu-id="dfc9f-134">-VM</span></span>
<span data-ttu-id="dfc9f-135">Bu cmdlet 'in veri diskini değiştirdiği sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-135">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="dfc9f-136">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-136">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfc9f-137">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="dfc9f-137">-WriteAccelerator</span></span>
<span data-ttu-id="dfc9f-138">Veri diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-138">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfc9f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc9f-139">CommonParameters</span></span>
<span data-ttu-id="dfc9f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc9f-141">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dfc9f-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc9f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dfc9f-142">INPUTS</span></span>

### <span data-ttu-id="dfc9f-143">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dfc9f-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="dfc9f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="dfc9f-144">System.String</span></span>

### <span data-ttu-id="dfc9f-145">System. Nullable ' 1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="dfc9f-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dfc9f-146">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Önbellekintypes, Microsoft. Azure. Management. COMPUTE, Version = 23.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="dfc9f-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="dfc9f-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dfc9f-147">OUTPUTS</span></span>

### <span data-ttu-id="dfc9f-148">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="dfc9f-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="dfc9f-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dfc9f-149">NOTES</span></span>

## <span data-ttu-id="dfc9f-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dfc9f-150">RELATED LINKS</span></span>

[<span data-ttu-id="dfc9f-151">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="dfc9f-151">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="dfc9f-152">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="dfc9f-152">Update-AzVM</span></span>](./Update-AzVM.md)

