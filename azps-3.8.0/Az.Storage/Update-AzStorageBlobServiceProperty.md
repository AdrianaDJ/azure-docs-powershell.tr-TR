---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: b7d6299af3f56dd8f09c73171ab6630cbbb9bc96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098002"
---
# <span data-ttu-id="bd718-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="bd718-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="bd718-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd718-102">SYNOPSIS</span></span>
<span data-ttu-id="bd718-103">Azure depolama blob hizmeti için hizmet özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bd718-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bd718-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bd718-104">SYNTAX</span></span>

### <span data-ttu-id="bd718-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bd718-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd718-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="bd718-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bd718-107">Blobservicepropertiesresourceıd</span><span class="sxs-lookup"><span data-stu-id="bd718-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd718-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bd718-108">DESCRIPTION</span></span>
<span data-ttu-id="bd718-109">**Update-AzStorageBlobServiceProperty** cmdlet 'ı, Azure depolama blob hizmeti için hizmet özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="bd718-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="bd718-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bd718-110">EXAMPLES</span></span>

### <span data-ttu-id="bd718-111">Örnek 1: blob hizmeti DefaultServiceVersion 'ı 2018-03-28 olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="bd718-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False                                                   
```

<span data-ttu-id="bd718-112">Bu komut, Blob hizmetinin Defaultservicesürümünü 2018-03-28 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="bd718-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="bd718-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bd718-113">PARAMETERS</span></span>

### <span data-ttu-id="bd718-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd718-114">-DefaultProfile</span></span>
<span data-ttu-id="bd718-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bd718-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd718-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="bd718-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="bd718-117">Ayarlanacak varsayılan hizmet sürümü</span><span class="sxs-lookup"><span data-stu-id="bd718-117">Default Service Version to Set</span></span>

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

### <span data-ttu-id="bd718-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd718-118">-ResourceGroupName</span></span>
<span data-ttu-id="bd718-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bd718-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="bd718-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bd718-120">-ResourceId</span></span>
<span data-ttu-id="bd718-121">Depolama hesabı kaynak kimliği veya blob hizmeti özellikleri kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="bd718-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="bd718-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd718-122">-StorageAccount</span></span>
<span data-ttu-id="bd718-123">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="bd718-123">Storage account object</span></span>

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

### <span data-ttu-id="bd718-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bd718-124">-StorageAccountName</span></span>
<span data-ttu-id="bd718-125">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="bd718-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="bd718-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="bd718-126">-Confirm</span></span>
<span data-ttu-id="bd718-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bd718-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd718-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd718-128">-WhatIf</span></span>
<span data-ttu-id="bd718-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bd718-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd718-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bd718-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd718-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd718-131">CommonParameters</span></span>
<span data-ttu-id="bd718-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bd718-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd718-133">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd718-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd718-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bd718-134">INPUTS</span></span>

### <span data-ttu-id="bd718-135">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bd718-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="bd718-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bd718-136">System.String</span></span>

## <span data-ttu-id="bd718-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bd718-137">OUTPUTS</span></span>

### <span data-ttu-id="bd718-138">Microsoft. Azure. Commands. Management. Storage. model. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="bd718-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="bd718-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bd718-139">NOTES</span></span>

## <span data-ttu-id="bd718-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bd718-140">RELATED LINKS</span></span>
