---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 1d2a4bc1dd9dab05e56f8b69c92d98985cf98e15
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275783"
---
# <span data-ttu-id="e9c4d-101">Set-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="e9c4d-101">Set-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="e9c4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9c4d-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c4d-103">Belirtilen yolda ACL yinelemeli olarak ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-103">Set ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="e9c4d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9c4d-104">SYNTAX</span></span>

```
Set-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e9c4d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9c4d-105">DESCRIPTION</span></span>
<span data-ttu-id="e9c4d-106">**Set-AzDataLakeGen2AclRecursive** cmdlet 'i BELIRTILEN yoldaki ACL 'yi yinelemeli olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-106">The **Set-AzDataLakeGen2AclRecursive** cmdlet sets ACL recursively on the specified path.</span></span> <span data-ttu-id="e9c4d-107">Giriş ACL 'SI özgün ACL 'yi tamamen değiştirir.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-107">The input ACL will replace original ACL completely.</span></span>

## <span data-ttu-id="e9c4d-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9c4d-108">EXAMPLES</span></span>

### <span data-ttu-id="e9c4d-109">Örnek 1: bir doğruarda ACL 'yi yinelemeli olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="e9c4d-109">Example 1: Set ACL recursively on a directiry</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="e9c4d-110">Bu komut öncelikle 3 ACL girişi olan bir ACL nesnesi oluşturur ve ardından ACL 'yi özyinelemeli olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-110">This command first creates an ACL object with 3 acl entries, then sets ACL recursively on a directory.</span></span>

### <span data-ttu-id="e9c4d-111">Örnek 2: FileSystem 'ın kök dizininde ACL 'yi yinelemeli olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="e9c4d-111">Example 2: Set ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl  -Context $ctx

PS C:\> $result

FailedEntries                   : {dir1/dir2/file4}
TotalDirectoriesSuccessfulCount : 500
TotalFilesSuccessfulCount       : 2500
TotalFailureCount               : 1
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="e9c4d-112">Bu komut önce ACL 'yi özyinelemeli olarak bir kök dizine ayarlar ve başarısız oldu, ardından Kullanıcı başarısız dosyayı düzelttikten sonra ContinuationToken ile devam edin.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-112">This command first sets ACL recursively to a root directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="e9c4d-113">Örnek 3: ACL yinelemeli öbeği öbeği ile ayarlama</span><span class="sxs-lookup"><span data-stu-id="e9c4d-113">Example 3: Set ACL recursively chunk by chunk</span></span>
```
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 2 -ContinuationToken $token -Context $ctx

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and ($result.TotalFailureCount -eq 0))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="e9c4d-114">Bu komut dosyası, ACL 'yi, öbek boyutu BatchSize \* MaxBatchCount olarak öbek boyutu ile öbek ile dizin öbeğiyle birlikte ayarlar.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-114">This script sets ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="e9c4d-115">Öbek boyutu bu betikte 200.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-115">Chunk size is 200 in this script.</span></span>

### <span data-ttu-id="e9c4d-116">Örnek 4: ACL 'yi yinelemeli olarak bir dizinde ayarlama ve devam etme</span><span class="sxs-lookup"><span data-stu-id="e9c4d-116">Example 4: Set ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

PS C:\> $result

FailedEntries                   : {dir0/dir1/file1, dir0/dir2/file4}
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 500
TotalFailureCount               : 2
ContinuationToken               : VBaHi5TfyO2ai1wYTRhIL2FjbGNibjA2c3RmATAxRDVEN0UzRENFQzZCRTAvYWRsc3Rlc3QyATAxRDY2M0ZCQTZBN0JGQTkvZGlyMC9kaXIxL2ZpbGUzFgAAAA==

PS C:\> $result.FailedEntries

Name            IsDirectory ErrorMessage                                                                   
----            ----------- ------------                                                                   
dir0/dir1/file1       False This request is not authorized to perform this operation using this permission.
dir0/dir2/file4       False This request is not authorized to perform this operation using this permission.

# user need fix the failed item , then can resume with ContinuationToken

PS C:\> foreach ($path in $result.FailedEntries.Name)
        {
            # user code to fix failed entry in $path
            
            #set ACL again
            Set-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path $path -Acl $acl -Context $ctx
        }
