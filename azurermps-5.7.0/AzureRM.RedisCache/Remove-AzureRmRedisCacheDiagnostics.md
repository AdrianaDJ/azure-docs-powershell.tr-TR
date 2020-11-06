---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BCF989AE-A718-4AFE-B7C0-8B148468D4EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachediagnostics
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCacheDiagnostics.md
ms.openlocfilehash: fca64401f4671db63d76d491476f0e276e92055a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591639"
---
# <span data-ttu-id="82420-101">Remove-AzureRmRedisCacheDiagnostics</span><span class="sxs-lookup"><span data-stu-id="82420-101">Remove-AzureRmRedisCacheDiagnostics</span></span>

## <span data-ttu-id="82420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82420-102">SYNOPSIS</span></span>
<span data-ttu-id="82420-103">Azure Redis Cache 'de tanılamayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="82420-103">Disables diagnostics on an Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82420-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82420-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCacheDiagnostics [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82420-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="82420-105">DESCRIPTION</span></span>
<span data-ttu-id="82420-106">**Remove-Azurermrediscachediagnosks** cmdlet 'ı Azure Redis Cache 'de tanılamayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="82420-106">The **Remove-AzureRmRedisCacheDiagnostics** cmdlet disables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="82420-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82420-107">EXAMPLES</span></span>

### <span data-ttu-id="82420-108">Örnek 1: tanılamayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="82420-108">Example 1: Disable diagnostics</span></span>
```
PS C:\>Remove-AzureRmRedisCacheDiagnostics -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -Force
```

<span data-ttu-id="82420-109">Bu komut, belirtilen Azure Redis Cache 'de tanılamayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="82420-109">This command disables diagnostics on specified Azure Redis Cache.</span></span>

<span data-ttu-id="82420-110">Bu, aboneliğin tüm Azure Redis önbelleklerinin tanılamasını devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="82420-110">This disables diagnostics for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="82420-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82420-111">PARAMETERS</span></span>

### <span data-ttu-id="82420-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82420-112">-DefaultProfile</span></span>
<span data-ttu-id="82420-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="82420-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82420-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="82420-114">-Name</span></span>
<span data-ttu-id="82420-115">Önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82420-115">Specifies the name of the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82420-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82420-116">-ResourceGroupName</span></span>
<span data-ttu-id="82420-117">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="82420-117">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82420-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="82420-118">-Confirm</span></span>
<span data-ttu-id="82420-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="82420-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82420-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82420-120">-WhatIf</span></span>
<span data-ttu-id="82420-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="82420-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82420-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="82420-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82420-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82420-123">CommonParameters</span></span>
<span data-ttu-id="82420-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82420-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82420-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82420-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82420-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82420-126">INPUTS</span></span>

### <span data-ttu-id="82420-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="82420-127">None</span></span>

## <span data-ttu-id="82420-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82420-128">OUTPUTS</span></span>

### <span data-ttu-id="82420-129">Kılmak</span><span class="sxs-lookup"><span data-stu-id="82420-129">Void</span></span>

## <span data-ttu-id="82420-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82420-130">NOTES</span></span>
* <span data-ttu-id="82420-131">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="82420-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="82420-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82420-132">RELATED LINKS</span></span>

[<span data-ttu-id="82420-133">Set-Azurermrediscachedibelirsiz</span><span class="sxs-lookup"><span data-stu-id="82420-133">Set-AzureRmRedisCacheDiagnostics</span></span>](./Set-AzureRmRedisCacheDiagnostics.md)


