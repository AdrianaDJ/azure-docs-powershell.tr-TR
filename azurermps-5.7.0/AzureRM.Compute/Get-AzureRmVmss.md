---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: b3e9f2608703eebd5ad24846aad7b5a1ad11e8ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594126"
---
# <span data-ttu-id="ccdac-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccdac-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="ccdac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccdac-102">SYNOPSIS</span></span>
<span data-ttu-id="ccdac-103">Bir VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ccdac-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccdac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ccdac-104">SYNTAX</span></span>

### <span data-ttu-id="ccdac-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ccdac-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [<CommonParameters>]
```

### <span data-ttu-id="ccdac-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="ccdac-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [<CommonParameters>]
```

## <span data-ttu-id="ccdac-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ccdac-107">DESCRIPTION</span></span>
<span data-ttu-id="ccdac-108">**Get-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesinin (VMSS) modelini ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="ccdac-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="ccdac-109">Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="ccdac-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="ccdac-110">Örnek görünümü sanal makinenin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="ccdac-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="ccdac-111">Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="ccdac-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="ccdac-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ccdac-112">EXAMPLES</span></span>

### <span data-ttu-id="ccdac-113">Örnek 1: bir VMSS özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="ccdac-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="ccdac-114">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="ccdac-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="ccdac-115">Komut, *InstanceView* anahtar parametresini belirtmediğinden, cmdlet sanal makinenin model görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="ccdac-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="ccdac-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ccdac-116">PARAMETERS</span></span>

### <span data-ttu-id="ccdac-117">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="ccdac-117">-InstanceView</span></span>
<span data-ttu-id="ccdac-118">Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ccdac-118">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccdac-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccdac-119">-ResourceGroupName</span></span>
<span data-ttu-id="ccdac-120">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ccdac-120">Specifies the name of the Resource Group of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccdac-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ccdac-121">-VMScaleSetName</span></span>
<span data-ttu-id="ccdac-122">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="ccdac-122">Species the name of the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccdac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccdac-123">CommonParameters</span></span>
<span data-ttu-id="ccdac-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ccdac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccdac-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccdac-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccdac-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ccdac-126">INPUTS</span></span>

### <span data-ttu-id="ccdac-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ccdac-127">None</span></span>
<span data-ttu-id="ccdac-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ccdac-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ccdac-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ccdac-129">OUTPUTS</span></span>

### <span data-ttu-id="ccdac-130">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ccdac-130">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ccdac-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ccdac-131">NOTES</span></span>

## <span data-ttu-id="ccdac-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ccdac-132">RELATED LINKS</span></span>

[<span data-ttu-id="ccdac-133">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccdac-133">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="ccdac-134">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccdac-134">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="ccdac-135">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccdac-135">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="ccdac-136">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccdac-136">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="ccdac-137">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccdac-137">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="ccdac-138">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccdac-138">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="ccdac-139">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ccdac-139">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


