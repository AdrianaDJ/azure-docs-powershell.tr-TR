---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: 0edfec1d98423f444b2291d43e6f2a3489e20b29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593026"
---
# <span data-ttu-id="ed2c9-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ed2c9-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="ed2c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed2c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2c9-103">Azure Redis önbelleğinden verileri bir kapsayıcıya aktarır.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed2c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed2c9-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed2c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed2c9-105">DESCRIPTION</span></span>
<span data-ttu-id="ed2c9-106">**Export-AzureRmRedisCache** cmdlet 'ı Azure Redis Cache 'den bir kapsayıcıya veri aktarır.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="ed2c9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed2c9-107">EXAMPLES</span></span>

### <span data-ttu-id="ed2c9-108">Örnek 1: verileri dışarı aktarma</span><span class="sxs-lookup"><span data-stu-id="ed2c9-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="ed2c9-109">Bu komut, Azure Redis önbellek örneğindeki verileri SAS URL 'SI tarafından belirtilen kapsayıcıya aktarır.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="ed2c9-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed2c9-110">PARAMETERS</span></span>

### <span data-ttu-id="ed2c9-111">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="ed2c9-111">-Container</span></span>
<span data-ttu-id="ed2c9-112">Bu cmdlet 'in verileri dışarı aktardığı kapsayıcının hizmet SAS URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="ed2c9-113">Aşağıdaki PowerShell komutlarını kullanarak bir hizmet SAS URL 'SI oluşturabilirsiniz:</span><span class="sxs-lookup"><span data-stu-id="ed2c9-113">You can generate a Service SAS URL using the following PowerShell commands:</span></span>

<span data-ttu-id="ed2c9-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "Key"</span><span class="sxs-lookup"><span data-stu-id="ed2c9-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="ed2c9-115">$sasKeyForContainer = New-AzureStorageContainerSASToken-Name "kapsayıcıadı"-Permission "rwdl"-başlangıçsaati ([System. DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DATETIME]:: Now). AddHours (5)-bağlam $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="ed2c9-115">$sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span> 

<span data-ttu-id="ed2c9-116">Export-AzureRmRedisCache-ResourceGroupName "Kaynakgrupadı"-ad "cacheName"-prefix "blobprefix"-Container ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="ed2c9-116">Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="ed2c9-117">Biçimli</span><span class="sxs-lookup"><span data-stu-id="ed2c9-117">-Format</span></span>
<span data-ttu-id="ed2c9-118">Blob için biçim belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-118">Specifies a format for the blob.</span></span>
<span data-ttu-id="ed2c9-119">Şu anda RDB, desteklenen tek biçimdir.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-119">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="ed2c9-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed2c9-120">-Name</span></span>
<span data-ttu-id="ed2c9-121">Bir önbelleğin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-121">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="ed2c9-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="ed2c9-122">-PassThru</span></span>
<span data-ttu-id="ed2c9-123">Bu cmdlet 'in işlemin başarılı olup olmadığını belirten bir Boole değeri döndürdüğünden emin olur.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-123">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="ed2c9-124">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ed2c9-125">-Önek</span><span class="sxs-lookup"><span data-stu-id="ed2c9-125">-Prefix</span></span>
<span data-ttu-id="ed2c9-126">Blob adları için kullanılacak bir önek belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-126">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="ed2c9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed2c9-127">-ResourceGroupName</span></span>
<span data-ttu-id="ed2c9-128">Önbelleği içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-128">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="ed2c9-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2c9-129">-DefaultProfile</span></span>
<span data-ttu-id="ed2c9-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed2c9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2c9-131">CommonParameters</span></span>
<span data-ttu-id="ed2c9-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2c9-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed2c9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2c9-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed2c9-134">INPUTS</span></span>

### <span data-ttu-id="ed2c9-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ed2c9-135">None</span></span>
<span data-ttu-id="ed2c9-136">Bu cmdlet 'e girişi, değer olarak değil, özellik adıyla yöneltme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ed2c9-136">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="ed2c9-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed2c9-137">OUTPUTS</span></span>

### <span data-ttu-id="ed2c9-138">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ed2c9-138">None</span></span>

## <span data-ttu-id="ed2c9-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed2c9-139">NOTES</span></span>
* <span data-ttu-id="ed2c9-140">Anahtar sözcükler: Azure, azurerm, ARM, Resource, Management, Manager, Redis, Cache, Web, WebApp, Web sitesi</span><span class="sxs-lookup"><span data-stu-id="ed2c9-140">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="ed2c9-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed2c9-141">RELATED LINKS</span></span>

[<span data-ttu-id="ed2c9-142">Import-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ed2c9-142">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="ed2c9-143">Yeni-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ed2c9-143">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="ed2c9-144">Remove-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ed2c9-144">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="ed2c9-145">Reset-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ed2c9-145">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="ed2c9-146">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="ed2c9-146">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


