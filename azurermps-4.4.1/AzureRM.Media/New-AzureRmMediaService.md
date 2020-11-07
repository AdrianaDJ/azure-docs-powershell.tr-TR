---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaService.md
ms.openlocfilehash: 86f1667c1383f226d47afed2a842af6386dad81e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763700"
---
# <span data-ttu-id="2b405-101">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="2b405-101">New-AzureRmMediaService</span></span>

## <span data-ttu-id="2b405-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b405-102">SYNOPSIS</span></span>
<span data-ttu-id="2b405-103">Medya hizmeti oluşturur medya hizmeti zaten varsa, tüm özellikleri sağlanan girişle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2b405-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b405-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b405-104">SYNTAX</span></span>

### <span data-ttu-id="2b405-105">Storageaccountivseçparametre</span><span class="sxs-lookup"><span data-stu-id="2b405-105">StorageAccountIdParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b405-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="2b405-106">StorageAccountsParamSet</span></span>
```
New-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b405-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b405-107">DESCRIPTION</span></span>
<span data-ttu-id="2b405-108">**Yeni-AzureRmMediaService** cmdlet 'i bir medya hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b405-108">The **New-AzureRmMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="2b405-109">Medya hizmeti zaten varsa, bu cmdlet 'in özelliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="2b405-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="2b405-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b405-110">EXAMPLES</span></span>

### <span data-ttu-id="2b405-111">Example1: yalnızca birincil depolama hesabıyla medya hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b405-111">Example1: Create a media service with the primary storage account only</span></span>
```
PS C:\># Variables
## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName = "Storage1"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tags $Tags
```

<span data-ttu-id="2b405-112">Bu örnekte, yalnızca birincil depolama hesabı belirtilerek medya hizmeti oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="2b405-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="2b405-113">Bu komut dosyası birkaç başka cmdlet kullanır.</span><span class="sxs-lookup"><span data-stu-id="2b405-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="2b405-114">Örnek 2: birden çok depolama ile medya hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b405-114">Example 2: Create a media service with multiple storage</span></span>
```
PS C:\># Variables

## Global
$ResourceGroupName = "ResourceGroup001"
$Location = "East US"

## Storage
$StorageName1 = "storage1"
$StorageName2 = "storage2"
$StorageType = "Standard_GRS"

## Media Service
$Tags = @{"tag1" = "value1"; "tag2" = "value2"}
$MediaServiceName = "MediaService1"

# Resource Group
PS C:\> New-AzureRmResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzureRmMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tags $Tags
```

<span data-ttu-id="2b405-115">Bu örnekte, birden fazla depolama hesabı içeren bir medya hizmeti oluşturulması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="2b405-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="2b405-116">Bu komut dosyası birkaç başka cmdlet kullanır.</span><span class="sxs-lookup"><span data-stu-id="2b405-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="2b405-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b405-117">PARAMETERS</span></span>

### <span data-ttu-id="2b405-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2b405-118">-AccountName</span></span>
<span data-ttu-id="2b405-119">Bu cmdlet 'in oluşturduğu medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b405-119">Specifies the name of the media service that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b405-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="2b405-120">-Location</span></span>
<span data-ttu-id="2b405-121">Bu cmdlet 'in medya hizmetini oluşturduğu bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b405-121">Specifies the region that this cmdlet creates the media service in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b405-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b405-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b405-123">Medya hizmetinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b405-123">Specifies the name of the resource group that the media service is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b405-124">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="2b405-124">-StorageAccountId</span></span>
<span data-ttu-id="2b405-125">Medya Hizmeti hesabıyla ilişkilendirilmiş depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b405-125">Specifies the storage account associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: StorageAccountIdParamSet
Aliases: Id

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b405-126">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="2b405-126">-StorageAccounts</span></span>
<span data-ttu-id="2b405-127">Medya hizmetiyle ilişkilendirilecek bir depolama hesapları dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b405-127">Specifies an array of storage accounts to associate with the media service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]
Parameter Sets: StorageAccountsParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b405-128">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="2b405-128">-Tags</span></span>
<span data-ttu-id="2b405-129">Medya hizmeti için Etiketler belirtir.</span><span class="sxs-lookup"><span data-stu-id="2b405-129">Specifies tags for the media service.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b405-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="2b405-130">-Confirm</span></span>
<span data-ttu-id="2b405-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2b405-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b405-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b405-132">-WhatIf</span></span>
<span data-ttu-id="2b405-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b405-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b405-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2b405-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b405-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b405-135">-DefaultProfile</span></span>
<span data-ttu-id="2b405-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2b405-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b405-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b405-137">CommonParameters</span></span>
<span data-ttu-id="2b405-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b405-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b405-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b405-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b405-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b405-140">INPUTS</span></span>

## <span data-ttu-id="2b405-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b405-141">OUTPUTS</span></span>

### <span data-ttu-id="2b405-142">Microsoft. Azure. Commands. Media. modeller. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="2b405-142">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="2b405-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b405-143">NOTES</span></span>

## <span data-ttu-id="2b405-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b405-144">RELATED LINKS</span></span>

[<span data-ttu-id="2b405-145">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="2b405-145">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="2b405-146">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="2b405-146">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="2b405-147">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="2b405-147">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)