```

<span data-ttu-id="e9c4d-117">Bu komut önce ACL 'yi yinelemeli olarak devam eden bir dizine ayarlar ve bazı öğeler başarısız oldu ve bazı öğeler başarısız oldu, ardından başarısız öğeleri teker teker devam ettirir.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-117">This command first sets ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="e9c4d-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9c4d-118">PARAMETERS</span></span>

### <span data-ttu-id="e9c4d-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="e9c4d-119">-Acl</span></span>
<span data-ttu-id="e9c4d-120">Dosya veya dizin için yinelemeli olarak ayarlanacak POSIX erişimi denetim listesi.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-120">The POSIX access control list to set recursively for the file or directory.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSPathAccessControlEntry[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c4d-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="e9c4d-121">-AsJob</span></span>
<span data-ttu-id="e9c4d-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="e9c4d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e9c4d-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="e9c4d-123">-BatchSize</span></span>
<span data-ttu-id="e9c4d-124">Veri kümesi boyutu, toplu işlem boyutunu aşıyorsa, işlem birden çok isteklere bölünecek ve böylece ilerleme izlenebilir.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="e9c4d-125">Toplu iş boyutu 1 ile 2000 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="e9c4d-126">Varsayılan 2000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-126">Default is 2000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c4d-127">-Context</span><span class="sxs-lookup"><span data-stu-id="e9c4d-127">-Context</span></span>
<span data-ttu-id="e9c4d-128">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="e9c4d-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="e9c4d-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="e9c4d-129">-ContinuationToken</span></span>
<span data-ttu-id="e9c4d-130">Devam belirteci.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-130">Continuation Token.</span></span>

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

### <span data-ttu-id="e9c4d-131">-Devam et</span><span class="sxs-lookup"><span data-stu-id="e9c4d-131">-ContinueOnFailure</span></span>
<span data-ttu-id="e9c4d-132">Bu parametreyi, hataları yoksaymak ve dizinin diğer alt varlıklarındaki işlemi sürdürmek için ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="e9c4d-133">Varsayılan işlem, hatalarla karşılaşmasında hızla sonlandırılır.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="e9c4d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c4d-134">-DefaultProfile</span></span>
<span data-ttu-id="e9c4d-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9c4d-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="e9c4d-136">-FileSystem</span></span>
<span data-ttu-id="e9c4d-137">FileSystem adı</span><span class="sxs-lookup"><span data-stu-id="e9c4d-137">FileSystem name</span></span>

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

### <span data-ttu-id="e9c4d-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="e9c4d-138">-MaxBatchCount</span></span>
<span data-ttu-id="e9c4d-139">Tek tek erişim denetimi işleminin yürütüleceği en fazla toplu iş sayısı.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="e9c4d-140">Veri kümesi boyutu MaxBatchCount çarp BatchSize değerini aşıyorsa, devam belirteci döndürülür.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c4d-141">-Yol</span><span class="sxs-lookup"><span data-stu-id="e9c4d-141">-Path</span></span>
<span data-ttu-id="e9c4d-142">Belirtilen FileSystem 'daki, ACL 'yi özyinelemeli olarak değiştirmesi gereken yol.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="e9c4d-143">Dosya veya dizin olabilir.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-143">Can be a file or directory.</span></span>
<span data-ttu-id="e9c4d-144">' Dizin/file.txt ' veya ' directory1/directory2/' biçiminde.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="e9c4d-145">Atla bu parametreyi, ACL 'yi özyinelemeli olarak FileSystem 'ın kök dizininden değiştirmek için ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="e9c4d-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9c4d-146">-Confirm</span></span>
<span data-ttu-id="e9c4d-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9c4d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9c4d-148">-WhatIf</span></span>
<span data-ttu-id="e9c4d-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9c4d-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9c4d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c4d-151">CommonParameters</span></span>
<span data-ttu-id="e9c4d-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9c4d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c4d-153">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c4d-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c4d-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9c4d-154">INPUTS</span></span>

### <span data-ttu-id="e9c4d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="e9c4d-155">System.String</span></span>

### <span data-ttu-id="e9c4d-156">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="e9c4d-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e9c4d-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9c4d-157">OUTPUTS</span></span>

### <span data-ttu-id="e9c4d-158">System. String</span><span class="sxs-lookup"><span data-stu-id="e9c4d-158">System.String</span></span>

## <span data-ttu-id="e9c4d-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9c4d-159">NOTES</span></span>

## <span data-ttu-id="e9c4d-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9c4d-160">RELATED LINKS</span></span>
