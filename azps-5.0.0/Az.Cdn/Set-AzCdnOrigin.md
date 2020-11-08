---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 1c3b195f868db5d4e579aa833c4d9ce5a6203c56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277644"
---
# <span data-ttu-id="5846a-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="5846a-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="5846a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5846a-102">SYNOPSIS</span></span>
<span data-ttu-id="5846a-103">CDN kaynak sunucusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5846a-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="5846a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5846a-104">SYNTAX</span></span>

### <span data-ttu-id="5846a-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5846a-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5846a-106">ByFieldsPrivateLinkParameterSet</span><span class="sxs-lookup"><span data-stu-id="5846a-106">ByFieldsPrivateLinkParameterSet</span></span>
```
Set-AzCdnOrigin -EndpointName <String> -HostName <String> [-HttpPort <Int32>] [-HttpsPort <Int32>]
 [-OriginHostHeader <String>] -OriginName <String> -ProfileName <String> [-Priority <Int32>]
 [-PrivateLinkApprovalMessage <String>] -PrivateLinkLocation <String> -PrivateLinkResourceId <String>
 -ResourceGroupName <String> [-Weight <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5846a-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5846a-107">ByObjectParameterSet</span></span>
```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5846a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5846a-108">DESCRIPTION</span></span>
<span data-ttu-id="5846a-109">**Set-Azcdnorigın** cmdlet 'i, bir Azure Içerik teslim ağı (CDN) kaynak sunucusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5846a-109">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="5846a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5846a-110">EXAMPLES</span></span>

## <span data-ttu-id="5846a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5846a-111">PARAMETERS</span></span>

### <span data-ttu-id="5846a-112">-Cdnorigın</span><span class="sxs-lookup"><span data-stu-id="5846a-112">-CdnOrigin</span></span>
<span data-ttu-id="5846a-113">Bu cmdlet 'in güncelleştirdiği kaynak sunucuyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5846a-113">Specifies the origin server that this cmdlet updates.</span></span>

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

### <span data-ttu-id="5846a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5846a-114">-DefaultProfile</span></span>
<span data-ttu-id="5846a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5846a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5846a-116">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5846a-116">-EndpointName</span></span>
<span data-ttu-id="5846a-117">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="5846a-117">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="5846a-118">-Ana bilgisayar adı</span><span class="sxs-lookup"><span data-stu-id="5846a-118">-HostName</span></span>
<span data-ttu-id="5846a-119">Azure CDN kaynak ana bilgisayar adı.</span><span class="sxs-lookup"><span data-stu-id="5846a-119">Azure CDN origin host name.</span></span>

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

### <span data-ttu-id="5846a-120">-HttpPort</span><span class="sxs-lookup"><span data-stu-id="5846a-120">-HttpPort</span></span>
<span data-ttu-id="5846a-121">Azure CDN kaynak http bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="5846a-121">Azure CDN origin http port.</span></span>

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

### <span data-ttu-id="5846a-122">-HttpsPort</span><span class="sxs-lookup"><span data-stu-id="5846a-122">-HttpsPort</span></span>
<span data-ttu-id="5846a-123">Azure CDN başlangıç HTTPS bağlantı noktası.</span><span class="sxs-lookup"><span data-stu-id="5846a-123">Azure CDN origin https port.</span></span>

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

### <span data-ttu-id="5846a-124">-OriginHostHeader</span><span class="sxs-lookup"><span data-stu-id="5846a-124">-OriginHostHeader</span></span>
<span data-ttu-id="5846a-125">Azure CDN kaynak ana bilgisayar üst bilgisi.</span><span class="sxs-lookup"><span data-stu-id="5846a-125">Azure CDN origin host header.</span></span>

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

### <span data-ttu-id="5846a-126">-AdName</span><span class="sxs-lookup"><span data-stu-id="5846a-126">-OriginName</span></span>
<span data-ttu-id="5846a-127">Azure CDN kaynak adı.</span><span class="sxs-lookup"><span data-stu-id="5846a-127">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="5846a-128">-Öncelik</span><span class="sxs-lookup"><span data-stu-id="5846a-128">-Priority</span></span>
<span data-ttu-id="5846a-129">Azure CDN kaynak önceliği.</span><span class="sxs-lookup"><span data-stu-id="5846a-129">Azure CDN origin priority.</span></span>

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

### <span data-ttu-id="5846a-130">-PrivateLinkApprovalMessage</span><span class="sxs-lookup"><span data-stu-id="5846a-130">-PrivateLinkApprovalMessage</span></span>
<span data-ttu-id="5846a-131">Özel bağlantısına bağlanma onay isteğine dahil edilecek özel bir ileti.</span><span class="sxs-lookup"><span data-stu-id="5846a-131">A custom message to be included in the approval request to connect to the Private Link.</span></span>

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

### <span data-ttu-id="5846a-132">-PrivateLinkLocation</span><span class="sxs-lookup"><span data-stu-id="5846a-132">-PrivateLinkLocation</span></span>
<span data-ttu-id="5846a-133">Azure CDN kaynak özel bağlantı konumu.</span><span class="sxs-lookup"><span data-stu-id="5846a-133">Azure CDN origin private link location.</span></span>

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

### <span data-ttu-id="5846a-134">-Privatelinkresourceıd</span><span class="sxs-lookup"><span data-stu-id="5846a-134">-PrivateLinkResourceId</span></span>
<span data-ttu-id="5846a-135">Azure CDN kaynak özel bağlantısı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="5846a-135">Azure CDN origin private link resource id.</span></span>

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

### <span data-ttu-id="5846a-136">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5846a-136">-ProfileName</span></span>
<span data-ttu-id="5846a-137">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="5846a-137">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="5846a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5846a-138">-ResourceGroupName</span></span>
<span data-ttu-id="5846a-139">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="5846a-139">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="5846a-140">-Kalınlık</span><span class="sxs-lookup"><span data-stu-id="5846a-140">-Weight</span></span>
<span data-ttu-id="5846a-141">Azure CDN kaynak ağırlığı.</span><span class="sxs-lookup"><span data-stu-id="5846a-141">Azure CDN origin weight.</span></span>

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

### <span data-ttu-id="5846a-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="5846a-142">-Confirm</span></span>
<span data-ttu-id="5846a-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5846a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5846a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5846a-144">-WhatIf</span></span>
<span data-ttu-id="5846a-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5846a-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5846a-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5846a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5846a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5846a-147">CommonParameters</span></span>
<span data-ttu-id="5846a-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5846a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5846a-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5846a-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5846a-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5846a-150">INPUTS</span></span>

### <span data-ttu-id="5846a-151">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="5846a-151">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="5846a-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5846a-152">OUTPUTS</span></span>

### <span data-ttu-id="5846a-153">Microsoft. Azure. Commands. CDN. model. Origin. Psorigın</span><span class="sxs-lookup"><span data-stu-id="5846a-153">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="5846a-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5846a-154">NOTES</span></span>

## <span data-ttu-id="5846a-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5846a-155">RELATED LINKS</span></span>

[<span data-ttu-id="5846a-156">Get-Azcdnorigın</span><span class="sxs-lookup"><span data-stu-id="5846a-156">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


