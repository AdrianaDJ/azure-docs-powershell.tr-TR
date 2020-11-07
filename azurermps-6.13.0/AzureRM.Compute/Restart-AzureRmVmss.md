---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 9f4727fc9bc5a735f837d3bec5eced9cd20e9254
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764678"
---
# <span data-ttu-id="b3236-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3236-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="b3236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3236-102">SYNOPSIS</span></span>
<span data-ttu-id="b3236-103">Vmsubnet 'de VMSS veya sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="b3236-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3236-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3236-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3236-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3236-105">DESCRIPTION</span></span>
<span data-ttu-id="b3236-106">**Restart-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesini (VMSS) yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="b3236-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="b3236-107">Bu cmdlet, *InstanceId* parametresini kullanarak VMSS içinde belirli bir sanal makineyi yeniden başlatmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="b3236-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="b3236-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3236-108">EXAMPLES</span></span>

### <span data-ttu-id="b3236-109">Örnek 1: VMSS 'yi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="b3236-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="b3236-110">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'yi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="b3236-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="b3236-111">Örnek 2: VMSS içinde belirli bir sanal makineyi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="b3236-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="b3236-112">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'de 1 örnek KIMLIĞINE sahip bir sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="b3236-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="b3236-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3236-113">PARAMETERS</span></span>

### <span data-ttu-id="b3236-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="b3236-114">-AsJob</span></span>
<span data-ttu-id="b3236-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="b3236-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b3236-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3236-116">-DefaultProfile</span></span>
<span data-ttu-id="b3236-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3236-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3236-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="b3236-118">-InstanceId</span></span>
<span data-ttu-id="b3236-119">Dize dizisi olarak, yeniden başlatılması gereken örneklerin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3236-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="b3236-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3236-120">-ResourceGroupName</span></span>
<span data-ttu-id="b3236-121">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3236-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="b3236-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b3236-122">-VMScaleSetName</span></span>
<span data-ttu-id="b3236-123">Türleri, bu cmdlet 'in yeniden başlattığı VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="b3236-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="b3236-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="b3236-124">-Confirm</span></span>
<span data-ttu-id="b3236-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b3236-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3236-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3236-126">-WhatIf</span></span>
<span data-ttu-id="b3236-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b3236-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3236-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b3236-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3236-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3236-129">CommonParameters</span></span>
<span data-ttu-id="b3236-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3236-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3236-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3236-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3236-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3236-132">INPUTS</span></span>

### <span data-ttu-id="b3236-133">System. String</span><span class="sxs-lookup"><span data-stu-id="b3236-133">System.String</span></span>

### <span data-ttu-id="b3236-134">System. String []</span><span class="sxs-lookup"><span data-stu-id="b3236-134">System.String[]</span></span>

## <span data-ttu-id="b3236-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3236-135">OUTPUTS</span></span>

### <span data-ttu-id="b3236-136">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="b3236-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b3236-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3236-137">NOTES</span></span>

## <span data-ttu-id="b3236-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3236-138">RELATED LINKS</span></span>

[<span data-ttu-id="b3236-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3236-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="b3236-140">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3236-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="b3236-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3236-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="b3236-142">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3236-142">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="b3236-143">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3236-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="b3236-144">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3236-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="b3236-145">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b3236-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


