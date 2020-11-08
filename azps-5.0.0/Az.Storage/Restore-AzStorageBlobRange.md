---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/restore-azstorageblobrange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Restore-AzStorageBlobRange.md
ms.openlocfilehash: ee8a8bd6a12d3f4aa1dc1624d0dc5c11de972b11
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94275787"
---
# <span data-ttu-id="c8068-101">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="c8068-101">Restore-AzStorageBlobRange</span></span>

## <span data-ttu-id="c8068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8068-102">SYNOPSIS</span></span>
<span data-ttu-id="c8068-103">Belirli blob aralıkları için depolama hesabını geri yükler.</span><span class="sxs-lookup"><span data-stu-id="c8068-103">Restores a Storage account for specific blob ranges.</span></span>

## <span data-ttu-id="c8068-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8068-104">SYNTAX</span></span>

### <span data-ttu-id="c8068-105">AccountName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c8068-105">AccountName (Default)</span></span>
```
Restore-AzStorageBlobRange [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -TimeToRestore <DateTime> [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8068-106">Accountresourceıd</span><span class="sxs-lookup"><span data-stu-id="c8068-106">AccountResourceId</span></span>
```
Restore-AzStorageBlobRange [-ResourceId] <String> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8068-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c8068-107">AccountObject</span></span>
```
Restore-AzStorageBlobRange -StorageAccount <PSStorageAccount> -TimeToRestore <DateTime>
 [-BlobRestoreRange <PSBlobRestoreRange[]>] [-WaitForComplete] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8068-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8068-108">DESCRIPTION</span></span>
<span data-ttu-id="c8068-109">**Restore-AzStorageBlobRange** cmdlet 'i, belirli blob aralıkları için depolama hesabındaki blob 'ları geri yükler.</span><span class="sxs-lookup"><span data-stu-id="c8068-109">The **Restore-AzStorageBlobRange** cmdlet restores blobs in a Storage account for specific blob ranges.</span></span>
<span data-ttu-id="c8068-110">Başlangıç aralığı dahildir ve son Aralık blob geri yükleme 'de dışarıda bırakılır.</span><span class="sxs-lookup"><span data-stu-id="c8068-110">The start range is included, and the end range is excluded in blob restore.</span></span>

## <span data-ttu-id="c8068-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8068-111">EXAMPLES</span></span>

### <span data-ttu-id="c8068-112">Örnek 1: belirli blob aralıkları içeren bir depolama hesabında blob 'ları geri yükleme</span><span class="sxs-lookup"><span data-stu-id="c8068-112">Example 1: Start restores blobs in a Storage account with specific blob ranges</span></span>
```powershell
PS C:\> $range1 = New-AzStorageBlobRangeToRestore -StartRange container1/blob1 -EndRange container2/blob2
PS C:\> $range2 = New-AzStorageBlobRangeToRestore -StartRange container3/blob3 -EndRange container4/blob4
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddDays(-1) -BlobRestoreRange $range1,$range2

Status     RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------     ---------                            ------------- ------------------------     ---------------------                     
InProgress 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]

PS C:\> (Get-AzStorageAccount -ResourceGroupName $rgname -StorageAccountName $accountName -IncludeBlobRestoreStatus).BlobRestoreStatus 

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges                     
------   ---------                            ------------- ------------------------     ---------------------                     
Complete 6ca55a8b-fca0-461a-8e4c-13927a9707e6               2020-02-10T13:58:44.6841810Z ["container1/blob1" -> "container2/blob2",...]
```

<span data-ttu-id="c8068-113">Bu komut önce 2 blob aralığı oluşturur, ardından 1 günden fazla önce 2 blob aralığı içeren bir depolama hesabında blob 'ları geri yükler 'i başlatır.</span><span class="sxs-lookup"><span data-stu-id="c8068-113">This command first creates 2 blob ranges, then start restores blobs in a Storage account with the 2 blob ranges from 1 day ago.</span></span> <span data-ttu-id="c8068-114">Kullanıcı, daha sonra geri yükleme durumunu izlemek için Get-AzStorageAccount kullanabilir.</span><span class="sxs-lookup"><span data-stu-id="c8068-114">User can use Get-AzStorageAccount to trace the restore status later.</span></span>

### <span data-ttu-id="c8068-115">Örnek 2: Arka ucun depolama hesabındaki tüm blob 'ları geri yükler</span><span class="sxs-lookup"><span data-stu-id="c8068-115">Example 2: Restores all blobs in a Storage account in the backend</span></span>
```powershell
PS C:\> $job = Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -TimeToRestore (Get-Date).AddMinutes(-30) -WaitForComplete -asjob

PS C:\> $job | Wait-Job

