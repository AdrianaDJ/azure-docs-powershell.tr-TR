---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 54c6f9f399cfabf7a418939b4662c9bcfdc83d34
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593296"
---
# <span data-ttu-id="9e68e-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e68e-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="9e68e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e68e-102">SYNOPSIS</span></span>
<span data-ttu-id="9e68e-103">VMSS 'deki bir sanal makineyi veya VMSS 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e68e-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e68e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9e68e-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e68e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9e68e-105">DESCRIPTION</span></span>
<span data-ttu-id="9e68e-106">**Remove-AzureRmVmss** cmdlet 'i Azure 'Dan sanal makine ölçek kümesini (VMSS) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e68e-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="9e68e-107">Bu cmdlet, VMSS içindeki belirli bir sanal makineyi kaldırmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9e68e-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="9e68e-108">*InstanceId* içindeki belirli bir sanal makineyi kaldırmak için InstanceId parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9e68e-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="9e68e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9e68e-109">EXAMPLES</span></span>

### <span data-ttu-id="9e68e-110">Örnek 1: VMSUBNET 'i kaldırma</span><span class="sxs-lookup"><span data-stu-id="9e68e-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="9e68e-111">Bu komut, Group001 adındaki kaynak grubuna ait olan VMScaleSet001 adındaki VMSS 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e68e-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="9e68e-112">Örnek 2: bir VMSS 'den sanal makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="9e68e-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="9e68e-113">Bu komut, Group002 adındaki kaynak grubuna ait VMScaleSet002 adındaki VMSS 'den örnek KIMLIĞI 3 olan sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e68e-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="9e68e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9e68e-114">PARAMETERS</span></span>

### <span data-ttu-id="9e68e-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="9e68e-115">-AsJob</span></span>
<span data-ttu-id="9e68e-116">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="9e68e-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9e68e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e68e-117">-DefaultProfile</span></span>
<span data-ttu-id="9e68e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9e68e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e68e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9e68e-119">-Force</span></span>
<span data-ttu-id="9e68e-120">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9e68e-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e68e-121">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="9e68e-121">-InstanceId</span></span>
<span data-ttu-id="9e68e-122">Bir dize dizisi olarak, başlaması gereken örneklerin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e68e-122">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="9e68e-123">Örneğin: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="9e68e-123">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e68e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e68e-124">-ResourceGroupName</span></span>
<span data-ttu-id="9e68e-125">VMSS 'nin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9e68e-125">Specifies the name of the resource group that the VMSS belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e68e-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9e68e-126">-VMScaleSetName</span></span>
<span data-ttu-id="9e68e-127">Türleri bu cmdlet 'in kaldırdığı VMSUBNET 'in adını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="9e68e-127">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="9e68e-128">*InstanceId* parametresini belirtirseniz cmdlet, belirtilen sanal makineyi Bu parametreyle adlandırılan VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9e68e-128">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e68e-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="9e68e-129">-Confirm</span></span>
<span data-ttu-id="9e68e-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9e68e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e68e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e68e-131">-WhatIf</span></span>
<span data-ttu-id="9e68e-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9e68e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e68e-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9e68e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e68e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e68e-134">CommonParameters</span></span>
<span data-ttu-id="9e68e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9e68e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e68e-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e68e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e68e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9e68e-137">INPUTS</span></span>

### <span data-ttu-id="9e68e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9e68e-138">System.String</span></span>

### <span data-ttu-id="9e68e-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="9e68e-139">System.String[]</span></span>

## <span data-ttu-id="9e68e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9e68e-140">OUTPUTS</span></span>

### <span data-ttu-id="9e68e-141">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="9e68e-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9e68e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9e68e-142">NOTES</span></span>

## <span data-ttu-id="9e68e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9e68e-143">RELATED LINKS</span></span>

[<span data-ttu-id="9e68e-144">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e68e-144">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="9e68e-145">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e68e-145">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="9e68e-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e68e-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="9e68e-147">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e68e-147">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="9e68e-148">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e68e-148">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="9e68e-149">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e68e-149">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="9e68e-150">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="9e68e-150">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


