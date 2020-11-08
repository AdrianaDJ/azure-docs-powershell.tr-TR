---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOrigin.md
ms.openlocfilehash: a9ef1687333851e2ac67dfb3f0146509f3b77183
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276265"
---
# <span data-ttu-id="6dfc7-101">New-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="6dfc7-101">New-AzCdnOrigin</span></span>

## <span data-ttu-id="6dfc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dfc7-102">SYNOPSIS</span></span>
<span data-ttu-id="6dfc7-103">Yeni bir CDN kaynağı oluşturur</span><span class="sxs-lookup"><span data-stu-id="6dfc7-103">Creates a new CDN origin</span></span>

## <span data-ttu-id="6dfc7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6dfc7-104">SYNTAX</span></span>

### <span data-ttu-id="6dfc7-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6dfc7-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6dfc7-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dfc7-106">ByFieldsPrivateLinkParameterSet</span></span>
```
New-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6dfc7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dfc7-107">ByObjectParameterSet</span></span>
```
New-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6dfc7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6dfc7-108">DESCRIPTION</span></span>
<span data-ttu-id="6dfc7-109">New-AzCdnOrigin belirtilen uç noktada yeni bir CDN kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-109">The New-AzCdnOrigin will create a new CDN origin within the specified endpoint.</span></span>

## <span data-ttu-id="6dfc7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6dfc7-110">EXAMPLES</span></span>

### <span data-ttu-id="6dfc7-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6dfc7-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName -HostName $hostName
```

<span data-ttu-id="6dfc7-112">Bu cmdlet, belirtilen uç nokta için yeni bir CDN kaynağı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-112">This cmdlet will create a new CDN origin for the specified endpoint.</span></span> <span data-ttu-id="6dfc7-113">Sağlanan ana bilgisayar adını başlangıç olarak kullanır.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-113">It will use the provided hostname as the origin.</span></span> 

## <span data-ttu-id="6dfc7-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6dfc7-114">PARAMETERS</span></span>

### <span data-ttu-id="6dfc7-115">-Cdnorigın</span><span class="sxs-lookup"><span data-stu-id="6dfc7-115">-CdnOrigin</span></span>
<span data-ttu-id="6dfc7-116">CDN kaynak nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dfc7-117">-DefaultProfile</span></span>
<span data-ttu-id="6dfc7-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dfc7-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="6dfc7-119">-EndpointName</span></span>
<span data-ttu-id="6dfc7-120">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-120">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-121">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="6dfc7-121">-HostName</span></span>
<span data-ttu-id="6dfc7-122">Azure CDN kaynak ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-122">Azure CDN origin host name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-123">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="6dfc7-123">-HttpPort</span></span>
<span data-ttu-id="6dfc7-124">Azure CDN kaynak http bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-124">Azure CDN origin http port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-125">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="6dfc7-125">-HttpsPort</span></span>
<span data-ttu-id="6dfc7-126">Azure CDN başlangıç HTTPS bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-126">Azure CDN origin https port.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-127">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="6dfc7-127">-OriginHostHeader</span></span>
<span data-ttu-id="6dfc7-128">Azure CDN kaynak ana bilgisayar üst bilgisi.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-128">Azure CDN origin host header.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-129">-AdName</span><span class="sxs-lookup"><span data-stu-id="6dfc7-129">-OriginName</span></span>
<span data-ttu-id="6dfc7-130">Azure CDN kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-130">Azure CDN origin name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-131">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="6dfc7-131">-Priority</span></span>
<span data-ttu-id="6dfc7-132">Azure CDN kaynak önceliği.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-132">Azure CDN origin priority.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-133">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="6dfc7-133">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="6dfc7-134">Özel bağlantısına bağlanma onay isteğine dahil edilecek özel bir ileti.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-134">A custom message to be included in the approval request to connect to the Private Link.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-135">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="6dfc7-135">-PrivateLinkLocation</span></span>
<span data-ttu-id="6dfc7-136">Azure CDN kaynak özel bağlantı konumu.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-136">Azure CDN origin private link location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-137">-Privatelinkresourceıd</span><span class="sxs-lookup"><span data-stu-id="6dfc7-137">-PrivateLinkResourceId</span></span>
<span data-ttu-id="6dfc7-138">Azure CDN kaynak özel bağlantısı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-138">Azure CDN origin private link resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-139">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="6dfc7-139">-ProfileName</span></span>
<span data-ttu-id="6dfc7-140">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-140">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dfc7-141">-ResourceGroupName</span></span>
<span data-ttu-id="6dfc7-142">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-142">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-143">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="6dfc7-143">-Weight</span></span>
<span data-ttu-id="6dfc7-144">Azure CDN kaynak ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-144">Azure CDN origin weight.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet, ByFieldsPrivateLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6dfc7-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="6dfc7-145">-Confirm</span></span>
<span data-ttu-id="6dfc7-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dfc7-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dfc7-147">-WhatIf</span></span>
<span data-ttu-id="6dfc7-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6dfc7-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dfc7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dfc7-150">CommonParameters</span></span>
<span data-ttu-id="6dfc7-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dfc7-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6dfc7-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dfc7-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6dfc7-153">INPUTS</span></span>

### <span data-ttu-id="6dfc7-154">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6dfc7-154">None</span></span>

## <span data-ttu-id="6dfc7-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6dfc7-155">OUTPUTS</span></span>

### <span data-ttu-id="6dfc7-156">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="6dfc7-156">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="6dfc7-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6dfc7-157">NOTES</span></span>

## <span data-ttu-id="6dfc7-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6dfc7-158">RELATED LINKS</span></span>
