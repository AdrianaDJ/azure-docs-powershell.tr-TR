---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCachePatchSchedule.md
ms.openlocfilehash: 0e63f8e5f427a251db13c76f915dc615f259defc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268382"
---
# <span data-ttu-id="00b2b-101">Get-AzRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="00b2b-101">Get-AzRedisCachePatchSchedule</span></span>

## <span data-ttu-id="00b2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="00b2b-103">Bir düzeltme eki zamanlama alır.</span><span class="sxs-lookup"><span data-stu-id="00b2b-103">Gets a patch schedule.</span></span>

## <span data-ttu-id="00b2b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00b2b-104">SYNTAX</span></span>

```
Get-AzRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00b2b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00b2b-105">DESCRIPTION</span></span>
<span data-ttu-id="00b2b-106">**Get-Azrediscachepatchzamanlama** cmdlet 'ı Azure Redis Cache 'de bir önbellek için bir düzeltme programı alır.</span><span class="sxs-lookup"><span data-stu-id="00b2b-106">The **Get-AzRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="00b2b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00b2b-107">EXAMPLES</span></span>

### <span data-ttu-id="00b2b-108">Örnek 1: düzeltme ekini alma</span><span class="sxs-lookup"><span data-stu-id="00b2b-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="00b2b-109">Bu komut düzeltme programını RedisCache06 adlı önbellekten alır.</span><span class="sxs-lookup"><span data-stu-id="00b2b-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="00b2b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00b2b-110">PARAMETERS</span></span>

### <span data-ttu-id="00b2b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00b2b-111">-DefaultProfile</span></span>
<span data-ttu-id="00b2b-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00b2b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00b2b-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="00b2b-113">-Name</span></span>
<span data-ttu-id="00b2b-114">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00b2b-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="00b2b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00b2b-115">-ResourceGroupName</span></span>
<span data-ttu-id="00b2b-116">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00b2b-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="00b2b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00b2b-117">CommonParameters</span></span>
<span data-ttu-id="00b2b-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00b2b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00b2b-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00b2b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00b2b-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00b2b-120">INPUTS</span></span>

### <span data-ttu-id="00b2b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="00b2b-121">System.String</span></span>

## <span data-ttu-id="00b2b-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00b2b-122">OUTPUTS</span></span>

### <span data-ttu-id="00b2b-123">Microsoft. Azure. Commands. RedisCache. modeller. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="00b2b-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="00b2b-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00b2b-124">NOTES</span></span>
* <span data-ttu-id="00b2b-125">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="00b2b-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="00b2b-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00b2b-126">RELATED LINKS</span></span>

[<span data-ttu-id="00b2b-127">Yeni-Azredecachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="00b2b-127">New-AzRedisCachePatchSchedule</span></span>](./New-AzRedisCachePatchSchedule.md)

[<span data-ttu-id="00b2b-128">Yeni-Azredecachescheduleentry</span><span class="sxs-lookup"><span data-stu-id="00b2b-128">New-AzRedisCacheScheduleEntry</span></span>](./New-AzRedisCacheScheduleEntry.md)

[<span data-ttu-id="00b2b-129">Remove-Azredecachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="00b2b-129">Remove-AzRedisCachePatchSchedule</span></span>](./Remove-AzRedisCachePatchSchedule.md)


