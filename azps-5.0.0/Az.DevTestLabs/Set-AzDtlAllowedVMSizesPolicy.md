---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: d5e8b16fec390c4b4d900760d3efb60abfb7da0e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275543"
---
# <span data-ttu-id="81c9d-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="81c9d-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="81c9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="81c9d-103">DevTest laboratuvarlarında bir laboratuvarın izin verilen sanal makine boyutları ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="81c9d-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="81c9d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81c9d-104">SYNTAX</span></span>

### <span data-ttu-id="81c9d-105">Etkinleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="81c9d-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="81c9d-106">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="81c9d-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="81c9d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="81c9d-107">DESCRIPTION</span></span>
<span data-ttu-id="81c9d-108">**Set-AzDtlAllowedVMSizesPolicy** cmdlet 'i, bir laboratuvarda izin verilen sanal makine boyutlarının listesini belirten izin verilen sanal makine boyutları ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="81c9d-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="81c9d-109">Cmdlet, ilkeyi ayarlamak için belirtilen kaynak grubunu ve laboratuarın adını kullanır.</span><span class="sxs-lookup"><span data-stu-id="81c9d-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="81c9d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81c9d-110">EXAMPLES</span></span>

## <span data-ttu-id="81c9d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81c9d-111">PARAMETERS</span></span>

### <span data-ttu-id="81c9d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c9d-112">-DefaultProfile</span></span>
<span data-ttu-id="81c9d-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="81c9d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81c9d-114">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="81c9d-114">-Disable</span></span>
<span data-ttu-id="81c9d-115">Bu cmdlet 'in ilkeyi devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81c9d-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c9d-116">-Enable</span><span class="sxs-lookup"><span data-stu-id="81c9d-116">-Enable</span></span>
<span data-ttu-id="81c9d-117">Bu cmdlet 'in ilkeyi etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c9d-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c9d-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="81c9d-118">-LabName</span></span>
<span data-ttu-id="81c9d-119">Bu cmdlet 'in sanal makine boyutları ilkesini ayarladığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c9d-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="81c9d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81c9d-120">-ResourceGroupName</span></span>
<span data-ttu-id="81c9d-121">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c9d-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="81c9d-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="81c9d-122">-VmSizes</span></span>
<span data-ttu-id="81c9d-123">Bir dize dizisi olarak, laboratuvarda izin verilen sanal makine boyutlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="81c9d-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c9d-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="81c9d-124">-Confirm</span></span>
<span data-ttu-id="81c9d-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="81c9d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c9d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c9d-126">-WhatIf</span></span>
<span data-ttu-id="81c9d-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="81c9d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81c9d-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="81c9d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81c9d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c9d-129">CommonParameters</span></span>
<span data-ttu-id="81c9d-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81c9d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c9d-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81c9d-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c9d-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81c9d-132">INPUTS</span></span>

### <span data-ttu-id="81c9d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="81c9d-133">System.String</span></span>

## <span data-ttu-id="81c9d-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81c9d-134">OUTPUTS</span></span>

### <span data-ttu-id="81c9d-135">Microsoft. Azure. Commands. DevTestLabs. model. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="81c9d-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="81c9d-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81c9d-136">NOTES</span></span>

## <span data-ttu-id="81c9d-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81c9d-137">RELATED LINKS</span></span>

[<span data-ttu-id="81c9d-138">Get-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="81c9d-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


