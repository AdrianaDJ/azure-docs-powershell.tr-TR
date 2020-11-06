---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: BC00DEF9-6A93-4DF5-8E5B-C488551BA1D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/import-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Import-AzureRmRedisCache.md
ms.openlocfilehash: 278afd493d66fdc817bd61b0a11e15b1c6b54391
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592759"
---
# <span data-ttu-id="23593-101">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23593-101">Import-AzureRmRedisCache</span></span>

## <span data-ttu-id="23593-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23593-102">SYNOPSIS</span></span>
<span data-ttu-id="23593-103">Verileri blob 'dan Azure Redis Cache 'e aktarır.</span><span class="sxs-lookup"><span data-stu-id="23593-103">Imports data from blobs to Azure Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23593-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="23593-104">SYNTAX</span></span>

```
Import-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Files <String[]> [-Format <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23593-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="23593-105">DESCRIPTION</span></span>
<span data-ttu-id="23593-106">**Import-AzureRmRedisCache** cmdlet 'i Bloblardan Azure Redis Cache 'e aktarır.</span><span class="sxs-lookup"><span data-stu-id="23593-106">The **Import-AzureRmRedisCache** cmdlet imports data from blobs into Azure Redis Cache.</span></span>

## <span data-ttu-id="23593-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="23593-107">EXAMPLES</span></span>

### <span data-ttu-id="23593-108">Örnek 1: veri Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="23593-108">Example 1: Import data</span></span>
```
PS C:\>Import-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Files @("https://mystorageaccount.blob.core.windows.net/container22/blobname?sv=2015-04-05&sr=b&sig=caIwutG2uDa0NZ8mjdNJdgOY8%2F8mhwRuGNdICU%2B0pI4%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwd") -Force
```

<span data-ttu-id="23593-109">Bu komut, SAS URL 'SI tarafından belirtilen blob 'dan Azure redin önbelleğine veri aktarır.</span><span class="sxs-lookup"><span data-stu-id="23593-109">This command imports data from the blob that is specified by the SAS URL into Azure Redis Cache.</span></span>

## <span data-ttu-id="23593-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="23593-110">PARAMETERS</span></span>

### <span data-ttu-id="23593-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23593-111">-DefaultProfile</span></span>
<span data-ttu-id="23593-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="23593-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23593-113">-Dosyalar</span><span class="sxs-lookup"><span data-stu-id="23593-113">-Files</span></span>
<span data-ttu-id="23593-114">Bu cmdlet 'in önbelleğe aldığı blob 'ların SAS URL 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23593-114">Specifies the SAS URLs of blobs whose content this cmdlet imports into the cache.</span></span> <span data-ttu-id="23593-115">Aşağıdaki PowerShell komutlarını kullanarak SAS URL 'Leri oluşturabilirsiniz: $storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "Key" $sasKeyForBlob = New-AzureStorageBlobSASToken-Container "Kapsayıcıadı ()" Blobadı "-Permission" rwdl "-StartTime ([System. DATETIME]:: Now). AddMinutes (-15)-ExpiryTime ([System. DATETIME]:: Now). AddHours (5)-bağlam $storageAccountContext-FullUri Import-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-dosyalar ($sasKeyForBlob)-Force</span><span class="sxs-lookup"><span data-stu-id="23593-115">You can generate the SAS URLs using the following PowerShell commands: $storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForBlob = New-AzureStorageBlobSASToken -Container "containerName" -blob "blobName" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Import-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Files ($sasKeyForBlob) -Force</span></span>

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

### <span data-ttu-id="23593-116">-Force</span><span class="sxs-lookup"><span data-stu-id="23593-116">-Force</span></span>
<span data-ttu-id="23593-117">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="23593-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="23593-118">Biçimli</span><span class="sxs-lookup"><span data-stu-id="23593-118">-Format</span></span>
<span data-ttu-id="23593-119">Blob 'un biçimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="23593-119">Specifies the format of the blob.</span></span>
<span data-ttu-id="23593-120">Şu anda RDB, desteklenen tek biçimdir.</span><span class="sxs-lookup"><span data-stu-id="23593-120">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="23593-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="23593-121">-Name</span></span>
<span data-ttu-id="23593-122">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23593-122">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="23593-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="23593-123">-PassThru</span></span>
<span data-ttu-id="23593-124">Bu cmdlet 'in işlemin başarılı olup olmadığını belirten bir Boole değeri döndürdüğünden emin olur.</span><span class="sxs-lookup"><span data-stu-id="23593-124">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="23593-125">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="23593-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="23593-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23593-126">-ResourceGroupName</span></span>
<span data-ttu-id="23593-127">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="23593-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="23593-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="23593-128">-Confirm</span></span>
<span data-ttu-id="23593-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="23593-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23593-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23593-130">-WhatIf</span></span>
<span data-ttu-id="23593-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="23593-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23593-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="23593-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23593-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23593-133">CommonParameters</span></span>
<span data-ttu-id="23593-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="23593-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23593-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23593-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23593-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="23593-136">INPUTS</span></span>

### <span data-ttu-id="23593-137">System. String</span><span class="sxs-lookup"><span data-stu-id="23593-137">System.String</span></span>

### <span data-ttu-id="23593-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="23593-138">System.String[]</span></span>

## <span data-ttu-id="23593-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="23593-139">OUTPUTS</span></span>

### <span data-ttu-id="23593-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23593-140">System.Boolean</span></span>

## <span data-ttu-id="23593-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="23593-141">NOTES</span></span>
* <span data-ttu-id="23593-142">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="23593-142">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="23593-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="23593-143">RELATED LINKS</span></span>

[<span data-ttu-id="23593-144">Dışarı aktarma-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23593-144">Export-AzureRmRedisCache</span></span>](./Export-AzureRmRedisCache.md)

[<span data-ttu-id="23593-145">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23593-145">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="23593-146">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23593-146">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="23593-147">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23593-147">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="23593-148">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="23593-148">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


