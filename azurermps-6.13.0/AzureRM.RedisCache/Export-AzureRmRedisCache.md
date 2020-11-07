---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/export-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: ceba71f729de627e0e7231b9c295d0cad1ccc105
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763442"
---
# <span data-ttu-id="a1d78-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a1d78-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="a1d78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1d78-102">SYNOPSIS</span></span>
<span data-ttu-id="a1d78-103">Azure Redis önbelleğinden verileri bir kapsayıcıya aktarır.</span><span class="sxs-lookup"><span data-stu-id="a1d78-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1d78-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a1d78-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1d78-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a1d78-105">DESCRIPTION</span></span>
<span data-ttu-id="a1d78-106">**Export-AzureRmRedisCache** cmdlet 'ı Azure Redis Cache 'den bir kapsayıcıya veri aktarır.</span><span class="sxs-lookup"><span data-stu-id="a1d78-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="a1d78-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a1d78-107">EXAMPLES</span></span>

### <span data-ttu-id="a1d78-108">Örnek 1: verileri dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="a1d78-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="a1d78-109">Bu komut, Azure Redis önbellek örneğindeki verileri SAS URL 'SI tarafından belirtilen kapsayıcıya aktarır.</span><span class="sxs-lookup"><span data-stu-id="a1d78-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="a1d78-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a1d78-110">PARAMETERS</span></span>

### <span data-ttu-id="a1d78-111">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="a1d78-111">-Container</span></span>
<span data-ttu-id="a1d78-112">Bu cmdlet 'in verileri dışarı aktardığı kapsayıcının hizmet SAS URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1d78-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="a1d78-113">Aşağıdaki PowerShell komutlarını kullanarak bir hizmet SAS URL 'SI oluşturabilirsiniz: $storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "Key" $sasKeyForContainer = New-AzureStorageContainerSASToken-Name "kapsayıcıadı AddMinutes (-15)-ExpiryTime ([System. DATETIME]:: Now). AddHours (5)-bağlam $storageAccountContext-FullUri Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-prefix "blobprefix"-Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="a1d78-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="a1d78-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1d78-114">-DefaultProfile</span></span>
<span data-ttu-id="a1d78-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a1d78-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1d78-116">Biçimli</span><span class="sxs-lookup"><span data-stu-id="a1d78-116">-Format</span></span>
<span data-ttu-id="a1d78-117">Blob için biçim belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1d78-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="a1d78-118">Şu anda RDB, desteklenen tek biçimdir.</span><span class="sxs-lookup"><span data-stu-id="a1d78-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="a1d78-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="a1d78-119">-Name</span></span>
<span data-ttu-id="a1d78-120">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1d78-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="a1d78-121">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a1d78-121">-PassThru</span></span>
<span data-ttu-id="a1d78-122">Bu cmdlet 'in işlemin başarılı olup olmadığını belirten bir Boole değeri döndürdüğünden emin olur.</span><span class="sxs-lookup"><span data-stu-id="a1d78-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="a1d78-123">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="a1d78-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a1d78-124">-Önek</span><span class="sxs-lookup"><span data-stu-id="a1d78-124">-Prefix</span></span>
<span data-ttu-id="a1d78-125">Blob adları için kullanılacak bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1d78-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="a1d78-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1d78-126">-ResourceGroupName</span></span>
<span data-ttu-id="a1d78-127">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a1d78-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="a1d78-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="a1d78-128">-Confirm</span></span>
<span data-ttu-id="a1d78-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a1d78-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1d78-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1d78-130">-WhatIf</span></span>
<span data-ttu-id="a1d78-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a1d78-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1d78-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a1d78-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1d78-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1d78-133">CommonParameters</span></span>
<span data-ttu-id="a1d78-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a1d78-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1d78-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1d78-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1d78-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a1d78-136">INPUTS</span></span>

### <span data-ttu-id="a1d78-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a1d78-137">System.String</span></span>

## <span data-ttu-id="a1d78-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a1d78-138">OUTPUTS</span></span>

### <span data-ttu-id="a1d78-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a1d78-139">System.Boolean</span></span>

## <span data-ttu-id="a1d78-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a1d78-140">NOTES</span></span>
* <span data-ttu-id="a1d78-141">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="a1d78-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="a1d78-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a1d78-142">RELATED LINKS</span></span>

[<span data-ttu-id="a1d78-143">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a1d78-143">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="a1d78-144">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a1d78-144">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="a1d78-145">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a1d78-145">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="a1d78-146">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a1d78-146">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="a1d78-147">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="a1d78-147">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)

