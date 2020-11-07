---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: AF0DDDD0-B664-4AD8-A569-1363FB2EDB40
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVmss.md
ms.openlocfilehash: eb05601028d43a7260186754f2a3e55b0691793d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752652"
---
# <span data-ttu-id="4bda2-101">Stop-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bda2-101">Stop-AzVmss</span></span>

## <span data-ttu-id="4bda2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bda2-102">SYNOPSIS</span></span>
<span data-ttu-id="4bda2-103">VMSS 'yi veya VMSS içindeki sanal makinelerin kümesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="4bda2-103">Stops the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="4bda2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4bda2-104">SYNTAX</span></span>

### <span data-ttu-id="4bda2-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4bda2-105">DefaultParameter (Default)</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4bda2-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="4bda2-106">FriendMethod</span></span>
```
Stop-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-StayProvisioned] [-SkipShutdown] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4bda2-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4bda2-107">DESCRIPTION</span></span>
<span data-ttu-id="4bda2-108">**Stop-AzVmss** cmdlet 'ı sanal makine ölçek kümesindeki tüm sanal makineleri veya sanal makineler kümesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="4bda2-108">The **Stop-AzVmss** cmdlet stops all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="4bda2-109">*InstanceId* parametresini kullanarak bir sanal makine kümesi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4bda2-109">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="4bda2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4bda2-110">EXAMPLES</span></span>

### <span data-ttu-id="4bda2-111">Örnek 1: VMSS içindeki tüm sanal makineleri durdurma</span><span class="sxs-lookup"><span data-stu-id="4bda2-111">Example 1: Stop all the virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="4bda2-112">Bu komut, ContosoVMSS adlı VMSS 'ye ait tüm sanal makineleri durdurur.</span><span class="sxs-lookup"><span data-stu-id="4bda2-112">This command stops all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="4bda2-113">Örnek 2: VMSS içinde belirli bir sanal makine kümesini durdurma</span><span class="sxs-lookup"><span data-stu-id="4bda2-113">Example 2: Stop a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Stop-AzVmss -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS" -InstanceId "3","5"
```

<span data-ttu-id="4bda2-114">Bu komut, ContosoVMSS adlı VMSS 'ye ait örnek KIMLIĞI dizesi dizisiyle belirtilen belirli bir sanal makine kümesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="4bda2-114">This command stops a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="4bda2-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4bda2-115">PARAMETERS</span></span>

### <span data-ttu-id="4bda2-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="4bda2-116">-AsJob</span></span>
<span data-ttu-id="4bda2-117">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="4bda2-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4bda2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bda2-118">-DefaultProfile</span></span>
<span data-ttu-id="4bda2-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4bda2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bda2-120">-Force</span><span class="sxs-lookup"><span data-stu-id="4bda2-120">-Force</span></span>
<span data-ttu-id="4bda2-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="4bda2-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4bda2-122">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="4bda2-122">-InstanceId</span></span>
<span data-ttu-id="4bda2-123">Bu cmdlet 'in durdurduğu sanal makine örneklerinin KIMLIĞINI veya kimliklerini dize dizisi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bda2-123">Specifies, as a string array, the ID or IDs of the virtual machine instances that this cmdlet stops.</span></span>
<span data-ttu-id="4bda2-124">Örneğin: `-InstanceId "0", "3"` .</span><span class="sxs-lookup"><span data-stu-id="4bda2-124">For instance: `-InstanceId "0", "3"`.</span></span>

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

### <span data-ttu-id="4bda2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bda2-125">-ResourceGroupName</span></span>
<span data-ttu-id="4bda2-126">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bda2-126">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="4bda2-127">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="4bda2-127">-SkipShutdown</span></span>
<span data-ttu-id="4bda2-128">Düzgün olmayan VM kapatması istemek için</span><span class="sxs-lookup"><span data-stu-id="4bda2-128">To request non-graceful VM shutdown</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4bda2-129">-Staysağlandı</span><span class="sxs-lookup"><span data-stu-id="4bda2-129">-StayProvisioned</span></span>
<span data-ttu-id="4bda2-130">Belirtilmişse, sanal makine durdurulmuş duruma girer.</span><span class="sxs-lookup"><span data-stu-id="4bda2-130">If specified, the virtual machine will enter stopped state.</span></span> <span data-ttu-id="4bda2-131">Belirtilmezse, sanal makine durduruldu-serbest işlem durumuna girer.</span><span class="sxs-lookup"><span data-stu-id="4bda2-131">If not specified, the virtual machine will enter stopped-deallocated state.</span></span> <span data-ttu-id="4bda2-132">Kullanıcı hala durdurulmuş durumda VM 'Ler için ücretlendirilecek, ancak durdurulan serbest durumda VM 'Ler için kullanılmaz.</span><span class="sxs-lookup"><span data-stu-id="4bda2-132">The user is still charged for VMs in stopped state but not for VMs in stopped-deallocated state.</span></span>

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

### <span data-ttu-id="4bda2-133">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4bda2-133">-VMScaleSetName</span></span>
<span data-ttu-id="4bda2-134">Bu cmdlet 'in sanal makineleri durdurduğu VMSS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4bda2-134">Specifies the name of the VMSS for which this cmdlet stops the virtual machines.</span></span>

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

### <span data-ttu-id="4bda2-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="4bda2-135">-Confirm</span></span>
<span data-ttu-id="4bda2-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4bda2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4bda2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4bda2-137">-WhatIf</span></span>
<span data-ttu-id="4bda2-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4bda2-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4bda2-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4bda2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4bda2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bda2-140">CommonParameters</span></span>
<span data-ttu-id="4bda2-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4bda2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bda2-142">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4bda2-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bda2-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4bda2-143">INPUTS</span></span>

### <span data-ttu-id="4bda2-144">System. String</span><span class="sxs-lookup"><span data-stu-id="4bda2-144">System.String</span></span>

### <span data-ttu-id="4bda2-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="4bda2-145">System.String[]</span></span>

## <span data-ttu-id="4bda2-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4bda2-146">OUTPUTS</span></span>

### <span data-ttu-id="4bda2-147">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="4bda2-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4bda2-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4bda2-148">NOTES</span></span>

## <span data-ttu-id="4bda2-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4bda2-149">RELATED LINKS</span></span>

[<span data-ttu-id="4bda2-150">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bda2-150">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="4bda2-151">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bda2-151">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="4bda2-152">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bda2-152">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="4bda2-153">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bda2-153">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="4bda2-154">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bda2-154">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="4bda2-155">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bda2-155">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="4bda2-156">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4bda2-156">Update-AzVmss</span></span>](./Update-AzVmss.md)

