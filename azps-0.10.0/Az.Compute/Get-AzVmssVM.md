---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 43c6f96556cb283ef21f24df00d6a6ddb9c5397a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936994"
---
# <span data-ttu-id="cf14f-101">Get-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="cf14f-101">Get-AzVmssVM</span></span>

## <span data-ttu-id="cf14f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf14f-102">SYNOPSIS</span></span>
<span data-ttu-id="cf14f-103">Bir VMSS sanal makinesinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="cf14f-103">Gets the properties of a VMSS virtual machine.</span></span>

## <span data-ttu-id="cf14f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cf14f-104">SYNTAX</span></span>

### <span data-ttu-id="cf14f-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cf14f-105">DefaultParameter (Default)</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf14f-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="cf14f-106">FriendMethod</span></span>
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf14f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="cf14f-107">DESCRIPTION</span></span>
<span data-ttu-id="cf14f-108">**Get-AzVmssVM** cmdlet 'ı sanal makine ölçeği KÜMESI (VMSS) sanal makinesinin model görünümünü ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="cf14f-108">The **Get-AzVmssVM** cmdlet gets the model view and instance view of a Virtual Machine Scale Set (VMSS) virtual machine.</span></span>
<span data-ttu-id="cf14f-109">Model görünümü, Kullanıcı tarafından belirtilen sanal makinenin özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="cf14f-109">The model view is the user specified properties of the virtual machine.</span></span>
<span data-ttu-id="cf14f-110">Örnek görünümü sanal makinenin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="cf14f-110">The instance view is the instance level status of the virtual machine.</span></span>
<span data-ttu-id="cf14f-111">Bir sanal makinenin yalnızca örnek görünümüne ulaşmak için *durum* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="cf14f-111">Specify the *Status* parameter to get only the instance view of a virtual machine.</span></span>

## <span data-ttu-id="cf14f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cf14f-112">EXAMPLES</span></span>

### <span data-ttu-id="cf14f-113">Örnek 1: VMSS sanal makinesinin özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="cf14f-113">Example 1: Get the properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="cf14f-114">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS sanal makinesinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="cf14f-114">This command gets the properties of the VMSS virtual machine named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="cf14f-115">Komut, *InstanceView* anahtar parametresini belirtmediğinden, cmdlet sanal makinenin model görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="cf14f-115">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine.</span></span>

### <span data-ttu-id="cf14f-116">Örnek 2: bir VMSS sanal makinesinin model görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="cf14f-116">Example 2: Get the model view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

<span data-ttu-id="cf14f-117">Bu komut, Group002 adındaki kaynak grubuna ait olan VMSS004 adındaki VMSS sanal makinesinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="cf14f-117">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="cf14f-118">Bu komut, $ID değişkeninde depolanan örnek KIMLIĞINI model görünümünün alınacağı şekilde alır.</span><span class="sxs-lookup"><span data-stu-id="cf14f-118">The command gets the instance ID stored in the variable $ID for which to get the model view.</span></span>

### <span data-ttu-id="cf14f-119">Örnek 3: bir VMSS sanal makinesinin örnek görünümü özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="cf14f-119">Example 3: Get the instance view properties of a VMSS virtual machine</span></span>
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

<span data-ttu-id="cf14f-120">Bu komut, Group002 adındaki kaynak grubuna ait olan VMSS004 adındaki VMSS sanal makinesinin özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="cf14f-120">This command gets the properties of the VMSS virtual machine named VMSS004 that belongs to the resource group named Group002.</span></span>
<span data-ttu-id="cf14f-121">Komut, *InstanceView* Switch parametresini belirttiğinden cmdlet sanal makinenin örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="cf14f-121">Since the command specifies the *InstanceView* switch parameter, the cmdlet gets the instance view of the virtual machine.</span></span>
<span data-ttu-id="cf14f-122">Komut, örnek görünümünün alınacağı değişken $ID depolanan örnek KIMLIĞINI alır.</span><span class="sxs-lookup"><span data-stu-id="cf14f-122">The command gets the instance ID stored in the variable $ID for which to get the instance view.</span></span>

## <span data-ttu-id="cf14f-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cf14f-123">PARAMETERS</span></span>

### <span data-ttu-id="cf14f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf14f-124">-DefaultProfile</span></span>
<span data-ttu-id="cf14f-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cf14f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf14f-126">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="cf14f-126">-InstanceId</span></span>
<span data-ttu-id="cf14f-127">Model görünümünün alınacağı örnek KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf14f-127">Specifies the instance ID for which to get the model view.</span></span>

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

### <span data-ttu-id="cf14f-128">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="cf14f-128">-InstanceView</span></span>
<span data-ttu-id="cf14f-129">Bu cmdlet 'in yalnızca sanal makinenin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cf14f-129">Indicates that this cmdlet gets only the instance view of the virtual machine.</span></span>

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

### <span data-ttu-id="cf14f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf14f-130">-ResourceGroupName</span></span>
<span data-ttu-id="cf14f-131">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cf14f-131">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="cf14f-132">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="cf14f-132">-VMScaleSetName</span></span>
<span data-ttu-id="cf14f-133">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="cf14f-133">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="cf14f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf14f-134">CommonParameters</span></span>
<span data-ttu-id="cf14f-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cf14f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf14f-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf14f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf14f-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cf14f-137">INPUTS</span></span>

### <span data-ttu-id="cf14f-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cf14f-138">None</span></span>
<span data-ttu-id="cf14f-139">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cf14f-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cf14f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cf14f-140">OUTPUTS</span></span>

### <span data-ttu-id="cf14f-141">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="cf14f-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="cf14f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cf14f-142">NOTES</span></span>

## <span data-ttu-id="cf14f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cf14f-143">RELATED LINKS</span></span>

[<span data-ttu-id="cf14f-144">Set-AzVmssVM</span><span class="sxs-lookup"><span data-stu-id="cf14f-144">Set-AzVmssVM</span></span>](./Set-AzVmssVM.md)

[<span data-ttu-id="cf14f-145">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cf14f-145">Get-AzVmss</span></span>](./Get-AzVmss.md)


