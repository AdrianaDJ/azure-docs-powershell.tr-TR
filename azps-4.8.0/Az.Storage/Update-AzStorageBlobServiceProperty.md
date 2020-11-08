---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 84f2303b0907e05bfe03ffacf50f4bcd895500c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266237"
---
# <span data-ttu-id="03037-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="03037-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="03037-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03037-102">SYNOPSIS</span></span>
<span data-ttu-id="03037-103">Azure depolama blob hizmeti için hizmet özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="03037-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="03037-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="03037-104">SYNTAX</span></span>

### <span data-ttu-id="03037-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="03037-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03037-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="03037-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03037-107">Blobservicepropertiesresourceıd</span><span class="sxs-lookup"><span data-stu-id="03037-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-EnableChangeFeed <Boolean>] [-IsVersioningEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03037-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="03037-108">DESCRIPTION</span></span>
<span data-ttu-id="03037-109">**Update-AzStorageBlobServiceProperty** cmdlet 'ı, Azure depolama blob hizmeti için hizmet özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="03037-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="03037-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="03037-110">EXAMPLES</span></span>

### <span data-ttu-id="03037-111">Örnek 1: blob hizmeti DefaultServiceVersion 'ı 2018-03-28 olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="03037-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 2018-03-28
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           :
```

<span data-ttu-id="03037-112">Bu komut, Blob hizmetinin Defaultservicesürümünü 2018-03-28 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="03037-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

### <span data-ttu-id="03037-113">Örnek 2: depolama hesabının blob hizmetinde changefeed 'i etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="03037-113">Example 2: Enable Changefeed on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : True
IsVersioningEnabled           :
```

<span data-ttu-id="03037-114">Bu komut bir depolama hesabının blob hizmetinde changefeed 'i etkinleştirirse, herhangi bir blob düzeyi oluşturma, değiştirme veya silme etkinliği</span><span class="sxs-lookup"><span data-stu-id="03037-114">This command enables Changefeed on Blob service of a Storage account Change feed support in Azure Blob Storage works by listening to a GPv2 or Blob storage account for any blob level creation, modification, or deletion events.</span></span> <span data-ttu-id="03037-115">Ardından, depolama hesabındaki $blobchangefeed kapsayıcısında depolanan BLOB 'lar için sıralı olayların günlüğünü verir.</span><span class="sxs-lookup"><span data-stu-id="03037-115">It then outputs an ordered log of events for the blobs stored in the $blobchangefeed container within the storage account.</span></span> <span data-ttu-id="03037-116">Serileştirilmiş değişiklikler Apache avro dosyası olarak kalıcıdır ve zaman uyumsuz ve artımlı olarak işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="03037-116">The serialized changes are persisted as an Apache Avro file and can be processed asynchronously and incrementally.</span></span>

### <span data-ttu-id="03037-117">Örnek 3: depolama hesabının blob hizmetinde sürüm oluşturmayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="03037-117">Example 3: Enable Versioning on Blob service of a Storage account</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IsVersioningEnabled $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegroup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : False
DeleteRetentionPolicy.Days    : 
RestorePolicy.Enabled         : 
RestorePolicy.Days            : 
ChangeFeed                    : 
IsVersioningEnabled           : True
```

<span data-ttu-id="03037-118">Bu komut, depolama hesabının blob hizmetinde sürüm oluşturmayı olanaklı kılar</span><span class="sxs-lookup"><span data-stu-id="03037-118">This command enables Versioning on Blob service of a Storage account</span></span>

## <span data-ttu-id="03037-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="03037-119">PARAMETERS</span></span>

### <span data-ttu-id="03037-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03037-120">-DefaultProfile</span></span>
<span data-ttu-id="03037-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="03037-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03037-122">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="03037-122">-DefaultServiceVersion</span></span>
<span data-ttu-id="03037-123">Ayarlanacak varsayılan hizmet sürümü</span><span class="sxs-lookup"><span data-stu-id="03037-123">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03037-124">-EnableChangeFeed</span><span class="sxs-lookup"><span data-stu-id="03037-124">-EnableChangeFeed</span></span>
<span data-ttu-id="03037-125">Depolama hesabı için günlük kaydını Değiştir 'i $true olarak ayarlayarak, $false olarak ayarlayarak akış günlüğünü Değiştir 'i devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="03037-125">Enable Change Feed logging for the storage account by set to $true, disable Change Feed logging by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03037-126">-Isversioningenabled</span><span class="sxs-lookup"><span data-stu-id="03037-126">-IsVersioningEnabled</span></span>
<span data-ttu-id="03037-127">Doğru olarak ayarlandığında sürüm oluşturma özelliği etkin olur veya ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="03037-127">Gets or sets versioning is enabled if set to true.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03037-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03037-128">-ResourceGroupName</span></span>
<span data-ttu-id="03037-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="03037-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03037-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="03037-130">-ResourceId</span></span>
<span data-ttu-id="03037-131">Depolama hesabı kaynak kimliği veya blob hizmeti özellikleri kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="03037-131">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03037-132">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="03037-132">-StorageAccount</span></span>
<span data-ttu-id="03037-133">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="03037-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03037-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="03037-134">-StorageAccountName</span></span>
<span data-ttu-id="03037-135">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="03037-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03037-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="03037-136">-Confirm</span></span>
<span data-ttu-id="03037-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="03037-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03037-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03037-138">-WhatIf</span></span>
<span data-ttu-id="03037-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="03037-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03037-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="03037-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03037-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03037-141">CommonParameters</span></span>
<span data-ttu-id="03037-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="03037-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03037-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03037-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03037-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="03037-144">INPUTS</span></span>

### <span data-ttu-id="03037-145">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="03037-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="03037-146">System. String</span><span class="sxs-lookup"><span data-stu-id="03037-146">System.String</span></span>

## <span data-ttu-id="03037-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="03037-147">OUTPUTS</span></span>

### <span data-ttu-id="03037-148">Microsoft. Azure. Commands. Management. Storage. model. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="03037-148">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="03037-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="03037-149">NOTES</span></span>

## <span data-ttu-id="03037-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="03037-150">RELATED LINKS</span></span>
