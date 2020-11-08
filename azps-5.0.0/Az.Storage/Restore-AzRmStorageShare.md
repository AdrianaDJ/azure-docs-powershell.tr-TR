---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzRmStorageShare.md
ms.openlocfilehash: 70d3c8c435a88b4f0f968d1519efd9af6d9907e8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275791"
---
# <span data-ttu-id="6aa84-101">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6aa84-101">Restore-AzRmStorageShare</span></span>

## <span data-ttu-id="6aa84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aa84-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa84-103">Silinmiş dosya paylaşımını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="6aa84-103">Restores a deleted file share.</span></span>

## <span data-ttu-id="6aa84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6aa84-104">SYNTAX</span></span>

### <span data-ttu-id="6aa84-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6aa84-105">AccountName (Default)</span></span>
```
Restore-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 -DeletedShareVersion <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6aa84-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6aa84-106">AccountObject</span></span>
```
Restore-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> -DeletedShareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aa84-107">ShareObject</span><span class="sxs-lookup"><span data-stu-id="6aa84-107">ShareObject</span></span>
```
Restore-AzRmStorageShare -InputObject <PSShare> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6aa84-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6aa84-108">DESCRIPTION</span></span>
<span data-ttu-id="6aa84-109">**Restore-Azrmstoragesshare** cmdlet 'i, yumuşak silme Paylaş etkinse geçerli bir bekletme günü içindeki silinmiş dosya paylaşımını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="6aa84-109">The **Restore-AzRmStorageShare** cmdlet restores a deleted file share within a valid retention days if share soft delete is enabled.</span></span>

## <span data-ttu-id="6aa84-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6aa84-110">EXAMPLES</span></span>

### <span data-ttu-id="6aa84-111">Örnek 1: paylaşımı kaldırma ve geri yükleme</span><span class="sxs-lookup"><span data-stu-id="6aa84-111">Example 1: Remove and restore a share</span></span>
```powershell
PS C:\> Remove-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -Force

PS C:\> Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6                

PS C:\> Restore-AzRmStorageShare -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Name $shareName -DeletedShareVersion 01D61FD1FC5498B6

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   100
```

<span data-ttu-id="6aa84-112">Bu komut önce bir dosya paylaşımını silip ardından paylaşımları listeler ve silinen paylaşım sürümünü görüntüle, son olarak normal bir paylaşıma geri yükle.</span><span class="sxs-lookup"><span data-stu-id="6aa84-112">This command first delete a file share, and then list shares and see the deleted share version, finally restore it back to a normal share.</span></span> <span data-ttu-id="6aa84-113">Paylaşımı silmeden önce Update-Azstoragefileserviceözelliğiyle, yazılım silme özelliğini etkinleştirmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="6aa84-113">Need enabled share soft delete with Update-AzStorageFileServiceProperty, before delete the share.</span></span>

## <span data-ttu-id="6aa84-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6aa84-114">PARAMETERS</span></span>

### <span data-ttu-id="6aa84-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa84-115">-DefaultProfile</span></span>
<span data-ttu-id="6aa84-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6aa84-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aa84-117">-DeletedShareVersion</span><span class="sxs-lookup"><span data-stu-id="6aa84-117">-DeletedShareVersion</span></span>
<span data-ttu-id="6aa84-118">Silinecek olan paylaşım sürümü.</span><span class="sxs-lookup"><span data-stu-id="6aa84-118">Deleted Share Version, which will be restored from.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6aa84-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6aa84-119">-InputObject</span></span>
<span data-ttu-id="6aa84-120">Silinen paylaşım nesnesi</span><span class="sxs-lookup"><span data-stu-id="6aa84-120">Deleted Share object</span></span>

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

### <span data-ttu-id="6aa84-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="6aa84-121">-Name</span></span>
<span data-ttu-id="6aa84-122">Geri yüklenecek olan paylaşım adı silindi.</span><span class="sxs-lookup"><span data-stu-id="6aa84-122">Deleted Share Name, which will be restored.</span></span>

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

### <span data-ttu-id="6aa84-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aa84-123">-ResourceGroupName</span></span>
<span data-ttu-id="6aa84-124">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6aa84-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="6aa84-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6aa84-125">-StorageAccount</span></span>
<span data-ttu-id="6aa84-126">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="6aa84-126">Storage account object</span></span>

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

### <span data-ttu-id="6aa84-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6aa84-127">-StorageAccountName</span></span>
<span data-ttu-id="6aa84-128">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="6aa84-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="6aa84-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="6aa84-129">-Confirm</span></span>
<span data-ttu-id="6aa84-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6aa84-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aa84-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aa84-131">-WhatIf</span></span>
<span data-ttu-id="6aa84-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6aa84-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aa84-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6aa84-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aa84-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa84-134">CommonParameters</span></span>
<span data-ttu-id="6aa84-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6aa84-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa84-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa84-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa84-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6aa84-137">INPUTS</span></span>

### <span data-ttu-id="6aa84-138">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6aa84-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6aa84-139">Microsoft. Azure. Commands. Management. Storage. model. PSShare</span><span class="sxs-lookup"><span data-stu-id="6aa84-139">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="6aa84-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6aa84-140">OUTPUTS</span></span>

### <span data-ttu-id="6aa84-141">Microsoft. Azure. Commands. Management. Storage. model. PSShare</span><span class="sxs-lookup"><span data-stu-id="6aa84-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="6aa84-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6aa84-142">NOTES</span></span>

## <span data-ttu-id="6aa84-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6aa84-143">RELATED LINKS</span></span>
