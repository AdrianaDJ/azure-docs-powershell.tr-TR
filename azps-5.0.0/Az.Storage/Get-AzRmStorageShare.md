---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 90edd254eb77b03f4f4d26761020d71025960426
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279761"
---
# <span data-ttu-id="22850-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="22850-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="22850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22850-102">SYNOPSIS</span></span>
<span data-ttu-id="22850-103">Depolama dosya paylaşımlarını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="22850-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="22850-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22850-104">SYNTAX</span></span>

### <span data-ttu-id="22850-105">Hesapadları (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="22850-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22850-106">Adı</span><span class="sxs-lookup"><span data-stu-id="22850-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22850-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="22850-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22850-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="22850-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22850-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="22850-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22850-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="22850-110">DESCRIPTION</span></span>
<span data-ttu-id="22850-111">**Get-Azrmstoragesshares** cmdlet 'ı, depolama dosya paylaşımlarını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="22850-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="22850-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22850-112">EXAMPLES</span></span>

### <span data-ttu-id="22850-113">Örnek 1: depolama hesabı adı ve paylaşım adıyla bir depolama dosya paylaşımı alın</span><span class="sxs-lookup"><span data-stu-id="22850-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="22850-114">Bu komut, depolama hesabı adı ve paylaşım adıyla bir depolama dosya paylaşımı alır.</span><span class="sxs-lookup"><span data-stu-id="22850-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="22850-115">Örnek 2: depolama hesabının tüm depolama dosyası paylaşımlarını listeler</span><span class="sxs-lookup"><span data-stu-id="22850-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="22850-116">Bu komut, depolama hesabı adı olan depolama hesabının tüm depolama dosyası paylaşımlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="22850-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="22850-117">Örnek 3: depolama hesabı nesnesi ve kapsayıcı adı içeren bir depolama blob kapsayıcısı edinin.</span><span class="sxs-lookup"><span data-stu-id="22850-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="22850-118">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı olan bir depolama blob kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="22850-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="22850-119">Örnek 4: kullanımdaki paylaşım kullanımıyla bir depolama dosya paylaşımı alın</span><span class="sxs-lookup"><span data-stu-id="22850-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="22850-120">Bu komut, depolama hesabı adı ve paylaşım adı olan bir depolama dosya paylaşımını alır ve paylaşım kullanımını bayt olarak ekler.</span><span class="sxs-lookup"><span data-stu-id="22850-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="22850-121">Örnek 5: depolama hesabının tüm depolama dosyası paylaşımlarını liste, silinmiş paylaşımları içer</span><span class="sxs-lookup"><span data-stu-id="22850-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="22850-122">Bu komut tüm depolama dosya paylaşımlarına, depolama hesabı adı bulunan bir depolama hesabının silinmiş paylaşımlarını içerir.</span><span class="sxs-lookup"><span data-stu-id="22850-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="22850-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22850-123">PARAMETERS</span></span>

### <span data-ttu-id="22850-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22850-124">-DefaultProfile</span></span>
<span data-ttu-id="22850-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22850-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22850-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="22850-126">-GetShareUsage</span></span>
<span data-ttu-id="22850-127">Paylaşım kullanımını bayt cinsinden almak için bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="22850-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameSingle, AccountObjectSingle, ShareResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22850-128">-Includedeleted</span><span class="sxs-lookup"><span data-stu-id="22850-128">-IncludeDeleted</span></span>
<span data-ttu-id="22850-129">Silinmiş paylaşımları içer varsayılan olarak, liste paylaşımları silinmiş paylaşımları içermez</span><span class="sxs-lookup"><span data-stu-id="22850-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22850-130">-Ad</span><span class="sxs-lookup"><span data-stu-id="22850-130">-Name</span></span>
<span data-ttu-id="22850-131">Paylaşım adı</span><span class="sxs-lookup"><span data-stu-id="22850-131">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, ShareResourceId
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountObjectSingle
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22850-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22850-132">-ResourceGroupName</span></span>
<span data-ttu-id="22850-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="22850-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22850-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="22850-134">-ResourceId</span></span>
<span data-ttu-id="22850-135">Dosya Paylaşımı kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="22850-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="22850-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="22850-136">-StorageAccount</span></span>
<span data-ttu-id="22850-137">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="22850-137">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectSingle, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22850-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="22850-138">-StorageAccountName</span></span>
<span data-ttu-id="22850-139">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="22850-139">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22850-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22850-140">CommonParameters</span></span>
<span data-ttu-id="22850-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22850-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22850-142">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22850-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22850-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22850-143">INPUTS</span></span>

### <span data-ttu-id="22850-144">System. String</span><span class="sxs-lookup"><span data-stu-id="22850-144">System.String</span></span>

### <span data-ttu-id="22850-145">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="22850-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="22850-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22850-146">OUTPUTS</span></span>

### <span data-ttu-id="22850-147">Microsoft. Azure. Commands. Management. Storage. model. PSShare</span><span class="sxs-lookup"><span data-stu-id="22850-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="22850-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22850-148">NOTES</span></span>

## <span data-ttu-id="22850-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22850-149">RELATED LINKS</span></span>
