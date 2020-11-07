---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: b927e9b61e4d76795e35f2356b900b959a94e082
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936833"
---
# <span data-ttu-id="9e4cf-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="9e4cf-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="9e4cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e4cf-102">SYNOPSIS</span></span>
<span data-ttu-id="9e4cf-103">Sanal makine veri diskinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="9e4cf-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e4cf-104">SYNTAX</span></span>

### <span data-ttu-id="9e4cf-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="9e4cf-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e4cf-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="9e4cf-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e4cf-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e4cf-107">DESCRIPTION</span></span>
<span data-ttu-id="9e4cf-108">**Set-AzVMDataDisk** cmdlet 'i sanal makine veri diskinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="9e4cf-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e4cf-109">EXAMPLES</span></span>

### <span data-ttu-id="9e4cf-110">Örnek 1: veri diskinin önbelleğe alma modunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="9e4cf-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="9e4cf-111">İlk komut ContosoVM07 adındaki sanal makineyi **Get-AzVM** kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="9e4cf-112">Komut, $VM değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="9e4cf-113">İkinci komut $VM sanal makinesindeki DataDisk01 adlı veri diskinin önbelleğe alma modunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="9e4cf-114">Komut sonucu değişikliklerinizi uygulayan Update-AzVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="9e4cf-115">Nakit modunda yapılan değişiklik, sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="9e4cf-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e4cf-116">PARAMETERS</span></span>

### <span data-ttu-id="9e4cf-117">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="9e4cf-117">-Caching</span></span>
<span data-ttu-id="9e4cf-118">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="9e4cf-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="9e4cf-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e4cf-120">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="9e4cf-120">ReadOnly</span></span>
- <span data-ttu-id="9e4cf-121">Yazma</span><span class="sxs-lookup"><span data-stu-id="9e4cf-121">ReadWrite</span></span>

<span data-ttu-id="9e4cf-122">Varsayılan değer ReadWrite değeridir.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="9e4cf-123">Bu değerin değiştirilmesi sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="9e4cf-124">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-124">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4cf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e4cf-125">-DefaultProfile</span></span>
<span data-ttu-id="9e4cf-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e4cf-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="9e4cf-127">-DiskSizeInGB</span></span>
<span data-ttu-id="9e4cf-128">Veri diskinin boyutunu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-128">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4cf-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="9e4cf-129">-Lun</span></span>
<span data-ttu-id="9e4cf-130">Bu cmdlet 'in değiştirdiği veri diskinin mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4cf-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="9e4cf-131">-Name</span></span>
<span data-ttu-id="9e4cf-132">Bu cmdlet 'in değiştirdiği veri diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4cf-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="9e4cf-133">-StorageAccountType</span></span>
<span data-ttu-id="9e4cf-134">Sanal makine yönetilen diskinin hesap türü.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-134">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="9e4cf-135">-VM</span><span class="sxs-lookup"><span data-stu-id="9e4cf-135">-VM</span></span>
<span data-ttu-id="9e4cf-136">Bu cmdlet 'in veri diskini değiştirdiği sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="9e4cf-137">Sanal makine nesnesi edinmek için Get-AzVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-137">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e4cf-138">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="9e4cf-138">-WriteAccelerator</span></span>
<span data-ttu-id="9e4cf-139">Veri diskinde WriteAccelerator 'in etkinleştirilip etkinleştirilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-139">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="9e4cf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e4cf-140">CommonParameters</span></span>
<span data-ttu-id="9e4cf-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e4cf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e4cf-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e4cf-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e4cf-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e4cf-143">INPUTS</span></span>

### <span data-ttu-id="9e4cf-144">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9e4cf-144">PSVirtualMachine</span></span>
<span data-ttu-id="9e4cf-145">' VM ' parametresi ardışık düzene ' PSVirtualMachine ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="9e4cf-145">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="9e4cf-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e4cf-146">OUTPUTS</span></span>

### <span data-ttu-id="9e4cf-147">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="9e4cf-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="9e4cf-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e4cf-148">NOTES</span></span>

## <span data-ttu-id="9e4cf-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e4cf-149">RELATED LINKS</span></span>

[<span data-ttu-id="9e4cf-150">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e4cf-150">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9e4cf-151">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e4cf-151">Update-AzVM</span></span>](./Update-AzVM.md)


