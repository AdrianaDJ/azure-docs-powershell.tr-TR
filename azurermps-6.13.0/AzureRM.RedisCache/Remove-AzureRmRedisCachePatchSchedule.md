---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 7224e83333b281fac849ee9e5d99a0691aba3ccc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763437"
---
# <span data-ttu-id="1bb6b-101">Remove-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="1bb6b-101">Remove-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="1bb6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bb6b-102">SYNOPSIS</span></span>
<span data-ttu-id="1bb6b-103">Düzeltme Eki zamanlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1bb6b-103">Removes the patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1bb6b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1bb6b-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bb6b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1bb6b-105">DESCRIPTION</span></span>
<span data-ttu-id="1bb6b-106">**Remove-Azurermrediscachepatchzamanlama** cmdlet 'ı, Azure Redis önbelleğindeki düzeltme eki zamanlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1bb6b-106">The **Remove-AzureRmRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="1bb6b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1bb6b-107">EXAMPLES</span></span>

### <span data-ttu-id="1bb6b-108">Örnek 1: Düzeltme Eki zamanlamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="1bb6b-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="1bb6b-109">Bu komut düzeltme eki zamanlamasını RedisCache06 adlı önbellekten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="1bb6b-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="1bb6b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1bb6b-110">PARAMETERS</span></span>

### <span data-ttu-id="1bb6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bb6b-111">-DefaultProfile</span></span>
<span data-ttu-id="1bb6b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1bb6b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bb6b-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="1bb6b-113">-Name</span></span>
<span data-ttu-id="1bb6b-114">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bb6b-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="1bb6b-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="1bb6b-115">-PassThru</span></span>
<span data-ttu-id="1bb6b-116">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="1bb6b-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1bb6b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bb6b-117">-ResourceGroupName</span></span>
<span data-ttu-id="1bb6b-118">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1bb6b-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="1bb6b-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="1bb6b-119">-Confirm</span></span>
<span data-ttu-id="1bb6b-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1bb6b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bb6b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bb6b-121">-WhatIf</span></span>
<span data-ttu-id="1bb6b-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1bb6b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bb6b-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1bb6b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bb6b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bb6b-124">CommonParameters</span></span>
<span data-ttu-id="1bb6b-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1bb6b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bb6b-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bb6b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bb6b-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1bb6b-127">INPUTS</span></span>

### <span data-ttu-id="1bb6b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1bb6b-128">System.String</span></span>

## <span data-ttu-id="1bb6b-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1bb6b-129">OUTPUTS</span></span>

### <span data-ttu-id="1bb6b-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1bb6b-130">System.Boolean</span></span>

## <span data-ttu-id="1bb6b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1bb6b-131">NOTES</span></span>
* <span data-ttu-id="1bb6b-132">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="1bb6b-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="1bb6b-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1bb6b-133">RELATED LINKS</span></span>

[<span data-ttu-id="1bb6b-134">Get-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="1bb6b-134">Get-AzureRmRedisCachePatchSchedule</span></span>](./Get-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="1bb6b-135">Yeni-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="1bb6b-135">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="1bb6b-136">Yeni-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="1bb6b-136">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)


