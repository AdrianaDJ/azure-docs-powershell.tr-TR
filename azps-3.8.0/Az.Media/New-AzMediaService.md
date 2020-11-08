---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 5CEA7323-4CF7-42B2-BA94-BB3C8F73D2E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaService.md
ms.openlocfilehash: a7554468824e85dbd922c0fac874ca9d881c13d0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104534"
---
# <span data-ttu-id="f1c2f-101">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f1c2f-101">New-AzMediaService</span></span>

## <span data-ttu-id="f1c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f1c2f-103">Medya hizmeti oluşturur medya hizmeti zaten varsa, tüm özellikleri sağlanan girişle güncelleştirilir.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-103">Creates a media service if the media service already exists, all its properties are updated with the input provided.</span></span>

## <span data-ttu-id="f1c2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1c2f-104">SYNTAX</span></span>

### <span data-ttu-id="f1c2f-105">Storageaccountivseçparametre</span><span class="sxs-lookup"><span data-stu-id="f1c2f-105">StorageAccountIdParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccountId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1c2f-106">StorageAccountsParamSet</span><span class="sxs-lookup"><span data-stu-id="f1c2f-106">StorageAccountsParamSet</span></span>
```
New-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String> [-Location] <String>
 [-StorageAccounts] <PSStorageAccount[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1c2f-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1c2f-107">DESCRIPTION</span></span>
<span data-ttu-id="f1c2f-108">**Yeni-AzMediaService** cmdlet 'i bir medya hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-108">The **New-AzMediaService** cmdlet creates a media service.</span></span>
<span data-ttu-id="f1c2f-109">Medya hizmeti zaten varsa, bu cmdlet 'in özelliklerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-109">If the media service already exists, this cmdlet update its properties.</span></span>

## <span data-ttu-id="f1c2f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1c2f-110">EXAMPLES</span></span>

### <span data-ttu-id="f1c2f-111">Example1: yalnızca birincil depolama hesabıyla medya hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="f1c2f-111">Example1: Create a media service with the primary storage account only</span></span>
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
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName -Location $Location -Type $StorageType

# Media Service
PS C:\> New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccountId $StorageAccount.Id -Tag $Tags
```

<span data-ttu-id="f1c2f-112">Bu örnekte, yalnızca birincil depolama hesabı belirtilerek medya hizmeti oluşturulur.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-112">This example shows how to  create a media service with specifying primary storage account only.</span></span>
<span data-ttu-id="f1c2f-113">Bu komut dosyası birkaç başka cmdlet kullanır.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-113">This script uses several other cmdlets.</span></span>

### <span data-ttu-id="f1c2f-114">Örnek 2: birden çok depolama ile medya hizmeti oluşturma</span><span class="sxs-lookup"><span data-stu-id="f1c2f-114">Example 2: Create a media service with multiple storage</span></span>
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
PS C:\> New-AzResourceGroup -Name $ResourceGroupName -Location $Location

# Storage
$StorageAccount1 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName1 -Location $Location -Type $StorageType


$StorageAccount2 = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name $StorageName2 -Location $Location -Type $StorageType

# Media Service

## Setup the storage configuration object.
PS C:\> $PrimaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount1.Id -IsPrimary
PS C:\> $SecondaryStorageAccount = New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount2.Id
PS C:\> $StorageAccounts = @($PrimaryStorageAccount, $SecondaryStorageAccount)

## Create a media service.New-AzMediaService -ResourceGroupName $ResourceGroupName -AccountName $MediaServiceName -Location $Location -StorageAccounts $StorageAccounts -Tag $Tags
```

<span data-ttu-id="f1c2f-115">Bu örnekte, birden fazla depolama hesabı içeren bir medya hizmeti oluşturulması gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-115">This example shows how to create a media service with multiple storage accounts.</span></span>
<span data-ttu-id="f1c2f-116">Bu komut dosyası birkaç başka cmdlet kullanır.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-116">This script uses several other cmdlets.</span></span>

## <span data-ttu-id="f1c2f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1c2f-117">PARAMETERS</span></span>

### <span data-ttu-id="f1c2f-118">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f1c2f-118">-AccountName</span></span>
<span data-ttu-id="f1c2f-119">Bu cmdlet 'in oluşturduğu medya hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-119">Specifies the name of the media service that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f1c2f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1c2f-120">-DefaultProfile</span></span>
<span data-ttu-id="f1c2f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f1c2f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1c2f-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="f1c2f-122">-Location</span></span>
<span data-ttu-id="f1c2f-123">Bu cmdlet 'in medya hizmetini oluşturduğu bölgeyi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-123">Specifies the region that this cmdlet creates the media service in.</span></span>

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

### <span data-ttu-id="f1c2f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1c2f-124">-ResourceGroupName</span></span>
<span data-ttu-id="f1c2f-125">Medya hizmetinin atandığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-125">Specifies the name of the resource group that the media service is assigned to.</span></span>

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

### <span data-ttu-id="f1c2f-126">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="f1c2f-126">-StorageAccountId</span></span>
<span data-ttu-id="f1c2f-127">Medya Hizmeti hesabıyla ilişkilendirilmiş depolama hesabını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-127">Specifies the storage account associated with the media service account.</span></span>

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

### <span data-ttu-id="f1c2f-128">-StorageAccounts</span><span class="sxs-lookup"><span data-stu-id="f1c2f-128">-StorageAccounts</span></span>
<span data-ttu-id="f1c2f-129">Medya hizmetiyle ilişkilendirilecek bir depolama hesapları dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-129">Specifies an array of storage accounts to associate with the media service.</span></span>

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

### <span data-ttu-id="f1c2f-130">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f1c2f-130">-Tag</span></span>
<span data-ttu-id="f1c2f-131">Medya Hizmeti hesabıyla ilişkilendirilmiş Etiketler.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-131">The tags associated with the media service account.</span></span>

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

### <span data-ttu-id="f1c2f-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="f1c2f-132">-Confirm</span></span>
<span data-ttu-id="f1c2f-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1c2f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1c2f-134">-WhatIf</span></span>
<span data-ttu-id="f1c2f-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1c2f-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1c2f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1c2f-137">CommonParameters</span></span>
<span data-ttu-id="f1c2f-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1c2f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1c2f-139">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1c2f-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1c2f-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1c2f-140">INPUTS</span></span>

### <span data-ttu-id="f1c2f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f1c2f-141">System.String</span></span>

### <span data-ttu-id="f1c2f-142">Microsoft. Azure. Commands. Media. modeller. PSStorageAccount []</span><span class="sxs-lookup"><span data-stu-id="f1c2f-142">Microsoft.Azure.Commands.Media.Models.PSStorageAccount[]</span></span>

## <span data-ttu-id="f1c2f-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1c2f-143">OUTPUTS</span></span>

### <span data-ttu-id="f1c2f-144">Microsoft. Azure. Commands. Media. modeller. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="f1c2f-144">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="f1c2f-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1c2f-145">NOTES</span></span>

## <span data-ttu-id="f1c2f-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1c2f-146">RELATED LINKS</span></span>

[<span data-ttu-id="f1c2f-147">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f1c2f-147">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="f1c2f-148">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f1c2f-148">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="f1c2f-149">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f1c2f-149">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


