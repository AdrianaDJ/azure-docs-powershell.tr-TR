---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: 5fcb99a6e909675b47d245755ffd42e3c058a37a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588524"
---
# <span data-ttu-id="e8271-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e8271-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="e8271-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8271-102">SYNOPSIS</span></span>
<span data-ttu-id="e8271-103">Belirtilen bir VMSS 'de belirli eylemleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e8271-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8271-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8271-104">SYNTAX</span></span>

### <span data-ttu-id="e8271-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8271-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8271-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="e8271-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8271-107">RedeployMethodParameter</span><span class="sxs-lookup"><span data-stu-id="e8271-107">RedeployMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Redeploy]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8271-108">PerformMaintenanceMethodParameter</span><span class="sxs-lookup"><span data-stu-id="e8271-108">PerformMaintenanceMethodParameter</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-PerformMaintenance] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8271-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8271-109">DESCRIPTION</span></span>
<span data-ttu-id="e8271-110">**Set-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesinde belirli eylemleri ayarlar (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e8271-110">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e8271-111">Bu cmdlet 'in desteklediği tek eylem yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e8271-111">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="e8271-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8271-112">EXAMPLES</span></span>

### <span data-ttu-id="e8271-113">Örnek 1: VMSS 'yi yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="e8271-113">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="e8271-114">Bu komut, ContosoGroup adlı kaynak grubuna ait olan ContosoVMSS adlı VMSUBNET 'leri yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="e8271-114">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="e8271-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8271-115">PARAMETERS</span></span>

### <span data-ttu-id="e8271-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="e8271-116">-AsJob</span></span>
<span data-ttu-id="e8271-117">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="e8271-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e8271-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8271-118">-DefaultProfile</span></span>
<span data-ttu-id="e8271-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8271-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8271-120">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e8271-120">-InstanceId</span></span>
<span data-ttu-id="e8271-121">Sanal makinenin örnek KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="e8271-121">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="e8271-122">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="e8271-122">-PerformMaintenance</span></span>
<span data-ttu-id="e8271-123">Bu cmdlet 'in VMSS 'de bir veya birden çok sanal makine olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8271-123">Indicates that this cmdlet performs maintenance one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="e8271-124">-Yeniden dağıtma</span><span class="sxs-lookup"><span data-stu-id="e8271-124">-Redeploy</span></span>
<span data-ttu-id="e8271-125">Cmdlet 'in VMSS 'de bir veya daha fazla sanal makineyi geri dağıttığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8271-125">Indicates that the cmdlet redeploys one or more virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="e8271-126">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="e8271-126">-Reimage</span></span>
<span data-ttu-id="e8271-127">Cmdlet 'in VMSS 'yi yeniden görüntüdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8271-127">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="e8271-128">-Reımageall</span><span class="sxs-lookup"><span data-stu-id="e8271-128">-ReimageAll</span></span>
<span data-ttu-id="e8271-129">Cmdlet 'in VMSS 'deki tüm diskleri yeniden göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8271-129">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="e8271-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8271-130">-ResourceGroupName</span></span>
<span data-ttu-id="e8271-131">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8271-131">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="e8271-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e8271-132">-VMScaleSetName</span></span>
<span data-ttu-id="e8271-133">Türleri bu cmdlet 'in eylemleri ayarladığı VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="e8271-133">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="e8271-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8271-134">-Confirm</span></span>
<span data-ttu-id="e8271-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8271-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8271-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8271-136">-WhatIf</span></span>
<span data-ttu-id="e8271-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8271-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8271-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8271-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8271-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8271-139">CommonParameters</span></span>
<span data-ttu-id="e8271-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8271-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8271-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8271-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8271-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8271-142">INPUTS</span></span>

### <span data-ttu-id="e8271-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e8271-143">System.String</span></span>

### <span data-ttu-id="e8271-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="e8271-144">System.String[]</span></span>

## <span data-ttu-id="e8271-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8271-145">OUTPUTS</span></span>

### <span data-ttu-id="e8271-146">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="e8271-146">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e8271-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8271-147">NOTES</span></span>

## <span data-ttu-id="e8271-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8271-148">RELATED LINKS</span></span>

[<span data-ttu-id="e8271-149">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e8271-149">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="e8271-150">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e8271-150">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="e8271-151">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e8271-151">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="e8271-152">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e8271-152">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="e8271-153">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e8271-153">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="e8271-154">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e8271-154">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="e8271-155">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e8271-155">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


