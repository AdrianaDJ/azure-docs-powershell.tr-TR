---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmss.md
ms.openlocfilehash: e02ddb83e40495fbcf729428a737f27e6665d765
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103662"
---
# <span data-ttu-id="756f8-101">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="756f8-101">Remove-AzVmss</span></span>

## <span data-ttu-id="756f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="756f8-102">SYNOPSIS</span></span>
<span data-ttu-id="756f8-103">VMSS 'deki bir sanal makineyi veya VMSS 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="756f8-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

## <span data-ttu-id="756f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="756f8-104">SYNTAX</span></span>

```
Remove-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="756f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="756f8-105">DESCRIPTION</span></span>
<span data-ttu-id="756f8-106">**Remove-AzVmss** cmdlet 'i Azure 'Dan sanal makine ölçek kümesini (VMSS) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="756f8-106">The **Remove-AzVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="756f8-107">Bu cmdlet, VMSS içindeki belirli bir sanal makineyi kaldırmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="756f8-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="756f8-108">*InstanceId* içindeki belirli bir sanal makineyi kaldırmak için InstanceId parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="756f8-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="756f8-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="756f8-109">EXAMPLES</span></span>

### <span data-ttu-id="756f8-110">Örnek 1: VMSUBNET 'i kaldırma</span><span class="sxs-lookup"><span data-stu-id="756f8-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="756f8-111">Bu komut, Group001 adındaki kaynak grubuna ait olan VMScaleSet001 adındaki VMSS 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="756f8-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="756f8-112">Örnek 2: bir VMSS 'den sanal makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="756f8-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="756f8-113">Bu komut, Group002 adındaki kaynak grubuna ait VMScaleSet002 adındaki VMSS 'den örnek KIMLIĞI 3 olan sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="756f8-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="756f8-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="756f8-114">PARAMETERS</span></span>

### <span data-ttu-id="756f8-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="756f8-115">-AsJob</span></span>
<span data-ttu-id="756f8-116">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="756f8-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="756f8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="756f8-117">-DefaultProfile</span></span>
<span data-ttu-id="756f8-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="756f8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="756f8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="756f8-119">-Force</span></span>
<span data-ttu-id="756f8-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="756f8-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="756f8-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="756f8-121">-InstanceId</span></span>
<span data-ttu-id="756f8-122">Bir dize dizisi olarak, başlaması gereken örneklerin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="756f8-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="756f8-123">Örneğin: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="756f8-123">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="756f8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="756f8-124">-ResourceGroupName</span></span>
<span data-ttu-id="756f8-125">VMSS 'nin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="756f8-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="756f8-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="756f8-126">-VMScaleSetName</span></span>
<span data-ttu-id="756f8-127">Türleri bu cmdlet 'in kaldırdığı VMSUBNET 'in adını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="756f8-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="756f8-128">*InstanceId* parametresini belirtirseniz cmdlet, belirtilen sanal makineyi Bu parametreyle adlandırılan VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="756f8-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="756f8-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="756f8-129">-Confirm</span></span>
<span data-ttu-id="756f8-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="756f8-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756f8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="756f8-131">-WhatIf</span></span>
<span data-ttu-id="756f8-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="756f8-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="756f8-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="756f8-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="756f8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="756f8-134">CommonParameters</span></span>
<span data-ttu-id="756f8-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="756f8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="756f8-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="756f8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="756f8-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="756f8-137">INPUTS</span></span>

### <span data-ttu-id="756f8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="756f8-138">System.String</span></span>

### <span data-ttu-id="756f8-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="756f8-139">System.String[]</span></span>

## <span data-ttu-id="756f8-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="756f8-140">OUTPUTS</span></span>

### <span data-ttu-id="756f8-141">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="756f8-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="756f8-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="756f8-142">NOTES</span></span>

## <span data-ttu-id="756f8-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="756f8-143">RELATED LINKS</span></span>

[<span data-ttu-id="756f8-144">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="756f8-144">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="756f8-145">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="756f8-145">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="756f8-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="756f8-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="756f8-147">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="756f8-147">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="756f8-148">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="756f8-148">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="756f8-149">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="756f8-149">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="756f8-150">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="756f8-150">Update-AzVmss</span></span>](./Update-AzVmss.md)


