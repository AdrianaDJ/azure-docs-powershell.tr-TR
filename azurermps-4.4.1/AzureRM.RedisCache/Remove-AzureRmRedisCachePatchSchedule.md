---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 768b37444155829ba33a5996fb969c21f85ca797
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587805"
---
# <span data-ttu-id="1466f-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1466f-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="1466f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1466f-102">SYNOPSIS</span></span>
<span data-ttu-id="1466f-103">Düzeltme Eki zamanlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1466f-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1466f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1466f-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1466f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1466f-105">DESCRIPTION</span></span>
<span data-ttu-id="1466f-106">**Remove-Azurermrediscachepatchzamanlama** cmdlet 'ı, Azure Redis önbelleğindeki düzeltme eki zamanlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1466f-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="1466f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1466f-107">EXAMPLES</span></span>

### <span data-ttu-id="1466f-108">Örnek 1: Düzeltme Eki zamanlamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1466f-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="1466f-109">Bu komut düzeltme eki zamanlamasını RedisCache06 adlı önbellekten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1466f-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="1466f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1466f-110">PARAMETERS</span></span>

### <span data-ttu-id="1466f-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="1466f-111">-Name</span></span>
<span data-ttu-id="1466f-112">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1466f-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="1466f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1466f-113">-ResourceGroupName</span></span>
<span data-ttu-id="1466f-114">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1466f-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="1466f-115">-Onay</span><span class="sxs-lookup"><span data-stu-id="1466f-115">-Confirm</span></span>
<span data-ttu-id="1466f-116">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1466f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1466f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1466f-117">-WhatIf</span></span>
<span data-ttu-id="1466f-118">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1466f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1466f-119">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1466f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1466f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1466f-120">-DefaultProfile</span></span>
<span data-ttu-id="1466f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1466f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1466f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1466f-122">CommonParameters</span></span>
<span data-ttu-id="1466f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1466f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1466f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1466f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1466f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1466f-125">INPUTS</span></span>

### <span data-ttu-id="1466f-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1466f-126">None</span></span>
<span data-ttu-id="1466f-127">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1466f-127">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="1466f-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1466f-128">OUTPUTS</span></span>

### <span data-ttu-id="1466f-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1466f-129">None</span></span>

## <span data-ttu-id="1466f-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1466f-130">NOTES</span></span>
* <span data-ttu-id="1466f-131">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="1466f-131">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="1466f-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1466f-132">RELATED LINKS</span></span>

[<span data-ttu-id="1466f-133">Get-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="1466f-133">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="1466f-134">Yeni-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="1466f-134">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="1466f-135">Yeni-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="1466f-135">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


