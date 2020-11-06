---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/get-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: 67ec6bdcce5121c2a80e1f76ea1081f249f15682
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589717"
---
# <span data-ttu-id="37b07-101">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="37b07-101">Get-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="37b07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37b07-102">SYNOPSIS</span></span>
<span data-ttu-id="37b07-103">Kırmızın önbelleğinin erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="37b07-103">Gets the access keys for a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37b07-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37b07-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37b07-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="37b07-105">DESCRIPTION</span></span>
<span data-ttu-id="37b07-106">**Get-AzureRmRedisCacheKey** cmdlet 'ı, Azure Redis önbelleğinin erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="37b07-106">The **Get-AzureRmRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="37b07-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37b07-107">EXAMPLES</span></span>

### <span data-ttu-id="37b07-108">Örnek 1: kırmızı bir önbelleğin erişim tuşlarını alma</span><span class="sxs-lookup"><span data-stu-id="37b07-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="37b07-109">Bu komut MyCacheKey adlı erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="37b07-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="37b07-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37b07-110">PARAMETERS</span></span>

### <span data-ttu-id="37b07-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b07-111">-DefaultProfile</span></span>
<span data-ttu-id="37b07-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37b07-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37b07-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="37b07-113">-Name</span></span>
<span data-ttu-id="37b07-114">Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37b07-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="37b07-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b07-115">-ResourceGroupName</span></span>
<span data-ttu-id="37b07-116">Redis önbelleğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37b07-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="37b07-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b07-117">CommonParameters</span></span>
<span data-ttu-id="37b07-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37b07-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b07-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37b07-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b07-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37b07-120">INPUTS</span></span>

### <span data-ttu-id="37b07-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="37b07-121">None</span></span>
<span data-ttu-id="37b07-122">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="37b07-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="37b07-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37b07-123">OUTPUTS</span></span>

### <span data-ttu-id="37b07-124">Microsoft. Azure. Management. Redis. modeller. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="37b07-124">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="37b07-125">Bu cmdlet, Redis önbelleğine birincil ve ikincil erişim anahtarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="37b07-125">This cmdlet returns primary and secondary access keys for a Redis Cache.</span></span>

## <span data-ttu-id="37b07-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37b07-126">NOTES</span></span>

## <span data-ttu-id="37b07-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37b07-127">RELATED LINKS</span></span>

[<span data-ttu-id="37b07-128">Yeni-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="37b07-128">New-AzureRmRedisCacheKey</span></span>](./New-AzureRmRedisCacheKey.md)


