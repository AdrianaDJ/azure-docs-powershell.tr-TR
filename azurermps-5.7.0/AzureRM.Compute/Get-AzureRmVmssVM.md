---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssVM.md
ms.openlocfilehash: 8d24aadd185a58472268fc4edf9ca504e7592bb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588977"
---
# <span data-ttu-id="6ef13-101">Get-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="6ef13-101">Get-AzureRmVmssVM</span></span>

## <span data-ttu-id="6ef13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ef13-102">SYNOPSIS</span></span>
<span data-ttu-id="6ef13-103">Bir VMSS sanal makinesinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6ef13-103">Gets the properties of a VMSS virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ef13-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ef13-104">SYNTAX</span></span>

### <span data-ttu-id="6ef13-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ef13-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ef13-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="6ef13-106">FriendMethod</span></span>
```
Get-AzureRmVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [<CommonParameters>]
```

## <span data-ttu-id="6ef13-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ef13-107">DESCRIPTION</span></span>
<span data-ttu-id="6ef13-108">**Get-AzureRmVmssVM** cmdlet 'ı, sanal makine ölçeği KÜMESI (VMSS) sanal makinesinin model görünümünü ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="6ef13-108">The **Get-AzureRmVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="6ef13-109">Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="6ef13-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="6ef13-110">Örnek görünümü sanal makinenin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="6ef13-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="6ef13-111">Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="6ef13-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="6ef13-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ef13-112">EXAMPLES</span></span>

### <span data-ttu-id="6ef13-113">Örnek 1: VMSS sanal makinesinin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="6ef13-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="6ef13-114">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS sanal makinesinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6ef13-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="6ef13-115">Komut, *InstanceView* anahtar parametresini belirtmediğinden, cmdlet sanal makinenin model görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="6ef13-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="6ef13-116">Örnek 2: bir VMSS sanal makinesinin model görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="6ef13-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="6ef13-117">Bu komut, Group002 adındaki kaynak grubuna ait olan VMSS004 adındaki VMSS sanal makinesinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6ef13-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="6ef13-118">Bu komut, $ID değişkeninde depolanan örnek KIMLIĞINI model görünümünün alınacağı şekilde alır.</span><span class="sxs-lookup"><span data-stu-id="6ef13-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="6ef13-119">Örnek 3: bir VMSS sanal makinesinin örnek görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="6ef13-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzureRmVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="6ef13-120">Bu komut, Group002 adındaki kaynak grubuna ait olan VMSS004 adındaki VMSS sanal makinesinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="6ef13-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="6ef13-121">Komut, *InstanceView* Switch parametresini belirttiğinden cmdlet sanal makinenin örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="6ef13-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="6ef13-122">Komut, örnek görünümünün alınacağı değişken $ID depolanan örnek KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="6ef13-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="6ef13-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ef13-123">PARAMETERS</span></span>

### <span data-ttu-id="6ef13-124">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="6ef13-124">-InstanceId</span></span>
<span data-ttu-id="6ef13-125">Model görünümünün alınacağı örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ef13-125">Specifies the instance ID for which to get the model view.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ef13-126">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="6ef13-126">-InstanceView</span></span>
<span data-ttu-id="6ef13-127">Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ef13-127">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ef13-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ef13-128">-ResourceGroupName</span></span>
<span data-ttu-id="6ef13-129">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ef13-129">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="6ef13-130">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6ef13-130">-VMScaleSetName</span></span>
<span data-ttu-id="6ef13-131">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="6ef13-131">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="6ef13-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ef13-132">CommonParameters</span></span>
<span data-ttu-id="6ef13-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ef13-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ef13-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ef13-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ef13-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ef13-135">INPUTS</span></span>

### <span data-ttu-id="6ef13-136">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6ef13-136">None</span></span>
<span data-ttu-id="6ef13-137">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6ef13-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6ef13-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ef13-138">OUTPUTS</span></span>

### <span data-ttu-id="6ef13-139">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="6ef13-139">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="6ef13-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ef13-140">NOTES</span></span>

## <span data-ttu-id="6ef13-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ef13-141">RELATED LINKS</span></span>

[<span data-ttu-id="6ef13-142">Set-AzureRmVmssVM</span><span class="sxs-lookup"><span data-stu-id="6ef13-142">Set-AzureRmVmssVM</span></span>](./Set-AzureRmVmssVM.md)

[<span data-ttu-id="6ef13-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="6ef13-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


