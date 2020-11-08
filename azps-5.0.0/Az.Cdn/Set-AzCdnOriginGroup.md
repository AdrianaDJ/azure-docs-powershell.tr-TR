---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277639"
---
# <span data-ttu-id="1b420-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="1b420-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="1b420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b420-102">SYNOPSIS</span></span>
<span data-ttu-id="1b420-103">CDN kaynak grubunu güncelleştirir</span><span class="sxs-lookup"><span data-stu-id="1b420-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="1b420-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1b420-104">SYNTAX</span></span>

### <span data-ttu-id="1b420-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1b420-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b420-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b420-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b420-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="1b420-107">DESCRIPTION</span></span>
<span data-ttu-id="1b420-108">Set-AzCdnOriginGroup belirtilen uç nokta içinde belirtilen kaynak grubu güncelleştirecek.</span><span class="sxs-lookup"><span data-stu-id="1b420-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="1b420-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1b420-109">EXAMPLES</span></span>

### <span data-ttu-id="1b420-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1b420-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="1b420-111">Bu cmdlet, kaynak grubundaki Probeıntervalınseconds özelliğini güncelleştirecek.</span><span class="sxs-lookup"><span data-stu-id="1b420-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="1b420-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1b420-112">PARAMETERS</span></span>

### <span data-ttu-id="1b420-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="1b420-113">-CdnOriginGroup</span></span>
<span data-ttu-id="1b420-114">CDN kaynak grubu nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1b420-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="1b420-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b420-115">-DefaultProfile</span></span>
<span data-ttu-id="1b420-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1b420-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b420-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1b420-117">-EndpointName</span></span>
<span data-ttu-id="1b420-118">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="1b420-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="1b420-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="1b420-119">-OriginGroupName</span></span>
<span data-ttu-id="1b420-120">Azure CDN kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1b420-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="1b420-121">-OriginalID</span><span class="sxs-lookup"><span data-stu-id="1b420-121">-OriginId</span></span>
<span data-ttu-id="1b420-122">Azure CDN kaynak grup kimlikleri.</span><span class="sxs-lookup"><span data-stu-id="1b420-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="1b420-123">-Probeıntervalınseconds</span><span class="sxs-lookup"><span data-stu-id="1b420-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="1b420-124">Sağlık sondaları arasındaki saniye sayısı.</span><span class="sxs-lookup"><span data-stu-id="1b420-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="1b420-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="1b420-125">-ProbePath</span></span>
<span data-ttu-id="1b420-126">Origin 'in durumunu belirlemek için kullanılan kaynağa göre yol.</span><span class="sxs-lookup"><span data-stu-id="1b420-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="1b420-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="1b420-127">-ProbeProtocol</span></span>
<span data-ttu-id="1b420-128">Sistem durumu araştırması için kullanılacak protokol.</span><span class="sxs-lookup"><span data-stu-id="1b420-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="1b420-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="1b420-129">-ProbeRequestType</span></span>
<span data-ttu-id="1b420-130">Kurulan durum araştırma isteği türü.</span><span class="sxs-lookup"><span data-stu-id="1b420-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="1b420-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1b420-131">-ProfileName</span></span>
<span data-ttu-id="1b420-132">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="1b420-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="1b420-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b420-133">-ResourceGroupName</span></span>
<span data-ttu-id="1b420-134">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="1b420-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="1b420-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="1b420-135">-Confirm</span></span>
<span data-ttu-id="1b420-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1b420-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b420-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b420-137">-WhatIf</span></span>
<span data-ttu-id="1b420-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1b420-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b420-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1b420-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b420-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b420-140">CommonParameters</span></span>
<span data-ttu-id="1b420-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1b420-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b420-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="1b420-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b420-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1b420-143">INPUTS</span></span>

### <span data-ttu-id="1b420-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="1b420-144">System.Object</span></span>

## <span data-ttu-id="1b420-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1b420-145">OUTPUTS</span></span>

### <span data-ttu-id="1b420-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="1b420-146">System.Object</span></span>

## <span data-ttu-id="1b420-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1b420-147">NOTES</span></span>

## <span data-ttu-id="1b420-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1b420-148">RELATED LINKS</span></span>
