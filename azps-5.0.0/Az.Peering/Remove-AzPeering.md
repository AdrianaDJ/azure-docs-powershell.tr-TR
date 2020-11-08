---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: 414a732dd80850a31a87f88d3dfdbf091cb4a6a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279185"
---
# <span data-ttu-id="a7c70-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="a7c70-101">Remove-AzPeering</span></span>

## <span data-ttu-id="a7c70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7c70-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c70-103">Eşlemeyi silme veya kaldırma.</span><span class="sxs-lookup"><span data-stu-id="a7c70-103">Delete or remove a peering.</span></span> <span data-ttu-id="a7c70-104">Bu işlem, kaynaktaki tüm alt kaynakları veya bir uyarı silecek.</span><span class="sxs-lookup"><span data-stu-id="a7c70-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="a7c70-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7c70-105">SYNTAX</span></span>

### <span data-ttu-id="a7c70-106">ByName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7c70-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7c70-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="a7c70-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7c70-108">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="a7c70-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7c70-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7c70-109">DESCRIPTION</span></span>
<span data-ttu-id="a7c70-110">Bir eşleme kaynağını silme.</span><span class="sxs-lookup"><span data-stu-id="a7c70-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="a7c70-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7c70-111">EXAMPLES</span></span>

### <span data-ttu-id="a7c70-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7c70-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="a7c70-113">Kaynak kimliğiyle bir eşlemeyi kaldırma.</span><span class="sxs-lookup"><span data-stu-id="a7c70-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="a7c70-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7c70-114">PARAMETERS</span></span>

### <span data-ttu-id="a7c70-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="a7c70-115">-AsJob</span></span>
<span data-ttu-id="a7c70-116">Arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="a7c70-116">Run in the background.</span></span>

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

### <span data-ttu-id="a7c70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7c70-117">-DefaultProfile</span></span>
<span data-ttu-id="a7c70-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7c70-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7c70-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a7c70-119">-Force</span></span>
<span data-ttu-id="a7c70-120">İşlemin tamamlamasını zorunlu kılın</span><span class="sxs-lookup"><span data-stu-id="a7c70-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="a7c70-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7c70-121">-InputObject</span></span>
<span data-ttu-id="a7c70-122">Bu nesneyi almak için Get-AzPeering kullanın.</span><span class="sxs-lookup"><span data-stu-id="a7c70-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c70-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7c70-123">-Name</span></span>
<span data-ttu-id="a7c70-124">Takdirin benzersiz adı.</span><span class="sxs-lookup"><span data-stu-id="a7c70-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c70-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a7c70-125">-PassThru</span></span>
<span data-ttu-id="a7c70-126">Tamamlandığında doğru döndür</span><span class="sxs-lookup"><span data-stu-id="a7c70-126">Return true if complete</span></span>

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

### <span data-ttu-id="a7c70-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7c70-127">-ResourceGroupName</span></span>
<span data-ttu-id="a7c70-128">Var olan kaynak grubu adını oluştur veya kullan.</span><span class="sxs-lookup"><span data-stu-id="a7c70-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7c70-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a7c70-129">-ResourceId</span></span>
<span data-ttu-id="a7c70-130">Kaynak kimliği dize adı.</span><span class="sxs-lookup"><span data-stu-id="a7c70-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c70-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7c70-131">-Confirm</span></span>
<span data-ttu-id="a7c70-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7c70-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7c70-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7c70-133">-WhatIf</span></span>
<span data-ttu-id="a7c70-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7c70-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7c70-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7c70-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7c70-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c70-136">CommonParameters</span></span>
<span data-ttu-id="a7c70-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7c70-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c70-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a7c70-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c70-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7c70-139">INPUTS</span></span>

### <span data-ttu-id="a7c70-140">Microsoft. Azure. PowerShell. cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7c70-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="a7c70-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a7c70-141">System.String</span></span>

## <span data-ttu-id="a7c70-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7c70-142">OUTPUTS</span></span>

### <span data-ttu-id="a7c70-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a7c70-143">System.Boolean</span></span>

## <span data-ttu-id="a7c70-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7c70-144">NOTES</span></span>

## <span data-ttu-id="a7c70-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7c70-145">RELATED LINKS</span></span>
