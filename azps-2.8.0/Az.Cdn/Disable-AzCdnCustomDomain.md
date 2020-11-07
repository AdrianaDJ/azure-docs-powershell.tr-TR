---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/disable-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Disable-AzCdnCustomDomain.md
ms.openlocfilehash: 4107ae55b42e35ae600766deb037c8c0590c8731
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753097"
---
# <span data-ttu-id="758bb-101">Disable-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="758bb-101">Disable-AzCdnCustomDomain</span></span>

## <span data-ttu-id="758bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="758bb-102">SYNOPSIS</span></span>
<span data-ttu-id="758bb-103">HTTPS (kullanım dışı) özel etki alanını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="758bb-103">Disables Custom Domain HTTPS (Deprecated).</span></span>

## <span data-ttu-id="758bb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="758bb-104">SYNTAX</span></span>

### <span data-ttu-id="758bb-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="758bb-105">ByFieldsParameterSet (Default)</span></span>
```
Disable-AzCdnCustomDomain -CustomDomainName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="758bb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="758bb-106">ByObjectParameterSet</span></span>
```
Disable-AzCdnCustomDomain -InputObject <PSCustomDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="758bb-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="758bb-107">DESCRIPTION</span></span>
<span data-ttu-id="758bb-108">**Disable-Azcıdncustomdomain** CMDLET 'i CDN özel etki ALANıNıN güvenli https teslimini devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="758bb-108">The **Disable-AzCdnCustomDomain** cmdlet disables the secured HTTPS delivery of a CDN custom domain.</span></span>

## <span data-ttu-id="758bb-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="758bb-109">EXAMPLES</span></span>

### <span data-ttu-id="758bb-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="758bb-110">Example 1</span></span>
```powershell
Disable-AzCdnCustomDomain -CustomDomainName $customDomainName -EndpointName $endpointName -ProfileName $profileName -ResourceGroupName $resourceGroupName
true
```

<span data-ttu-id="758bb-111">Https dağıtımını devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="758bb-111">Disable https delivery of the custom domain.</span></span>

## <span data-ttu-id="758bb-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="758bb-112">PARAMETERS</span></span>

### <span data-ttu-id="758bb-113">-Custometkialanıadı</span><span class="sxs-lookup"><span data-stu-id="758bb-113">-CustomDomainName</span></span>
<span data-ttu-id="758bb-114">Azure CDN özel etki alanı görünen adı.</span><span class="sxs-lookup"><span data-stu-id="758bb-114">Azure CDN custom domain display name.</span></span>

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

### <span data-ttu-id="758bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="758bb-115">-DefaultProfile</span></span>
<span data-ttu-id="758bb-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="758bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="758bb-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="758bb-117">-EndpointName</span></span>
<span data-ttu-id="758bb-118">Azure CDN uç noktası adı.</span><span class="sxs-lookup"><span data-stu-id="758bb-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="758bb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="758bb-119">-InputObject</span></span>
<span data-ttu-id="758bb-120">Özel etki alanı nesnesi.</span><span class="sxs-lookup"><span data-stu-id="758bb-120">The custom domain object.</span></span>

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

### <span data-ttu-id="758bb-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="758bb-121">-PassThru</span></span>
<span data-ttu-id="758bb-122">Return Object (belirtilmişse).</span><span class="sxs-lookup"><span data-stu-id="758bb-122">Return object (if specified).</span></span>

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

### <span data-ttu-id="758bb-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="758bb-123">-ProfileName</span></span>
<span data-ttu-id="758bb-124">Azure CDN profil adı.</span><span class="sxs-lookup"><span data-stu-id="758bb-124">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="758bb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="758bb-125">-ResourceGroupName</span></span>
<span data-ttu-id="758bb-126">Azure CDN profilinin kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="758bb-126">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="758bb-127">-Onay</span><span class="sxs-lookup"><span data-stu-id="758bb-127">-Confirm</span></span>
<span data-ttu-id="758bb-128">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="758bb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="758bb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="758bb-129">-WhatIf</span></span>
<span data-ttu-id="758bb-130">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="758bb-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="758bb-131">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="758bb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="758bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="758bb-132">CommonParameters</span></span>
<span data-ttu-id="758bb-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="758bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="758bb-134">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="758bb-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="758bb-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="758bb-135">INPUTS</span></span>

### <span data-ttu-id="758bb-136">Microsoft. Azure. Commands. CDN. modeller. CustomDomain. Psccustomdomain</span><span class="sxs-lookup"><span data-stu-id="758bb-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="758bb-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="758bb-137">OUTPUTS</span></span>

### <span data-ttu-id="758bb-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="758bb-138">System.Boolean</span></span>

## <span data-ttu-id="758bb-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="758bb-139">NOTES</span></span>

## <span data-ttu-id="758bb-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="758bb-140">RELATED LINKS</span></span>
