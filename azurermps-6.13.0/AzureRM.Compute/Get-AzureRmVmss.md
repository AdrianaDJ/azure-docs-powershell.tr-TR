---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: FC6BC096-DBC4-48DA-A366-B87EB18A0496
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmss.md
ms.openlocfilehash: d2e9ad0d83c573292996b65924ab7078368d328f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763907"
---
# <span data-ttu-id="f962e-101">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f962e-101">Get-AzureRmVmss</span></span>

## <span data-ttu-id="f962e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f962e-102">SYNOPSIS</span></span>
<span data-ttu-id="f962e-103">Bir VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="f962e-103">Gets the properties of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f962e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f962e-104">SYNTAX</span></span>

### <span data-ttu-id="f962e-105">DefaultParameter (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f962e-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f962e-106">Kolay Yöntem</span><span class="sxs-lookup"><span data-stu-id="f962e-106">FriendMethod</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-InstanceView]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f962e-107">Osupgrade, Methodparameter</span><span class="sxs-lookup"><span data-stu-id="f962e-107">OSUpgradeHistoryMethodParameter</span></span>
```
Get-AzureRmVmss [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [-OSUpgradeHistory]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f962e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f962e-108">DESCRIPTION</span></span>
<span data-ttu-id="f962e-109">**Get-AzureRmVmss** cmdlet 'ı sanal makine ölçek kümesinin (VMSS) modelini ve örnek görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="f962e-109">The **Get-AzureRmVmss** cmdlet gets the model and instance view of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f962e-110">Model görünümü, kullanıcının belirttiği sanal makine ölçeği kümesi özellikleridir.</span><span class="sxs-lookup"><span data-stu-id="f962e-110">The model view is the user specified properties of the virtual machine scale set.</span></span>
<span data-ttu-id="f962e-111">Örnek görünümü, sanal makine ölçek kümesinin örnek düzeyi durumudur.</span><span class="sxs-lookup"><span data-stu-id="f962e-111">The instance view is the instance level status of the virtual machine scale set.</span></span>
<span data-ttu-id="f962e-112">Yalnızca sanal makine ölçek kümesinin örnek görünümünü almak için *InstanceView* parametresini belirtin.</span><span class="sxs-lookup"><span data-stu-id="f962e-112">Specify the *InstanceView* parameter to get only the instance view of a virtual machine scale set.</span></span>

## <span data-ttu-id="f962e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f962e-113">EXAMPLES</span></span>

### <span data-ttu-id="f962e-114">Örnek 1: bir VMSS özelliklerini alma</span><span class="sxs-lookup"><span data-stu-id="f962e-114">Example 1: Get the properties of a VMSS</span></span>
```
PS C:\> Get-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

<span data-ttu-id="f962e-115">Bu komut, Group001 adındaki kaynak grubuna ait olan VMSS001 adındaki VMSS özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="f962e-115">This command gets the properties of the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>
<span data-ttu-id="f962e-116">Komut, *InstanceView* anahtar parametresini belirtmediğinden, cmdlet sanal makine ölçek kümesinin model görünümünü alır.</span><span class="sxs-lookup"><span data-stu-id="f962e-116">Since the command does not specify the *InstanceView* switch parameter, the cmdlet gets the model view of the virtual machine scale set.</span></span>

## <span data-ttu-id="f962e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f962e-117">PARAMETERS</span></span>

### <span data-ttu-id="f962e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f962e-118">-DefaultProfile</span></span>
<span data-ttu-id="f962e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f962e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f962e-120">-InstanceView</span><span class="sxs-lookup"><span data-stu-id="f962e-120">-InstanceView</span></span>
<span data-ttu-id="f962e-121">Bu cmdlet 'in yalnızca sanal makine ölçek kümesinin örnek görünümünü aldığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f962e-121">Indicates that this cmdlet gets only the instance view of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="f962e-122">-Osupın geçmiş</span><span class="sxs-lookup"><span data-stu-id="f962e-122">-OSUpgradeHistory</span></span>
<span data-ttu-id="f962e-123">Bu cmdlet 'in sanal makine ölçek kümesinin işletim sistemi yükseltme geçmişini listediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f962e-123">Indicates that this cmdlet lists the os upgrade history of the virtual machine scale set.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: OSUpgradeHistoryMethodParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f962e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f962e-124">-ResourceGroupName</span></span>
<span data-ttu-id="f962e-125">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f962e-125">Specifies the name of the Resource Group of the VMSS.</span></span>

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

### <span data-ttu-id="f962e-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f962e-126">-VMScaleSetName</span></span>
<span data-ttu-id="f962e-127">Türleri, VMSS 'nin adını.</span><span class="sxs-lookup"><span data-stu-id="f962e-127">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="f962e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f962e-128">CommonParameters</span></span>
<span data-ttu-id="f962e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f962e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f962e-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f962e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f962e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f962e-131">INPUTS</span></span>

### <span data-ttu-id="f962e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f962e-132">System.String</span></span>

## <span data-ttu-id="f962e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f962e-133">OUTPUTS</span></span>

### <span data-ttu-id="f962e-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f962e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f962e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f962e-135">NOTES</span></span>

## <span data-ttu-id="f962e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f962e-136">RELATED LINKS</span></span>

[<span data-ttu-id="f962e-137">Yeni-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f962e-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="f962e-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f962e-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="f962e-139">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f962e-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="f962e-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f962e-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="f962e-141">Başlangıç-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f962e-141">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="f962e-142">Dur-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f962e-142">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="f962e-143">Güncelleştirme-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="f962e-143">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


