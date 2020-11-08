---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: fb44ca997fd3b7599c25c5ba986ed0ca0771b3e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098981"
---
# <span data-ttu-id="778f1-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="778f1-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="778f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="778f1-102">SYNOPSIS</span></span>
<span data-ttu-id="778f1-103">Azure Redis önbelleğinden verileri bir kapsayıcıya aktarır.</span><span class="sxs-lookup"><span data-stu-id="778f1-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="778f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="778f1-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="778f1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="778f1-105">DESCRIPTION</span></span>
<span data-ttu-id="778f1-106">**Export-AzRedisCache** cmdlet 'ı Azure Redis önbelleğinden bir kapsayıcıya veri aktarır.</span><span class="sxs-lookup"><span data-stu-id="778f1-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="778f1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="778f1-107">EXAMPLES</span></span>

### <span data-ttu-id="778f1-108">Örnek 1: verileri dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="778f1-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="778f1-109">Bu komut, Azure Redis önbellek örneğindeki verileri SAS URL 'SI tarafından belirtilen kapsayıcıya aktarır.</span><span class="sxs-lookup"><span data-stu-id="778f1-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="778f1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="778f1-110">PARAMETERS</span></span>

### <span data-ttu-id="778f1-111">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="778f1-111">-Container</span></span>
<span data-ttu-id="778f1-112">Bu cmdlet 'in verileri dışarı aktardığı kapsayıcının hizmet SAS URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="778f1-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="778f1-113">Aşağıdaki PowerShell komutlarını kullanarak bir hizmet SAS URL 'SI oluşturabilirsiniz: $storageAccountContext = New-AzStorageContext-StorageAccountName "storageName"-StorageAccountKey "Key" $sasKeyForContainer = New-AzStorageContainerSASToken-Name "kapsayıcıadı AddMinutes (-15)-ExpiryTime ([System. DATETIME]:: Now). AddHours (5)-bağlam $storageAccountContext-FullUri Export-AzRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-prefix "blobprefix"-Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="778f1-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="778f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778f1-114">-DefaultProfile</span></span>
<span data-ttu-id="778f1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="778f1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="778f1-116">Biçimli</span><span class="sxs-lookup"><span data-stu-id="778f1-116">-Format</span></span>
<span data-ttu-id="778f1-117">Blob için biçim belirtir.</span><span class="sxs-lookup"><span data-stu-id="778f1-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="778f1-118">Şu anda RDB, desteklenen tek biçimdir.</span><span class="sxs-lookup"><span data-stu-id="778f1-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="778f1-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="778f1-119">-Name</span></span>
<span data-ttu-id="778f1-120">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="778f1-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="778f1-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="778f1-121">-PassThru</span></span>
<span data-ttu-id="778f1-122">Bu cmdlet 'in işlemin başarılı olup olmadığını belirten bir Boole değeri döndürdüğünden emin olur.</span><span class="sxs-lookup"><span data-stu-id="778f1-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="778f1-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="778f1-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="778f1-124">-Önek</span><span class="sxs-lookup"><span data-stu-id="778f1-124">-Prefix</span></span>
<span data-ttu-id="778f1-125">Blob adları için kullanılacak bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="778f1-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="778f1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="778f1-126">-ResourceGroupName</span></span>
<span data-ttu-id="778f1-127">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="778f1-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="778f1-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="778f1-128">-Confirm</span></span>
<span data-ttu-id="778f1-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="778f1-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="778f1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="778f1-130">-WhatIf</span></span>
<span data-ttu-id="778f1-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="778f1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="778f1-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="778f1-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="778f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778f1-133">CommonParameters</span></span>
<span data-ttu-id="778f1-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="778f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778f1-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="778f1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778f1-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="778f1-136">INPUTS</span></span>

### <span data-ttu-id="778f1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="778f1-137">System.String</span></span>

## <span data-ttu-id="778f1-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="778f1-138">OUTPUTS</span></span>

### <span data-ttu-id="778f1-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="778f1-139">System.Boolean</span></span>

## <span data-ttu-id="778f1-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="778f1-140">NOTES</span></span>
* <span data-ttu-id="778f1-141">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="778f1-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="778f1-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="778f1-142">RELATED LINKS</span></span>

[<span data-ttu-id="778f1-143">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="778f1-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="778f1-144">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="778f1-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="778f1-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="778f1-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="778f1-146">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="778f1-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="778f1-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="778f1-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