PS C:\> $job.Output

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges
------   ---------                            ------------- ------------------------     ---------------------
Complete 0387953a-bbe6-4602-818d-e661581ee44b               2020-08-28T07:11:33.9843100Z ["" -> ""]
```

<span data-ttu-id="c8068-116">Bu komut, bir depolama hesabındaki tüm blob 'ları 30 dakikadan önce geri yükler ve geri yüklemenin tamamlanmasını bekler.</span><span class="sxs-lookup"><span data-stu-id="c8068-116">This command restores all blobs in a Storage account from 30 minutes ago, and wait for the restore complete.</span></span> <span data-ttu-id="c8068-117">Geri yükleme blob 'ları uzun zaman alabilir, en uç-Iş parametresi ile bu işlemi tamamlayın ve ardından işin tamamlanmasını bekleyin ve sonucu gösterin.</span><span class="sxs-lookup"><span data-stu-id="c8068-117">Since restore blobs might take a long time, run it in the backend with -Asjob parameter, and then wait for the job complete and show the result.</span></span>

### <span data-ttu-id="c8068-118">Örnek 3: blob 'ları doğrudan giriş blob aralıklarına göre geri yükler ve tamamlanması için bekleyin</span><span class="sxs-lookup"><span data-stu-id="c8068-118">Example 3: Restores blobs by input blob ranges directly, and wait for complete</span></span>
```powershell
PS C:\> Restore-AzStorageBlobRange -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount" -WaitForComplete `
    -TimeToRestore (Get-Date).AddSeconds(-1) `
    -BlobRestoreRange @{StartRange="aaa/abc";EndRange="bbb/abc"},@{StartRange="bbb/acc";EndRange=""}
WARNING: Restore blob rang with Id 'd66d1d02-6e48-47ef-b516-0155dd8319c6' started. Restore blob ranges time to complete is dependent on the size of the restore.

Status   RestoreId                            FailureReason Parameters.TimeToRestore     Parameters.BlobRanges   
------   ---------                            ------------- ------------------------     ---------------------   
Complete d66d1d02-6e48-47ef-b516-0155dd8319c6               2020-02-10T14:17:46.8189116Z ["aaa/abc" -> "bbb/abc",...]
```

<span data-ttu-id="c8068-119">Bu komut, depolama hesabındaki blob 'ları 1 günden önce giriş 2 blob aralıklarına doğrudan Restore-AzStorageBlobRange cmdlet 'ine geri yükler.</span><span class="sxs-lookup"><span data-stu-id="c8068-119">This command restores blobs in a Storage account from 1 day ago, by input 2 blob ranges directly to the Restore-AzStorageBlobRange cmdlet.</span></span> <span data-ttu-id="c8068-120">Bu komut geri yüklemenin tamamlanmasını bekler.</span><span class="sxs-lookup"><span data-stu-id="c8068-120">This command will wait for the restore complete.</span></span>

## <span data-ttu-id="c8068-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8068-121">PARAMETERS</span></span>

### <span data-ttu-id="c8068-122">-Iş</span><span class="sxs-lookup"><span data-stu-id="c8068-122">-AsJob</span></span>
<span data-ttu-id="c8068-123">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c8068-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8068-124">-BlobRestoreRange</span><span class="sxs-lookup"><span data-stu-id="c8068-124">-BlobRestoreRange</span></span>
<span data-ttu-id="c8068-125">Geri yüklenecek blob aralığı.</span><span class="sxs-lookup"><span data-stu-id="c8068-125">The blob range to Restore.</span></span>
<span data-ttu-id="c8068-126">Bu parametreyi belirtistemezseniz tüm blob 'ları geri yükler.</span><span class="sxs-lookup"><span data-stu-id="c8068-126">If not specify this parameter, will restore all blobs.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreRange[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8068-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8068-127">-DefaultProfile</span></span>
<span data-ttu-id="c8068-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8068-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8068-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8068-129">-ResourceGroupName</span></span>
<span data-ttu-id="c8068-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c8068-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="c8068-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c8068-131">-ResourceId</span></span>
<span data-ttu-id="c8068-132">Depolama hesabı kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c8068-132">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8068-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8068-133">-StorageAccount</span></span>
<span data-ttu-id="c8068-134">Depolama hesabı nesnesi</span><span class="sxs-lookup"><span data-stu-id="c8068-134">Storage account object</span></span>

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

### <span data-ttu-id="c8068-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c8068-135">-StorageAccountName</span></span>
<span data-ttu-id="c8068-136">Depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="c8068-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="c8068-137">-TimeToRestore</span><span class="sxs-lookup"><span data-stu-id="c8068-137">-TimeToRestore</span></span>
<span data-ttu-id="c8068-138">Blob 'U geri yükleme zamanı.</span><span class="sxs-lookup"><span data-stu-id="c8068-138">The Time to Restore Blob.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8068-139">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="c8068-139">-WaitForComplete</span></span>
<span data-ttu-id="c8068-140">Geri yükleme görevinin tamamlanmasını bekle</span><span class="sxs-lookup"><span data-stu-id="c8068-140">Wait for Restore task complete</span></span>

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

### <span data-ttu-id="c8068-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="c8068-141">-Confirm</span></span>
<span data-ttu-id="c8068-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c8068-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8068-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8068-143">-WhatIf</span></span>
<span data-ttu-id="c8068-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c8068-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8068-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c8068-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8068-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8068-146">CommonParameters</span></span>
<span data-ttu-id="c8068-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8068-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8068-148">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8068-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8068-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8068-149">INPUTS</span></span>

### <span data-ttu-id="c8068-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c8068-150">System.String</span></span>

### <span data-ttu-id="c8068-151">Microsoft. Azure. Commands. Management. Storage. model. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c8068-151">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="c8068-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8068-152">OUTPUTS</span></span>

### <span data-ttu-id="c8068-153">Microsoft. Azure. Commands. Management. Storage. model. PSBlobRestoreStatus</span><span class="sxs-lookup"><span data-stu-id="c8068-153">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobRestoreStatus</span></span>

## <span data-ttu-id="c8068-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8068-154">NOTES</span></span>

## <span data-ttu-id="c8068-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8068-155">RELATED LINKS</span></span>
