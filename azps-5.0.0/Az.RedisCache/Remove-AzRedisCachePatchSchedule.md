---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 2EA765B8-D82B-4789-8F10-88F79BDF44D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 8e66391ff613578d1306543c626908763a932d06
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324508"
---
# <span data-ttu-id="9811c-101">Remove-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="9811c-101">Remove-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="9811c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9811c-102">SYNOPSIS</span></span>
<span data-ttu-id="9811c-103">Düzeltme Eki zamanlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9811c-103">Removes the patch schedule.</span></span>

## <span data-ttu-id="9811c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9811c-104">SYNTAX</span></span>

```
Remove-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9811c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9811c-105">DESCRIPTION</span></span>
<span data-ttu-id="9811c-106">**Remove-Azrediscachepatchzamanlama** cmdlet 'ı, Azure Redis önbelleğindeki düzeltme eki zamanlamasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9811c-106">The **Remove-AzRedisCachePatchSchedule** cmdlet removes the patch schedule from a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="9811c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9811c-107">EXAMPLES</span></span>

### <span data-ttu-id="9811c-108">Örnek 1: Düzeltme Eki zamanlamasını kaldırma</span><span class="sxs-lookup"><span data-stu-id="9811c-108">Example 1: Remove the patch schedule</span></span>
```
PS C:\>Remove-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="9811c-109">Bu komut düzeltme eki zamanlamasını RedisCache06 adlı önbellekten kaldırır.</span><span class="sxs-lookup"><span data-stu-id="9811c-109">This command removes the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="9811c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9811c-110">PARAMETERS</span></span>

### <span data-ttu-id="9811c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9811c-111">-DefaultProfile</span></span>
<span data-ttu-id="9811c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9811c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9811c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="9811c-113">-Name</span></span>
<span data-ttu-id="9811c-114">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9811c-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="9811c-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9811c-115">-PassThru</span></span>
<span data-ttu-id="9811c-116">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="9811c-116">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9811c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9811c-117">-ResourceGroupName</span></span>
<span data-ttu-id="9811c-118">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9811c-118">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="9811c-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="9811c-119">-Confirm</span></span>
<span data-ttu-id="9811c-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9811c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9811c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9811c-121">-WhatIf</span></span>
<span data-ttu-id="9811c-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9811c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9811c-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9811c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9811c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9811c-124">CommonParameters</span></span>
<span data-ttu-id="9811c-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9811c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9811c-126">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9811c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9811c-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9811c-127">INPUTS</span></span>

### <span data-ttu-id="9811c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9811c-128">System.String</span></span>

## <span data-ttu-id="9811c-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9811c-129">OUTPUTS</span></span>

### <span data-ttu-id="9811c-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9811c-130">System.Boolean</span></span>

## <span data-ttu-id="9811c-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9811c-131">NOTES</span></span>
* <span data-ttu-id="9811c-132">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="9811c-132">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="9811c-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9811c-133">RELATED LINKS</span></span>

[<span data-ttu-id="9811c-134">Get-Azredecachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="9811c-134">Get-AzRedisCachePatchSchedule</span></span>](./Get-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="9811c-135">Yeni-Azredecachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="9811c-135">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="9811c-136">Yeni-Azredecachescheduleentry</span><span class="sxs-lookup"><span data-stu-id="9811c-136">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)


