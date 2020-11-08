---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938182"
---
# <span data-ttu-id="38d58-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="38d58-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="38d58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38d58-102">SYNOPSIS</span></span>
<span data-ttu-id="38d58-103">Azure Redis Cache 'de tanılamayı mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="38d58-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="38d58-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38d58-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38d58-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="38d58-105">DESCRIPTION</span></span>
<span data-ttu-id="38d58-106">**Set-AzRedisCacheDiagnostic** cmdlet 'ı, Azure Redis önbelleğinin tanılamasını etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="38d58-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="38d58-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38d58-107">EXAMPLES</span></span>

### <span data-ttu-id="38d58-108">Örnek 1: tanılamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="38d58-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="38d58-109">Bu komut, Azure Redis önbelleğinin tanılamasını mümkün kılar.</span><span class="sxs-lookup"><span data-stu-id="38d58-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="38d58-110">Bu komut, abonelikler için aynı bölgedeki tüm Azure redin önbelleklerinin tanılama veya depolama hesabını güncellemesine olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="38d58-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="38d58-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38d58-111">PARAMETERS</span></span>

### <span data-ttu-id="38d58-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d58-112">-DefaultProfile</span></span>
<span data-ttu-id="38d58-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38d58-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38d58-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="38d58-114">-Name</span></span>
<span data-ttu-id="38d58-115">Önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38d58-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="38d58-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d58-116">-ResourceGroupName</span></span>
<span data-ttu-id="38d58-117">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38d58-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="38d58-118">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="38d58-118">-StorageAccountId</span></span>
<span data-ttu-id="38d58-119">Tanılama verilerini depolamak için kullanılan depolama hesabının kaynak KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="38d58-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="38d58-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="38d58-120">-Confirm</span></span>
<span data-ttu-id="38d58-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38d58-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38d58-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d58-122">-WhatIf</span></span>
<span data-ttu-id="38d58-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="38d58-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38d58-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="38d58-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38d58-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d58-125">CommonParameters</span></span>
<span data-ttu-id="38d58-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38d58-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d58-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d58-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d58-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38d58-128">INPUTS</span></span>

### <span data-ttu-id="38d58-129">System. String</span><span class="sxs-lookup"><span data-stu-id="38d58-129">System.String</span></span>

## <span data-ttu-id="38d58-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38d58-130">OUTPUTS</span></span>

### <span data-ttu-id="38d58-131">System. void</span><span class="sxs-lookup"><span data-stu-id="38d58-131">System.Void</span></span>

## <span data-ttu-id="38d58-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38d58-132">NOTES</span></span>
* <span data-ttu-id="38d58-133">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="38d58-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="38d58-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38d58-134">RELATED LINKS</span></span>

[<span data-ttu-id="38d58-135">Remove-Azrediscachedıtik</span><span class="sxs-lookup"><span data-stu-id="38d58-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)

