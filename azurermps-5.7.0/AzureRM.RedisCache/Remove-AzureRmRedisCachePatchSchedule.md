---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: dab4333907d50853474ff795d33263846af249b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592418"
---
# <span data-ttu-id="ca56a-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="ca56a-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="ca56a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca56a-102">SYNOPSIS</span></span>
<span data-ttu-id="ca56a-103">Düzeltme Eki zamanlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ca56a-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca56a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ca56a-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca56a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ca56a-105">DESCRIPTION</span></span>
<span data-ttu-id="ca56a-106">**Remove-Azurermrediscachepatchzamanlama** cmdlet 'ı, Azure Redis önbelleğindeki düzeltme eki zamanlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ca56a-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="ca56a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ca56a-107">EXAMPLES</span></span>

### <span data-ttu-id="ca56a-108">Örnek 1: Düzeltme Eki zamanlamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="ca56a-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="ca56a-109">Bu komut düzeltme eki zamanlamasını RedisCache06 adlı önbellekten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ca56a-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="ca56a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ca56a-110">PARAMETERS</span></span>

### <span data-ttu-id="ca56a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca56a-111">-DefaultProfile</span></span>
<span data-ttu-id="ca56a-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ca56a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca56a-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="ca56a-113">-Name</span></span>
<span data-ttu-id="ca56a-114">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca56a-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="ca56a-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ca56a-115">-PassThru</span></span>
<span data-ttu-id="ca56a-116">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="ca56a-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca56a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca56a-117">-ResourceGroupName</span></span>
<span data-ttu-id="ca56a-118">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ca56a-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="ca56a-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="ca56a-119">-Confirm</span></span>
<span data-ttu-id="ca56a-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ca56a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca56a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca56a-121">-WhatIf</span></span>
<span data-ttu-id="ca56a-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ca56a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca56a-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ca56a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca56a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca56a-124">CommonParameters</span></span>
<span data-ttu-id="ca56a-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ca56a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca56a-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca56a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca56a-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ca56a-127">INPUTS</span></span>

### <span data-ttu-id="ca56a-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ca56a-128">None</span></span>
<span data-ttu-id="ca56a-129">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ca56a-129">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="ca56a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ca56a-130">OUTPUTS</span></span>

### <span data-ttu-id="ca56a-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ca56a-131">None</span></span>

## <span data-ttu-id="ca56a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ca56a-132">NOTES</span></span>
* <span data-ttu-id="ca56a-133">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="ca56a-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="ca56a-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ca56a-134">RELATED LINKS</span></span>

[<span data-ttu-id="ca56a-135">Get-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="ca56a-135">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="ca56a-136">Yeni-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="ca56a-136">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="ca56a-137">Yeni-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="ca56a-137">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


