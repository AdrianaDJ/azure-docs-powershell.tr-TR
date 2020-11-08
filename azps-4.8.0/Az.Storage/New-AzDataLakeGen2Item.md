---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzDataLakeGen2Item.md
ms.openlocfilehash: 26f3dbc3462688458647e2e9676916063ffa3586
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266257"
---
# <span data-ttu-id="6ceda-101">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="6ceda-101">New-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="6ceda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ceda-102">SYNOPSIS</span></span>
<span data-ttu-id="6ceda-103">FileSystem 'da dosya veya dizin oluşturma.</span><span class="sxs-lookup"><span data-stu-id="6ceda-103">Create a file or directory in a filesystem.</span></span>

## <span data-ttu-id="6ceda-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ceda-104">SYNTAX</span></span>

### <span data-ttu-id="6ceda-105">Dosya (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ceda-105">File (Default)</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -Source <String> [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ceda-106">Directory</span><span class="sxs-lookup"><span data-stu-id="6ceda-106">Directory</span></span>
```
New-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Directory] [-Umask <String>]
 [-Permission <String>] [-Property <Hashtable>] [-Metadata <Hashtable>] [-Force] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ceda-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ceda-107">DESCRIPTION</span></span>
<span data-ttu-id="6ceda-108">**New-AzDataLakeGen2Item** cmdlet 'ı, Azure depolama hesabındaki bir FileSystem 'da dosya veya dizin oluşturur.</span><span class="sxs-lookup"><span data-stu-id="6ceda-108">The **New-AzDataLakeGen2Item** cmdlet creates a file or directory in a Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="6ceda-109">Bu cmdlet yalnızca depolama hesabı için hiyerarşik ad alanı etkinleştirilmişse çalışır.</span><span class="sxs-lookup"><span data-stu-id="6ceda-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="6ceda-110">Bu hesap türü, "New-AzStorageAccount" cmdlet 'i "-EnableHierarchicalNamespace $true" ile çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="6ceda-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="6ceda-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ceda-111">EXAMPLES</span></span>

### <span data-ttu-id="6ceda-112">Örnek 1: belirtilen izin, umask, Özellikler ve meta veriler içeren bir dizin oluşturma</span><span class="sxs-lookup"><span data-stu-id="6ceda-112">Example 1: Create a directory with specified permission, Umask, properties, and metadata</span></span>
```
PS C:\>New-AzDataLakeGen2Item -FileSystem "testfilesystem" -Path "dir1/dir2/" -Directory -Permission rwxrwxrwx -Umask ---rw---- -Property @{"CacheControl" = "READ"; "ContentDisposition" = "True"} -Metadata  @{"tag1" = "value1"; "tag2" = "value2" }

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2            True                         2020-03-23 09:15:56Z rwx---rwx    $superuser           $superuser
```

<span data-ttu-id="6ceda-113">Bu komut, belirtilen Izin, umask, Özellikler ve meta veriler içeren bir dizin oluşturur</span><span class="sxs-lookup"><span data-stu-id="6ceda-113">This command creates a directory with specified Permission, Umask, properties, and metadata</span></span>

### <span data-ttu-id="6ceda-114">Örnek 2: yerel kaynak dosyasından bir Data Lake dosyası oluşturma (karşıya yükleme) ve cmdlet arka planda çalışır</span><span class="sxs-lookup"><span data-stu-id="6ceda-114">Example 2: Create(upload) a data lake file from a local source file, and the cmdlet runs in background</span></span>
```
PS C:\> $task = New-AzDataLakeGen2Item  -FileSystem "testfilesystem" -Path "dir1/dir2/file1" -Source "c:\sourcefile.txt" -Force -asjob
PS C:\> $task | Wait-Job
PS C:\> $task.Output

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group                
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir2/file1      False        14400000        2020-03-23 09:19:13Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="6ceda-115">Bu komut, yerel kaynak dosyasından bir Data Lake dosyası oluşturur (karşıya yükler) ve cmdlet arka planda çalışır.</span><span class="sxs-lookup"><span data-stu-id="6ceda-115">This command creates(upload) a data lake file from a local source file, and the cmdlet runs in background.</span></span>

## <span data-ttu-id="6ceda-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ceda-116">PARAMETERS</span></span>

### <span data-ttu-id="6ceda-117">-Iş</span><span class="sxs-lookup"><span data-stu-id="6ceda-117">-AsJob</span></span>
<span data-ttu-id="6ceda-118">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6ceda-118">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ceda-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6ceda-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6ceda-120">Eşzamanlı eşzamansız görevlerin toplam miktarı.</span><span class="sxs-lookup"><span data-stu-id="6ceda-120">The total amount of concurrent async tasks.</span></span> <span data-ttu-id="6ceda-121">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="6ceda-121">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ceda-122">-Context</span><span class="sxs-lookup"><span data-stu-id="6ceda-122">-Context</span></span>
<span data-ttu-id="6ceda-123">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="6ceda-123">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="6ceda-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ceda-124">-DefaultProfile</span></span>
<span data-ttu-id="6ceda-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ceda-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ceda-126">-Dizin</span><span class="sxs-lookup"><span data-stu-id="6ceda-126">-Directory</span></span>
<span data-ttu-id="6ceda-127">Bu yeni öğenin bir dosya değil dizin olduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ceda-127">Indicates that this new item is a directory and not a file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Directory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ceda-128">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="6ceda-128">-FileSystem</span></span>
<span data-ttu-id="6ceda-129">FileSystem adı</span><span class="sxs-lookup"><span data-stu-id="6ceda-129">FileSystem name</span></span>

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

