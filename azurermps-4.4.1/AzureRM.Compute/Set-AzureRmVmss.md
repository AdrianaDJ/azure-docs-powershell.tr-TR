---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: efb24aa4f8770e1911b9bf85a1fbf4dd366ea34d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586924"
---
# <span data-ttu-id="c9cc3-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c9cc3-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="c9cc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="c9cc3-103">Belirtilen bir VMSS 'de belirli eylemleri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9cc3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9cc3-104">SYNTAX</span></span>

### <span data-ttu-id="c9cc3-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c9cc3-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9cc3-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="c9cc3-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9cc3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9cc3-107">DESCRIPTION</span></span>
<span data-ttu-id="c9cc3-108">**Set-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesinde belirli eylemleri ayarlar (VMSS).</span><span class="sxs-lookup"><span data-stu-id="c9cc3-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="c9cc3-109">Bu cmdlet 'in desteklediği tek eylem yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="c9cc3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9cc3-110">EXAMPLES</span></span>

### <span data-ttu-id="c9cc3-111">Örnek 1: VMSS 'yi yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="c9cc3-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="c9cc3-112">Bu komut, ContosoGroup adlı kaynak grubuna ait olan ContosoVMSS adlı VMSUBNET 'leri yeniden görüntüler.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="c9cc3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9cc3-113">PARAMETERS</span></span>

### <span data-ttu-id="c9cc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9cc3-114">-DefaultProfile</span></span>
<span data-ttu-id="c9cc3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9cc3-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c9cc3-116">-InstanceId</span></span>
<span data-ttu-id="c9cc3-117">Sanal makinenin örnek KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-117">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="c9cc3-118">-Yeniden görüntü</span><span class="sxs-lookup"><span data-stu-id="c9cc3-118">-Reimage</span></span>
<span data-ttu-id="c9cc3-119">Cmdlet 'in VMSS 'yi yeniden görüntüdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-119">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="c9cc3-120">-Reımageall</span><span class="sxs-lookup"><span data-stu-id="c9cc3-120">-ReimageAll</span></span>
<span data-ttu-id="c9cc3-121">Cmdlet 'in VMSS 'deki tüm diskleri yeniden göndereceğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-121">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="c9cc3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9cc3-122">-ResourceGroupName</span></span>
<span data-ttu-id="c9cc3-123">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-123">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="c9cc3-124">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c9cc3-124">-VMScaleSetName</span></span>
<span data-ttu-id="c9cc3-125">Türleri bu cmdlet 'in eylemleri ayarladığı VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-125">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="c9cc3-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="c9cc3-126">-Confirm</span></span>
<span data-ttu-id="c9cc3-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9cc3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9cc3-128">-WhatIf</span></span>
<span data-ttu-id="c9cc3-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9cc3-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9cc3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9cc3-131">CommonParameters</span></span>
<span data-ttu-id="c9cc3-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9cc3-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9cc3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9cc3-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9cc3-134">INPUTS</span></span>

## <span data-ttu-id="c9cc3-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9cc3-135">OUTPUTS</span></span>

### <span data-ttu-id="c9cc3-136">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="c9cc3-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c9cc3-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9cc3-137">NOTES</span></span>

## <span data-ttu-id="c9cc3-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9cc3-138">RELATED LINKS</span></span>

[<span data-ttu-id="c9cc3-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c9cc3-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="c9cc3-140">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c9cc3-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c9cc3-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c9cc3-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c9cc3-142">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c9cc3-142">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c9cc3-143">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c9cc3-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="c9cc3-144">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c9cc3-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="c9cc3-145">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c9cc3-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


