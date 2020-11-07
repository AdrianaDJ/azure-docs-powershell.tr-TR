---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachepatchschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: ac1184dcdcc55a0b5cac28f996c29c3476ba3613
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763813"
---
# <span data-ttu-id="f76fa-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="f76fa-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="f76fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f76fa-102">SYNOPSIS</span></span>
<span data-ttu-id="f76fa-103">Bir düzeltme eki zamanlama alır.</span><span class="sxs-lookup"><span data-stu-id="f76fa-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f76fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f76fa-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f76fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f76fa-105">DESCRIPTION</span></span>
<span data-ttu-id="f76fa-106">**Get-Azurermrediscachepatchzamanlama** cmdlet 'ı Azure Redis Cache 'de bir önbellek için bir düzeltme zamanlama alır.</span><span class="sxs-lookup"><span data-stu-id="f76fa-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="f76fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f76fa-107">EXAMPLES</span></span>

### <span data-ttu-id="f76fa-108">Örnek 1: düzeltme ekini alma</span><span class="sxs-lookup"><span data-stu-id="f76fa-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="f76fa-109">Bu komut düzeltme programını RedisCache06 adlı önbellekten alır.</span><span class="sxs-lookup"><span data-stu-id="f76fa-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="f76fa-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f76fa-110">PARAMETERS</span></span>

### <span data-ttu-id="f76fa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f76fa-111">-DefaultProfile</span></span>
<span data-ttu-id="f76fa-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f76fa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f76fa-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="f76fa-113">-Name</span></span>
<span data-ttu-id="f76fa-114">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f76fa-114">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="f76fa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f76fa-115">-ResourceGroupName</span></span>
<span data-ttu-id="f76fa-116">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f76fa-116">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="f76fa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f76fa-117">CommonParameters</span></span>
<span data-ttu-id="f76fa-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f76fa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f76fa-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f76fa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f76fa-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f76fa-120">INPUTS</span></span>

### <span data-ttu-id="f76fa-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f76fa-121">System.String</span></span>

## <span data-ttu-id="f76fa-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f76fa-122">OUTPUTS</span></span>

### <span data-ttu-id="f76fa-123">Microsoft. Azure. Commands. RedisCache. modeller. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="f76fa-123">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>

## <span data-ttu-id="f76fa-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f76fa-124">NOTES</span></span>
* <span data-ttu-id="f76fa-125">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="f76fa-125">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="f76fa-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f76fa-126">RELATED LINKS</span></span>

[<span data-ttu-id="f76fa-127">Yeni-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="f76fa-127">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="f76fa-128">Yeni-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="f76fa-128">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="f76fa-129">Remove-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="f76fa-129">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


