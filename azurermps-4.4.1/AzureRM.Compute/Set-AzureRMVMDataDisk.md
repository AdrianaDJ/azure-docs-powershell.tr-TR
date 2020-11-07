---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 3bc870be1628f5fbf22042155e6a889dbdaadc84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762063"
---
# <span data-ttu-id="4010f-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="4010f-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="4010f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4010f-102">SYNOPSIS</span></span>
<span data-ttu-id="4010f-103">Sanal makine veri diskinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4010f-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4010f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4010f-104">SYNTAX</span></span>

### <span data-ttu-id="4010f-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="4010f-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4010f-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="4010f-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4010f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4010f-107">DESCRIPTION</span></span>
<span data-ttu-id="4010f-108">**Set-AzureRmVMDataDisk** cmdlet 'i, sanal makine veri diskinin özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4010f-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="4010f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4010f-109">EXAMPLES</span></span>

### <span data-ttu-id="4010f-110">Örnek 1: veri diskinin önbelleğe alma modunu değiştirme</span><span class="sxs-lookup"><span data-stu-id="4010f-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="4010f-111">İlk komut ContosoVM07 adındaki sanal makineyi **Get-AzureRmVM** kullanarak alır.</span><span class="sxs-lookup"><span data-stu-id="4010f-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="4010f-112">Komut, $VM değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="4010f-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="4010f-113">İkinci komut $VM sanal makinesindeki DataDisk01 adlı veri diskinin önbelleğe alma modunu değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4010f-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="4010f-114">Komut sonucu değişikliklerinizi uygulayan Update-AzureRmVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="4010f-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="4010f-115">Nakit modunda yapılan değişiklik, sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="4010f-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="4010f-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4010f-116">PARAMETERS</span></span>

### <span data-ttu-id="4010f-117">-Önbelleğe alma</span><span class="sxs-lookup"><span data-stu-id="4010f-117">-Caching</span></span>
<span data-ttu-id="4010f-118">Diskin önbelleğe alma modunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="4010f-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="4010f-119">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="4010f-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4010f-120">Özelliğinin</span><span class="sxs-lookup"><span data-stu-id="4010f-120">ReadOnly</span></span>
- <span data-ttu-id="4010f-121">Yazma</span><span class="sxs-lookup"><span data-stu-id="4010f-121">ReadWrite</span></span>

<span data-ttu-id="4010f-122">Varsayılan değer ReadWrite değeridir.</span><span class="sxs-lookup"><span data-stu-id="4010f-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="4010f-123">Bu değerin değiştirilmesi sanal makinenin yeniden başlatılmasına neden olur.</span><span class="sxs-lookup"><span data-stu-id="4010f-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="4010f-124">Bu ayar, diskin tutarlılığını ve performansını etkiler.</span><span class="sxs-lookup"><span data-stu-id="4010f-124">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="4010f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4010f-125">-DefaultProfile</span></span>
<span data-ttu-id="4010f-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4010f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4010f-127">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="4010f-127">-DiskSizeInGB</span></span>
<span data-ttu-id="4010f-128">Veri diskinin boyutunu gigabayt cinsinden belirtir.</span><span class="sxs-lookup"><span data-stu-id="4010f-128">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="4010f-129">-LUN</span><span class="sxs-lookup"><span data-stu-id="4010f-129">-Lun</span></span>
<span data-ttu-id="4010f-130">Bu cmdlet 'in değiştirdiği veri diskinin mantıksal birim numarasını (LUN) belirtir.</span><span class="sxs-lookup"><span data-stu-id="4010f-130">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4010f-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="4010f-131">-Name</span></span>
<span data-ttu-id="4010f-132">Bu cmdlet 'in değiştirdiği veri diskinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4010f-132">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4010f-133">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4010f-133">-StorageAccountType</span></span>
<span data-ttu-id="4010f-134">Sanal makine yönetilen diskinin hesap türü.</span><span class="sxs-lookup"><span data-stu-id="4010f-134">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes]
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4010f-135">-VM</span><span class="sxs-lookup"><span data-stu-id="4010f-135">-VM</span></span>
<span data-ttu-id="4010f-136">Bu cmdlet 'in veri diskini değiştirdiği sanal makineyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4010f-136">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="4010f-137">Sanal makine nesnesi edinmek için Get-AzureRmVM cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="4010f-137">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="4010f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4010f-138">CommonParameters</span></span>
<span data-ttu-id="4010f-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4010f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4010f-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4010f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4010f-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4010f-141">INPUTS</span></span>

## <span data-ttu-id="4010f-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4010f-142">OUTPUTS</span></span>

## <span data-ttu-id="4010f-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4010f-143">NOTES</span></span>

## <span data-ttu-id="4010f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4010f-144">RELATED LINKS</span></span>

[<span data-ttu-id="4010f-145">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4010f-145">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="4010f-146">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4010f-146">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


