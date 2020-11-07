---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 195bc966bb47bf921eb0150272cfb9af6d73c63a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934039"
---
# <span data-ttu-id="d73d8-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d73d8-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="d73d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d73d8-102">SYNOPSIS</span></span>
<span data-ttu-id="d73d8-103">Azure depolama blob hizmeti için hizmet özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d73d8-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d73d8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d73d8-104">SYNTAX</span></span>

### <span data-ttu-id="d73d8-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d73d8-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d73d8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d73d8-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d73d8-107">Blobservicepropertiesresourceıd</span><span class="sxs-lookup"><span data-stu-id="d73d8-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d73d8-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="d73d8-108">DESCRIPTION</span></span>
<span data-ttu-id="d73d8-109">**Update-AzStorageBlobServiceProperty** cmdlet 'ı, Azure depolama blob hizmeti için hizmet özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="d73d8-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="d73d8-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d73d8-110">EXAMPLES</span></span>

### <span data-ttu-id="d73d8-111">Örnek 1: blob hizmeti DefaultServiceVersion 'ı 2018-03-28 olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="d73d8-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False
```

<span data-ttu-id="d73d8-112">Bu komut, Blob hizmetinin Defaultservicesürümünü 2018-03-28 olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="d73d8-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="d73d8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d73d8-113">PARAMETERS</span></span>

### <span data-ttu-id="d73d8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d73d8-114">-DefaultProfile</span></span>
<span data-ttu-id="d73d8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d73d8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d73d8-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="d73d8-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="d73d8-117">Ayarlanacak varsayılan hizmet sürümü</span><span class="sxs-lookup"><span data-stu-id="d73d8-117">Default Service Version to Set</span></span>

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

### <span data-ttu-id="d73d8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d73d8-118">-ResourceGroupName</span></span>
<span data-ttu-id="d73d8-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d73d8-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="d73d8-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d73d8-120">-ResourceId</span></span>
<span data-ttu-id="d73d8-121">Depolama hesabı kaynak kimliği veya blob hizmeti özellikleri kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="d73d8-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="d73d8-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d73d8-122">-StorageAccount</span></span>
<span data-ttu-id="d73d8-123">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="d73d8-123">Storage account object</span></span>

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

### <span data-ttu-id="d73d8-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d73d8-124">-StorageAccountName</span></span>
<span data-ttu-id="d73d8-125">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="d73d8-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="d73d8-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="d73d8-126">-Confirm</span></span>
<span data-ttu-id="d73d8-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d73d8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d73d8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d73d8-128">-WhatIf</span></span>
<span data-ttu-id="d73d8-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d73d8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d73d8-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d73d8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d73d8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d73d8-131">CommonParameters</span></span>
<span data-ttu-id="d73d8-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d73d8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d73d8-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d73d8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d73d8-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d73d8-134">INPUTS</span></span>

### <span data-ttu-id="d73d8-135">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d73d8-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d73d8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d73d8-136">System.String</span></span>

## <span data-ttu-id="d73d8-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d73d8-137">OUTPUTS</span></span>

### <span data-ttu-id="d73d8-138">Microsoft. Azure. Commands. Management. Storage. model. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="d73d8-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="d73d8-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d73d8-139">NOTES</span></span>

## <span data-ttu-id="d73d8-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d73d8-140">RELATED LINKS</span></span>
