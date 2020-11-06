---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVmss.md
ms.openlocfilehash: 3798590f3b4df738bc38231018adabf99ba39237
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594113"
---
# <span data-ttu-id="c876f-101">Stop-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c876f-101">Stop-AzureRmVmss</span></span>

## <span data-ttu-id="c876f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c876f-102">SYNOPSIS</span></span>
<span data-ttu-id="c876f-103">VMSS 'yi veya VMSS içindeki sanal makinelerin kümesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="c876f-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c876f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c876f-104">SYNTAX</span></span>

### <span data-ttu-id="c876f-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c876f-105">DefaultParameter (Default)</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c876f-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="c876f-106">FriendMethod</span></span>
```
Stop-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c876f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c876f-107">DESCRIPTION</span></span>
<span data-ttu-id="c876f-108">**Stop-AzureRmVmss** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) veya sanal makine kümesi içindeki tüm sanal makineleri durdurur.</span><span class="sxs-lookup"><span data-stu-id="c876f-108">The **Stop-AzureRmVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="c876f-109">*InstanceId* parametresini kullanarak bir sanal makine kümesi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="c876f-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="c876f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c876f-110">EXAMPLES</span></span>

### <span data-ttu-id="c876f-111">Örnek 1: VMSS içindeki tüm sanal makineleri durdurma</span><span class="sxs-lookup"><span data-stu-id="c876f-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="c876f-112">Bu komut, ContosoVMSS adlı VMSS 'ye ait tüm sanal makineleri durdurur.</span><span class="sxs-lookup"><span data-stu-id="c876f-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="c876f-113">Örnek 2: VMSS içinde belirli bir sanal makine kümesini durdurma</span><span class="sxs-lookup"><span data-stu-id="c876f-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzureRmVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="c876f-114">Bu komut, ContosoVMSS adlı VMSS 'ye ait örnek KIMLIĞI dizesi dizisiyle belirtilen belirli bir sanal makine kümesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="c876f-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="c876f-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c876f-115">PARAMETERS</span></span>

### <span data-ttu-id="c876f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c876f-116">-Force</span></span>
<span data-ttu-id="c876f-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c876f-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c876f-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c876f-118">-InstanceId</span></span>
<span data-ttu-id="c876f-119">Bu cmdlet 'in durdurduğu sanal makine örneklerinin KIMLIĞINI veya kimliklerini dize dizisi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="c876f-119">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="c876f-120">Örneğin: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="c876f-120">For instance: `-InstanceId "0", "3"`.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c876f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c876f-121">-ResourceGroupName</span></span>
<span data-ttu-id="c876f-122">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c876f-122">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c876f-123">-Staysağlandı</span><span class="sxs-lookup"><span data-stu-id="c876f-123">-StayProvisioned</span></span>
<span data-ttu-id="c876f-124">Belirtilmişse, sanal makine durdurulmuş duruma girer.</span><span class="sxs-lookup"><span data-stu-id="c876f-124">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="c876f-125">Belirtilmezse, sanal makine durduruldu-serbest işlem durumuna girer.</span><span class="sxs-lookup"><span data-stu-id="c876f-125">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="c876f-126">Kullanıcı hala durdurulmuş durumda VM 'Ler için ücretlendirilecek, ancak durdurulan serbest durumda VM 'Ler için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="c876f-126">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c876f-127">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c876f-127">-VMScaleSetName</span></span>
<span data-ttu-id="c876f-128">Bu cmdlet 'in sanal makineleri durdurduğu VMSS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c876f-128">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c876f-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="c876f-129">-Confirm</span></span>
<span data-ttu-id="c876f-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c876f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c876f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c876f-131">-WhatIf</span></span>
<span data-ttu-id="c876f-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c876f-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c876f-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c876f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c876f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c876f-134">CommonParameters</span></span>
<span data-ttu-id="c876f-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c876f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c876f-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c876f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c876f-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c876f-137">INPUTS</span></span>

### <span data-ttu-id="c876f-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c876f-138">None</span></span>
<span data-ttu-id="c876f-139">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c876f-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c876f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c876f-140">OUTPUTS</span></span>

## <span data-ttu-id="c876f-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c876f-141">NOTES</span></span>

## <span data-ttu-id="c876f-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c876f-142">RELATED LINKS</span></span>

[<span data-ttu-id="c876f-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c876f-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="c876f-144">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c876f-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c876f-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c876f-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c876f-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c876f-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c876f-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c876f-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="c876f-148">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c876f-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="c876f-149">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c876f-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


