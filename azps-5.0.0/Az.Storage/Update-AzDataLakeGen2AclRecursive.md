---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azdatalakegen2aclrecursive
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzDataLakeGen2AclRecursive.md
ms.openlocfilehash: 80b1816dff686db7e84bf876fd74f9642389b42f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278460"
---
# <span data-ttu-id="2a2e2-101">Update-AzDataLakeGen2AclRecursive</span><span class="sxs-lookup"><span data-stu-id="2a2e2-101">Update-AzDataLakeGen2AclRecursive</span></span>

## <span data-ttu-id="2a2e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a2e2-102">SYNOPSIS</span></span>
<span data-ttu-id="2a2e2-103">Belirtilen yolda ACL 'yi yinelemeli olarak güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-103">Update ACL recursively on the specified path.</span></span> 

## <span data-ttu-id="2a2e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a2e2-104">SYNTAX</span></span>

```
Update-AzDataLakeGen2AclRecursive [-FileSystem] <String> [[-Path] <String>] [-ContinuationToken <String>]
 -Acl <PSPathAccessControlEntry[]> [-ContinueOnFailure] [-BatchSize <Int32>] [-MaxBatchCount <Int32>] [-AsJob]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a2e2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a2e2-105">DESCRIPTION</span></span>
<span data-ttu-id="2a2e2-106">**Update-AzDataLakeGen2AclRecursive** cmdlet 'i BELIRTILEN yoldaki ACL 'yi yinelemeli olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-106">The **Update-AzDataLakeGen2AclRecursive** cmdlet updates ACL recursively on the specified path.</span></span> <span data-ttu-id="2a2e2-107">Giriş ACL 'si özgün ACL 'yi birleşir: aynı AccessControlType/EntityId/DefaultScope içeren ACL girdisi varsa, Güncelleştir izni; başka bir ACL girişi ekleyin.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-107">The input ACL will merge the the original ACL: If ACL entry with same AccessControlType/EntityId/DefaultScope exist, update permission; else add a new ACL entry.</span></span>

## <span data-ttu-id="2a2e2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a2e2-108">EXAMPLES</span></span>

### <span data-ttu-id="2a2e2-109">Örnek 1: FileSystem 'ın kök dizininde</span><span class="sxs-lookup"><span data-stu-id="2a2e2-109">Example 1: Update ACL recursively on a root directiry of filesystem</span></span>
```
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType user -Permission rwx 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType group -Permission rw- -InputObject $acl 
PS C:\>$acl = New-AzDataLakeGen2ItemAclObject -AccessControlType other -Permission "rw-" -InputObject $acl
PS C:\> Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Acl $acl -Context $ctx

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 7
TotalFilesSuccessfulCount       : 5
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="2a2e2-110">Bu komut öncelikle 3 ACL girişi olan bir ACL nesnesi oluşturur, ardından dosya sisteminin kök dizininde ACL 'yi özyinelemeli olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-110">This command first creates an ACL object with 3 acl entries, then updates ACL recursively on a root directory of a file system.</span></span>

### <span data-ttu-id="2a2e2-111">Örnek 2: ACL 'yi özyinelemeli olarak güncelleştirme ve ContinuationToken ile hatadan sürdürme</span><span class="sxs-lookup"><span data-stu-id="2a2e2-111">Example 2: Update ACL recursively on a directory, and resume from failure with ContinuationToken</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -Context $ctx

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

PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinuationToken $result.ContinuationToken -Context $ctx

PS C:\> $result

