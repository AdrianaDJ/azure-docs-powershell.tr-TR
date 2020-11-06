---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 1F86CE62-AA01-44FB-A935-484EC51DDE5A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCacheKey.md
ms.openlocfilehash: 51fff2f79435c6806b126fbc0a9c120ee8b8842e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573329"
---
# <span data-ttu-id="1050f-101">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="1050f-101">New-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="1050f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1050f-102">SYNOPSIS</span></span>
<span data-ttu-id="1050f-103">Kırmızı bir önbelleğin erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1050f-103">Regenerates the access key of a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1050f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1050f-104">SYNTAX</span></span>

```
New-AzureRmRedisCacheKey [-ResourceGroupName <String>] -Name <String> -KeyType <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1050f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1050f-105">DESCRIPTION</span></span>
<span data-ttu-id="1050f-106">**Yeni-AzureRmRedisCacheKey** cmdlet 'ı, Azure Redis önbelleğinin erişim anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1050f-106">The **New-AzureRmRedisCacheKey** cmdlet regenerates the access key of an Azure Redis Cache.</span></span>

## <span data-ttu-id="1050f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1050f-107">EXAMPLES</span></span>

### <span data-ttu-id="1050f-108">Örnek 1: Birinci anahtarı yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="1050f-108">Example 1: Regenerate a primary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Primary" -Force

          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="1050f-109">Bu komut, Redis önbelleğinin birincil anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1050f-109">This command regenerates the primary key of a Redis Cache.</span></span>

### <span data-ttu-id="1050f-110">Örnek 2: ikincil anahtarı yeniden oluşturma</span><span class="sxs-lookup"><span data-stu-id="1050f-110">Example 2: Regenerate a secondary key</span></span>
```
PS C:\>New-AzureRmRedisCacheKey -ResourceGroupName "ResourceGroup03" -Name "myCache" -KeyType "Secondary" -Force
          PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=

          SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="1050f-111">Bu komut, Redis önbelleğinin ikincil anahtarını yeniden oluşturur.</span><span class="sxs-lookup"><span data-stu-id="1050f-111">This command regenerates the secondary key of a Redis Cache.</span></span>

## <span data-ttu-id="1050f-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1050f-112">PARAMETERS</span></span>

### <span data-ttu-id="1050f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1050f-113">-DefaultProfile</span></span>
<span data-ttu-id="1050f-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1050f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1050f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1050f-115">-Force</span></span>
<span data-ttu-id="1050f-116">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="1050f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1050f-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="1050f-117">-KeyType</span></span>
<span data-ttu-id="1050f-118">Birincil veya ikincil erişim anahtarının yeniden oluşturulup oluşturulmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1050f-118">Specifies whether to regenerate the primary or secondary access key.</span></span>
<span data-ttu-id="1050f-119">Geçerli değerler: Primary, Secondary.</span><span class="sxs-lookup"><span data-stu-id="1050f-119">Valid values are: Primary, Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1050f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="1050f-120">-Name</span></span>
<span data-ttu-id="1050f-121">Redis önbelleğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1050f-121">Specifies the name of the Redis Cache.</span></span>

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

### <span data-ttu-id="1050f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1050f-122">-ResourceGroupName</span></span>
<span data-ttu-id="1050f-123">Redis önbelleğini içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1050f-123">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="1050f-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="1050f-124">-Confirm</span></span>
<span data-ttu-id="1050f-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="1050f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1050f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1050f-126">-WhatIf</span></span>
<span data-ttu-id="1050f-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="1050f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1050f-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="1050f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1050f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1050f-129">CommonParameters</span></span>
<span data-ttu-id="1050f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1050f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1050f-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1050f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1050f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1050f-132">INPUTS</span></span>

### <span data-ttu-id="1050f-133">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="1050f-133">None</span></span>
<span data-ttu-id="1050f-134">Bu cmdlet 'e giriş 'i değere göre değil, ada göre kanal olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="1050f-134">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="1050f-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1050f-135">OUTPUTS</span></span>

### <span data-ttu-id="1050f-136">Microsoft. Azure. Management. Redis. modeller. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="1050f-136">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="1050f-137">Bu cmdlet, Redis önbelleğinin birincil ve ikincil erişim anahtarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="1050f-137">This cmdlet returns the primary and secondary access key of a Redis Cache.</span></span>

## <span data-ttu-id="1050f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1050f-138">NOTES</span></span>

## <span data-ttu-id="1050f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1050f-139">RELATED LINKS</span></span>

[<span data-ttu-id="1050f-140">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="1050f-140">Get-AzureRmRedisCacheKey</span></span>](./Get-AzureRmRedisCacheKey.md)


