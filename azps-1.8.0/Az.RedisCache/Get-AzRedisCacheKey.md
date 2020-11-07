---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 96eed93e4020384b0c989a05f549aa21f5482493
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759559"
---
# <span data-ttu-id="54b8f-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="54b8f-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="54b8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="54b8f-103">Kırmızın önbelleğinin erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="54b8f-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="54b8f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="54b8f-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54b8f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="54b8f-105">DESCRIPTION</span></span>
<span data-ttu-id="54b8f-106">**Get-AzRedisCacheKey** cmdlet 'ı, Azure Redis önbelleğinin erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="54b8f-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="54b8f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="54b8f-107">EXAMPLES</span></span>

### <span data-ttu-id="54b8f-108">Örnek 1: kırmızı bir önbelleğin erişim tuşlarını alma</span><span class="sxs-lookup"><span data-stu-id="54b8f-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="54b8f-109">Bu komut MyCacheKey adlı erişim tuşlarını alır.</span><span class="sxs-lookup"><span data-stu-id="54b8f-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="54b8f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="54b8f-110">PARAMETERS</span></span>

### <span data-ttu-id="54b8f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54b8f-111">-DefaultProfile</span></span>
<span data-ttu-id="54b8f-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="54b8f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54b8f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="54b8f-113">-Name</span></span>
<span data-ttu-id="54b8f-114">Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54b8f-114">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="54b8f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54b8f-115">-ResourceGroupName</span></span>
<span data-ttu-id="54b8f-116">Redis önbelleğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="54b8f-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="54b8f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54b8f-117">CommonParameters</span></span>
<span data-ttu-id="54b8f-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="54b8f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54b8f-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54b8f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54b8f-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="54b8f-120">INPUTS</span></span>

### <span data-ttu-id="54b8f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="54b8f-121">System.String</span></span>

## <span data-ttu-id="54b8f-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="54b8f-122">OUTPUTS</span></span>

### <span data-ttu-id="54b8f-123">Microsoft. Azure. Management. Redis. modeller. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="54b8f-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="54b8f-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="54b8f-124">NOTES</span></span>

## <span data-ttu-id="54b8f-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="54b8f-125">RELATED LINKS</span></span>

[<span data-ttu-id="54b8f-126">Yeni-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="54b8f-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


