---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 0f2d86fca85364fa71d50c05d83f278bd997252e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323560"
---
# <span data-ttu-id="4c05f-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="4c05f-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="4c05f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c05f-102">SYNOPSIS</span></span>
<span data-ttu-id="4c05f-103">Depolama dosya paylaşımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4c05f-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="4c05f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4c05f-104">SYNTAX</span></span>

### <span data-ttu-id="4c05f-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4c05f-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c05f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4c05f-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4c05f-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="4c05f-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c05f-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="4c05f-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c05f-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="4c05f-109">DESCRIPTION</span></span>
<span data-ttu-id="4c05f-110">**Yeni-Azrmstoragesshare** cmdlet 'ı bir depolama dosya paylaşımını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4c05f-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="4c05f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4c05f-111">EXAMPLES</span></span>

### <span data-ttu-id="4c05f-112">Örnek 1: depolama alanı adı ve paylaşım adıyla birlikte depolama dosya paylaşımının meta verilerini ve paylaşım kotasını değiştirir</span><span class="sxs-lookup"><span data-stu-id="4c05f-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  200

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="4c05f-113">Bu komut, depolama dosya paylaşımının meta verilerini değiştirir ve kota kotasını depolama hesabı adı ve paylaşım adıyla değiştirir ve değiştirme sonucunu döndürülen dosya paylaşımı nesnesiyle gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c05f-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="4c05f-114">Örnek 2: depolama hesabı nesnesiyle depolama</span><span class="sxs-lookup"><span data-stu-id="4c05f-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="4c05f-115">Bu komut, depolama hesabı nesnesi ve paylaşım adıyla birlikte depolama dosya paylaşımında meta verileri değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4c05f-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="4c05f-116">Örnek 3: ardışık düzene sahip bir depolama hesabındaki tüm depolama dosyası paylaşımlarının paylaşım kotasını değiştirir</span><span class="sxs-lookup"><span data-stu-id="4c05f-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="4c05f-117">Bu komut, ardışık düzene sahip bir depolama hesabındaki tüm depolama dosya paylaşımları için 5000 GIB paylaşım kotasını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4c05f-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

### <span data-ttu-id="4c05f-118">Örnek 4: accesstier ile bir depolama dosya paylaşımını Cool olarak değiştirme</span><span class="sxs-lookup"><span data-stu-id="4c05f-118">Example 4: Modify a Storage file share with accesstier as Cool</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Cool

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Cool
```

<span data-ttu-id="4c05f-119">Bu komut, paylaşım katmanıyla birlikte bir depolama dosya paylaşımını serin olarak değiştirir.</span><span class="sxs-lookup"><span data-stu-id="4c05f-119">This command modifies a Storage file share with accesstier as Cool.</span></span>

## <span data-ttu-id="4c05f-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4c05f-120">PARAMETERS</span></span>

### <span data-ttu-id="4c05f-121">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="4c05f-121">-AccessTier</span></span>
<span data-ttu-id="4c05f-122">Belirli bir paylaşım için erişim katmanı.</span><span class="sxs-lookup"><span data-stu-id="4c05f-122">Access tier for specific share.</span></span> <span data-ttu-id="4c05f-123">StorageV2 hesabı, Transactionoptimize edilmiş (varsayılan), sıcak ve serin arasında seçim yapabilir.</span><span class="sxs-lookup"><span data-stu-id="4c05f-123">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="4c05f-124">FileStorage hesabı Premium 'u seçebilir.</span><span class="sxs-lookup"><span data-stu-id="4c05f-124">FileStorage account can choose Premium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: TransactionOptimized, Premium, Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c05f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c05f-125">-DefaultProfile</span></span>
<span data-ttu-id="4c05f-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4c05f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c05f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c05f-127">-InputObject</span></span>
<span data-ttu-id="4c05f-128">Depolama paylaşım nesnesi</span><span class="sxs-lookup"><span data-stu-id="4c05f-128">Storage Share object</span></span>

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

### <span data-ttu-id="4c05f-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4c05f-129">-Metadata</span></span>
<span data-ttu-id="4c05f-130">Meta verileri paylaşma</span><span class="sxs-lookup"><span data-stu-id="4c05f-130">Share Metadata</span></span>

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

### <span data-ttu-id="4c05f-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="4c05f-131">-Name</span></span>
<span data-ttu-id="4c05f-132">Paylaşım adı</span><span class="sxs-lookup"><span data-stu-id="4c05f-132">Share Name</span></span>

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

### <span data-ttu-id="4c05f-133">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="4c05f-133">-QuotaGiB</span></span>
<span data-ttu-id="4c05f-134">Gibıbyte 'ta kotayı paylaşın.</span><span class="sxs-lookup"><span data-stu-id="4c05f-134">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="4c05f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c05f-135">-ResourceGroupName</span></span>
<span data-ttu-id="4c05f-136">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4c05f-136">Resource Group Name.</span></span>

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

### <span data-ttu-id="4c05f-137">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4c05f-137">-ResourceId</span></span>
<span data-ttu-id="4c05f-138">Dosya Paylaşımı kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="4c05f-138">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="4c05f-139">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c05f-139">-StorageAccount</span></span>
<span data-ttu-id="4c05f-140">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="4c05f-140">Storage account object</span></span>

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

### <span data-ttu-id="4c05f-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4c05f-141">-StorageAccountName</span></span>
<span data-ttu-id="4c05f-142">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="4c05f-142">Storage Account Name.</span></span>

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

### <span data-ttu-id="4c05f-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="4c05f-143">-Confirm</span></span>
<span data-ttu-id="4c05f-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4c05f-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c05f-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c05f-145">-WhatIf</span></span>
<span data-ttu-id="4c05f-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4c05f-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c05f-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4c05f-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c05f-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c05f-148">CommonParameters</span></span>
<span data-ttu-id="4c05f-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4c05f-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c05f-150">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c05f-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c05f-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4c05f-151">INPUTS</span></span>

### <span data-ttu-id="4c05f-152">System. String</span><span class="sxs-lookup"><span data-stu-id="4c05f-152">System.String</span></span>

### <span data-ttu-id="4c05f-153">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c05f-153">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="4c05f-154">Microsoft. Azure. Commands. Management. Storage. model. PSShare</span><span class="sxs-lookup"><span data-stu-id="4c05f-154">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="4c05f-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4c05f-155">OUTPUTS</span></span>

### <span data-ttu-id="4c05f-156">Microsoft. Azure. Commands. Management. Storage. model. PSShare</span><span class="sxs-lookup"><span data-stu-id="4c05f-156">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="4c05f-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4c05f-157">NOTES</span></span>

## <span data-ttu-id="4c05f-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4c05f-158">RELATED LINKS</span></span>
