---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 5ceb420f30525817ebccd6d3f38a53e6c1cad66e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936812"
---
# <span data-ttu-id="eea9f-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="eea9f-101">Set-AzVmss</span></span>

## <span data-ttu-id="eea9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eea9f-102">SYNOPSIS</span></span>
<span data-ttu-id="eea9f-103">Belirtilen bir VMSS 'de belirli eylemleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="eea9f-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="eea9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eea9f-104">SYNTAX</span></span>

### <span data-ttu-id="eea9f-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eea9f-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eea9f-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="eea9f-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eea9f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="eea9f-107">DESCRIPTION</span></span>
<span data-ttu-id="eea9f-108">**Set-AzVmss** cmdlet 'ı sanal makine ölçek kümesinde belirli eylemleri ayarlar (VMSS).</span><span class="sxs-lookup"><span data-stu-id="eea9f-108">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="eea9f-109">Bu cmdlet 'in desteklediği tek eylem yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="eea9f-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="eea9f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eea9f-110">EXAMPLES</span></span>

### <span data-ttu-id="eea9f-111">Örnek 1: VMSS 'yi yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="eea9f-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="eea9f-112">Bu komut, ContosoGroup adlı kaynak grubuna ait olan ContosoVMSS adlı VMSUBNET 'leri yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="eea9f-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="eea9f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eea9f-113">PARAMETERS</span></span>

### <span data-ttu-id="eea9f-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="eea9f-114">-AsJob</span></span>
<span data-ttu-id="eea9f-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="eea9f-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eea9f-116">-DefaultProfile</span></span>
<span data-ttu-id="eea9f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eea9f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea9f-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="eea9f-118">-InstanceId</span></span>
<span data-ttu-id="eea9f-119">Sanal makinenin örnek KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="eea9f-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="eea9f-120">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="eea9f-120">-Reimage</span></span>
<span data-ttu-id="eea9f-121">Cmdlet 'in VMSS 'yi yeniden görüntüdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="eea9f-121">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea9f-122">-Reımageall</span><span class="sxs-lookup"><span data-stu-id="eea9f-122">-ReimageAll</span></span>
<span data-ttu-id="eea9f-123">Cmdlet 'in VMSS 'deki tüm diskleri yeniden göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="eea9f-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eea9f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eea9f-124">-ResourceGroupName</span></span>
<span data-ttu-id="eea9f-125">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="eea9f-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="eea9f-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="eea9f-126">-VMScaleSetName</span></span>
<span data-ttu-id="eea9f-127">Türleri bu cmdlet 'in eylemleri ayarladığı VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="eea9f-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="eea9f-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="eea9f-128">-Confirm</span></span>
<span data-ttu-id="eea9f-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eea9f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eea9f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eea9f-130">-WhatIf</span></span>
<span data-ttu-id="eea9f-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eea9f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eea9f-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eea9f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eea9f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eea9f-133">CommonParameters</span></span>
<span data-ttu-id="eea9f-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eea9f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eea9f-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eea9f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eea9f-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eea9f-136">INPUTS</span></span>

### <span data-ttu-id="eea9f-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="eea9f-137">None</span></span>
<span data-ttu-id="eea9f-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="eea9f-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eea9f-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eea9f-139">OUTPUTS</span></span>

### <span data-ttu-id="eea9f-140">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="eea9f-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="eea9f-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eea9f-141">NOTES</span></span>

## <span data-ttu-id="eea9f-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eea9f-142">RELATED LINKS</span></span>

[<span data-ttu-id="eea9f-143">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="eea9f-143">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="eea9f-144">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="eea9f-144">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="eea9f-145">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="eea9f-145">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="eea9f-146">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="eea9f-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="eea9f-147">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="eea9f-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="eea9f-148">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="eea9f-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="eea9f-149">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="eea9f-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


