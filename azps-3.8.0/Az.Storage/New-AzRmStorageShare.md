---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 040e4e8584c29f77e6b847eea886851c41e606e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098625"
---
# <span data-ttu-id="04a4e-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="04a4e-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="04a4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04a4e-102">SYNOPSIS</span></span>
<span data-ttu-id="04a4e-103">Bir depolama dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04a4e-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="04a4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="04a4e-104">SYNTAX</span></span>

### <span data-ttu-id="04a4e-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="04a4e-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04a4e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="04a4e-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04a4e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="04a4e-107">DESCRIPTION</span></span>
<span data-ttu-id="04a4e-108">**Yeni-Azrmstoragesshare** cmdlet 'ı bir depolama dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04a4e-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="04a4e-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="04a4e-109">EXAMPLES</span></span>

### <span data-ttu-id="04a4e-110">Örnek 1: meta veri ve 100 paylaşım adıyla birlikte meta veri ve paylaşım adı olan bir depolama dosya paylaşımı oluşturun.</span><span class="sxs-lookup"><span data-stu-id="04a4e-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup
```

<span data-ttu-id="04a4e-111">Bu komut meta veri ve paylaşım kotasıyla 100 GiB olarak bir depolama dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04a4e-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="04a4e-112">Örnek 2: depolama hesabı nesnesiyle depolama dosyası paylaşımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="04a4e-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | New-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup
```

<span data-ttu-id="04a4e-113">Bu komut depolama hesabı nesnesi ve paylaşım adıyla bir depolama dosya paylaşımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="04a4e-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="04a4e-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="04a4e-114">PARAMETERS</span></span>

### <span data-ttu-id="04a4e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a4e-115">-DefaultProfile</span></span>
<span data-ttu-id="04a4e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="04a4e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04a4e-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="04a4e-117">-Metadata</span></span>
<span data-ttu-id="04a4e-118">Meta verileri paylaşma</span><span class="sxs-lookup"><span data-stu-id="04a4e-118">Share Metadata</span></span>

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

### <span data-ttu-id="04a4e-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="04a4e-119">-Name</span></span>
<span data-ttu-id="04a4e-120">Azure dosya paylaşımı adı</span><span class="sxs-lookup"><span data-stu-id="04a4e-120">Azure File share name</span></span>

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

### <span data-ttu-id="04a4e-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="04a4e-121">-QuotaGiB</span></span>
<span data-ttu-id="04a4e-122">Gibıbyte 'ta kotayı paylaşın.</span><span class="sxs-lookup"><span data-stu-id="04a4e-122">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="04a4e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04a4e-123">-ResourceGroupName</span></span>
<span data-ttu-id="04a4e-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="04a4e-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="04a4e-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="04a4e-125">-StorageAccount</span></span>
<span data-ttu-id="04a4e-126">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="04a4e-126">Storage account object</span></span>

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

### <span data-ttu-id="04a4e-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="04a4e-127">-StorageAccountName</span></span>
<span data-ttu-id="04a4e-128">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="04a4e-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="04a4e-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="04a4e-129">-Confirm</span></span>
<span data-ttu-id="04a4e-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="04a4e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04a4e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04a4e-131">-WhatIf</span></span>
<span data-ttu-id="04a4e-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="04a4e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04a4e-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="04a4e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04a4e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a4e-134">CommonParameters</span></span>
<span data-ttu-id="04a4e-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="04a4e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a4e-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04a4e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a4e-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="04a4e-137">INPUTS</span></span>

### <span data-ttu-id="04a4e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="04a4e-138">System.String</span></span>

### <span data-ttu-id="04a4e-139">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04a4e-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="04a4e-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="04a4e-140">OUTPUTS</span></span>

### <span data-ttu-id="04a4e-141">Microsoft. Azure. Commands. Management. Storage. model. PSShare</span><span class="sxs-lookup"><span data-stu-id="04a4e-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="04a4e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="04a4e-142">NOTES</span></span>

## <span data-ttu-id="04a4e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="04a4e-143">RELATED LINKS</span></span>