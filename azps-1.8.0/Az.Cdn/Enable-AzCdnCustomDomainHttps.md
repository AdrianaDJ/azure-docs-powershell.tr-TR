---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/enable-azcdncustomdomainhttps
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Enable-AzCdnCustomDomainHttps.md
ms.openlocfilehash: 87c6928b6b1a8863bdde7126b782d07d4c496207
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761424"
---
# <span data-ttu-id="dd7d2-101">Enable-AzCdnCustomDomainHttps</span><span class="sxs-lookup"><span data-stu-id="dd7d2-101">Enable-AzCdnCustomDomainHttps</span></span>

## <span data-ttu-id="dd7d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd7d2-103">Özel HTTPS 'yi etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-103">Enables custom HTTPS.</span></span>

## <span data-ttu-id="dd7d2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd7d2-104">SYNTAX</span></span>

### <span data-ttu-id="dd7d2-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="dd7d2-105">ByFieldsParameterSet (Default)</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceGroupName <String> -ProfileName <String> -EndpointName <String>
 -CustomDomainName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd7d2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd7d2-106">ByObjectParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -InputObject <PSCustomDomain> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd7d2-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="dd7d2-107">ByResourceIdParameterSet</span></span>
```
Enable-AzCdnCustomDomainHttps -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd7d2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd7d2-108">DESCRIPTION</span></span>
<span data-ttu-id="dd7d2-109">**Enable-AzCdnCustomDomainHttps** CMDLET 'i CDN özel etki ALANıNıN güvenli https teslimini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-109">The **Enable-AzCdnCustomDomainHttps** cmdlet enables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="dd7d2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd7d2-110">EXAMPLES</span></span>

### <span data-ttu-id="dd7d2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dd7d2-111">Example 1</span></span>
```powershell
PS C:\> Enable-AzCdnCustomDomainHttps -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -CustomDomainName $customDomainName
```

<span data-ttu-id="dd7d2-112">Özel etki alanının güvenli dağıtımını etkinleştirme.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-112">Enable secure delivery of the custom domain.</span></span>

## <span data-ttu-id="dd7d2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd7d2-113">PARAMETERS</span></span>

### <span data-ttu-id="dd7d2-114">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="dd7d2-114">-CustomDomainName</span></span>
<span data-ttu-id="dd7d2-115">Azure CDN özel etki alanı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-115">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="dd7d2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd7d2-116">-DefaultProfile</span></span>
<span data-ttu-id="dd7d2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd7d2-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="dd7d2-118">-EndpointName</span></span>
<span data-ttu-id="dd7d2-119">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="dd7d2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd7d2-120">-InputObject</span></span>
<span data-ttu-id="dd7d2-121">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-121">The custom domain object.</span></span>

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

### <span data-ttu-id="dd7d2-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="dd7d2-122">-PassThru</span></span>
<span data-ttu-id="dd7d2-123">Belirtilmişse nesneyi döndür.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-123">Return object if specified.</span></span>

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

### <span data-ttu-id="dd7d2-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="dd7d2-124">-ProfileName</span></span>
<span data-ttu-id="dd7d2-125">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="dd7d2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd7d2-126">-ResourceGroupName</span></span>
<span data-ttu-id="dd7d2-127">Azure CDN profilinin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="dd7d2-127">The resource group of the Azure CDN profile</span></span>

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

### <span data-ttu-id="dd7d2-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dd7d2-128">-ResourceId</span></span>
<span data-ttu-id="dd7d2-129">Özel etki alanının RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="dd7d2-129">ResourceId of the Custom Domain</span></span>

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

### <span data-ttu-id="dd7d2-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="dd7d2-130">-Confirm</span></span>
<span data-ttu-id="dd7d2-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd7d2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd7d2-132">-WhatIf</span></span>
<span data-ttu-id="dd7d2-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd7d2-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd7d2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd7d2-135">CommonParameters</span></span>
<span data-ttu-id="dd7d2-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd7d2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd7d2-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd7d2-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd7d2-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd7d2-138">INPUTS</span></span>

### <span data-ttu-id="dd7d2-139">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="dd7d2-139">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

### <span data-ttu-id="dd7d2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="dd7d2-140">System.String</span></span>

## <span data-ttu-id="dd7d2-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd7d2-141">OUTPUTS</span></span>

### <span data-ttu-id="dd7d2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dd7d2-142">System.Boolean</span></span>

## <span data-ttu-id="dd7d2-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd7d2-143">NOTES</span></span>

## <span data-ttu-id="dd7d2-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd7d2-144">RELATED LINKS</span></span>
