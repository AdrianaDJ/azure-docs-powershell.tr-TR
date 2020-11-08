---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azdatalakegen2childitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzDataLakeGen2ChildItem.md
ms.openlocfilehash: 9160eabf2492969ad7fa3916791854abd4ef6c44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279359"
---
# <span data-ttu-id="22572-101">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="22572-101">Get-AzDataLakeGen2ChildItem</span></span>

## <span data-ttu-id="22572-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22572-102">SYNOPSIS</span></span>
<span data-ttu-id="22572-103">Dizindeki veya FileSystem kökünden alt dizini ve dosyaları listeler.</span><span class="sxs-lookup"><span data-stu-id="22572-103">Lists sub directorys and files from a directory or filesystem root.</span></span>

## <span data-ttu-id="22572-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="22572-104">SYNTAX</span></span>

```
Get-AzDataLakeGen2ChildItem [-FileSystem] <String> [[-Path] <String>] [-FetchProperty] [-Recurse]
 [-MaxCount <Int32>] [-ContinuationToken <String>] [-AsJob] [-OutputUserPrincipalName]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22572-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="22572-105">DESCRIPTION</span></span>
<span data-ttu-id="22572-106">**Get-AzDataLakeGen2ChildItem** cmdlet 'ı bir Azure depolama hesabında dizindeki veya dizindeki alt dizini ve dosyaları listeler.</span><span class="sxs-lookup"><span data-stu-id="22572-106">The **Get-AzDataLakeGen2ChildItem** cmdlet lists sub directorys and files in a directory or Filesystem in an Azure storage account.</span></span>
<span data-ttu-id="22572-107">Bu cmdlet yalnızca depolama hesabı için hiyerarşik ad alanı etkinleştirilmişse çalışır.</span><span class="sxs-lookup"><span data-stu-id="22572-107">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="22572-108">Bu hesap türü, "New-AzStorageAccount" cmdlet 'i "-EnableHierarchicalNamespace $true" ile çalıştırılabilir.</span><span class="sxs-lookup"><span data-stu-id="22572-108">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="22572-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="22572-109">EXAMPLES</span></span>

### <span data-ttu-id="22572-110">Örnek 1: FileSystem 'dan doğrudan alt öğeleri Listeleme</span><span class="sxs-lookup"><span data-stu-id="22572-110">Example 1: List the direct sub items from a Filesystem</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" 

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1                 True                         2020-03-13 13:07:34Z rwxr-x---    $superuser           $superuser          
dir2                 True                         2020-03-23 09:28:36Z rwxr-x---    $superuser           $superuser
```

