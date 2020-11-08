---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: cb11377c4ee18278dee2a3dc97c16bb58a02f5d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279208"
---
# <span data-ttu-id="7ba9f-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="7ba9f-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="7ba9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ba9f-102">SYNOPSIS</span></span>
<span data-ttu-id="7ba9f-103">Özel HTTPS 'yi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="7ba9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ba9f-104">SYNTAX</span></span>

### <span data-ttu-id="7ba9f-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7ba9f-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ba9f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ba9f-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ba9f-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="7ba9f-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ba9f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ba9f-108">DESCRIPTION</span></span>
<span data-ttu-id="7ba9f-109">**Enable-AzCdnCustomDomainHttps** CMDLET 'i CDN özel etki ALANıNıN güvenli https teslimini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="7ba9f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ba9f-110">EXAMPLES</span></span>

### <span data-ttu-id="7ba9f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7ba9f-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="7ba9f-112">Özel etki alanının güvenli dağıtımını etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="7ba9f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ba9f-113">PARAMETERS</span></span>

### <span data-ttu-id="7ba9f-114">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="7ba9f-114">-CustomDomainName</span></span>
<span data-ttu-id="7ba9f-115">Azure CDN özel etki alanı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="7ba9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ba9f-116">-DefaultProfile</span></span>
<span data-ttu-id="7ba9f-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ba9f-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7ba9f-118">-EndpointName</span></span>
<span data-ttu-id="7ba9f-119">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="7ba9f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ba9f-120">-InputObject</span></span>
<span data-ttu-id="7ba9f-121">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-121">The custom domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ba9f-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7ba9f-122">-PassThru</span></span>
<span data-ttu-id="7ba9f-123">Belirtilmişse nesneyi döndür.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-123">Return object if specified.</span></span>

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

### <span data-ttu-id="7ba9f-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7ba9f-124">-ProfileName</span></span>
<span data-ttu-id="7ba9f-125">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="7ba9f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ba9f-126">-ResourceGroupName</span></span>
<span data-ttu-id="7ba9f-127">Azure CDN profilinin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="7ba9f-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="7ba9f-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7ba9f-128">-ResourceId</span></span>
<span data-ttu-id="7ba9f-129">Özel etki alanının RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7ba9f-129">ResourceId of the Custom Domain</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ba9f-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="7ba9f-130">-Confirm</span></span>
<span data-ttu-id="7ba9f-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ba9f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ba9f-132">-WhatIf</span></span>
<span data-ttu-id="7ba9f-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ba9f-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ba9f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ba9f-135">CommonParameters</span></span>
<span data-ttu-id="7ba9f-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ba9f-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7ba9f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ba9f-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ba9f-138">INPUTS</span></span>

### <span data-ttu-id="7ba9f-139">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="7ba9f-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="7ba9f-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7ba9f-140">System.String</span></span>

## <span data-ttu-id="7ba9f-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ba9f-141">OUTPUTS</span></span>

### <span data-ttu-id="7ba9f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ba9f-142">System.Boolean</span></span>

## <span data-ttu-id="7ba9f-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ba9f-143">NOTES</span></span>

## <span data-ttu-id="7ba9f-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ba9f-144">RELATED LINKS</span></span>
