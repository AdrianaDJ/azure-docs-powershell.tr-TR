---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
ms.openlocfilehash: ec66d20e0d9a63b8101b1a9a46410c9e64ac2079
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939611"
---
# <span data-ttu-id="55e59-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="55e59-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="55e59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55e59-102">SYNOPSIS</span></span>
<span data-ttu-id="55e59-103">Bir VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="55e59-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55e59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="55e59-104">SYNTAX</span></span>

### <span data-ttu-id="55e59-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="55e59-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55e59-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="55e59-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55e59-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="55e59-107">DESCRIPTION</span></span>
<span data-ttu-id="55e59-108">**Get-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesinin (VMSS) modelini ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="55e59-108">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="55e59-109">Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="55e59-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="55e59-110">Örnek görünümü sanal makinenin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="55e59-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="55e59-111">Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="55e59-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="55e59-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="55e59-112">EXAMPLES</span></span>

### <span data-ttu-id="55e59-113">Örnek 1: bir VMSS özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="55e59-113">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="55e59-114">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="55e59-114">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="55e59-115">Komut, *InstanceView* anahtar parametresini belirtmediğinden, cmdlet sanal makinenin model görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="55e59-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

## <span data-ttu-id="55e59-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="55e59-116">PARAMETERS</span></span>

### <span data-ttu-id="55e59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e59-117">-DefaultProfile</span></span>
<span data-ttu-id="55e59-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="55e59-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55e59-119">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="55e59-119">-InstanceView</span></span>
<span data-ttu-id="55e59-120">Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="55e59-120">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="55e59-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55e59-121">-ResourceGroupName</span></span>
<span data-ttu-id="55e59-122">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="55e59-122">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="55e59-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="55e59-123">-VMScaleSetName</span></span>
<span data-ttu-id="55e59-124">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="55e59-124">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="55e59-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e59-125">CommonParameters</span></span>
<span data-ttu-id="55e59-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="55e59-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e59-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55e59-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e59-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="55e59-128">INPUTS</span></span>

### <span data-ttu-id="55e59-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="55e59-129">None</span></span>
<span data-ttu-id="55e59-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="55e59-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55e59-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="55e59-131">OUTPUTS</span></span>

### <span data-ttu-id="55e59-132">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="55e59-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="55e59-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="55e59-133">NOTES</span></span>

## <span data-ttu-id="55e59-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="55e59-134">RELATED LINKS</span></span>

[<span data-ttu-id="55e59-135">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="55e59-135">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="55e59-136">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="55e59-136">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="55e59-137">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="55e59-137">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="55e59-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="55e59-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="55e59-139">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="55e59-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="55e59-140">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="55e59-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="55e59-141">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="55e59-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