### <span data-ttu-id="6ceda-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6ceda-130">-Force</span></span>
<span data-ttu-id="6ceda-131">Geçmişse, yeni öğe hiçbir istem olmadan oluşturulur</span><span class="sxs-lookup"><span data-stu-id="6ceda-131">If passed then new item is created without any prompt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ceda-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6ceda-132">-Metadata</span></span>
<span data-ttu-id="6ceda-133">Oluşturulan dizin veya dosyanın meta verilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ceda-133">Specifies metadata for the created directory or file.</span></span>

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

### <span data-ttu-id="6ceda-134">-Yol</span><span class="sxs-lookup"><span data-stu-id="6ceda-134">-Path</span></span>
<span data-ttu-id="6ceda-135">Belirtilen FileSystem 'da oluşturulması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="6ceda-135">The path in the specified Filesystem that should be create.</span></span>
<span data-ttu-id="6ceda-136">' Dizin/file.txt ' veya ' directory1/directory2/' biçiminde bir dosya veya dizin olabilir</span><span class="sxs-lookup"><span data-stu-id="6ceda-136">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ceda-137">-İzin</span><span class="sxs-lookup"><span data-stu-id="6ceda-137">-Permission</span></span>
<span data-ttu-id="6ceda-138">Dosya sahibi, dosya sahibi grubu ve diğerleri için POSIX erişim izinlerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6ceda-138">Sets POSIX access permissions for the file owner, the file owning group, and others.</span></span>
<span data-ttu-id="6ceda-139">Her sınıfa okuma, yazma veya yürütme izni verilebilir.</span><span class="sxs-lookup"><span data-stu-id="6ceda-139">Each class may be granted read, write, or execute permission.</span></span>
<span data-ttu-id="6ceda-140">Sembolik (rwxrw-RW-) desteklenir.</span><span class="sxs-lookup"><span data-stu-id="6ceda-140">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="6ceda-141">-Özellik</span><span class="sxs-lookup"><span data-stu-id="6ceda-141">-Property</span></span>
<span data-ttu-id="6ceda-142">Oluşturulan dizin veya dosyanın özelliklerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ceda-142">Specifies properties for the created directory or file.</span></span> <span data-ttu-id="6ceda-143">Dosya için desteklenen özellikler: CacheControl, ContentDisposition, Contentenkodlamaya, ContentLanguage, ContentMD5, ContentType.</span><span class="sxs-lookup"><span data-stu-id="6ceda-143">The supported properties for file are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentMD5, ContentType.</span></span>
<span data-ttu-id="6ceda-144">Dizin için desteklenen özellikler: CacheControl, ContentDisposition, Contentenkodlama, Içerik dili.</span><span class="sxs-lookup"><span data-stu-id="6ceda-144">The supported properties for directory are: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage.</span></span>

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

### <span data-ttu-id="6ceda-145">-Kaynak</span><span class="sxs-lookup"><span data-stu-id="6ceda-145">-Source</span></span>
<span data-ttu-id="6ceda-146">Datalake Gen2 dosyasına yüklenecek yerel kaynak dosyası yolunu belirtin.</span><span class="sxs-lookup"><span data-stu-id="6ceda-146">Specify the local source file path which will be upload to a Datalake Gen2 file.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ceda-147">-Umask</span><span class="sxs-lookup"><span data-stu-id="6ceda-147">-Umask</span></span>
<span data-ttu-id="6ceda-148">Yeni öğe oluştururken ve üst dizinin varsayılan ACL 'si yoksa umask, dosya veya dizinin izinlerini kısıtlar.</span><span class="sxs-lookup"><span data-stu-id="6ceda-148">When creating New Item and the parent directory does not have a default ACL, the umask restricts the permissions of the file or directory to be created.</span></span>
<span data-ttu-id="6ceda-149">Sonuç izni p & ^ u tarafından verilir; burada p izni, umasdır.</span><span class="sxs-lookup"><span data-stu-id="6ceda-149">The resulting permission is given by p & ^u, where p is the permission and u is the umask.</span></span>
<span data-ttu-id="6ceda-150">Sembolik (rwxrw-RW-) desteklenir.</span><span class="sxs-lookup"><span data-stu-id="6ceda-150">Symbolic (rwxrw-rw-) is supported.</span></span>

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

### <span data-ttu-id="6ceda-151">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ceda-151">-Confirm</span></span>
<span data-ttu-id="6ceda-152">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ceda-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ceda-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ceda-153">-WhatIf</span></span>
<span data-ttu-id="6ceda-154">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ceda-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ceda-155">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ceda-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ceda-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ceda-156">CommonParameters</span></span>
<span data-ttu-id="6ceda-157">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ceda-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ceda-158">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ceda-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ceda-159">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ceda-159">INPUTS</span></span>

### <span data-ttu-id="6ceda-160">System. String</span><span class="sxs-lookup"><span data-stu-id="6ceda-160">System.String</span></span>

### <span data-ttu-id="6ceda-161">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="6ceda-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6ceda-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ceda-162">OUTPUTS</span></span>

### <span data-ttu-id="6ceda-163">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="6ceda-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="6ceda-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ceda-164">NOTES</span></span>

## <span data-ttu-id="6ceda-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ceda-165">RELATED LINKS</span></span>
