---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: 61bd867f7790f47599ac10ebd6523327e4e1868a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761262"
---
# <span data-ttu-id="4cbbb-101">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4cbbb-101">Restart-AzVmss</span></span>

## <span data-ttu-id="4cbbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cbbb-102">SYNOPSIS</span></span>
<span data-ttu-id="4cbbb-103">Vmsubnet 'de VMSS veya sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

## <span data-ttu-id="4cbbb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4cbbb-104">SYNTAX</span></span>

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cbbb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4cbbb-105">DESCRIPTION</span></span>
<span data-ttu-id="4cbbb-106">**Restart-AzVmss** cmdlet 'ı sanal makine ölçeği kümesini (VMSS) yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-106">The **Restart-AzVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="4cbbb-107">Bu cmdlet, *InstanceId* parametresini kullanarak VMSS içinde belirli bir sanal makineyi yeniden başlatmak için de kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="4cbbb-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4cbbb-108">EXAMPLES</span></span>

### <span data-ttu-id="4cbbb-109">Örnek 1: VMSS 'yi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="4cbbb-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="4cbbb-110">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'yi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="4cbbb-111">Örnek 2: VMSS içinde belirli bir sanal makineyi yeniden başlatın</span><span class="sxs-lookup"><span data-stu-id="4cbbb-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="4cbbb-112">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS 'de 1 örnek KIMLIĞINE sahip bir sanal makineyi yeniden başlatır.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="4cbbb-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4cbbb-113">PARAMETERS</span></span>

### <span data-ttu-id="4cbbb-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="4cbbb-114">-AsJob</span></span>
<span data-ttu-id="4cbbb-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4cbbb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cbbb-116">-DefaultProfile</span></span>
<span data-ttu-id="4cbbb-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cbbb-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="4cbbb-118">-InstanceId</span></span>
<span data-ttu-id="4cbbb-119">Dize dizisi olarak, yeniden başlatılması gereken örneklerin KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-119">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="4cbbb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cbbb-120">-ResourceGroupName</span></span>
<span data-ttu-id="4cbbb-121">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-121">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="4cbbb-122">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4cbbb-122">-VMScaleSetName</span></span>
<span data-ttu-id="4cbbb-123">Türleri, bu cmdlet 'in yeniden başlattığı VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-123">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="4cbbb-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="4cbbb-124">-Confirm</span></span>
<span data-ttu-id="4cbbb-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cbbb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cbbb-126">-WhatIf</span></span>
<span data-ttu-id="4cbbb-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cbbb-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cbbb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cbbb-129">CommonParameters</span></span>
<span data-ttu-id="4cbbb-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4cbbb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cbbb-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cbbb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cbbb-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4cbbb-132">INPUTS</span></span>

### <span data-ttu-id="4cbbb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4cbbb-133">System.String</span></span>

### <span data-ttu-id="4cbbb-134">System. String []</span><span class="sxs-lookup"><span data-stu-id="4cbbb-134">System.String[]</span></span>

## <span data-ttu-id="4cbbb-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4cbbb-135">OUTPUTS</span></span>

### <span data-ttu-id="4cbbb-136">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="4cbbb-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4cbbb-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4cbbb-137">NOTES</span></span>

## <span data-ttu-id="4cbbb-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4cbbb-138">RELATED LINKS</span></span>

[<span data-ttu-id="4cbbb-139">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4cbbb-139">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="4cbbb-140">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4cbbb-140">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="4cbbb-141">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4cbbb-141">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="4cbbb-142">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4cbbb-142">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="4cbbb-143">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4cbbb-143">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="4cbbb-144">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4cbbb-144">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="4cbbb-145">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4cbbb-145">Update-AzVmss</span></span>](./Update-AzVmss.md)


