---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCacheDiagnostic.md
ms.openlocfilehash: b309875fd330df5695283c187e454556669b6652
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322429"
---
# <span data-ttu-id="e171c-101">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="e171c-101">Remove-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="e171c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e171c-102">SYNOPSIS</span></span>
<span data-ttu-id="e171c-103">Azure Redis Cache 'de tanılamayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e171c-103">Disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="e171c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e171c-104">SYNTAX</span></span>

```
Remove-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e171c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e171c-105">DESCRIPTION</span></span>
<span data-ttu-id="e171c-106">**Remove-AzRedisCacheDiagnostic** cmdlet 'ı, Azure Redis önbelleğindeki tanılamayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e171c-106">The **Remove-AzRedisCacheDiagnostic** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="e171c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e171c-107">EXAMPLES</span></span>

### <span data-ttu-id="e171c-108">Örnek 1: tanılamayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="e171c-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="e171c-109">Bu komut, belirtilen Azure Redis Cache 'de tanılamayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e171c-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>
<span data-ttu-id="e171c-110">Bu, aboneliğin tüm Azure Redis önbelleklerinin tanılamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="e171c-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="e171c-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e171c-111">PARAMETERS</span></span>

### <span data-ttu-id="e171c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e171c-112">-DefaultProfile</span></span>
<span data-ttu-id="e171c-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e171c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e171c-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="e171c-114">-Name</span></span>
<span data-ttu-id="e171c-115">Önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e171c-115">Specifies the name of the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e171c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e171c-116">-ResourceGroupName</span></span>
<span data-ttu-id="e171c-117">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e171c-117">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e171c-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="e171c-118">-Confirm</span></span>
<span data-ttu-id="e171c-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e171c-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e171c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e171c-120">-WhatIf</span></span>
<span data-ttu-id="e171c-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e171c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e171c-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e171c-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e171c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e171c-123">CommonParameters</span></span>
<span data-ttu-id="e171c-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e171c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e171c-125">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e171c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e171c-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e171c-126">INPUTS</span></span>

### <span data-ttu-id="e171c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e171c-127">System.String</span></span>

## <span data-ttu-id="e171c-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e171c-128">OUTPUTS</span></span>

### <span data-ttu-id="e171c-129">System. void</span><span class="sxs-lookup"><span data-stu-id="e171c-129">System.Void</span></span>

## <span data-ttu-id="e171c-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e171c-130">NOTES</span></span>
* <span data-ttu-id="e171c-131">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="e171c-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="e171c-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e171c-132">RELATED LINKS</span></span>

[<span data-ttu-id="e171c-133">Set-Azredecachedıtik</span><span class="sxs-lookup"><span data-stu-id="e171c-133">Set-AzRedisCacheDiagnostic</span></span>](./Set-AzRedisCacheDiagnostic.md)


