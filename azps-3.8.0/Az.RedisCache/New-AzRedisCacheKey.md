---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCacheKey.md
ms.openlocfilehash: f48d49a59b21cbae3f314926f4de92e74a2b10e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096795"
---
# <span data-ttu-id="5a801-101">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="5a801-101">New-AzRedisCacheKey</span></span>

## <span data-ttu-id="5a801-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a801-102">SYNOPSIS</span></span>
<span data-ttu-id="5a801-103">Kırmızı bir önbelleğin erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5a801-103">Regenerates the access key of a Redis Cache.</span></span>

## <span data-ttu-id="5a801-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a801-104">SYNTAX</span></span>

```
New-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a801-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a801-105">DESCRIPTION</span></span>
<span data-ttu-id="5a801-106">**Yeni-AzRedisCacheKey** cmdlet 'ı Azure Redis önbelleğinin erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5a801-106">The **New-AzRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="5a801-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a801-107">EXAMPLES</span></span>

### <span data-ttu-id="5a801-108">Örnek 1: Birinci anahtarı yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="5a801-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="5a801-109">Bu komut, Redis önbelleğinin birincil anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5a801-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="5a801-110">Örnek 2: ikincil anahtarı yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="5a801-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="5a801-111">Bu komut, Redis önbelleğinin ikincil anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5a801-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="5a801-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a801-112">PARAMETERS</span></span>

### <span data-ttu-id="5a801-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a801-113">-DefaultProfile</span></span>
<span data-ttu-id="5a801-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a801-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a801-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5a801-115">-Force</span></span>
<span data-ttu-id="5a801-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5a801-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a801-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5a801-117">-KeyType</span></span>
<span data-ttu-id="5a801-118">Birincil veya ikincil erişim anahtarının yeniden oluşturulup oluşturulmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a801-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="5a801-119">Geçerli değerler: Primary, Secondary.</span><span class="sxs-lookup"><span data-stu-id="5a801-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a801-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="5a801-120">-Name</span></span>
<span data-ttu-id="5a801-121">Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a801-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="5a801-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a801-122">-ResourceGroupName</span></span>
<span data-ttu-id="5a801-123">Redis önbelleğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a801-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="5a801-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="5a801-124">-Confirm</span></span>
<span data-ttu-id="5a801-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5a801-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a801-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a801-126">-WhatIf</span></span>
<span data-ttu-id="5a801-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5a801-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a801-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5a801-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a801-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a801-129">CommonParameters</span></span>
<span data-ttu-id="5a801-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a801-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a801-131">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a801-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a801-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a801-132">INPUTS</span></span>

### <span data-ttu-id="5a801-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5a801-133">System.String</span></span>

## <span data-ttu-id="5a801-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a801-134">OUTPUTS</span></span>

### <span data-ttu-id="5a801-135">Microsoft. Azure. Management. Redis. modeller. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="5a801-135">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="5a801-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a801-136">NOTES</span></span>

## <span data-ttu-id="5a801-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a801-137">RELATED LINKS</span></span>

[<span data-ttu-id="5a801-138">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="5a801-138">Get-AzRedisCacheKey</span></span>](./Get-AzRedisCacheKey.md)

