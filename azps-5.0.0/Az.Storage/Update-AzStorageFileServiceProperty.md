---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324976"
---
# <span data-ttu-id="47487-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="47487-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="47487-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47487-102">SYNOPSIS</span></span>
<span data-ttu-id="47487-103">Azure depolama dosya hizmeti 'nin hizmet özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="47487-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="47487-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47487-104">SYNTAX</span></span>

### <span data-ttu-id="47487-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47487-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47487-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="47487-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47487-107">Fileservicepropertiesresourceıd</span><span class="sxs-lookup"><span data-stu-id="47487-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47487-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="47487-108">DESCRIPTION</span></span>
<span data-ttu-id="47487-109">**Update-AzStorageFileServiceProperty** cmdlet 'ı, Azure depolama dosya hizmeti 'nin hizmet özelliklerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="47487-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="47487-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47487-110">EXAMPLES</span></span>

### <span data-ttu-id="47487-111">Örnek 1: dosya paylaşımı yazılım silinmesini etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="47487-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="47487-112">Bu komut dosya paylaşımı yazılım</span><span class="sxs-lookup"><span data-stu-id="47487-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="47487-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47487-113">PARAMETERS</span></span>

### <span data-ttu-id="47487-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47487-114">-DefaultProfile</span></span>
<span data-ttu-id="47487-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47487-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47487-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="47487-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="47487-117">Depolama hesabı için paylaşım silme bekletme Ilkesini $true olarak ayarlayarak, $false olarak ayarlayarak paylaşım silme bekletme Ilkesini devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="47487-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

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

### <span data-ttu-id="47487-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47487-118">-ResourceGroupName</span></span>
<span data-ttu-id="47487-119">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="47487-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="47487-120">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="47487-120">-ResourceId</span></span>
<span data-ttu-id="47487-121">Depolama hesabı kaynak kimliği veya dosya hizmeti özellikleri kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="47487-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47487-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="47487-122">-ShareRetentionDays</span></span>
<span data-ttu-id="47487-123">Paylaşım KayıtSayısı Ilkesi için bekletme günü sayısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="47487-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="47487-124">Değer yalnızca paylaşım silme bekletme Ilkesi etkinleştir Ilkesine göre ayarlanmalıdır.</span><span class="sxs-lookup"><span data-stu-id="47487-124">The value should only be set when enable share Delete Retention Policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days, RetentionDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47487-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="47487-125">-StorageAccount</span></span>
<span data-ttu-id="47487-126">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="47487-126">Storage account object</span></span>

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

### <span data-ttu-id="47487-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="47487-127">-StorageAccountName</span></span>
<span data-ttu-id="47487-128">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="47487-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="47487-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="47487-129">-Confirm</span></span>
<span data-ttu-id="47487-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47487-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47487-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47487-131">-WhatIf</span></span>
<span data-ttu-id="47487-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47487-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47487-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47487-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47487-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47487-134">CommonParameters</span></span>
<span data-ttu-id="47487-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47487-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47487-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47487-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47487-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47487-137">INPUTS</span></span>

### <span data-ttu-id="47487-138">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="47487-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="47487-139">System. String</span><span class="sxs-lookup"><span data-stu-id="47487-139">System.String</span></span>

## <span data-ttu-id="47487-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47487-140">OUTPUTS</span></span>

### <span data-ttu-id="47487-141">Microsoft. Azure. Commands. Management. Storage. model. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="47487-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="47487-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47487-142">NOTES</span></span>

## <span data-ttu-id="47487-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47487-143">RELATED LINKS</span></span>
