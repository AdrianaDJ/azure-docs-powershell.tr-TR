---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2Item.md
ms.openlocfilehash: 6af68da41e1d5ea212d23d0cbc2296a68a6fa7e5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096977"
---
# <span data-ttu-id="5363e-101">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="5363e-101">Update-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="5363e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5363e-102">SYNOPSIS</span></span>
<span data-ttu-id="5363e-103">Özellikler, meta veriler, izin, ACL ve sahip özellikleri</span><span class="sxs-lookup"><span data-stu-id="5363e-103">Update a file or directory on properties, metadata, permission, ACL, and owner.</span></span>

## <span data-ttu-id="5363e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5363e-104">SYNTAX</span></span>

### <span data-ttu-id="5363e-105">ReceiveManual (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5363e-105">ReceiveManual (Default)</span></span>
```
Update-AzDataLakeGen2Item [-FileSystem] <String> [-Path <String>] [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5363e-106">Itempipeline</span><span class="sxs-lookup"><span data-stu-id="5363e-106">ItemPipeline</span></span>
```
Update-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Permission <String>] [-Owner <String>]
 [-Group <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Acl <PSPathAccessControlEntry[]>]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5363e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5363e-107">DESCRIPTION</span></span>
<span data-ttu-id="5363e-108">**Update-AzDataLakeGen2Item** cmdlet 'i, özellikleri, meta verileri, ızın, ACL ve sahip dosyalarını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5363e-108">The **Update-AzDataLakeGen2Item** cmdlet updates a file or directory on properties, metadata, permission, ACL, and owner.</span></span>
<span data-ttu-id="5363e-109">Bu cmdlet yalnızca depolama hesabı için hiyerarşik ad alanı etkinleştirilmişse çalışır.</span><span class="sxs-lookup"><span data-stu-id="5363e-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="5363e-110">Bu hesap türü, "New-AzStorageAccount" cmdlet 'i "-EnableHierarchicalNamespace $true" ile çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="5363e-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="5363e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5363e-111">EXAMPLES</span></span>

### <span data-ttu-id="5363e-112">Örnek 1:3 ACL girişi olan bir ACL nesnesi oluşturma ve bir FileSystem 'daki tüm öğelere ACL 'yi yinelemeli olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="5363e-112">Example 1: Create an ACL object with 3 ACL entry, and update ACL to all items in a Filesystem recursively</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Recurse | Update-AzDataLakeGen2Item -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser           
dir1/file1           False        1024            2020-03-23 09:29:18Z rwxrw-rw-    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="5363e-113">Bu komut önce, 3 ACL girişi içeren bir ACL nesnesi oluşturur (var olan ACL nesnesine ACL girişi eklemek için-InputObject parametresi kullanın), sonra bir FileSystem 'daki tüm öğeleri alın ve öğelerde ACL 'yi güncelleştirin.</span><span class="sxs-lookup"><span data-stu-id="5363e-113">This command first creates an ACL object with 3 acl entry (use -InputObject parameter to add acl entry to existing acl object), then get all items in a filesystem and update acl on the items.</span></span>

### <span data-ttu-id="5363e-114">Örnek 2: dosyadaki tüm özellikleri güncelleştirme ve gösterme</span><span class="sxs-lookup"><span data-stu-id="5363e-114">Example 2: Update all properties on a file, and show them</span></span>
```
PS C:\> $file = Update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" `
                 -Acl $acl `
                 -Property @{"ContentType" = "image/jpeg"; "ContentMD5" = "i727sP7HigloQDsqadNLHw=="; "ContentEncoding" = "UDF8"; "CacheControl" = "READ"; "ContentDisposition" = "True"; "ContentLanguage" = "EN-US"} `
                 -Metadata  @{"tag1" = "value1"; "tag2" = "value2" } `
                 -Permission rw-rw-rwx `
                 -Owner '$superuser' `
                 -Group '$superuser'

PS C:\> $file

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/file1           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser          

PS C:\> $file.ACL

DefaultScope AccessControlType EntityId Permissions
------------ ----------------- -------- -----------
False        User                       rwx        
False        Group                      rw-        
False        Other                      rw-        

PS C:\> $file.Permissions

Owner        : Execute, Write, Read
Group        : Write, Read
Other        : Write, Read
StickyBit    : False
ExtendedAcls : False

PS C:\> $file.Properties.Metadata

Key  Value 
---  ----- 
tag2 value2
tag1 value1

PS C:\> $file.Properties


LastModified          : 3/23/2020 9:57:33 AM +00:00
CreatedOn             : 3/23/2020 9:29:18 AM +00:00
Metadata              : {[tag2, value2], [tag1, value1]}
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
ContentLength         : 1024
ContentType           : image/jpeg
ETag                  : "0x8D7CF109B9878CC"
ContentHash           : {139, 189, 187, 176...}
ContentEncoding       : UDF8
ContentDisposition    : True
ContentLanguage       : EN-US
CacheControl          : READ
AcceptRanges          : bytes
IsServerEncrypted     : True
EncryptionKeySha256   : 
AccessTier            : Cool
ArchiveStatus         : 
AccessTierChangedOn   : 1/1/0001 12:00:00 AM +00:00
```

