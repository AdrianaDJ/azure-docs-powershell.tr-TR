---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azvmssinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzVmssInstance.md
ms.openlocfilehash: f7adb9ef086b233d44f2e5d9c6eb132669b102e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108104"
---
# <span data-ttu-id="6595e-101">Update-AzVmssInstance</span><span class="sxs-lookup"><span data-stu-id="6595e-101">Update-AzVmssInstance</span></span>

## <span data-ttu-id="6595e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6595e-102">SYNOPSIS</span></span>
<span data-ttu-id="6595e-103">VMSS örneğinin el ile yükseltilmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="6595e-103">Starts a manual upgrade of the VMSS instance.</span></span>

## <span data-ttu-id="6595e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6595e-104">SYNTAX</span></span>

```
Update-AzVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6595e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6595e-105">DESCRIPTION</span></span>
<span data-ttu-id="6595e-106">Update-AzVmssInstance cmdlet 'i, belirtilen sanal makine ölçek kümesi (VMSS) örneğinin el ile yükseltilmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="6595e-106">The Update-AzVmssInstance cmdlet starts a manual upgrade of the specified Virtual Machine Scale Set (VMSS) instance.</span></span>
<span data-ttu-id="6595e-107">Bu, VMSS ölçek kümesindeki yükseltme ilkesi el ile olarak ayarlandığında kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6595e-107">This is used when the upgrade policy on the VMSS Scale Set is set to manual.</span></span>

## <span data-ttu-id="6595e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6595e-108">EXAMPLES</span></span>

### <span data-ttu-id="6595e-109">Örnek 1: VMSS örneğinin yükseltmesini başlatma</span><span class="sxs-lookup"><span data-stu-id="6595e-109">Example 1: Start an upgrade of the VMSS instance</span></span>
```
PS C:\> Update-AzVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

<span data-ttu-id="6595e-110">Bu komut, VMScaleSet001 adında, örnek KIMLIĞI 0 olan bir yükseltme başlatır.</span><span class="sxs-lookup"><span data-stu-id="6595e-110">This command starts an upgrade of the VMSS named VMScaleSet001 that has the instance ID of 0.</span></span>

## <span data-ttu-id="6595e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6595e-111">PARAMETERS</span></span>

### <span data-ttu-id="6595e-112">-Iş</span><span class="sxs-lookup"><span data-stu-id="6595e-112">-AsJob</span></span>
<span data-ttu-id="6595e-113">Arka planda cmdlet 'i çalıştırın ve ilerlemeyi izlemek için bir Iş dönün.</span><span class="sxs-lookup"><span data-stu-id="6595e-113">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6595e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6595e-114">-DefaultProfile</span></span>
<span data-ttu-id="6595e-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6595e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6595e-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="6595e-116">-InstanceId</span></span>
<span data-ttu-id="6595e-117">Bir dize dizisi, Yükseltilecek olan Örneğin KIMLIĞINI veya kimliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6595e-117">Specifies, as a string array, the ID or IDs of the instance to upgrade.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6595e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6595e-118">-ResourceGroupName</span></span>
<span data-ttu-id="6595e-119">VMSS 'nin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6595e-119">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="6595e-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="6595e-120">-VMScaleSetName</span></span>
<span data-ttu-id="6595e-121">Bu cmdlet 'in yükseltmelerine sahip VMSS örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6595e-121">Specifies the name of the VMSS instance that this cmdlet upgrades.</span></span>

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

### <span data-ttu-id="6595e-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="6595e-122">-Confirm</span></span>
<span data-ttu-id="6595e-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6595e-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6595e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6595e-124">-WhatIf</span></span>
<span data-ttu-id="6595e-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6595e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6595e-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6595e-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6595e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6595e-127">CommonParameters</span></span>
<span data-ttu-id="6595e-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6595e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6595e-129">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6595e-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6595e-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6595e-130">INPUTS</span></span>

### <span data-ttu-id="6595e-131">System. String</span><span class="sxs-lookup"><span data-stu-id="6595e-131">System.String</span></span>

### <span data-ttu-id="6595e-132">System. String []</span><span class="sxs-lookup"><span data-stu-id="6595e-132">System.String[]</span></span>

## <span data-ttu-id="6595e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6595e-133">OUTPUTS</span></span>

### <span data-ttu-id="6595e-134">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. Psoperationdurumresponse</span><span class="sxs-lookup"><span data-stu-id="6595e-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6595e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6595e-135">NOTES</span></span>

## <span data-ttu-id="6595e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6595e-136">RELATED LINKS</span></span>

[<span data-ttu-id="6595e-137">Güncelleştirme-AzVmss</span><span class="sxs-lookup"><span data-stu-id="6595e-137">Update-AzVmss</span></span>](./Update-AzVmss.md)


