---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 703fc0d83fb17e1131c44cbd06593887ebcce020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586961"
---
# <span data-ttu-id="ede87-101">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ede87-101">Remove-AzureRmVmss</span></span>

## <span data-ttu-id="ede87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ede87-102">SYNOPSIS</span></span>
<span data-ttu-id="ede87-103">VMSS 'deki bir sanal makineyi veya VMSS 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ede87-103">Removes the VMSS or a virtual machine that is within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ede87-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ede87-104">SYNTAX</span></span>

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ede87-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ede87-105">DESCRIPTION</span></span>
<span data-ttu-id="ede87-106">**Remove-AzureRmVmss** cmdlet 'i Azure 'Dan sanal makine ölçek kümesini (VMSS) kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ede87-106">The **Remove-AzureRmVmss** cmdlet removes the Virtual Machine Scale Set (VMSS) from Azure.</span></span>
<span data-ttu-id="ede87-107">Bu cmdlet, VMSS içindeki belirli bir sanal makineyi kaldırmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ede87-107">This cmdlet can also be used to remove a specific virtual machine inside the VMSS.</span></span>
<span data-ttu-id="ede87-108">*InstanceId* içindeki belirli bir sanal makineyi kaldırmak için InstanceId parametresini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ede87-108">You can use the *InstanceId* parameter to remove a specific virtual machine inside the VMSS.</span></span>

## <span data-ttu-id="ede87-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ede87-109">EXAMPLES</span></span>

### <span data-ttu-id="ede87-110">Örnek 1: VMSUBNET 'i kaldırma</span><span class="sxs-lookup"><span data-stu-id="ede87-110">Example 1: Remove a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

<span data-ttu-id="ede87-111">Bu komut, Group001 adındaki kaynak grubuna ait olan VMScaleSet001 adındaki VMSS 'yi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ede87-111">This command removes the VMSS named VMScaleSet001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="ede87-112">Örnek 2: bir VMSS 'den sanal makineyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="ede87-112">Example 2: Remove a virtual machine from within a VMSS</span></span>
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

<span data-ttu-id="ede87-113">Bu komut, Group002 adındaki kaynak grubuna ait VMScaleSet002 adındaki VMSS 'den örnek KIMLIĞI 3 olan sanal makineyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ede87-113">This command removes the virtual machine with instance ID 3 from the VMSS named VMScaleSet002 that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="ede87-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ede87-114">PARAMETERS</span></span>

### <span data-ttu-id="ede87-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ede87-115">-DefaultProfile</span></span>
<span data-ttu-id="ede87-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ede87-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ede87-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ede87-117">-Force</span></span>
<span data-ttu-id="ede87-118">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ede87-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ede87-119">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="ede87-119">-InstanceId</span></span>
<span data-ttu-id="ede87-120">Bir dize dizisi olarak, başlaması gereken örneklerin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="ede87-120">Specifies, as a string array, the ID of the instances that need to be started.</span></span>
<span data-ttu-id="ede87-121">Örneğin: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="ede87-121">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="ede87-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ede87-122">-ResourceGroupName</span></span>
<span data-ttu-id="ede87-123">VMSS 'nin ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ede87-123">Specifies the name of the resource group that the VMSS belongs to.</span></span>

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

### <span data-ttu-id="ede87-124">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ede87-124">-VMScaleSetName</span></span>
<span data-ttu-id="ede87-125">Türleri bu cmdlet 'in kaldırdığı VMSUBNET 'in adını göstermektedir.</span><span class="sxs-lookup"><span data-stu-id="ede87-125">Species the name of the VMSS that this cmdlet removes.</span></span>
<span data-ttu-id="ede87-126">*InstanceId* parametresini belirtirseniz cmdlet, belirtilen sanal makineyi Bu parametreyle adlandırılan VMSS 'den kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ede87-126">If you specify the *InstanceId* parameter, the cmdlet will remove the specified virtual machine from the VMSS named by this parameter.</span></span>

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

### <span data-ttu-id="ede87-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="ede87-127">-Confirm</span></span>
<span data-ttu-id="ede87-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ede87-128">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="ede87-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ede87-129">-WhatIf</span></span>
<span data-ttu-id="ede87-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ede87-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ede87-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ede87-131">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="ede87-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede87-132">CommonParameters</span></span>
<span data-ttu-id="ede87-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ede87-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede87-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ede87-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede87-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ede87-135">INPUTS</span></span>

## <span data-ttu-id="ede87-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ede87-136">OUTPUTS</span></span>

## <span data-ttu-id="ede87-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ede87-137">NOTES</span></span>

## <span data-ttu-id="ede87-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ede87-138">RELATED LINKS</span></span>

[<span data-ttu-id="ede87-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ede87-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="ede87-140">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ede87-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="ede87-141">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ede87-141">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="ede87-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ede87-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="ede87-143">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ede87-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="ede87-144">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ede87-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="ede87-145">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ede87-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