<span data-ttu-id="5363e-115">Bu komut, bir dosyadaki tüm özellikleri güncelleştirir (ACL, izin, sahip, Grup, meta veri, özellik herhangi bir uyumluluk ile güncelleştirilebilir) ve bunları PowerShell konsolunda gösterebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5363e-115">This command updates all properties on a file (ACL, permission,owner, group, metadata, property can be updated with any conbination), and show them in Powershell console.</span></span>

### <span data-ttu-id="5363e-116">Örnek 3: dizine ACL girdisi ekleme</span><span class="sxs-lookup"><span data-stu-id="5363e-116">Example 3: Add an ACL entry to a directory</span></span>
```
## Get the origin ACL
PS C:\> $acl = (Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/').ACL

# Update permission of a new ACL entry (if ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry)
PS C:\> $acl = Set-AzDataLakeGen2ItemAclObject -AccessControlType user -EntityId $id -Permission rw- -InputObject $acl  

# set the new acl to the directory
PS C:\> update-AzDataLakeGen2Item -FileSystem "filesystem1" -Path 'dir1/dir3/' -ACL $acl

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwxrw-rw-+   $superuser           $superuser
```

<span data-ttu-id="5363e-117">Bu komut, bir dizinden ACL alır, bir ACL girişi ekler/dizine geri döner.</span><span class="sxs-lookup"><span data-stu-id="5363e-117">This command gets ACL from a directory, updates/adds an ACL entry, and sets back to the directory.</span></span>
<span data-ttu-id="5363e-118">Aynı AccessControlType/EntityId/DefaultScope içeren ACL girişi yoksa, yeni bir ACL girişi ekler, başka bir ACL girişi veya mevcut ACL girdisinin izinlerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5363e-118">If ACL entry with same AccessControlType/EntityId/DefaultScope not exist, will add a new ACL entry, else update permission of existing ACL entry.</span></span>

## <span data-ttu-id="5363e-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5363e-119">PARAMETERS</span></span>

### <span data-ttu-id="5363e-120">-ACL</span><span class="sxs-lookup"><span data-stu-id="5363e-120">-Acl</span></span>
<span data-ttu-id="5363e-121">Dosyalarda ve dizinlerde POSIX erişimi denetim haklarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5363e-121">Sets POSIX access control rights on files and directories.</span></span>
<span data-ttu-id="5363e-122">Bu nesneyi New-AzDataLakeGen2ItemAclObject ile oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5363e-122">Create this object with New-AzDataLakeGen2ItemAclObject.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5363e-123">-Context</span><span class="sxs-lookup"><span data-stu-id="5363e-123">-Context</span></span>
<span data-ttu-id="5363e-124">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="5363e-124">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="5363e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5363e-125">-DefaultProfile</span></span>
<span data-ttu-id="5363e-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5363e-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5363e-127">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="5363e-127">-FileSystem</span></span>
<span data-ttu-id="5363e-128">FileSystem adı</span><span class="sxs-lookup"><span data-stu-id="5363e-128">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5363e-129">-Group</span><span class="sxs-lookup"><span data-stu-id="5363e-129">-Group</span></span>
<span data-ttu-id="5363e-130">Blob 'un sahip olduğu grubu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5363e-130">Sets the owning group of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5363e-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5363e-131">-InputObject</span></span>
<span data-ttu-id="5363e-132">Güncelleştirilecek Azure Datalake Gen2 öğesi nesnesi</span><span class="sxs-lookup"><span data-stu-id="5363e-132">Azure Datalake Gen2 Item Object to update</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5363e-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5363e-133">-Metadata</span></span>
<span data-ttu-id="5363e-134">Dizinin veya dosyanın meta verilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5363e-134">Specifies metadata for the directory or file.</span></span>

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

