---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: fdac081aa6edc5ac43c98800ad2d857cb8f62b09
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933745"
---
# <span data-ttu-id="f5e3a-101">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f5e3a-101">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="f5e3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f5e3a-103">Azure depolama blob hizmeti için bekletme ilkesini silme özelliğini etkinleştirin.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-103">Enable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f5e3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5e3a-104">SYNTAX</span></span>

### <span data-ttu-id="f5e3a-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f5e3a-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RetentionDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5e3a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f5e3a-106">AccountObject</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5e3a-107">Blobservicepropertiesresourceıd</span><span class="sxs-lookup"><span data-stu-id="f5e3a-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> -RetentionDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5e3a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5e3a-108">DESCRIPTION</span></span>
<span data-ttu-id="f5e3a-109">**Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet 'ı Azure depolama blob hizmeti için bekletme ilkesini silme özelliğini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-109">The **Enable-AzStorageBlobDeleteRetentionPolicy** cmdlet enables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f5e3a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5e3a-110">EXAMPLES</span></span>

### <span data-ttu-id="f5e3a-111">Örnek 1: blob hizmeti için bekletme ilkesini silme özelliğini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f5e3a-111">Example 1: Enable delete retention policy for the Blob service</span></span>
```
C:\PS>Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru -RetentionDays 4

Enabled Days
------- ----
   True    4
```

<span data-ttu-id="f5e3a-112">Bu komut, blob hizmeti için bekletme ilkesini silme</span><span class="sxs-lookup"><span data-stu-id="f5e3a-112">This command enables delete retention policy for the Blob service, and set deleted blob retention days to 4.</span></span>

## <span data-ttu-id="f5e3a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5e3a-113">PARAMETERS</span></span>

### <span data-ttu-id="f5e3a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5e3a-114">-DefaultProfile</span></span>
<span data-ttu-id="f5e3a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5e3a-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f5e3a-116">-PassThru</span></span>
<span data-ttu-id="f5e3a-117">Hizmet özelliklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="f5e3a-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="f5e3a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5e3a-118">-ResourceGroupName</span></span>
<span data-ttu-id="f5e3a-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="f5e3a-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f5e3a-120">-ResourceId</span></span>
<span data-ttu-id="f5e3a-121">Depolama hesabı kaynak kimliği veya blob hizmeti özellikleri kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="f5e3a-122">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="f5e3a-122">-RetentionDays</span></span>
<span data-ttu-id="f5e3a-123">KayıtSayısı için bekletme günü sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-123">Sets the number of retention days for the DeleteRetentionPolicy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5e3a-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5e3a-124">-StorageAccount</span></span>
<span data-ttu-id="f5e3a-125">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="f5e3a-125">Storage account object</span></span>

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

### <span data-ttu-id="f5e3a-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f5e3a-126">-StorageAccountName</span></span>
<span data-ttu-id="f5e3a-127">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="f5e3a-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="f5e3a-128">-Confirm</span></span>
<span data-ttu-id="f5e3a-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5e3a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5e3a-130">-WhatIf</span></span>
<span data-ttu-id="f5e3a-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5e3a-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5e3a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5e3a-133">CommonParameters</span></span>
<span data-ttu-id="f5e3a-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5e3a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5e3a-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5e3a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5e3a-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5e3a-136">INPUTS</span></span>

### <span data-ttu-id="f5e3a-137">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5e3a-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f5e3a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="f5e3a-138">System.String</span></span>

## <span data-ttu-id="f5e3a-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5e3a-139">OUTPUTS</span></span>

### <span data-ttu-id="f5e3a-140">Microsoft. Azure. Commands. Management. Storage. model. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="f5e3a-140">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="f5e3a-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5e3a-141">NOTES</span></span>

## <span data-ttu-id="f5e3a-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5e3a-142">RELATED LINKS</span></span>
