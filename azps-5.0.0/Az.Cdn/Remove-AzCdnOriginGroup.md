---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279095"
---
# <span data-ttu-id="e622f-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="e622f-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="e622f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e622f-102">SYNOPSIS</span></span>
<span data-ttu-id="e622f-103">CDN kaynak grubunu kaldırır</span><span class="sxs-lookup"><span data-stu-id="e622f-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="e622f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e622f-104">SYNTAX</span></span>

### <span data-ttu-id="e622f-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e622f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e622f-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e622f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e622f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e622f-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e622f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e622f-108">DESCRIPTION</span></span>
<span data-ttu-id="e622f-109">Remove-AzCdnOriginGroup, belirtilen uç noktadan CDN kaynak grubunu kaldıracak.</span><span class="sxs-lookup"><span data-stu-id="e622f-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="e622f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e622f-110">EXAMPLES</span></span>

### <span data-ttu-id="e622f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e622f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="e622f-112">Bu cmdlet belirtilen kaynak grubu belirtilen uç noktasından kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e622f-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="e622f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e622f-113">PARAMETERS</span></span>

### <span data-ttu-id="e622f-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="e622f-114">-CdnOriginGroup</span></span>
<span data-ttu-id="e622f-115">CDN kaynak grubu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e622f-115">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e622f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e622f-116">-DefaultProfile</span></span>
<span data-ttu-id="e622f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e622f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e622f-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e622f-118">-EndpointName</span></span>
<span data-ttu-id="e622f-119">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="e622f-119">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e622f-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="e622f-120">-OriginGroupName</span></span>
<span data-ttu-id="e622f-121">Azure CDN kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e622f-121">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e622f-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="e622f-122">-PassThru</span></span>
<span data-ttu-id="e622f-123">Belirtilmişse nesneyi döndür.</span><span class="sxs-lookup"><span data-stu-id="e622f-123">Return object if specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e622f-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e622f-124">-ProfileName</span></span>
<span data-ttu-id="e622f-125">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="e622f-125">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e622f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e622f-126">-ResourceGroupName</span></span>
<span data-ttu-id="e622f-127">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="e622f-127">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e622f-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e622f-128">-ResourceId</span></span>
<span data-ttu-id="e622f-129">Azure CDN kaynak grubunun kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="e622f-129">The resource id of the Azure CDN origin group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e622f-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="e622f-130">-Confirm</span></span>
<span data-ttu-id="e622f-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e622f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e622f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e622f-132">-WhatIf</span></span>
<span data-ttu-id="e622f-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e622f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e622f-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e622f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e622f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e622f-135">CommonParameters</span></span>
<span data-ttu-id="e622f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e622f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e622f-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e622f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e622f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e622f-138">INPUTS</span></span>

### <span data-ttu-id="e622f-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e622f-139">None</span></span>

## <span data-ttu-id="e622f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e622f-140">OUTPUTS</span></span>

### <span data-ttu-id="e622f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e622f-141">System.Boolean</span></span>

## <span data-ttu-id="e622f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e622f-142">NOTES</span></span>

## <span data-ttu-id="e622f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e622f-143">RELATED LINKS</span></span>