### <span data-ttu-id="5363e-135">-Sahip</span><span class="sxs-lookup"><span data-stu-id="5363e-135">-Owner</span></span>
<span data-ttu-id="5363e-136">Blob 'un sahibini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5363e-136">Sets the owner of the blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5363e-137">-Yol</span><span class="sxs-lookup"><span data-stu-id="5363e-137">-Path</span></span>
<span data-ttu-id="5363e-138">Belirtilen FileSystem 'ın güncellenmesi gereken yolu.</span><span class="sxs-lookup"><span data-stu-id="5363e-138">The path in the specified Filesystem that should be updated.</span></span>
<span data-ttu-id="5363e-139">' Dizin/file.txt ' veya ' directory1/directory2/' biçiminde bir dosya veya dizin olabilir.</span><span class="sxs-lookup"><span data-stu-id="5363e-139">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="5363e-140">Belirtmiyor bu parametre FileSystem 'ın kök dizinini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="5363e-140">Not specify this parameter will update the root directory of the Filesystem.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5363e-141">-İzin</span><span class="sxs-lookup"><span data-stu-id="5363e-141">-Permission</span></span>
<span data-ttu-id="5363e-142">Dosya sahibi, dosya sahibi grubu ve diğerleri için POSIX erişim izinlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5363e-142">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="5363e-143">Her sınıfa okuma, yazma veya yürütme izni verilebilir.</span><span class="sxs-lookup"><span data-stu-id="5363e-143">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="5363e-144">Sembolik (rwxrw-RW-) desteklenir.</span><span class="sxs-lookup"><span data-stu-id="5363e-144">Symbolic (rwxrw-rw-) is supported.</span></span>
<span data-ttu-id="5363e-145">ACL ile birlikte geçersiz.</span><span class="sxs-lookup"><span data-stu-id="5363e-145">Invalid in conjunction with Acl.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5363e-146">-Özellik</span><span class="sxs-lookup"><span data-stu-id="5363e-146">-Property</span></span>
<span data-ttu-id="5363e-147">Dizin veya dosya için özellikleri belirtir.</span><span class="sxs-lookup"><span data-stu-id="5363e-147">Specifies properties for the directory or file.</span></span> <span data-ttu-id="5363e-148">Dosya için desteklenen özellikler: CacheControl, ContentDisposition, Contentenkodlamaya, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="5363e-148">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="5363e-149">Dizin için desteklenen özellikler: CacheControl, ContentDisposition, Contentenkodlama, Içerik dili.</span><span class="sxs-lookup"><span data-stu-id="5363e-149">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="5363e-150">-Onay</span><span class="sxs-lookup"><span data-stu-id="5363e-150">-Confirm</span></span>
<span data-ttu-id="5363e-151">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5363e-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5363e-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5363e-152">-WhatIf</span></span>
<span data-ttu-id="5363e-153">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5363e-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5363e-154">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5363e-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5363e-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5363e-155">CommonParameters</span></span>
<span data-ttu-id="5363e-156">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5363e-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5363e-157">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5363e-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5363e-158">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5363e-158">INPUTS</span></span>

### <span data-ttu-id="5363e-159">System. String</span><span class="sxs-lookup"><span data-stu-id="5363e-159">System.String</span></span>

### <span data-ttu-id="5363e-160">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="5363e-160">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="5363e-161">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="5363e-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="5363e-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5363e-162">OUTPUTS</span></span>

### <span data-ttu-id="5363e-163">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="5363e-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="5363e-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5363e-164">NOTES</span></span>

## <span data-ttu-id="5363e-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5363e-165">RELATED LINKS</span></span>