FailedEntries                   : 
TotalDirectoriesSuccessfulCount : 100
TotalFilesSuccessfulCount       : 1000
TotalFailureCount               : 0
ContinuationToken               :
```

<span data-ttu-id="2a2e2-112">Bu komut ilk olarak bir dizine özyinelemeli olarak güncelleştirme yapın ve başarısız oldu, ardından Kullanıcı başarısız dosyayı düzelttikten sonra ContinuationToken ile devam edin.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-112">This command first updateds ACL recursively to a directory and failed, then resume with ContinuationToken after user fix the failed file.</span></span>

### <span data-ttu-id="2a2e2-113">Örnek 3: ACL yinelemeli öbeği öbeğiyle güncelleştirin</span><span class="sxs-lookup"><span data-stu-id="2a2e2-113">Example 3: Update ACL recursively chunk by chunk</span></span>
```
$ContinueOnFailure = $true # Set it to $false if want to terminate the operation quickly on encountering failures
$token = $null
$TotalDirectoriesSuccess = 0
$TotalFilesSuccess = 0
$totalFailure = 0
$FailedEntries = New-Object System.Collections.Generic.List[System.Object]
do
{
    
    if ($ContinueOnFailure)
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx -ContinueOnFailure
    }
    else
    {
        $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl  -BatchSize 100 -MaxBatchCount 50 -ContinuationToken $token -Context $ctx
    }

    # echo $result
    $TotalFilesSuccess += $result.TotalFilesSuccessfulCount
    $TotalDirectoriesSuccess += $result.TotalDirectoriesSuccessfulCount
    $totalFailure += $result.TotalFailureCount
    $FailedEntries += $result.FailedEntries
    $token = $result.ContinuationToken
}while (($token -ne $null) -and (($ContinueOnFailure) -or ($result.TotalFailureCount -eq 0)))
echo ""
echo "[Result Summary]"
echo "TotalDirectoriesSuccessfulCount: `t$($TotalDirectoriesSuccess)"
echo "TotalFilesSuccessfulCount: `t`t`t$($TotalFilesSuccess)"
echo "TotalFailureCount: `t`t`t`t`t$($totalFailure)"
echo "ContinuationToken: `t`t`t`t`t$($token)"
echo "FailedEntries:"$($FailedEntries | ft)
```

<span data-ttu-id="2a2e2-114">Bu komut dosyası, ACL 'yi, öbek boyutu için BatchSize \* MaxBatchCount olarak öbek boyutu ile dizin öbeğiyle sırayla güncelleştirecek.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-114">This script will update ACL rescursively on directory chunk by chunk, with chunk size as BatchSize \* MaxBatchCount.</span></span> <span data-ttu-id="2a2e2-115">Öbek boyutu bu betikte 5000.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-115">Chunk size is 5000 in this script.</span></span>

### <span data-ttu-id="2a2e2-116">Örnek 4: ACL 'yi yinelemeli olarak güncelleştirme ve devam etme</span><span class="sxs-lookup"><span data-stu-id="2a2e2-116">Example 4: Update ACL recursively on a directory and ContinueOnFailure, then resume from failures one by one</span></span>
```
PS C:\> $result = Update-AzDataLakeGen2AclRecursive -FileSystem "filesystem1" -Path "dir1" -Acl $acl -ContinueOnFailure -Context $ctx

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

<span data-ttu-id="2a2e2-117">Bu komut ilk olarak devam eden bir dizine yinelemeli olarak güncelleştirmem ve bazı öğeler başarısız oldu ve bazı öğeler başarısız oldu, ardından başarısız öğeleri teker teker sürdürün.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-117">This command first updateds ACL recursively to a directory with ContinueOnFailure, and some items failed, then resume the failed items one by one.</span></span>

## <span data-ttu-id="2a2e2-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a2e2-118">PARAMETERS</span></span>

### <span data-ttu-id="2a2e2-119">-ACL</span><span class="sxs-lookup"><span data-stu-id="2a2e2-119">-Acl</span></span>
<span data-ttu-id="2a2e2-120">Dosya veya dizin için yinelemeli olarak ayarlanacak POSIX erişimi denetim listesi.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-120">The POSIX access control list to set recursively for the file or directory.</span></span>

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

### <span data-ttu-id="2a2e2-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="2a2e2-121">-AsJob</span></span>
<span data-ttu-id="2a2e2-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="2a2e2-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2a2e2-123">-BatchSize</span><span class="sxs-lookup"><span data-stu-id="2a2e2-123">-BatchSize</span></span>
<span data-ttu-id="2a2e2-124">Veri kümesi boyutu, toplu işlem boyutunu aşıyorsa, işlem birden çok isteklere bölünecek ve böylece ilerleme izlenebilir.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-124">If data set size exceeds batch size then operation will be split into multiple requests so that progress can be tracked.</span></span>
<span data-ttu-id="2a2e2-125">Toplu iş boyutu 1 ile 2000 arasında olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-125">Batch size should be between 1 and 2000.</span></span>
<span data-ttu-id="2a2e2-126">Varsayılan 2000 ' dır.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-126">Default is 2000.</span></span>

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

