---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 4dc3914e4a8bc9113dd16ab431db53ddcf00ab5a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94323566"
---
# <span data-ttu-id="ea980-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="ea980-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="ea980-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea980-102">SYNOPSIS</span></span>
<span data-ttu-id="ea980-103">Bir depolama dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea980-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="ea980-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ea980-104">SYNTAX</span></span>

### <span data-ttu-id="ea980-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ea980-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea980-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ea980-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-AccessTier <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea980-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ea980-107">DESCRIPTION</span></span>
<span data-ttu-id="ea980-108">**Yeni-Azrmstoragesshare** cmdlet 'ı bir depolama dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea980-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="ea980-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ea980-109">EXAMPLES</span></span>

### <span data-ttu-id="ea980-110">Örnek 1: meta veri ve 100 paylaşım adıyla birlikte meta veri ve paylaşım adı olan bir depolama dosya paylaşımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="ea980-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="ea980-111">Bu komut meta veri ve paylaşım kotasıyla 100 GiB olarak bir depolama dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea980-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="ea980-112">Örnek 2: depolama hesabı nesnesiyle depolama dosyası paylaşımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ea980-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | New-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare
```

<span data-ttu-id="ea980-113">Bu komut depolama hesabı nesnesi ve paylaşım adıyla bir depolama dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="ea980-113">This command creates a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="ea980-114">Örnek 3: paylaşım olarak accesstier ile depolama dosya paylaşımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="ea980-114">Example 3: Create a Storage file share with accesstier as Hot</span></span>
```
PS C:\>$share = New-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -AccessTier Hot

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocols AccessTier Deleted Version ShareUsageBytes
----     -------- ---------------- ---------- ------- ------- ---------------
myshare                            Hot
```

<span data-ttu-id="ea980-115">Bu komut, Hot.</span><span class="sxs-lookup"><span data-stu-id="ea980-115">This command creates a Storage file share with accesstier as Hot.</span></span>

## <span data-ttu-id="ea980-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ea980-116">PARAMETERS</span></span>

### <span data-ttu-id="ea980-117">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="ea980-117">-AccessTier</span></span>
<span data-ttu-id="ea980-118">Belirli bir paylaşım için erişim katmanı.</span><span class="sxs-lookup"><span data-stu-id="ea980-118">Access tier for specific share.</span></span> <span data-ttu-id="ea980-119">StorageV2 hesabı, Transactionoptimize edilmiş (varsayılan), sıcak ve serin arasında seçim yapabilir.</span><span class="sxs-lookup"><span data-stu-id="ea980-119">StorageV2 account can choose between TransactionOptimized (default), Hot, and Cool.</span></span> <span data-ttu-id="ea980-120">FileStorage hesabı Premium 'u seçebilir.</span><span class="sxs-lookup"><span data-stu-id="ea980-120">FileStorage account can choose Premium.</span></span>

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

### <span data-ttu-id="ea980-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea980-121">-DefaultProfile</span></span>
<span data-ttu-id="ea980-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ea980-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea980-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="ea980-123">-Metadata</span></span>
<span data-ttu-id="ea980-124">Meta verileri paylaşma</span><span class="sxs-lookup"><span data-stu-id="ea980-124">Share Metadata</span></span>

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

### <span data-ttu-id="ea980-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="ea980-125">-Name</span></span>
<span data-ttu-id="ea980-126">Azure dosya paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="ea980-126">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea980-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="ea980-127">-QuotaGiB</span></span>
<span data-ttu-id="ea980-128">Gibıbyte 'ta kotayı paylaşın.</span><span class="sxs-lookup"><span data-stu-id="ea980-128">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="ea980-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea980-129">-ResourceGroupName</span></span>
<span data-ttu-id="ea980-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="ea980-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea980-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea980-131">-StorageAccount</span></span>
<span data-ttu-id="ea980-132">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="ea980-132">Storage account object</span></span>

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

### <span data-ttu-id="ea980-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ea980-133">-StorageAccountName</span></span>
<span data-ttu-id="ea980-134">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="ea980-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="ea980-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="ea980-135">-Confirm</span></span>
<span data-ttu-id="ea980-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ea980-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea980-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea980-137">-WhatIf</span></span>
<span data-ttu-id="ea980-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ea980-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea980-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ea980-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea980-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea980-140">CommonParameters</span></span>
<span data-ttu-id="ea980-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ea980-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea980-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea980-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea980-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ea980-143">INPUTS</span></span>

### <span data-ttu-id="ea980-144">System. String</span><span class="sxs-lookup"><span data-stu-id="ea980-144">System.String</span></span>

### <span data-ttu-id="ea980-145">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea980-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ea980-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ea980-146">OUTPUTS</span></span>

### <span data-ttu-id="ea980-147">Microsoft. Azure. Commands. Management. Storage. model. PSShare</span><span class="sxs-lookup"><span data-stu-id="ea980-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="ea980-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ea980-148">NOTES</span></span>

## <span data-ttu-id="ea980-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ea980-149">RELATED LINKS</span></span>
