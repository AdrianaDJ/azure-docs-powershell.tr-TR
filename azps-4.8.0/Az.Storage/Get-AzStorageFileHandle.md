---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileHandle.md
ms.openlocfilehash: 72c3f13749088763348c60ebd27f4d024219c55e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267558"
---
# <span data-ttu-id="919aa-101">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="919aa-101">Get-AzStorageFileHandle</span></span>

## <span data-ttu-id="919aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="919aa-102">SYNOPSIS</span></span>
<span data-ttu-id="919aa-103">Dosya paylaşımının dosya tanıtıcılarını, dosya dizinini veya dosyayı listeler.</span><span class="sxs-lookup"><span data-stu-id="919aa-103">Lists file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="919aa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="919aa-104">SYNTAX</span></span>

### <span data-ttu-id="919aa-105">PaylaşımAdı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="919aa-105">ShareName (Default)</span></span>
```
Get-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="919aa-106">Paylaş</span><span class="sxs-lookup"><span data-stu-id="919aa-106">Share</span></span>
```
Get-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="919aa-107">Directory</span><span class="sxs-lookup"><span data-stu-id="919aa-107">Directory</span></span>
```
Get-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="919aa-108">Dosyasý</span><span class="sxs-lookup"><span data-stu-id="919aa-108">File</span></span>
```
Get-AzStorageFileHandle [-File] <CloudFile> [-Recursive] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="919aa-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="919aa-109">DESCRIPTION</span></span>
<span data-ttu-id="919aa-110">**Get-AzStorageFileHandle** cmdlet 'i, dosya paylaşımının veya dosya dizininin veya dosyanın dosya tanıtıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="919aa-110">The **Get-AzStorageFileHandle** cmdlet lists file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="919aa-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="919aa-111">EXAMPLES</span></span>

### <span data-ttu-id="919aa-112">Örnek 1: dosya paylaşımındaki tüm dosya tanıtıcılarını yinelemeli olarak listeleyin ve</span><span class="sxs-lookup"><span data-stu-id="919aa-112">Example 1: List all file handles on a file share recursively, and sort by ClientIp and OpenTime</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Recursive | Sort-Object ClientIP,OpenTime 

HandleId    Path                  ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----                  --------       ---------- --------             ----------------- ------               --------             ---------          
28506980357                       104.46.105.229 49805      2019-07-29 08:37:36Z                   0                    0                    9297571480349046273
28506980537 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28506980538 dir1                  104.46.105.229 49805      2019-07-30 09:28:48Z                   10376363910205800448 0                    9297571480349046273
28582543365                       104.46.119.170 51675      2019-07-30 09:29:32Z                   0                    0                    9477733061320772929
28582543375 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
28582543376 dir1                  104.46.119.170 51675      2019-07-30 09:29:38Z                   10376363910205800448 0                    9477733061320772929
```

<span data-ttu-id="919aa-113">Bu komut, dosya paylaşımındaki dosya tanıtıcılarını listeler ve çıktıyı, sonra da.</span><span class="sxs-lookup"><span data-stu-id="919aa-113">This command lists file handles on a file share, and sort the output by ClientIp, then by OpenTime.</span></span>

### <span data-ttu-id="919aa-114">Örnek 2: dosya dizininde ilk 2 dosya tutamaçlarını özyinelemeli olarak Listele</span><span class="sxs-lookup"><span data-stu-id="919aa-114">Example 2: List first 2 file handles on a file directory recursively</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2'  -Recursive -First 2

HandleId    Path      ClientIp       ClientPort OpenTime             LastReconnectTime FileId               ParentId             SessionId          
--------    ----      --------       ---------- --------             ----------------- ------               --------             ---------          
24057151779 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
24057151780 dir1/dir2 104.46.105.229 50861      2019-06-18 07:39:23Z                   16140971433240035328 11529285414812647424 9549812641162070049
```

<span data-ttu-id="919aa-115">Bu komut, dosya dizinindeki ilk 2 dosya tanıtıcılarını özyinelemeli olarak listeler.</span><span class="sxs-lookup"><span data-stu-id="919aa-115">This command lists first 2 file handles on a file directory recursively .</span></span>

### <span data-ttu-id="919aa-116">Örnek 3: dosyadaki üçüncü dosya tanıtıcılarını</span><span class="sxs-lookup"><span data-stu-id="919aa-116">Example 3: List the 3rd to the 6th file handles on a file</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -skip 2 -First 4 

