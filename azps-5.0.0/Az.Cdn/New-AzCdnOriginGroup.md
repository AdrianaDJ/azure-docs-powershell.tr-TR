---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276263"
---
# <span data-ttu-id="42534-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="42534-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="42534-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42534-102">SYNOPSIS</span></span>
<span data-ttu-id="42534-103">Yeni bir CDN kaynak grubu oluşturur</span><span class="sxs-lookup"><span data-stu-id="42534-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="42534-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42534-104">SYNTAX</span></span>

### <span data-ttu-id="42534-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42534-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="42534-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42534-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42534-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="42534-107">DESCRIPTION</span></span>
<span data-ttu-id="42534-108">New-AzCdnOriginGroup belirtilen uç noktada yeni bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42534-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="42534-109">Bu, son nokta için ilk başlangıç grubmuyorsa, DefaultOriginGroup özelliğinin de ayarlanması gerekir.</span><span class="sxs-lookup"><span data-stu-id="42534-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="42534-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42534-110">EXAMPLES</span></span>

### <span data-ttu-id="42534-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="42534-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="42534-112">Bu cmdlet, belirtilen uç nokta içinde yeni bir kaynak grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="42534-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="42534-113">Bu, verilen kaynak kimliklerini kaynak kümesi olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="42534-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="42534-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42534-114">PARAMETERS</span></span>

### <span data-ttu-id="42534-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="42534-115">-CdnOriginGroup</span></span>
<span data-ttu-id="42534-116">CDN kaynak grubu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="42534-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="42534-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42534-117">-DefaultProfile</span></span>
<span data-ttu-id="42534-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="42534-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42534-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="42534-119">-EndpointName</span></span>
<span data-ttu-id="42534-120">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="42534-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="42534-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="42534-121">-OriginGroupName</span></span>
<span data-ttu-id="42534-122">Azure CDN kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="42534-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="42534-123">-OriginalID</span><span class="sxs-lookup"><span data-stu-id="42534-123">-OriginId</span></span>
<span data-ttu-id="42534-124">Azure CDN kaynak grup kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="42534-124">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42534-125">-Probeıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="42534-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="42534-126">Sağlık sondaları arasındaki saniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="42534-126">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42534-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="42534-127">-ProbePath</span></span>
<span data-ttu-id="42534-128">Origin 'in durumunu belirlemek için kullanılan kaynağa göre yol.</span><span class="sxs-lookup"><span data-stu-id="42534-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42534-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="42534-129">-ProbeProtocol</span></span>
<span data-ttu-id="42534-130">Sistem durumu araştırması için kullanılacak protokol.</span><span class="sxs-lookup"><span data-stu-id="42534-130">Protocol to use for health probe.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42534-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="42534-131">-ProbeRequestType</span></span>
<span data-ttu-id="42534-132">Kurulan durum araştırma isteği türü.</span><span class="sxs-lookup"><span data-stu-id="42534-132">The type of health probe request that is made.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42534-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="42534-133">-ProfileName</span></span>
<span data-ttu-id="42534-134">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="42534-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="42534-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42534-135">-ResourceGroupName</span></span>
<span data-ttu-id="42534-136">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="42534-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="42534-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="42534-137">-Confirm</span></span>
<span data-ttu-id="42534-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="42534-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42534-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42534-139">-WhatIf</span></span>
<span data-ttu-id="42534-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="42534-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="42534-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="42534-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42534-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42534-142">CommonParameters</span></span>
<span data-ttu-id="42534-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42534-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42534-144">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="42534-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42534-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42534-145">INPUTS</span></span>

### <span data-ttu-id="42534-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="42534-146">System.Object</span></span>

## <span data-ttu-id="42534-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42534-147">OUTPUTS</span></span>

### <span data-ttu-id="42534-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="42534-148">System.Object</span></span>

## <span data-ttu-id="42534-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42534-149">NOTES</span></span>

## <span data-ttu-id="42534-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42534-150">RELATED LINKS</span></span>
