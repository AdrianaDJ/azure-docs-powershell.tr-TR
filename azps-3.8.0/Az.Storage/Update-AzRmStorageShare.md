---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 6e3c71900e5fe4a4ac8e4f092691dcde3e759c2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096970"
---
# <span data-ttu-id="b27cd-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="b27cd-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="b27cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b27cd-102">SYNOPSIS</span></span>
<span data-ttu-id="b27cd-103">Depolama dosya paylaşımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b27cd-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="b27cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b27cd-104">SYNTAX</span></span>

### <span data-ttu-id="b27cd-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b27cd-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b27cd-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b27cd-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b27cd-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="b27cd-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b27cd-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="b27cd-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b27cd-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="b27cd-109">DESCRIPTION</span></span>
<span data-ttu-id="b27cd-110">**Yeni-Azrmstoragesshare** cmdlet 'ı bir depolama dosya paylaşımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b27cd-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="b27cd-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b27cd-111">EXAMPLES</span></span>

### <span data-ttu-id="b27cd-112">Örnek 1: depolama alanı adı ve paylaşım adıyla birlikte depolama dosya paylaşımının meta verilerini ve paylaşım kotasını değiştirir</span><span class="sxs-lookup"><span data-stu-id="b27cd-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup                       200     

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="b27cd-113">Bu komut, depolama dosya paylaşımının meta verilerini değiştirir ve kota kotasını depolama hesabı adı ve paylaşım adıyla değiştirir ve değiştirme sonucunu döndürülen dosya paylaşımı nesnesiyle gösterir.</span><span class="sxs-lookup"><span data-stu-id="b27cd-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="b27cd-114">Örnek 2: depolama hesabı nesnesiyle depolama</span><span class="sxs-lookup"><span data-stu-id="b27cd-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="b27cd-115">Bu komut, depolama hesabı nesnesi ve paylaşım adıyla birlikte depolama dosya paylaşımında meta verileri değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b27cd-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="b27cd-116">Örnek 3: ardışık düzene sahip bir depolama hesabındaki tüm depolama dosyası paylaşımlarının paylaşım kotasını değiştirir</span><span class="sxs-lookup"><span data-stu-id="b27cd-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Update-AzRmStorageShare -QuotaGiB 5000

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup                       5000
share2   myStorageAccount   myResourceGroup                       5000
```

<span data-ttu-id="b27cd-117">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama dosya paylaşımları için 5000 GIB paylaşım kotasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="b27cd-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="b27cd-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b27cd-118">PARAMETERS</span></span>

### <span data-ttu-id="b27cd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b27cd-119">-DefaultProfile</span></span>
<span data-ttu-id="b27cd-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b27cd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b27cd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b27cd-121">-InputObject</span></span>
<span data-ttu-id="b27cd-122">Depolama paylaşım nesnesi</span><span class="sxs-lookup"><span data-stu-id="b27cd-122">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b27cd-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b27cd-123">-Metadata</span></span>
<span data-ttu-id="b27cd-124">Meta verileri paylaşma</span><span class="sxs-lookup"><span data-stu-id="b27cd-124">Share Metadata</span></span>

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

### <span data-ttu-id="b27cd-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="b27cd-125">-Name</span></span>
<span data-ttu-id="b27cd-126">Paylaşım adı</span><span class="sxs-lookup"><span data-stu-id="b27cd-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27cd-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="b27cd-127">-QuotaGiB</span></span>
<span data-ttu-id="b27cd-128">Gibıbyte 'ta kotayı paylaşın.</span><span class="sxs-lookup"><span data-stu-id="b27cd-128">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27cd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b27cd-129">-ResourceGroupName</span></span>
<span data-ttu-id="b27cd-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="b27cd-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="b27cd-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="b27cd-131">-ResourceId</span></span>
<span data-ttu-id="b27cd-132">Dosya Paylaşımı kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="b27cd-132">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b27cd-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b27cd-133">-StorageAccount</span></span>
<span data-ttu-id="b27cd-134">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="b27cd-134">Storage account object</span></span>

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

### <span data-ttu-id="b27cd-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b27cd-135">-StorageAccountName</span></span>
<span data-ttu-id="b27cd-136">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="b27cd-136">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b27cd-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="b27cd-137">-Confirm</span></span>
<span data-ttu-id="b27cd-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b27cd-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b27cd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b27cd-139">-WhatIf</span></span>
<span data-ttu-id="b27cd-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b27cd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b27cd-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b27cd-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b27cd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b27cd-142">CommonParameters</span></span>
<span data-ttu-id="b27cd-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b27cd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b27cd-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b27cd-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b27cd-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b27cd-145">INPUTS</span></span>

### <span data-ttu-id="b27cd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="b27cd-146">System.String</span></span>

### <span data-ttu-id="b27cd-147">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b27cd-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b27cd-148">Microsoft. Azure. Commands. Management. Storage. model. PSShare</span><span class="sxs-lookup"><span data-stu-id="b27cd-148">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="b27cd-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b27cd-149">OUTPUTS</span></span>

### <span data-ttu-id="b27cd-150">Microsoft. Azure. Commands. Management. Storage. model. PSShare</span><span class="sxs-lookup"><span data-stu-id="b27cd-150">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="b27cd-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b27cd-151">NOTES</span></span>

## <span data-ttu-id="b27cd-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b27cd-152">RELATED LINKS</span></span>
