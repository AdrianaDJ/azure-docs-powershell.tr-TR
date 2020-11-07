---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: e7e50488f69adb2b168453fd18264bf25a69942d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764788"
---
# <span data-ttu-id="9c846-101">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="9c846-101">Get-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="9c846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c846-102">SYNOPSIS</span></span>
<span data-ttu-id="9c846-103">Kırmızın önbelleğinin erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9c846-103">Gets the access keys for a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c846-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c846-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c846-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c846-105">DESCRIPTION</span></span>
<span data-ttu-id="9c846-106">**Get-AzureRmRedisCacheKey** cmdlet 'ı, Azure Redis önbelleğinin erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9c846-106">The **Get-AzureRmRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="9c846-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c846-107">EXAMPLES</span></span>

### <span data-ttu-id="9c846-108">Örnek 1: kırmızı bir önbelleğin erişim tuşlarını alma</span><span class="sxs-lookup"><span data-stu-id="9c846-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="9c846-109">Bu komut MyCacheKey adlı erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9c846-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="9c846-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c846-110">PARAMETERS</span></span>

### <span data-ttu-id="9c846-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="9c846-111">-Name</span></span>
<span data-ttu-id="9c846-112">Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c846-112">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="9c846-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c846-113">-ResourceGroupName</span></span>
<span data-ttu-id="9c846-114">Redis önbelleğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9c846-114">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="9c846-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c846-115">-DefaultProfile</span></span>
<span data-ttu-id="9c846-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c846-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c846-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c846-117">CommonParameters</span></span>
<span data-ttu-id="9c846-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c846-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c846-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c846-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c846-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c846-120">INPUTS</span></span>

### <span data-ttu-id="9c846-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9c846-121">None</span></span>
<span data-ttu-id="9c846-122">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c846-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="9c846-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c846-123">OUTPUTS</span></span>

### <span data-ttu-id="9c846-124">Microsoft. Azure. Management. Redis. modeller. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="9c846-124">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="9c846-125">Bu cmdlet, Redis önbelleğine birincil ve ikincil erişim anahtarlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="9c846-125">This cmdlet returns primary and secondary access keys for a Redis Cache.</span></span>

## <span data-ttu-id="9c846-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c846-126">NOTES</span></span>

## <span data-ttu-id="9c846-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c846-127">RELATED LINKS</span></span>

[<span data-ttu-id="9c846-128">Yeni-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="9c846-128">New-AzureRmRedisCacheKey</span></span>](./New-AzureRmRedisCacheKey.md)


