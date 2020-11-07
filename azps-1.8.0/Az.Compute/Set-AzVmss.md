---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 99f022f539ff5db9bb99537bb87fce8a8567947c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917220"
---
# <span data-ttu-id="edc81-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="edc81-101">Set-AzVmss</span></span>

## <span data-ttu-id="edc81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edc81-102">SYNOPSIS</span></span>
<span data-ttu-id="edc81-103">Belirtilen bir VMSS 'de belirli eylemleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="edc81-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="edc81-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="edc81-104">SYNTAX</span></span>

### <span data-ttu-id="edc81-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="edc81-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-TempDisk]
 [-Reimage] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edc81-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="edc81-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-ReimageAll]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edc81-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="edc81-107">RedeployMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edc81-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="edc81-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="edc81-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="edc81-109">DESCRIPTION</span></span>
<span data-ttu-id="edc81-110">**Set-AzVmss** cmdlet 'ı sanal makine ölçek kümesinde belirli eylemleri ayarlar (VMSS).</span><span class="sxs-lookup"><span data-stu-id="edc81-110">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="edc81-111">Bu cmdlet 'in desteklediği tek eylem yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="edc81-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="edc81-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="edc81-112">EXAMPLES</span></span>

### <span data-ttu-id="edc81-113">Örnek 1: VMSS 'yi yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="edc81-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="edc81-114">Bu komut, ContosoGroup adlı kaynak grubuna ait olan ContosoVMSS adlı VMSUBNET 'leri yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="edc81-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="edc81-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="edc81-115">PARAMETERS</span></span>

### <span data-ttu-id="edc81-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="edc81-116">-AsJob</span></span>
<span data-ttu-id="edc81-117">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="edc81-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="edc81-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edc81-118">-DefaultProfile</span></span>
<span data-ttu-id="edc81-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="edc81-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="edc81-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="edc81-120">-InstanceId</span></span>
<span data-ttu-id="edc81-121">Sanal makinenin örnek KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="edc81-121">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="edc81-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="edc81-122">-PerformMaintenance</span></span>
<span data-ttu-id="edc81-123">Bu cmdlet 'in VMSS 'de bir veya birden çok sanal makine olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="edc81-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PerformMaintenanceMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc81-124">-Yeniden dağıtma</span><span class="sxs-lookup"><span data-stu-id="edc81-124">-Redeploy</span></span>
<span data-ttu-id="edc81-125">Cmdlet 'in VMSS 'de bir veya daha fazla sanal makineyi geri dağıttığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edc81-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc81-126">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="edc81-126">-Reimage</span></span>
<span data-ttu-id="edc81-127">Cmdlet 'in VMSS 'yi yeniden görüntüdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="edc81-127">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc81-128">-Reımageall</span><span class="sxs-lookup"><span data-stu-id="edc81-128">-ReimageAll</span></span>
<span data-ttu-id="edc81-129">Cmdlet 'in VMSS 'deki tüm diskleri yeniden göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="edc81-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc81-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edc81-130">-ResourceGroupName</span></span>
<span data-ttu-id="edc81-131">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="edc81-131">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="edc81-132">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="edc81-132">-TempDisk</span></span>
<span data-ttu-id="edc81-133">Geçici diske yeniden görüntü uygulanıp gösterilmeyeceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="edc81-133">Specifies whether to reimage temp disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edc81-134">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="edc81-134">-VMScaleSetName</span></span>
<span data-ttu-id="edc81-135">Türleri bu cmdlet 'in eylemleri ayarladığı VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="edc81-135">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="edc81-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="edc81-136">-Confirm</span></span>
<span data-ttu-id="edc81-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="edc81-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edc81-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edc81-138">-WhatIf</span></span>
<span data-ttu-id="edc81-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="edc81-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="edc81-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="edc81-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edc81-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edc81-141">CommonParameters</span></span>
<span data-ttu-id="edc81-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="edc81-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edc81-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edc81-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edc81-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="edc81-144">INPUTS</span></span>

### <span data-ttu-id="edc81-145">System. String</span><span class="sxs-lookup"><span data-stu-id="edc81-145">System.String</span></span>

### <span data-ttu-id="edc81-146">System. String []</span><span class="sxs-lookup"><span data-stu-id="edc81-146">System.String[]</span></span>

## <span data-ttu-id="edc81-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="edc81-147">OUTPUTS</span></span>

### <span data-ttu-id="edc81-148">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="edc81-148">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="edc81-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="edc81-149">NOTES</span></span>

## <span data-ttu-id="edc81-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="edc81-150">RELATED LINKS</span></span>

[<span data-ttu-id="edc81-151">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="edc81-151">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="edc81-152">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="edc81-152">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="edc81-153">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="edc81-153">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="edc81-154">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="edc81-154">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="edc81-155">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="edc81-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="edc81-156">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="edc81-156">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="edc81-157">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="edc81-157">Update-AzVmss</span></span>](./Update-AzVmss.md)


