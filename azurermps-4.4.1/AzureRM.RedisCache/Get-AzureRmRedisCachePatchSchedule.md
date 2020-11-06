---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: DA180A4A-88B6-4359-94E0-CF72F66D1FE4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCachePatchSchedule.md
ms.openlocfilehash: 1899a35f183f66fb938abe0c6492e826ad661e43
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594586"
---
# <span data-ttu-id="844f1-101">Get-AzureRmRedisCachePatchSchedule</span><span class="sxs-lookup"><span data-stu-id="844f1-101">Get-AzureRmRedisCachePatchSchedule</span></span>

## <span data-ttu-id="844f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="844f1-102">SYNOPSIS</span></span>
<span data-ttu-id="844f1-103">Bir düzeltme eki zamanlama alır.</span><span class="sxs-lookup"><span data-stu-id="844f1-103">Gets a patch schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="844f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="844f1-104">SYNTAX</span></span>

```
Get-AzureRmRedisCachePatchSchedule -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="844f1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="844f1-105">DESCRIPTION</span></span>
<span data-ttu-id="844f1-106">**Get-Azurermrediscachepatchzamanlama** cmdlet 'ı Azure Redis Cache 'de bir önbellek için bir düzeltme zamanlama alır.</span><span class="sxs-lookup"><span data-stu-id="844f1-106">The **Get-AzureRmRedisCachePatchSchedule** cmdlet gets a patch schedule for a cache in Azure Redis Cache.</span></span>

## <span data-ttu-id="844f1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="844f1-107">EXAMPLES</span></span>

### <span data-ttu-id="844f1-108">Örnek 1: düzeltme ekini alma</span><span class="sxs-lookup"><span data-stu-id="844f1-108">Example 1: Get the patch schedule</span></span>
```
PS C:\>Get-AzureRmRedisCachePatchSchedule -ResourceGroupName "ResourceGroup13" -Name "RedisCache06"
```

<span data-ttu-id="844f1-109">Bu komut düzeltme programını RedisCache06 adlı önbellekten alır.</span><span class="sxs-lookup"><span data-stu-id="844f1-109">This command gets the patch schedule from the cache named RedisCache06.</span></span>

## <span data-ttu-id="844f1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="844f1-110">PARAMETERS</span></span>

### <span data-ttu-id="844f1-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="844f1-111">-Name</span></span>
<span data-ttu-id="844f1-112">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="844f1-112">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="844f1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="844f1-113">-ResourceGroupName</span></span>
<span data-ttu-id="844f1-114">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="844f1-114">Specifies the name of the resource group which contains the cache.</span></span>

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

### <span data-ttu-id="844f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="844f1-115">-DefaultProfile</span></span>
<span data-ttu-id="844f1-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="844f1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="844f1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="844f1-117">CommonParameters</span></span>
<span data-ttu-id="844f1-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="844f1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="844f1-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="844f1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="844f1-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="844f1-120">INPUTS</span></span>

### <span data-ttu-id="844f1-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="844f1-121">None</span></span>
<span data-ttu-id="844f1-122">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="844f1-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="844f1-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="844f1-123">OUTPUTS</span></span>

### <span data-ttu-id="844f1-124">Microsoft. Azure. Commands. RedisCache. modeller. PSScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="844f1-124">Microsoft.Azure.Commands.RedisCache.Models.PSScheduleEntry</span></span>
<span data-ttu-id="844f1-125">Bu cmdlet, önbellekte ayarlanan düzeltme eki zamanlama girdilerinin döndürür.</span><span class="sxs-lookup"><span data-stu-id="844f1-125">This cmdlet returns the of patch schedule entries set on the cache.</span></span>

## <span data-ttu-id="844f1-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="844f1-126">NOTES</span></span>
* <span data-ttu-id="844f1-127">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="844f1-127">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="844f1-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="844f1-128">RELATED LINKS</span></span>

[<span data-ttu-id="844f1-129">Yeni-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="844f1-129">New-AzureRmRedisCachePatchSchedule</span></span>](./New-AzureRmRedisCachePatchSchedule.md)

[<span data-ttu-id="844f1-130">Yeni-AzureRmRedisCacheScheduleEntry</span><span class="sxs-lookup"><span data-stu-id="844f1-130">New-AzureRmRedisCacheScheduleEntry</span></span>](./New-AzureRmRedisCacheScheduleEntry.md)

[<span data-ttu-id="844f1-131">Remove-Azurermrediscachepatchzamanlama</span><span class="sxs-lookup"><span data-stu-id="844f1-131">Remove-AzureRmRedisCachePatchSchedule</span></span>](./Remove-AzureRmRedisCachePatchSchedule.md)


