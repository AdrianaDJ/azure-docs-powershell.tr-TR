---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: 93c70344b2a5ce9f03e4b0c1088fa785989912da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917204"
---
# <span data-ttu-id="435a3-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="435a3-101">Start-AzVmss</span></span>

## <span data-ttu-id="435a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="435a3-102">SYNOPSIS</span></span>
<span data-ttu-id="435a3-103">VMSS 'yi veya VMSS içinde bir dizi sanal makineyi başlatır.</span><span class="sxs-lookup"><span data-stu-id="435a3-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="435a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="435a3-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="435a3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="435a3-105">DESCRIPTION</span></span>
<span data-ttu-id="435a3-106">**Start-AzVmss** cmdlet 'ı sanal makine ölçek KÜMESI (VMSS) içindeki tüm sanal makineleri veya sanal makineler kümesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="435a3-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="435a3-107">*InstanceId* parametresini kullanarak bir sanal makine kümesi seçebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="435a3-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="435a3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="435a3-108">EXAMPLES</span></span>

### <span data-ttu-id="435a3-109">Örnek 1: VMSS içinde belirli bir sanal makine kümesini başlatma</span><span class="sxs-lookup"><span data-stu-id="435a3-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="435a3-110">Bu komut, ContosoVMSS adlı VMSS 'ye ait örnek KIMLIĞI dizesi dizisiyle belirtilen belirli bir sanal makine kümesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="435a3-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="435a3-111">Örnek 2: VMSS içindeki tüm sanal makineleri başlatma</span><span class="sxs-lookup"><span data-stu-id="435a3-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="435a3-112">Bu komut, ContosoVMSS adlı VMSS 'ye ait tüm sanal makineleri başlatır.</span><span class="sxs-lookup"><span data-stu-id="435a3-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="435a3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="435a3-113">PARAMETERS</span></span>

### <span data-ttu-id="435a3-114">-Iş</span><span class="sxs-lookup"><span data-stu-id="435a3-114">-AsJob</span></span>
<span data-ttu-id="435a3-115">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="435a3-115">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="435a3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="435a3-116">-DefaultProfile</span></span>
<span data-ttu-id="435a3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="435a3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="435a3-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="435a3-118">-InstanceId</span></span>
<span data-ttu-id="435a3-119">Cmdlet 'in başladığı örneklerin KIMLIĞINI veya kimliklerini dize dizisi olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="435a3-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="435a3-120">Örneğin: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="435a3-120">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="435a3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="435a3-121">-ResourceGroupName</span></span>
<span data-ttu-id="435a3-122">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="435a3-122">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="435a3-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="435a3-123">-VMScaleSetName</span></span>
<span data-ttu-id="435a3-124">Bu cmdlet 'in sanal makineleri Başlatan VMSS adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="435a3-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="435a3-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="435a3-125">-Confirm</span></span>
<span data-ttu-id="435a3-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="435a3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="435a3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="435a3-127">-WhatIf</span></span>
<span data-ttu-id="435a3-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="435a3-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="435a3-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="435a3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="435a3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="435a3-130">CommonParameters</span></span>
<span data-ttu-id="435a3-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="435a3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="435a3-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="435a3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="435a3-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="435a3-133">INPUTS</span></span>

### <span data-ttu-id="435a3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="435a3-134">System.String</span></span>

### <span data-ttu-id="435a3-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="435a3-135">System.String[]</span></span>

## <span data-ttu-id="435a3-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="435a3-136">OUTPUTS</span></span>

### <span data-ttu-id="435a3-137">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="435a3-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="435a3-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="435a3-138">NOTES</span></span>

## <span data-ttu-id="435a3-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="435a3-139">RELATED LINKS</span></span>

[<span data-ttu-id="435a3-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="435a3-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="435a3-141">Yeni-AzVmss</span><span class="sxs-lookup"><span data-stu-id="435a3-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="435a3-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="435a3-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="435a3-143">Restart-AzVmss</span><span class="sxs-lookup"><span data-stu-id="435a3-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="435a3-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="435a3-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="435a3-145">Dur-AzVmss</span><span class="sxs-lookup"><span data-stu-id="435a3-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="435a3-146">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="435a3-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


