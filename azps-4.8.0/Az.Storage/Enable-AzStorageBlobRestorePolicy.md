---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/enable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Enable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: a5b5b1c761bb6e3c23a5dd5f0525d2d6627b3ab2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110193"
---
# <span data-ttu-id="f5a72-101">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="f5a72-101">Enable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="f5a72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5a72-102">SYNOPSIS</span></span>
<span data-ttu-id="f5a72-103">Depolama hesabında blob geri yükleme Ilkesini verir.</span><span class="sxs-lookup"><span data-stu-id="f5a72-103">Enables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="f5a72-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f5a72-104">SYNTAX</span></span>

### <span data-ttu-id="f5a72-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f5a72-105">AccountName (Default)</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -RestoreDays <Int32> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5a72-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f5a72-106">AccountObject</span></span>
```
Enable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5a72-107">Blobservicepropertiesresourceıd</span><span class="sxs-lookup"><span data-stu-id="f5a72-107">BlobServicePropertiesResourceId</span></span>
```
Enable-AzStorageBlobRestorePolicy [-ResourceId] <String> -RestoreDays <Int32> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5a72-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f5a72-108">DESCRIPTION</span></span>
<span data-ttu-id="f5a72-109">**Enable-AzStorageBlobRestorePolicy** cmdlet 'ı, Azure depolama blob hizmeti Için blob geri yükleme ilkesini etkinleştirir.</span><span class="sxs-lookup"><span data-stu-id="f5a72-109">The **Enable-AzStorageBlobRestorePolicy** cmdlet enables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="f5a72-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f5a72-110">EXAMPLES</span></span>

### <span data-ttu-id="f5a72-111">Örnek 1: depolama hesabında Azure depolama blob hizmeti için blob geri yükleme Ilkesini sağlayan</span><span class="sxs-lookup"><span data-stu-id="f5a72-111">Example 1: Enables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Enable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" $accountName -RetentionDays 5

PS C:\> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -EnableChangeFeed $true

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : False
RestorePolicy.Days            : 
RestorePolicy.MinRestoreTime  : 
ChangeFeed                    : True
IsVersioningEnabled           : True

PS C:\> Enable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -RestoreDays 4

PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"

StorageAccountName            : mystorageaccount
ResourceGroupName             : myresourcegoup
DefaultServiceVersion         : 
DeleteRetentionPolicy.Enabled : True
DeleteRetentionPolicy.Days    : 5
RestorePolicy.Enabled         : True
RestorePolicy.Days            : 4
RestorePolicy.MinRestoreTime  : 8/28/2020 6:00:59 AM
ChangeFeed                    : True
IsVersioningEnabled           : True
```

<span data-ttu-id="f5a72-112">Bu komut öncelikle blob yazılım silme ve changefeed 'i etkinleştirip ardından blob geri yükleme Ilkesini etkinleştirir, son olarak blob Hizmeti özelliklerindeki ayarı denetleyin.</span><span class="sxs-lookup"><span data-stu-id="f5a72-112">This command first enable Blob softdelete and changefeed, then enables Blob Restore Policy, finally check the setting in Blob service properties.</span></span>
<span data-ttu-id="f5a72-113">Blob hizmeti RestorePolicy. Days, DeleteRetentionPolicy. Days değerinden küçük olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="f5a72-113">The Blob service RestorePolicy.Days must be smaller than DeleteRetentionPolicy.Days.</span></span>
<span data-ttu-id="f5a72-114">Blob yazılım silme ve ChangeFeed, blob geri yükleme Ilkesini etkinleştirmeden önce etkinleştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="f5a72-114">Blob softdelete and ChangeFeed must be enabled before enable blob Restore Policy.</span></span>
<span data-ttu-id="f5a72-115">Softdelete ve changefeed yalnızca etkinleştirilmişse, blob geri yükleme ilkesini etkinleştirmeden önce sunucunun ayarı işlemesi biraz zaman alabilir.</span><span class="sxs-lookup"><span data-stu-id="f5a72-115">If softdelete and Changefeed are just enabled, might need wait for some time for server to handle the setting, before enable Blob restore policy.</span></span>

## <span data-ttu-id="f5a72-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f5a72-116">PARAMETERS</span></span>

### <span data-ttu-id="f5a72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5a72-117">-DefaultProfile</span></span>
<span data-ttu-id="f5a72-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f5a72-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5a72-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f5a72-119">-PassThru</span></span>
<span data-ttu-id="f5a72-120">Hizmet özelliklerini görüntüleme</span><span class="sxs-lookup"><span data-stu-id="f5a72-120">Display ServiceProperties</span></span>

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

### <span data-ttu-id="f5a72-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5a72-121">-ResourceGroupName</span></span>
<span data-ttu-id="f5a72-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f5a72-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="f5a72-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f5a72-123">-ResourceId</span></span>
<span data-ttu-id="f5a72-124">Depolama hesabı kaynak kimliği veya blob hizmeti özellikleri kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="f5a72-124">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="f5a72-125">-Restoregün</span><span class="sxs-lookup"><span data-stu-id="f5a72-125">-RestoreDays</span></span>
<span data-ttu-id="f5a72-126">Blob 'un geri yüklenebilmesi için gün sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="f5a72-126">Sets the number of days for the blob can be restored..</span></span>

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

### <span data-ttu-id="f5a72-127">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a72-127">-StorageAccount</span></span>
<span data-ttu-id="f5a72-128">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="f5a72-128">Storage account object</span></span>

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

### <span data-ttu-id="f5a72-129">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f5a72-129">-StorageAccountName</span></span>
<span data-ttu-id="f5a72-130">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="f5a72-130">Storage Account Name.</span></span>

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

### <span data-ttu-id="f5a72-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="f5a72-131">-Confirm</span></span>
<span data-ttu-id="f5a72-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f5a72-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5a72-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5a72-133">-WhatIf</span></span>
<span data-ttu-id="f5a72-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f5a72-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5a72-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f5a72-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5a72-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5a72-136">CommonParameters</span></span>
<span data-ttu-id="f5a72-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f5a72-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5a72-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5a72-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5a72-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f5a72-139">INPUTS</span></span>

### <span data-ttu-id="f5a72-140">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f5a72-140">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f5a72-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f5a72-141">System.String</span></span>

## <span data-ttu-id="f5a72-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f5a72-142">OUTPUTS</span></span>

### <span data-ttu-id="f5a72-143">Microsoft. Azure. Commands. Management. Storage. model. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="f5a72-143">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="f5a72-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f5a72-144">NOTES</span></span>

## <span data-ttu-id="f5a72-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f5a72-145">RELATED LINKS</span></span>