### <span data-ttu-id="2a2e2-127">-Context</span><span class="sxs-lookup"><span data-stu-id="2a2e2-127">-Context</span></span>
<span data-ttu-id="2a2e2-128">Azure depolama bağlamı nesnesi</span><span class="sxs-lookup"><span data-stu-id="2a2e2-128">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="2a2e2-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="2a2e2-129">-ContinuationToken</span></span>
<span data-ttu-id="2a2e2-130">Devam belirteci.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-130">Continuation Token.</span></span>

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

### <span data-ttu-id="2a2e2-131">-Devam et</span><span class="sxs-lookup"><span data-stu-id="2a2e2-131">-ContinueOnFailure</span></span>
<span data-ttu-id="2a2e2-132">Bu parametreyi, hataları yoksaymak ve dizinin diğer alt varlıklarındaki işlemi sürdürmek için ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-132">Set this parameter to ignore failures and continue proceeing with the operation on other sub-entities of the directory.</span></span> <span data-ttu-id="2a2e2-133">Varsayılan işlem, hatalarla karşılaşmasında hızla sonlandırılır.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-133">Default the operation will terminate quickly on encountering failures.</span></span>

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

### <span data-ttu-id="2a2e2-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a2e2-134">-DefaultProfile</span></span>
<span data-ttu-id="2a2e2-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a2e2-136">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="2a2e2-136">-FileSystem</span></span>
<span data-ttu-id="2a2e2-137">FileSystem adı</span><span class="sxs-lookup"><span data-stu-id="2a2e2-137">FileSystem name</span></span>

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

### <span data-ttu-id="2a2e2-138">-MaxBatchCount</span><span class="sxs-lookup"><span data-stu-id="2a2e2-138">-MaxBatchCount</span></span>
<span data-ttu-id="2a2e2-139">Tek tek erişim denetimi işleminin yürütüleceği en fazla toplu iş sayısı.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-139">Maximum number of batches that single change Access Control operation can execute.</span></span> <span data-ttu-id="2a2e2-140">Veri kümesi boyutu MaxBatchCount çarp BatchSize değerini aşıyorsa, devam belirteci döndürülür.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-140">If data set size exceeds MaxBatchCount multiply BatchSize, continuation token will be return.</span></span>

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

### <span data-ttu-id="2a2e2-141">-Yol</span><span class="sxs-lookup"><span data-stu-id="2a2e2-141">-Path</span></span>
<span data-ttu-id="2a2e2-142">Belirtilen FileSystem 'daki, ACL 'yi özyinelemeli olarak değiştirmesi gereken yol.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-142">The path in the specified FileSystem that to change Acl recursively.</span></span>
<span data-ttu-id="2a2e2-143">Dosya veya dizin olabilir.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-143">Can be a file or directory.</span></span>
<span data-ttu-id="2a2e2-144">' Dizin/file.txt ' veya ' directory1/directory2/' biçiminde.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-144">In the format 'directory/file.txt' or 'directory1/directory2/'.</span></span>
<span data-ttu-id="2a2e2-145">Atla bu parametreyi, ACL 'yi özyinelemeli olarak FileSystem 'ın kök dizininden değiştirmek için ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-145">Skip set this parameter to change Acl recursively from root directory of the Filesystem.</span></span>

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

### <span data-ttu-id="2a2e2-146">-Onay</span><span class="sxs-lookup"><span data-stu-id="2a2e2-146">-Confirm</span></span>
<span data-ttu-id="2a2e2-147">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a2e2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a2e2-148">-WhatIf</span></span>
<span data-ttu-id="2a2e2-149">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a2e2-150">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a2e2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a2e2-151">CommonParameters</span></span>
<span data-ttu-id="2a2e2-152">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a2e2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a2e2-153">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a2e2-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a2e2-154">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a2e2-154">INPUTS</span></span>

### <span data-ttu-id="2a2e2-155">System. String</span><span class="sxs-lookup"><span data-stu-id="2a2e2-155">System.String</span></span>

### <span data-ttu-id="2a2e2-156">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="2a2e2-156">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2a2e2-157">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a2e2-157">OUTPUTS</span></span>

### <span data-ttu-id="2a2e2-158">System. String</span><span class="sxs-lookup"><span data-stu-id="2a2e2-158">System.String</span></span>

## <span data-ttu-id="2a2e2-159">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a2e2-159">NOTES</span></span>

## <span data-ttu-id="2a2e2-160">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a2e2-160">RELATED LINKS</span></span>
