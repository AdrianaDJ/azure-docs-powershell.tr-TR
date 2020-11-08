---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 2ef5ddb4a260f4749d6ccca6fa964f5e205c4b4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097780"
---
# <span data-ttu-id="e362f-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="e362f-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="e362f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e362f-102">SYNOPSIS</span></span>
<span data-ttu-id="e362f-103">Depolama dosya paylaşımlarını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="e362f-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="e362f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e362f-104">SYNTAX</span></span>

### <span data-ttu-id="e362f-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e362f-105">AccountName (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e362f-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e362f-106">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e362f-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="e362f-107">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e362f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e362f-108">DESCRIPTION</span></span>
<span data-ttu-id="e362f-109">**Get-Azrmstoragesshares** cmdlet 'ı, depolama dosya paylaşımlarını alır veya listeler.</span><span class="sxs-lookup"><span data-stu-id="e362f-109">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="e362f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e362f-110">EXAMPLES</span></span>

### <span data-ttu-id="e362f-111">Örnek 1: depolama hesabı adı ve paylaşım adıyla bir depolama dosya paylaşımı alın</span><span class="sxs-lookup"><span data-stu-id="e362f-111">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="e362f-112">Bu komut, depolama hesabı adı ve paylaşım adıyla bir depolama dosya paylaşımı alır.</span><span class="sxs-lookup"><span data-stu-id="e362f-112">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="e362f-113">Örnek 2: depolama hesabının tüm depolama dosyası paylaşımlarını listeler</span><span class="sxs-lookup"><span data-stu-id="e362f-113">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
share2   myStorageAccount   myResourceGroup   "0x8D6FF862774FE57" 5120     2019-07-03 07:14:57Z
```

<span data-ttu-id="e362f-114">Bu komut, depolama hesabı adı olan depolama hesabının tüm depolama dosyası paylaşımlarını listeler.</span><span class="sxs-lookup"><span data-stu-id="e362f-114">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="e362f-115">Örnek 3: depolama hesabı nesnesi ve kapsayıcı adı içeren bir depolama blob kapsayıcısı edinin.</span><span class="sxs-lookup"><span data-stu-id="e362f-115">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Get-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="e362f-116">Bu komut, depolama hesabı nesnesi ve kapsayıcı adı olan bir depolama blob kapsayıcısını alır.</span><span class="sxs-lookup"><span data-stu-id="e362f-116">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="e362f-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e362f-117">PARAMETERS</span></span>

### <span data-ttu-id="e362f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e362f-118">-DefaultProfile</span></span>
<span data-ttu-id="e362f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e362f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e362f-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="e362f-120">-Name</span></span>
<span data-ttu-id="e362f-121">Paylaşım adı</span><span class="sxs-lookup"><span data-stu-id="e362f-121">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e362f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e362f-122">-ResourceGroupName</span></span>
<span data-ttu-id="e362f-123">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e362f-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="e362f-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e362f-124">-ResourceId</span></span>
<span data-ttu-id="e362f-125">Dosya Paylaşımı kaynak kimliği girin.</span><span class="sxs-lookup"><span data-stu-id="e362f-125">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="e362f-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e362f-126">-StorageAccount</span></span>
<span data-ttu-id="e362f-127">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="e362f-127">Storage account object</span></span>

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

### <span data-ttu-id="e362f-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e362f-128">-StorageAccountName</span></span>
<span data-ttu-id="e362f-129">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="e362f-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="e362f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e362f-130">CommonParameters</span></span>
<span data-ttu-id="e362f-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e362f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e362f-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e362f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e362f-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e362f-133">INPUTS</span></span>

### <span data-ttu-id="e362f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e362f-134">System.String</span></span>

### <span data-ttu-id="e362f-135">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e362f-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e362f-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e362f-136">OUTPUTS</span></span>

### <span data-ttu-id="e362f-137">Microsoft. Azure. Commands. Management. Storage. model. PSShare</span><span class="sxs-lookup"><span data-stu-id="e362f-137">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="e362f-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e362f-138">NOTES</span></span>

## <span data-ttu-id="e362f-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e362f-139">RELATED LINKS</span></span>
