---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmss.md
ms.openlocfilehash: 22e281d7aa6e2d71506ddb616f96a149dcff6068
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936999"
---
# <span data-ttu-id="4c304-101">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4c304-101">Get-AzVmss</span></span>

## <span data-ttu-id="4c304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c304-102">SYNOPSIS</span></span>
<span data-ttu-id="4c304-103">Bir VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="4c304-103">Gets the properties of a VMSS.</span></span>

## <span data-ttu-id="4c304-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c304-104">SYNTAX</span></span>

### <span data-ttu-id="4c304-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c304-105">DefaultParameter (Default)</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c304-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="4c304-106">FriendMethod</span></span>
```
Get-AzVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c304-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c304-107">DESCRIPTION</span></span>
<span data-ttu-id="4c304-108">**Get-AzVmss** cmdlet 'ı sanal makine ölçek kümesinin (VMSS) modelini ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="4c304-108">The **Get-AzVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="4c304-109">Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="4c304-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="4c304-110">Örnek görünümü sanal makinenin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="4c304-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="4c304-111">Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="4c304-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="4c304-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c304-112">EXAMPLES</span></span>

### <span data-ttu-id="4c304-113">Örnek 1: bir VMSS özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="4c304-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="4c304-114">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="4c304-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="4c304-115">Komut, *InstanceView* anahtar parametresini belirtmediğinden, cmdlet sanal makinenin model görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="4c304-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="4c304-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c304-116">PARAMETERS</span></span>

### <span data-ttu-id="4c304-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c304-117">-DefaultProfile</span></span>
<span data-ttu-id="4c304-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c304-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c304-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="4c304-119">-InstanceView</span></span>
<span data-ttu-id="4c304-120">Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c304-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="4c304-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c304-121">-ResourceGroupName</span></span>
<span data-ttu-id="4c304-122">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4c304-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="4c304-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="4c304-123">-VMScaleSetName</span></span>
<span data-ttu-id="4c304-124">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="4c304-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="4c304-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c304-125">CommonParameters</span></span>
<span data-ttu-id="4c304-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c304-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c304-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c304-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c304-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c304-128">INPUTS</span></span>

### <span data-ttu-id="4c304-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="4c304-129">None</span></span>
<span data-ttu-id="4c304-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="4c304-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4c304-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c304-131">OUTPUTS</span></span>

### <span data-ttu-id="4c304-132">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="4c304-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="4c304-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c304-133">NOTES</span></span>

## <span data-ttu-id="4c304-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c304-134">RELATED LINKS</span></span>

[<span data-ttu-id="4c304-135">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4c304-135">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="4c304-136">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4c304-136">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="4c304-137">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4c304-137">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="4c304-138">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4c304-138">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="4c304-139">Başlangıç-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4c304-139">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="4c304-140">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4c304-140">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="4c304-141">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="4c304-141">Update-AzVmss</span></span>](./Update-AzVmss.md)