<span data-ttu-id="22572-111">Bu komut FileSystem 'dan doğrudan alt öğeleri listeler</span><span class="sxs-lookup"><span data-stu-id="22572-111">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="22572-112">Örnek 2: bir dizinden yinelemeli olarak liste ve özellikleri/ACL 'yi getir</span><span class="sxs-lookup"><span data-stu-id="22572-112">Example 2: List recursively from a directory, and fetch Properties/ACL</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" -Path "dir1/" -Recurse -FetchProperty

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir1/dir3            True                         2020-03-23 09:34:31Z rwx---rwx    $superuser           $superuser          
dir1/file1           False        1024            2020-03-23 09:29:18Z rwx---rwx    $superuser           $superuser           
dir1/testfile_1K_0   False        1024            2020-03-23 09:29:21Z rw-r-----    $superuser           $superuser
```

<span data-ttu-id="22572-113">Bu komut FileSystem 'dan doğrudan alt öğeleri listeler</span><span class="sxs-lookup"><span data-stu-id="22572-113">This command lists the direct sub items from a Filesystem</span></span>

### <span data-ttu-id="22572-114">Örnek 3: birden çok toplu işlem içindeki öğeleri bir FileSystem 'dan yinelemeli olarak listeleme</span><span class="sxs-lookup"><span data-stu-id="22572-114">Example 3: List items recursively from a Filesystem in multiple batches</span></span>
```
PS C:\> $MaxReturn = 10000
PS C:\> $FileSystemName = "filesystem1"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $items = Get-AzDataLakeGen2ChildItem -FileSystem $FileSystemName -Recurse -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $items.Count
     if($items.Length -le 0) { Break;}
     $Token = $items[$items.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total items in Filesystem $FileSystemName"
```

<span data-ttu-id="22572-115">Bu örnekte, birden çok toplu işlem içindeki öğeleri yinelemeli olarak listelemek için *maxCount* ve *continuationtoken* parametreleri kullanılır.</span><span class="sxs-lookup"><span data-stu-id="22572-115">This example uses the *MaxCount* and *ContinuationToken* parameters to list items recursively from a Filesystem in multiple batches.</span></span>
<span data-ttu-id="22572-116">İlk dört komut, örnekte kullanılacak değişkenlere değerler atar.</span><span class="sxs-lookup"><span data-stu-id="22572-116">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="22572-117">Beşinci komut, öğeleri listelemek için **Get-AzDataLakeGen2ChildItem** cmdlet 'ini kullanan bir **do-while** ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="22572-117">The fifth command specifies a **Do-While** statement that uses the **Get-AzDataLakeGen2ChildItem** cmdlet to list items.</span></span>
<span data-ttu-id="22572-118">Bu ifadede $Token değişkeninde depolanan devam belirteci yer alır.</span><span class="sxs-lookup"><span data-stu-id="22572-118">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="22572-119">Döngü çalışırken $Token değişir.</span><span class="sxs-lookup"><span data-stu-id="22572-119">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="22572-120">Final komutu, toplam görüntülemek için **echo** komutunu kullanır.</span><span class="sxs-lookup"><span data-stu-id="22572-120">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="22572-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="22572-121">PARAMETERS</span></span>

### <span data-ttu-id="22572-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="22572-122">-AsJob</span></span>
<span data-ttu-id="22572-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="22572-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22572-124">-Context</span><span class="sxs-lookup"><span data-stu-id="22572-124">-Context</span></span>
<span data-ttu-id="22572-125">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="22572-125">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="22572-126">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="22572-126">-ContinuationToken</span></span>
<span data-ttu-id="22572-127">Devam belirteci.</span><span class="sxs-lookup"><span data-stu-id="22572-127">Continuation Token.</span></span>

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

### <span data-ttu-id="22572-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22572-128">-DefaultProfile</span></span>
<span data-ttu-id="22572-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="22572-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22572-130">-FetchProperty</span><span class="sxs-lookup"><span data-stu-id="22572-130">-FetchProperty</span></span>
<span data-ttu-id="22572-131">Datalake öğe özelliklerini ve ACL 'sini getirir.</span><span class="sxs-lookup"><span data-stu-id="22572-131">Fetch the datalake item properties and ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FetchPermission

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22572-132">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="22572-132">-FileSystem</span></span>
<span data-ttu-id="22572-133">FileSystem adı</span><span class="sxs-lookup"><span data-stu-id="22572-133">FileSystem name</span></span>

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

### <span data-ttu-id="22572-134">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="22572-134">-MaxCount</span></span>
<span data-ttu-id="22572-135">Döndürebileceğiniz en büyük BLOB sayısı.</span><span class="sxs-lookup"><span data-stu-id="22572-135">The max count of the blobs that can return.</span></span>

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

### <span data-ttu-id="22572-136">-OutputUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="22572-136">-OutputUserPrincipalName</span></span>
<span data-ttu-id="22572-137">Bu parametreyi arıyorsanız, her liste girdisinin sahip ve Grup alanlarında döndürülen Kullanıcı kimliği değerleri, Azure Active Directory nesne kimliklerinden, Kullanıcı asıl adlarına dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="22572-137">If speicify this parameter, the user identity values returned in the owner and group fields of each list entry will be transformed from Azure Active Directory Object IDs to User Principal Names.</span></span> <span data-ttu-id="22572-138">Bu parametreyi belirtmezseniz, değerler Azure Active Directory nesne kimlikleri olarak döndürülür.</span><span class="sxs-lookup"><span data-stu-id="22572-138">If not speicify this parameter, the values will be returned as Azure Active Directory Object IDs.</span></span> <span data-ttu-id="22572-139">Grup ve uygulama nesnesi kimliklerinin, benzersiz kolay adları olmadığından çevrilmediğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="22572-139">Note that group and application Object IDs are not translated because they do not have unique friendly names.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22572-140">-Yol</span><span class="sxs-lookup"><span data-stu-id="22572-140">-Path</span></span>
<span data-ttu-id="22572-141">Belirtilen FileSystem 'da alınması gereken yol.</span><span class="sxs-lookup"><span data-stu-id="22572-141">The path in the specified Filesystem that should be retrieved.</span></span>
<span data-ttu-id="22572-142">' Directory1/directory2/' biçiminde bir dizin olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="22572-142">Should be a directory, in the format 'directory1/directory2/'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22572-143">-Recurse</span><span class="sxs-lookup"><span data-stu-id="22572-143">-Recurse</span></span>
<span data-ttu-id="22572-144">Alt öğeyi yinelemeli olarak alır.</span><span class="sxs-lookup"><span data-stu-id="22572-144">Indicates if will recursively get the Child Item.</span></span>
<span data-ttu-id="22572-145">Varsayılan değer yanlıştır.</span><span class="sxs-lookup"><span data-stu-id="22572-145">The default is false.</span></span>

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

### <span data-ttu-id="22572-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22572-146">CommonParameters</span></span>
<span data-ttu-id="22572-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="22572-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22572-148">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22572-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22572-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="22572-149">INPUTS</span></span>

### <span data-ttu-id="22572-150">System. String</span><span class="sxs-lookup"><span data-stu-id="22572-150">System.String</span></span>

### <span data-ttu-id="22572-151">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="22572-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="22572-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="22572-152">OUTPUTS</span></span>

### <span data-ttu-id="22572-153">Microsoft. Windowsazme. Commands. Common. Storage. ResourceModel. AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="22572-153">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="22572-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="22572-154">NOTES</span></span>

## <span data-ttu-id="22572-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="22572-155">RELATED LINKS</span></span>
