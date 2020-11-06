---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 9837098586212cfa777c01fcb76a0db05f39eaf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591052"
---
# <span data-ttu-id="34f1f-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34f1f-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="34f1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="34f1f-103">VMSS 'deki bir sanal makineyi veya VMSS 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34f1f-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34f1f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34f1f-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34f1f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34f1f-105">DESCRIPTION</span></span>
<span data-ttu-id="34f1f-106">**Remove-AzureRmVmss** cmdlet 'i Azure 'Dan sanal makine ölçek kümesini (VMSS) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34f1f-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="34f1f-107">Bu cmdlet, VMSS içindeki belirli bir sanal makineyi kaldırmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="34f1f-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="34f1f-108">*InstanceId* içindeki belirli bir sanal makineyi kaldırmak için InstanceId parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34f1f-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="34f1f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34f1f-109">EXAMPLES</span></span>

### <span data-ttu-id="34f1f-110">Örnek 1: VMSUBNET 'i kaldırma</span><span class="sxs-lookup"><span data-stu-id="34f1f-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="34f1f-111">Bu komut, Group001 adındaki kaynak grubuna ait olan VMScaleSet001 adındaki VMSS 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34f1f-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="34f1f-112">Örnek 2: bir VMSS 'den sanal makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="34f1f-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="34f1f-113">Bu komut, Group002 adındaki kaynak grubuna ait VMScaleSet002 adındaki VMSS 'den örnek KIMLIĞI 3 olan sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34f1f-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="34f1f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34f1f-114">PARAMETERS</span></span>

### <span data-ttu-id="34f1f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="34f1f-115">-Force</span></span>
<span data-ttu-id="34f1f-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="34f1f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="34f1f-117">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="34f1f-117">-InstanceId</span></span>
<span data-ttu-id="34f1f-118">Bir dize dizisi olarak, başlaması gereken örneklerin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f1f-118">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="34f1f-119">Örneğin: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="34f1f-119">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="34f1f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f1f-120">-ResourceGroupName</span></span>
<span data-ttu-id="34f1f-121">VMSS 'nin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34f1f-121">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="34f1f-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="34f1f-122">-VMScaleSetName</span></span>
<span data-ttu-id="34f1f-123">Türleri bu cmdlet 'in kaldırdığı VMSUBNET 'in adını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="34f1f-123">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="34f1f-124">*InstanceId* parametresini belirtirseniz cmdlet, belirtilen sanal makineyi Bu parametreyle adlandırılan VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="34f1f-124">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="34f1f-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="34f1f-125">-Confirm</span></span>
<span data-ttu-id="34f1f-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34f1f-126">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f1f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f1f-127">-WhatIf</span></span>
<span data-ttu-id="34f1f-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34f1f-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34f1f-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34f1f-129">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f1f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f1f-130">CommonParameters</span></span>
<span data-ttu-id="34f1f-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34f1f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f1f-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34f1f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f1f-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34f1f-133">INPUTS</span></span>

### <span data-ttu-id="34f1f-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="34f1f-134">None</span></span>
<span data-ttu-id="34f1f-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="34f1f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34f1f-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34f1f-136">OUTPUTS</span></span>

## <span data-ttu-id="34f1f-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34f1f-137">NOTES</span></span>

## <span data-ttu-id="34f1f-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34f1f-138">RELATED LINKS</span></span>

[<span data-ttu-id="34f1f-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34f1f-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="34f1f-140">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34f1f-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="34f1f-141">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34f1f-141">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="34f1f-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34f1f-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="34f1f-143">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34f1f-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="34f1f-144">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34f1f-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="34f1f-145">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="34f1f-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


