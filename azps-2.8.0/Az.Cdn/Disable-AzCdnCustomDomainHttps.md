---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: c3b2cadcdcc57ffc2cba8281af804e0c98c800bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753096"
---
# <span data-ttu-id="c9c6b-101">Disable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="c9c6b-101">Disable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="c9c6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="c9c6b-103">HTTPS özel etki alanını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-103">Disables Custom Domain HTTPS.</span></span>

## <span data-ttu-id="c9c6b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9c6b-104">SYNTAX</span></span>

### <span data-ttu-id="c9c6b-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c9c6b-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9c6b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c9c6b-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9c6b-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c9c6b-107">ByResourceIdParameterSet</span></span>
```
Disable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9c6b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9c6b-108">DESCRIPTION</span></span>
<span data-ttu-id="c9c6b-109">**Disable-AzCdnCustomDomainHttps** CMDLET 'i CDN özel etki ALANıNıN güvenli https teslimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-109">The **Disable-AzCdnCustomDomainHttps** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="c9c6b-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9c6b-110">EXAMPLES</span></span>

### <span data-ttu-id="c9c6b-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c9c6b-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="c9c6b-112">Özel etki alanının güvenli dağıtımını devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-112">Disable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="c9c6b-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9c6b-113">PARAMETERS</span></span>

### <span data-ttu-id="c9c6b-114">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="c9c6b-114">-CustomDomainName</span></span>
<span data-ttu-id="c9c6b-115">Azure CDN özel etki alanı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="c9c6b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9c6b-116">-DefaultProfile</span></span>
<span data-ttu-id="c9c6b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9c6b-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c9c6b-118">-EndpointName</span></span>
<span data-ttu-id="c9c6b-119">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="c9c6b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c9c6b-120">-InputObject</span></span>
<span data-ttu-id="c9c6b-121">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-121">The custom domain object.</span></span>

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

### <span data-ttu-id="c9c6b-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c9c6b-122">-PassThru</span></span>
<span data-ttu-id="c9c6b-123">Belirtilmişse nesneyi döndür.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-123">Return object if specified.</span></span>

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

### <span data-ttu-id="c9c6b-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c9c6b-124">-ProfileName</span></span>
<span data-ttu-id="c9c6b-125">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="c9c6b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9c6b-126">-ResourceGroupName</span></span>
<span data-ttu-id="c9c6b-127">Azure CDN profilinin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="c9c6b-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="c9c6b-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c9c6b-128">-ResourceId</span></span>
<span data-ttu-id="c9c6b-129">Özel etki alanının RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c9c6b-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="c9c6b-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="c9c6b-130">-Confirm</span></span>
<span data-ttu-id="c9c6b-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9c6b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9c6b-132">-WhatIf</span></span>
<span data-ttu-id="c9c6b-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9c6b-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9c6b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9c6b-135">CommonParameters</span></span>
<span data-ttu-id="c9c6b-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9c6b-137">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c9c6b-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9c6b-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9c6b-138">INPUTS</span></span>

### <span data-ttu-id="c9c6b-139">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="c9c6b-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="c9c6b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c9c6b-140">System.String</span></span>

## <span data-ttu-id="c9c6b-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9c6b-141">OUTPUTS</span></span>

### <span data-ttu-id="c9c6b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9c6b-142">System.Boolean</span></span>

## <span data-ttu-id="c9c6b-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9c6b-143">NOTES</span></span>

## <span data-ttu-id="c9c6b-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9c6b-144">RELATED LINKS</span></span>