HandleId    Path               ClientIp       ClientPort OpenTime             LastReconnectTime FileId              ParentId             SessionId          
--------    ----               --------       ---------- --------             ----------------- ------              --------             ---------          
24055513248 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513249 dir1/dir2/test.txt 104.46.105.229 49817      2019-06-18 08:21:59Z                   9223407221226864640 16140971433240035328 9338416139169958321
24055513252 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
24055513253 dir1/dir2/test.txt 104.46.105.229 49964      2019-06-18 08:22:54Z                   9223407221226864640 16140971433240035328 9338416138431762125
```

<span data-ttu-id="919aa-117">Bu komut, bir dosyadaki 6 dosyası tutamaçlarının üçüncü bir listesini listeler.</span><span class="sxs-lookup"><span data-stu-id="919aa-117">This command lists the 3rd to the 6th file handles on a file.</span></span>

## <span data-ttu-id="919aa-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="919aa-118">PARAMETERS</span></span>

### <span data-ttu-id="919aa-119">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="919aa-119">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="919aa-120">Her isteğin saniye cinsinden istemci tarafı maksimum yürütme süresi.</span><span class="sxs-lookup"><span data-stu-id="919aa-120">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919aa-121">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="919aa-121">-ConcurrentTaskCount</span></span>
<span data-ttu-id="919aa-122">Eşzamanlı eşzamansız görevlerin toplam miktarı.</span><span class="sxs-lookup"><span data-stu-id="919aa-122">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="919aa-123">Varsayılan değer 10 ' dır.</span><span class="sxs-lookup"><span data-stu-id="919aa-123">The default value is 10.</span></span>

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

### <span data-ttu-id="919aa-124">-Context</span><span class="sxs-lookup"><span data-stu-id="919aa-124">-Context</span></span>
<span data-ttu-id="919aa-125">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="919aa-125">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="919aa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919aa-126">-DefaultProfile</span></span>
<span data-ttu-id="919aa-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="919aa-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="919aa-128">-Dizin</span><span class="sxs-lookup"><span data-stu-id="919aa-128">-Directory</span></span>
<span data-ttu-id="919aa-129">CloudFileDirectory nesnesi, dosyaların/dizinlerin listelenmekte olduğu temel klasörü belirtti.</span><span class="sxs-lookup"><span data-stu-id="919aa-129">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="919aa-130">-Dosya</span><span class="sxs-lookup"><span data-stu-id="919aa-130">-File</span></span>
<span data-ttu-id="919aa-131">CloudFile nesnesi dosya tanıtıcılarını listelemek için dosyayı belirtti.</span><span class="sxs-lookup"><span data-stu-id="919aa-131">CloudFile object indicated the file to list File Handles.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="919aa-132">-Yol</span><span class="sxs-lookup"><span data-stu-id="919aa-132">-Path</span></span>
<span data-ttu-id="919aa-133">Var olan bir dosyanın/dizinin yolu.</span><span class="sxs-lookup"><span data-stu-id="919aa-133">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919aa-134">-Yinelemeli</span><span class="sxs-lookup"><span data-stu-id="919aa-134">-Recursive</span></span>
<span data-ttu-id="919aa-135">Liste tutamaçları yinelemeli olarak.</span><span class="sxs-lookup"><span data-stu-id="919aa-135">List handles Recursively.</span></span>
<span data-ttu-id="919aa-136">Yalnızca dosya dizininde çalışır.</span><span class="sxs-lookup"><span data-stu-id="919aa-136">Only works on File Directory.</span></span>

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

### <span data-ttu-id="919aa-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="919aa-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="919aa-138">Her isteğin saniye cinsinden zaman aşımı.</span><span class="sxs-lookup"><span data-stu-id="919aa-138">The server time out for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919aa-139">-Paylaşım</span><span class="sxs-lookup"><span data-stu-id="919aa-139">-Share</span></span>
<span data-ttu-id="919aa-140">CloudFileShare nesnesi, dosyaların/dizinlerin listelendiği paylaşımı belirtti.</span><span class="sxs-lookup"><span data-stu-id="919aa-140">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="919aa-141">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="919aa-141">-ShareName</span></span>
<span data-ttu-id="919aa-142">Dosyaların/dizinlerin listelendiği dosya paylaşımının adı.</span><span class="sxs-lookup"><span data-stu-id="919aa-142">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919aa-143">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="919aa-143">-IncludeTotalCount</span></span>
<span data-ttu-id="919aa-144">Veri kümesindeki (bir tamsayı) ve sonra da nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="919aa-144">Reports the number of objects in the data set (an integer) followed by the objects.</span></span> <span data-ttu-id="919aa-145">Cmdlet toplam sayısını belirleyemiyorsa, ' bilinmeyen toplam sayı ' döndürür.</span><span class="sxs-lookup"><span data-stu-id="919aa-145">If the cmdlet cannot determine the total count, it returns 'Unknown total count'.</span></span>
<span data-ttu-id="919aa-146">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="919aa-146">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="919aa-147">-Atla</span><span class="sxs-lookup"><span data-stu-id="919aa-147">-Skip</span></span>
<span data-ttu-id="919aa-148">İlk ' n ' nesneleri yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="919aa-148">Ignores the first 'n' objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919aa-149">-Önce</span><span class="sxs-lookup"><span data-stu-id="919aa-149">-First</span></span>
<span data-ttu-id="919aa-150">Yalnızca ilk ' n ' nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="919aa-150">Gets only the first 'n' objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919aa-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919aa-151">CommonParameters</span></span>
<span data-ttu-id="919aa-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="919aa-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919aa-153">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="919aa-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919aa-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="919aa-154">INPUTS</span></span>

### <span data-ttu-id="919aa-155">Microsoft. Azure. Storage. File. CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="919aa-155">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="919aa-156">Microsoft. Azure. Storage. File. CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="919aa-156">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="919aa-157">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="919aa-157">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="919aa-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="919aa-158">OUTPUTS</span></span>

### <span data-ttu-id="919aa-159">Microsoft. Azure. Storage. File. FileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="919aa-159">Microsoft.Azure.Storage.File.FileHandleResultSegment</span></span>

## <span data-ttu-id="919aa-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="919aa-160">NOTES</span></span>

## <span data-ttu-id="919aa-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="919aa-161">RELATED LINKS</span></span>
