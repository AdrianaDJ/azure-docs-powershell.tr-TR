---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: A22D930B-5026-4915-B498-EE31153E1E9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/remove-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Remove-AzRedisCache.md
ms.openlocfilehash: 4b7719a43535de4af595e634dea2061ab9cba19d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276558"
---
# <span data-ttu-id="b5646-101">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b5646-101">Remove-AzRedisCache</span></span>

## <span data-ttu-id="b5646-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5646-102">SYNOPSIS</span></span>
<span data-ttu-id="b5646-103">Redis önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5646-103">Removes a Redis Cache.</span></span>

## <span data-ttu-id="b5646-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b5646-104">SYNTAX</span></span>

```
Remove-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5646-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b5646-105">DESCRIPTION</span></span>
<span data-ttu-id="b5646-106">**Remove-AzRedisCache** cmdlet 'ı, Azure Redis önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5646-106">The **Remove-AzRedisCache** cmdlet removes an Azure Redis Cache.</span></span>

## <span data-ttu-id="b5646-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b5646-107">EXAMPLES</span></span>

### <span data-ttu-id="b5646-108">Örnek 1: Redis önbelleğini kaldırma ve sonucu döndürme</span><span class="sxs-lookup"><span data-stu-id="b5646-108">Example 1: Remove a Redis Cache and return the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force -PassThru
True
```

<span data-ttu-id="b5646-109">Bu komut, Redis önbelleğini kaldırır ve işlemin başarılı olup olmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5646-109">This command removes a Redis Cache and displays whether the operation is successful.</span></span>

### <span data-ttu-id="b5646-110">Örnek 2: Redis önbelleğini kaldırma ve sonucu görüntüleme</span><span class="sxs-lookup"><span data-stu-id="b5646-110">Example 2: Remove a Redis Cache and do not display the result</span></span>
```
PS C:\>Remove-AzRedisCache -ResourceGroupName "ResourceGroup03" -Name "myCache" -Force
```

<span data-ttu-id="b5646-111">Bu komut, Redis önbelleğini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b5646-111">This command removes a Redis Cache.</span></span>
<span data-ttu-id="b5646-112">Geçiş parametresi *belirtilmediğinden, işlemin* sonucu görüntülenmiyor.</span><span class="sxs-lookup"><span data-stu-id="b5646-112">Because the *PassThru* parameter is not specified, the result of the operation is not displayed.</span></span>

## <span data-ttu-id="b5646-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b5646-113">PARAMETERS</span></span>

### <span data-ttu-id="b5646-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5646-114">-DefaultProfile</span></span>
<span data-ttu-id="b5646-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b5646-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5646-116">-Force</span><span class="sxs-lookup"><span data-stu-id="b5646-116">-Force</span></span>
<span data-ttu-id="b5646-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b5646-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b5646-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="b5646-118">-Name</span></span>
<span data-ttu-id="b5646-119">Kaldırılacak kırmızı önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5646-119">Specifies the name of the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="b5646-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="b5646-120">-PassThru</span></span>
<span data-ttu-id="b5646-121">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="b5646-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b5646-122">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="b5646-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b5646-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5646-123">-ResourceGroupName</span></span>
<span data-ttu-id="b5646-124">Kaldırılacak kırmızı önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b5646-124">Specifies the name of the resource group that contains the Redis Cache to remove.</span></span>

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

### <span data-ttu-id="b5646-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="b5646-125">-Confirm</span></span>
<span data-ttu-id="b5646-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b5646-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5646-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5646-127">-WhatIf</span></span>
<span data-ttu-id="b5646-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b5646-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5646-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b5646-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5646-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5646-130">CommonParameters</span></span>
<span data-ttu-id="b5646-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b5646-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5646-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5646-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5646-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b5646-133">INPUTS</span></span>

### <span data-ttu-id="b5646-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b5646-134">System.String</span></span>

## <span data-ttu-id="b5646-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b5646-135">OUTPUTS</span></span>

### <span data-ttu-id="b5646-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5646-136">System.Boolean</span></span>

## <span data-ttu-id="b5646-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b5646-137">NOTES</span></span>

## <span data-ttu-id="b5646-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b5646-138">RELATED LINKS</span></span>

[<span data-ttu-id="b5646-139">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b5646-139">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="b5646-140">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b5646-140">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="b5646-141">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="b5646-141">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


