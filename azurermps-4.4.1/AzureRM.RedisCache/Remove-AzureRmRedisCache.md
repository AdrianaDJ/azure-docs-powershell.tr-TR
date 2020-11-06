---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Remove-AzureRmRedisCache.md
ms.openlocfilehash: a9a879386bdbc22eef3094e2f1d0cf19cd42cc45
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587808"
---
# <span data-ttu-id="ff300-101">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ff300-101">Remove-AzureRmRedisCache</span></span>

## <span data-ttu-id="ff300-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff300-102">SYNOPSIS</span></span>
<span data-ttu-id="ff300-103">Redis önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ff300-103">Removes a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff300-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ff300-104">SYNTAX</span></span>

```
Remove-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff300-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ff300-105">DESCRIPTION</span></span>
<span data-ttu-id="ff300-106">**Remove-AzureRmRedisCache** cmdlet 'ı, Azure Redis önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ff300-106">The **Remove-AzureRmRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="ff300-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ff300-107">EXAMPLES</span></span>

### <span data-ttu-id="ff300-108">Örnek 1: Redis önbelleğini kaldırma ve sonucu döndürme</span><span class="sxs-lookup"><span data-stu-id="ff300-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="ff300-109">Bu komut, Redis önbelleğini kaldırır ve işlemin başarılı olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ff300-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="ff300-110">Örnek 2: Redis önbelleğini kaldırma ve sonucu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="ff300-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzureRmRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="ff300-111">Bu komut, Redis önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ff300-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="ff300-112">Geçiş parametresi *belirtilmediğinden, işlemin* sonucu görüntülenmiyor.</span><span class="sxs-lookup"><span data-stu-id="ff300-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="ff300-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ff300-113">PARAMETERS</span></span>

### <span data-ttu-id="ff300-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ff300-114">-Force</span></span>
<span data-ttu-id="ff300-115">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="ff300-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ff300-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="ff300-116">-Name</span></span>
<span data-ttu-id="ff300-117">Kaldırılacak kırmızı önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff300-117">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="ff300-118">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ff300-118">-PassThru</span></span>
<span data-ttu-id="ff300-119">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="ff300-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ff300-120">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ff300-120">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ff300-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff300-121">-ResourceGroupName</span></span>
<span data-ttu-id="ff300-122">Kaldırılacak kırmızı önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ff300-122">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="ff300-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="ff300-123">-Confirm</span></span>
<span data-ttu-id="ff300-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ff300-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff300-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff300-125">-WhatIf</span></span>
<span data-ttu-id="ff300-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ff300-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff300-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ff300-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff300-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff300-128">-DefaultProfile</span></span>
<span data-ttu-id="ff300-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ff300-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff300-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff300-130">CommonParameters</span></span>
<span data-ttu-id="ff300-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ff300-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff300-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff300-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff300-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ff300-133">INPUTS</span></span>

### <span data-ttu-id="ff300-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ff300-134">None</span></span>
<span data-ttu-id="ff300-135">Bu cmdlet 'e giriş 'i değere göre değil, ada göre kanal olarak kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ff300-135">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="ff300-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ff300-136">OUTPUTS</span></span>

### <span data-ttu-id="ff300-137">Boole</span><span class="sxs-lookup"><span data-stu-id="ff300-137">Boolean</span></span>
<span data-ttu-id="ff300-138">Özel durum oluşursa $True döndürür.</span><span class="sxs-lookup"><span data-stu-id="ff300-138">Returns $True if no exception occurs.</span></span>

## <span data-ttu-id="ff300-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ff300-139">NOTES</span></span>

## <span data-ttu-id="ff300-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ff300-140">RELATED LINKS</span></span>

[<span data-ttu-id="ff300-141">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ff300-141">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="ff300-142">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ff300-142">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="ff300-143">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ff300-143">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


