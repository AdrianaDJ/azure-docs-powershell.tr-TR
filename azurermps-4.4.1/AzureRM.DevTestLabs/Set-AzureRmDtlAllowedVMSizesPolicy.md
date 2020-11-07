---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 8248c5ef5e4de2ab945d7f5f39dd4eea6defdf8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763738"
---
# <span data-ttu-id="7f1ab-101">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="7f1ab-101">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="7f1ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="7f1ab-103">DevTest laboratuvarlarında bir laboratuvarın izin verilen sanal makine boyutları ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f1ab-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f1ab-104">SYNTAX</span></span>

### <span data-ttu-id="7f1ab-105">Etkinleştir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7f1ab-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7f1ab-106">Bırakılacağı</span><span class="sxs-lookup"><span data-stu-id="7f1ab-106">Disable</span></span>
```
Set-AzureRmDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f1ab-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f1ab-107">DESCRIPTION</span></span>
<span data-ttu-id="7f1ab-108">**Set-AzureRmDtlAllowedVMSizesPolicy** cmdlet 'i, bir laboratuvarda izin verilen sanal makine boyutlarının listesini belirten izin verilen sanal makine boyutları ilkesini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-108">The **Set-AzureRmDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="7f1ab-109">Cmdlet, ilkeyi ayarlamak için belirtilen kaynak grubunu ve laboratuarın adını kullanır.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="7f1ab-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f1ab-110">EXAMPLES</span></span>

## <span data-ttu-id="7f1ab-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f1ab-111">PARAMETERS</span></span>

### <span data-ttu-id="7f1ab-112">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="7f1ab-112">-Disable</span></span>
<span data-ttu-id="7f1ab-113">Bu cmdlet 'in ilkeyi devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-113">Indicates that this cmdlet disables the policy.</span></span>

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

### <span data-ttu-id="7f1ab-114">-Enable</span><span class="sxs-lookup"><span data-stu-id="7f1ab-114">-Enable</span></span>
<span data-ttu-id="7f1ab-115">Bu cmdlet 'in ilkeyi etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-115">Indicates that this cmdlet enables the policy.</span></span>

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

### <span data-ttu-id="7f1ab-116">-LabName</span><span class="sxs-lookup"><span data-stu-id="7f1ab-116">-LabName</span></span>
<span data-ttu-id="7f1ab-117">Bu cmdlet 'in sanal makine boyutları ilkesini ayarladığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-117">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="7f1ab-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f1ab-118">-ResourceGroupName</span></span>
<span data-ttu-id="7f1ab-119">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-119">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="7f1ab-120">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="7f1ab-120">-VmSizes</span></span>
<span data-ttu-id="7f1ab-121">Bir dize dizisi olarak, laboratuvarda izin verilen sanal makine boyutlarının listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-121">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

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

### <span data-ttu-id="7f1ab-122">-Onay</span><span class="sxs-lookup"><span data-stu-id="7f1ab-122">-Confirm</span></span>
<span data-ttu-id="7f1ab-123">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f1ab-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f1ab-124">-WhatIf</span></span>
<span data-ttu-id="7f1ab-125">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f1ab-126">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f1ab-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f1ab-127">-DefaultProfile</span></span>
<span data-ttu-id="7f1ab-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f1ab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f1ab-129">CommonParameters</span></span>
<span data-ttu-id="7f1ab-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f1ab-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f1ab-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f1ab-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f1ab-132">INPUTS</span></span>

## <span data-ttu-id="7f1ab-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f1ab-133">OUTPUTS</span></span>

### <span data-ttu-id="7f1ab-134">Microsoft. Azure. Commands. DevTestLabs. model. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="7f1ab-134">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="7f1ab-135">Bu cmdlet, laboratuvarda izin verilen sanal makine boyutlarının listesini belirten ilkeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="7f1ab-135">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="7f1ab-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f1ab-136">NOTES</span></span>

## <span data-ttu-id="7f1ab-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f1ab-137">RELATED LINKS</span></span>

[<span data-ttu-id="7f1ab-138">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="7f1ab-138">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Get-AzureRmDtlAllowedVMSizesPolicy.md)

