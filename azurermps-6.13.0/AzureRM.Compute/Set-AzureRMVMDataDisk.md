---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 4ed0abb355bf7a755e5acaa36f8bb11e88d80c5c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762626"
---
# <span data-ttu-id="7d85f-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7d85f-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="7d85f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d85f-102">SYNOPSIS</span></span>
<span data-ttu-id="7d85f-103">Sanal makine veri diskinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7d85f-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d85f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d85f-104">SYNTAX</span></span>

### <span data-ttu-id="7d85f-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="7d85f-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d85f-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="7d85f-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d85f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d85f-107">DESCRIPTION</span></span>
<span data-ttu-id="7d85f-108">**Set-AzureRmVMDataDisk** cmdlet 'i, sanal makine veri diskinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7d85f-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="7d85f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d85f-109">EXAMPLES</span></span>

### <span data-ttu-id="7d85f-110">Örnek 1: veri diskinin önbelleğe alma modunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="7d85f-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="7d85f-111">İlk komut ContosoVM07 adındaki sanal makineyi **Get-AzureRmVM** kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="7d85f-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="7d85f-112">Komut, $VM değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="7d85f-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="7d85f-113">İkinci komut $VM sanal makinesindeki DataDisk01 adlı veri diskinin önbelleğe alma modunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="7d85f-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="7d85f-114">Komut sonucu değişikliklerinizi uygulayan Update-AzureRmVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="7d85f-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="7d85f-115">Nakit modunda yapılan değişiklik, sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="7d85f-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="7d85f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d85f-116">PARAMETERS</span></span>

### <span data-ttu-id="7d85f-117">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="7d85f-117">-Caching</span></span>
<span data-ttu-id="7d85f-118">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d85f-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="7d85f-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="7d85f-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7d85f-120">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="7d85f-120">ReadOnly</span></span>
- <span data-ttu-id="7d85f-121">ReadWrite varsayılan değer ReadWrite.</span><span class="sxs-lookup"><span data-stu-id="7d85f-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="7d85f-122">Bu değerin değiştirilmesi sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="7d85f-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="7d85f-123">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="7d85f-123">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="7d85f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d85f-124">-DefaultProfile</span></span>
<span data-ttu-id="7d85f-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7d85f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d85f-126">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="7d85f-126">-DiskSizeInGB</span></span>
<span data-ttu-id="7d85f-127">Veri diskinin boyutunu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d85f-127">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="7d85f-128">-LUN</span><span class="sxs-lookup"><span data-stu-id="7d85f-128">-Lun</span></span>
<span data-ttu-id="7d85f-129">Bu cmdlet 'in değiştirdiği veri diskinin mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d85f-129">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7d85f-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="7d85f-130">-Name</span></span>
<span data-ttu-id="7d85f-131">Bu cmdlet 'in değiştirdiği veri diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d85f-131">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="7d85f-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="7d85f-132">-StorageAccountType</span></span>
<span data-ttu-id="7d85f-133">Sanal makine yönetilen diskinin hesap türü.</span><span class="sxs-lookup"><span data-stu-id="7d85f-133">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="7d85f-134">-VM</span><span class="sxs-lookup"><span data-stu-id="7d85f-134">-VM</span></span>
<span data-ttu-id="7d85f-135">Bu cmdlet 'in veri diskini değiştirdiği sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d85f-135">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="7d85f-136">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="7d85f-136">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="7d85f-137">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="7d85f-137">-WriteAccelerator</span></span>
<span data-ttu-id="7d85f-138">Veri diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7d85f-138">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="7d85f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d85f-139">CommonParameters</span></span>
<span data-ttu-id="7d85f-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7d85f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d85f-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d85f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d85f-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d85f-142">INPUTS</span></span>

### <span data-ttu-id="7d85f-143">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7d85f-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="7d85f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7d85f-144">System.String</span></span>

### <span data-ttu-id="7d85f-145">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7d85f-145">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7d85f-146">System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. Önbellekintypes, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7d85f-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="7d85f-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d85f-147">OUTPUTS</span></span>

### <span data-ttu-id="7d85f-148">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7d85f-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7d85f-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d85f-149">NOTES</span></span>

## <span data-ttu-id="7d85f-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d85f-150">RELATED LINKS</span></span>

[<span data-ttu-id="7d85f-151">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7d85f-151">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="7d85f-152">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="7d85f-152">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


