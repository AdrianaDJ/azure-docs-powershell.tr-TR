---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/import-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Import-AzRedisCache.md
ms.openlocfilehash: 018518f359c1142f9e20536f795b9080a942beaa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759553"
---
# <span data-ttu-id="7c9e5-101">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7c9e5-101">Import-AzRedisCache</span></span>

## <span data-ttu-id="7c9e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c9e5-102">SYNOPSIS</span></span>
<span data-ttu-id="7c9e5-103">Verileri blob 'dan Azure Redis Cache 'e aktarır.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-103">Imports data from blobs to Azure Redis Cache.</span></span>

## <span data-ttu-id="7c9e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c9e5-104">SYNTAX</span></span>

```
Import-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c9e5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c9e5-105">DESCRIPTION</span></span>
<span data-ttu-id="7c9e5-106">**Import-AzRedisCache** cmdlet 'i blob 'Dan Azure Redis Cache 'e aktarır.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-106">The **Import-AzRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="7c9e5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c9e5-107">EXAMPLES</span></span>

### <span data-ttu-id="7c9e5-108">Örnek 1: veri Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="7c9e5-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="7c9e5-109">Bu komut, SAS URL 'SI tarafından belirtilen blob 'dan Azure redin önbelleğine veri aktarır.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="7c9e5-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c9e5-110">PARAMETERS</span></span>

### <span data-ttu-id="7c9e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c9e5-111">-DefaultProfile</span></span>
<span data-ttu-id="7c9e5-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c9e5-113">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="7c9e5-113">-Files</span></span>
<span data-ttu-id="7c9e5-114">Bu cmdlet 'in önbelleğe aldığı blob 'ların SAS URL 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="7c9e5-115">Aşağıdaki PowerShell komutlarını kullanarak SAS URL 'Leri oluşturabilirsiniz: $storageAccountContext = New-AzStorageContext-StorageAccountName "storageName"-StorageAccountKey "Key" $sasKeyForBlob = New-AzStorageBlobSASToken-Container "Kapsayıcıadı ()" Blobadı "-Permission" rwdl "-StartTime ([System. DATETIME]:: Now). AddMinutes (-15)-ExpiryTime ([System. DATETIME]:: Now). AddHours (5)-bağlam $storageAccountContext-FullUri Import-AzRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-dosyalar ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="7c9e5-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c9e5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="7c9e5-116">-Force</span></span>
<span data-ttu-id="7c9e5-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c9e5-118">Biçimli</span><span class="sxs-lookup"><span data-stu-id="7c9e5-118">-Format</span></span>
<span data-ttu-id="7c9e5-119">Blob 'un biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="7c9e5-120">Şu anda RDB, desteklenen tek biçimdir.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="7c9e5-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="7c9e5-121">-Name</span></span>
<span data-ttu-id="7c9e5-122">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="7c9e5-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7c9e5-123">-PassThru</span></span>
<span data-ttu-id="7c9e5-124">Bu cmdlet 'in işlemin başarılı olup olmadığını belirten bir Boole değeri döndürdüğünden emin olur.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="7c9e5-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7c9e5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c9e5-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c9e5-127">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="7c9e5-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="7c9e5-128">-Confirm</span></span>
<span data-ttu-id="7c9e5-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c9e5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c9e5-130">-WhatIf</span></span>
<span data-ttu-id="7c9e5-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c9e5-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c9e5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c9e5-133">CommonParameters</span></span>
<span data-ttu-id="7c9e5-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c9e5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c9e5-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c9e5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c9e5-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c9e5-136">INPUTS</span></span>

### <span data-ttu-id="7c9e5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7c9e5-137">System.String</span></span>

### <span data-ttu-id="7c9e5-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="7c9e5-138">System.String[]</span></span>

## <span data-ttu-id="7c9e5-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c9e5-139">OUTPUTS</span></span>

### <span data-ttu-id="7c9e5-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7c9e5-140">System.Boolean</span></span>

## <span data-ttu-id="7c9e5-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c9e5-141">NOTES</span></span>
* <span data-ttu-id="7c9e5-142">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="7c9e5-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="7c9e5-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c9e5-143">RELATED LINKS</span></span>

[<span data-ttu-id="7c9e5-144">Dışarı aktarma-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7c9e5-144">Export-AzRedisCache</span></span>](./Export-AzRedisCache.md)

[<span data-ttu-id="7c9e5-145">Yeni-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7c9e5-145">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="7c9e5-146">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7c9e5-146">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="7c9e5-147">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7c9e5-147">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="7c9e5-148">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="7c9e5-148">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


