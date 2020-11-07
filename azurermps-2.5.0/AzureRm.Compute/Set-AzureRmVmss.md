---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2d33f111928d0b022c7836d0b5c86fb5ec6f203e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939406"
---
# <span data-ttu-id="903e1-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="903e1-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="903e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="903e1-102">SYNOPSIS</span></span>
<span data-ttu-id="903e1-103">Belirtilen bir VMSS 'de belirli eylemleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="903e1-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="903e1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="903e1-104">SYNTAX</span></span>

### <span data-ttu-id="903e1-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="903e1-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="903e1-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="903e1-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="903e1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="903e1-107">DESCRIPTION</span></span>
<span data-ttu-id="903e1-108">**Set-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesinde belirli eylemleri ayarlar (VMSS).</span><span class="sxs-lookup"><span data-stu-id="903e1-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="903e1-109">Bu cmdlet 'in desteklediği tek eylem yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="903e1-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="903e1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="903e1-110">EXAMPLES</span></span>

### <span data-ttu-id="903e1-111">Örnek 1: VMSS 'yi yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="903e1-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="903e1-112">Bu komut, ContosoGroup adlı kaynak grubuna ait olan ContosoVMSS adlı VMSUBNET 'leri yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="903e1-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="903e1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="903e1-113">PARAMETERS</span></span>

### <span data-ttu-id="903e1-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="903e1-114">-AsJob</span></span>
<span data-ttu-id="903e1-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="903e1-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="903e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903e1-116">-DefaultProfile</span></span>
<span data-ttu-id="903e1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="903e1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="903e1-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="903e1-118">-InstanceId</span></span>
<span data-ttu-id="903e1-119">Sanal makinenin örnek KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="903e1-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="903e1-120">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="903e1-120">-Reimage</span></span>
<span data-ttu-id="903e1-121">Cmdlet 'in VMSS 'yi yeniden görüntüdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="903e1-121">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="903e1-122">-Reımageall</span><span class="sxs-lookup"><span data-stu-id="903e1-122">-ReimageAll</span></span>
<span data-ttu-id="903e1-123">Cmdlet 'in VMSS 'deki tüm diskleri yeniden göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="903e1-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="903e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="903e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="903e1-125">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="903e1-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="903e1-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="903e1-126">-VMScaleSetName</span></span>
<span data-ttu-id="903e1-127">Türleri bu cmdlet 'in eylemleri ayarladığı VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="903e1-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="903e1-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="903e1-128">-Confirm</span></span>
<span data-ttu-id="903e1-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="903e1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="903e1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="903e1-130">-WhatIf</span></span>
<span data-ttu-id="903e1-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="903e1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="903e1-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="903e1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="903e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903e1-133">CommonParameters</span></span>
<span data-ttu-id="903e1-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="903e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903e1-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="903e1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903e1-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="903e1-136">INPUTS</span></span>

### <span data-ttu-id="903e1-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="903e1-137">None</span></span>
<span data-ttu-id="903e1-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="903e1-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="903e1-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="903e1-139">OUTPUTS</span></span>

### <span data-ttu-id="903e1-140">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="903e1-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="903e1-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="903e1-141">NOTES</span></span>

## <span data-ttu-id="903e1-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="903e1-142">RELATED LINKS</span></span>

[<span data-ttu-id="903e1-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="903e1-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="903e1-144">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="903e1-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="903e1-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="903e1-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="903e1-146">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="903e1-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="903e1-147">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="903e1-147">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="903e1-148">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="903e1-148">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="903e1-149">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="903e1-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


