---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/remove-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: 4e49fbd2ac2604dab09d79255e7134fee02afd97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589713"
---
# <span data-ttu-id="a7bc3-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a7bc3-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="a7bc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="a7bc3-103">Redis önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7bc3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7bc3-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7bc3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7bc3-105">DESCRIPTION</span></span>
<span data-ttu-id="a7bc3-106">**Remove-AzureRmRedisCache** cmdlet 'ı, Azure Redis önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="a7bc3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7bc3-107">EXAMPLES</span></span>

### <span data-ttu-id="a7bc3-108">Örnek 1: Redis önbelleğini kaldırma ve sonucu döndürme</span><span class="sxs-lookup"><span data-stu-id="a7bc3-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="a7bc3-109">Bu komut, Redis önbelleğini kaldırır ve işlemin başarılı olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="a7bc3-110">Örnek 2: Redis önbelleğini kaldırma ve sonucu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a7bc3-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="a7bc3-111">Bu komut, Redis önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="a7bc3-112">Geçiş parametresi *belirtilmediğinden, işlemin* sonucu görüntülenmiyor.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="a7bc3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7bc3-113">PARAMETERS</span></span>

### <span data-ttu-id="a7bc3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7bc3-114">-DefaultProfile</span></span>
<span data-ttu-id="a7bc3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a7bc3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a7bc3-116">-Force</span></span>
<span data-ttu-id="a7bc3-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a7bc3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7bc3-118">-Name</span></span>
<span data-ttu-id="a7bc3-119">Kaldırılacak kırmızı önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="a7bc3-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a7bc3-120">-PassThru</span></span>
<span data-ttu-id="a7bc3-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a7bc3-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a7bc3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7bc3-123">-ResourceGroupName</span></span>
<span data-ttu-id="a7bc3-124">Kaldırılacak kırmızı önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="a7bc3-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7bc3-125">-Confirm</span></span>
<span data-ttu-id="a7bc3-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7bc3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7bc3-127">-WhatIf</span></span>
<span data-ttu-id="a7bc3-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7bc3-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7bc3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7bc3-130">CommonParameters</span></span>
<span data-ttu-id="a7bc3-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7bc3-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7bc3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7bc3-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7bc3-133">INPUTS</span></span>

### <span data-ttu-id="a7bc3-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a7bc3-134">None</span></span>
<span data-ttu-id="a7bc3-135">Bu cmdlet 'e giriş 'i değere göre değil, ada göre kanal olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-135">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="a7bc3-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7bc3-136">OUTPUTS</span></span>

### <span data-ttu-id="a7bc3-137">Boole</span><span class="sxs-lookup"><span data-stu-id="a7bc3-137">Boolean</span></span>
<span data-ttu-id="a7bc3-138">Özel durum oluşursa $True döndürür.</span><span class="sxs-lookup"><span data-stu-id="a7bc3-138">Returns $True if no exception occurs.</span></span>

## <span data-ttu-id="a7bc3-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7bc3-139">NOTES</span></span>

## <span data-ttu-id="a7bc3-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7bc3-140">RELATED LINKS</span></span>

[<span data-ttu-id="a7bc3-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a7bc3-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="a7bc3-142">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a7bc3-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="a7bc3-143">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a7bc3-143">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


