---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: fa8681a8dab5aaba6d82b03a8b3885fd453e1faa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592640"
---
# <span data-ttu-id="e0029-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0029-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="e0029-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0029-102">SYNOPSIS</span></span>
<span data-ttu-id="e0029-103">Bir VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="e0029-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0029-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e0029-104">SYNTAX</span></span>

### <span data-ttu-id="e0029-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e0029-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0029-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="e0029-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0029-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e0029-107">DESCRIPTION</span></span>
<span data-ttu-id="e0029-108">**Get-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesinin (VMSS) modelini ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="e0029-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e0029-109">Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="e0029-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="e0029-110">Örnek görünümü sanal makinenin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="e0029-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="e0029-111">Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="e0029-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="e0029-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e0029-112">EXAMPLES</span></span>

### <span data-ttu-id="e0029-113">Örnek 1: bir VMSS özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="e0029-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="e0029-114">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="e0029-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="e0029-115">Komut, *InstanceView* anahtar parametresini belirtmediğinden, cmdlet sanal makinenin model görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="e0029-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="e0029-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e0029-116">PARAMETERS</span></span>

### <span data-ttu-id="e0029-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0029-117">-DefaultProfile</span></span>
<span data-ttu-id="e0029-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e0029-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0029-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="e0029-119">-InstanceView</span></span>
<span data-ttu-id="e0029-120">Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e0029-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="e0029-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0029-121">-ResourceGroupName</span></span>
<span data-ttu-id="e0029-122">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e0029-122">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0029-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e0029-123">-VMScaleSetName</span></span>
<span data-ttu-id="e0029-124">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="e0029-124">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0029-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0029-125">CommonParameters</span></span>
<span data-ttu-id="e0029-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e0029-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0029-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0029-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0029-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e0029-128">INPUTS</span></span>

## <span data-ttu-id="e0029-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e0029-129">OUTPUTS</span></span>

### <span data-ttu-id="e0029-130">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="e0029-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e0029-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e0029-131">NOTES</span></span>

## <span data-ttu-id="e0029-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e0029-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0029-133">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0029-133">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="e0029-134">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0029-134">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="e0029-135">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0029-135">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="e0029-136">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0029-136">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="e0029-137">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0029-137">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="e0029-138">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0029-138">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="e0029-139">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0029-139">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


