---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2Item.md
ms.openlocfilehash: ffbfad973e881c3ae88e961517d097d7c8d6cedd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097783"
---
# <span data-ttu-id="7f090-101">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7f090-101">Get-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="7f090-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f090-102">SYNOPSIS</span></span>
<span data-ttu-id="7f090-103">FileSystem 'da bir dosya veya dizinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="7f090-103">Gets the details of a file or directory in a filesystem.</span></span>

## <span data-ttu-id="7f090-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f090-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f090-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f090-105">DESCRIPTION</span></span>
<span data-ttu-id="7f090-106">**Get-AzDataLakeGen2Item** cmdlet 'i, bir Azure depolama hesabındaki bir dosya veya dizinin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="7f090-106">The **Get-AzDataLakeGen2Item** cmdlet gets the details of a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="7f090-107">Bu cmdlet yalnızca depolama hesabı için hiyerarşik ad alanı etkinleştirilmişse çalışır.</span><span class="sxs-lookup"><span data-stu-id="7f090-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="7f090-108">Bu hesap türü, "New-AzStorageAccount" cmdlet 'i "-EnableHierarchicalNamespace $true" ile çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="7f090-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="7f090-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f090-109">EXAMPLES</span></span>

### <span data-ttu-id="7f090-110">Örnek 1: FileSystem 'dan Dizin alma ve ayrıntıları gösterme</span><span class="sxs-lookup"><span data-stu-id="7f090-110">Example 1: Get a directory from a Filesystem, and show the details</span></span>
```
PS C:\> $dir1 = Get-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
PS C:\> $dir1

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser     
 
PS C:\WINDOWS\system32> $dir1.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      ---        
False        Other                      rwx      

PS C:\WINDOWS\system32> $dir1.Permissions

Owner        : Execute, Write, Read
Group        : None
Other        : Execute, Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\WINDOWS\system32> $dir1.Properties.Metadata

Key          Value 
---          ----- 
hdi_isfolder true  
tag1         value1
tag2         value2

PS C:\WINDOWS\system32> $dir1.Properties

LastModified          : 3/23/2020 9:15:56 AM +00:00
CreatedOn             : 3/23/2020 9:15:56 AM +00:00
Metadata              : {[hdi_isfolder, true], [tag1, value1], [tag2, value2]}
CopyCompletedOn       : 1/1/0001 12:00:00 AM +00:00
CopyStatusDescription : 
CopyId                : 
CopyProgress          : 
CopySource            : 
CopyStatus            : Pending
IsIncrementalCopy     : False
LeaseDuration         : Infinite
LeaseState            : Available
LeaseStatus           : Unlocked
ContentLength         : 0
ContentType           : application/octet-stream
ETag                  : "0x8D7CF0ACBA35FA8"
ContentHash           : 
ContentEncoding       : UDF12
ContentDisposition    : 
ContentLanguage       : 
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="7f090-111">Bu komut FileSystem 'dan bir dizin alır ve ayrıntıları gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f090-111">This command gets a directory from a Filesystem, and show the details.</span></span>

### <span data-ttu-id="7f090-112">Örnek 2: FileSystem 'dan dosya alma</span><span class="sxs-lookup"><span data-stu-id="7f090-112">Example 2: Get a file from a Filesystem</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:20:37Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="7f090-113">Bu komut FileSystem 'dan bir dosyanın ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="7f090-113">This command gets the details of a file from a Filesystem.</span></span> 

## <span data-ttu-id="7f090-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f090-114">PARAMETERS</span></span>

### <span data-ttu-id="7f090-115">-Context</span><span class="sxs-lookup"><span data-stu-id="7f090-115">-Context</span></span>
<span data-ttu-id="7f090-116">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="7f090-116">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f090-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f090-117">-DefaultProfile</span></span>
<span data-ttu-id="7f090-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f090-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f090-119">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="7f090-119">-FileSystem</span></span>
<span data-ttu-id="7f090-120">FileSystem adı</span><span class="sxs-lookup"><span data-stu-id="7f090-120">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f090-121">-Yol</span><span class="sxs-lookup"><span data-stu-id="7f090-121">-Path</span></span>
<span data-ttu-id="7f090-122">Belirtilen FileSystem 'da alınması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="7f090-122">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="7f090-123">' Dizin/file.txt ' veya ' directory1/directory2/' biçiminde bir dosya veya dizin olabilir.</span><span class="sxs-lookup"><span data-stu-id="7f090-123">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="7f090-124">FileSystem 'ın kök dizinini almak için bu parametreyi belirtmeyin.</span><span class="sxs-lookup"><span data-stu-id="7f090-124">Not specify this parameter to get the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f090-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f090-125">CommonParameters</span></span>
<span data-ttu-id="7f090-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f090-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f090-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f090-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f090-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f090-128">INPUTS</span></span>

### <span data-ttu-id="7f090-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7f090-129">System.String</span></span>

### <span data-ttu-id="7f090-130">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="7f090-130">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7f090-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f090-131">OUTPUTS</span></span>

### <span data-ttu-id="7f090-132">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="7f090-132">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="7f090-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f090-133">NOTES</span></span>

## <span data-ttu-id="7f090-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f090-134">RELATED LINKS</span></span>
