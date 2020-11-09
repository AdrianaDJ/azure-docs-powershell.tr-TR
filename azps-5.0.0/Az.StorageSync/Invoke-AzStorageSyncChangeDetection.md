---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: f76a399d9d2e592bbea10a9e304d8f6875eea227
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94324922"
---
# <span data-ttu-id="98b69-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="98b69-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="98b69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98b69-102">SYNOPSIS</span></span>
<span data-ttu-id="98b69-103">Bu komut, ad alanları değişikliklerinin algılanmasını el ile başlatmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="98b69-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="98b69-104">Tüm paylaşım, alt klasör veya dosya kümesini hedeflenebilir.</span><span class="sxs-lookup"><span data-stu-id="98b69-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="98b69-105">Maksimum 10.000 öğe algılanabilir.</span><span class="sxs-lookup"><span data-stu-id="98b69-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="98b69-106">Değişiklik kapsamı sizin için biliniyorsa, bu komutun yürütülmesini ad alanının bölümleriyle sınırlandırın, böylece algılama özelliğinin hızla ve 10.000 öğesi sınırının içinde tamamlanabilmesi için</span><span class="sxs-lookup"><span data-stu-id="98b69-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="98b69-107">Invoke-AzStorageSyncChangeDetection cmdlet 'i, Azure dosya paylaşımında aşağıdaki değişiklikleri algılamaz:</span><span class="sxs-lookup"><span data-stu-id="98b69-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="98b69-108">Silinen dosyalar.</span><span class="sxs-lookup"><span data-stu-id="98b69-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="98b69-109">Paylaşımdan taşınan dosyalar.</span><span class="sxs-lookup"><span data-stu-id="98b69-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="98b69-110">Aynı adla silinen ve oluşturulan dosyalar.</span><span class="sxs-lookup"><span data-stu-id="98b69-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="98b69-111">[Değişiklik algılama işi](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs->change-detection) çalıştığında bu değişiklikler saptanacaktır.</span><span class="sxs-lookup"><span data-stu-id="98b69-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs->change-detection) runs.</span></span>

## <span data-ttu-id="98b69-112">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98b69-112">SYNTAX</span></span>

### <span data-ttu-id="98b69-113">StringAndDirectoryParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="98b69-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98b69-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="98b69-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98b69-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="98b69-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98b69-116">Resourceıdandpathparameterset</span><span class="sxs-lookup"><span data-stu-id="98b69-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98b69-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="98b69-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98b69-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="98b69-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98b69-119">Tanım</span><span class="sxs-lookup"><span data-stu-id="98b69-119">DESCRIPTION</span></span>
<span data-ttu-id="98b69-120">Azure dosya eşitlemesi belirli aralıklarla, dosya paylaşımının eşitleme içindeki ad alanını, eşitlenenden başka yollarla denetler. Amaç, bu değişiklikleri ve son olarak bağlı sunuculara eşitlemeyi tanımlamaktır.</span><span class="sxs-lookup"><span data-stu-id="98b69-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="98b69-121">Bu komut, ad alanları değişikliklerinin algılanmasını el ile başlatmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="98b69-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="98b69-122">Tüm paylaşım, alt klasör veya dosya kümesini hedeflenebilir.</span><span class="sxs-lookup"><span data-stu-id="98b69-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="98b69-123">Değişiklik kapsamı sizin için biliniyorsa, bu komutun yürütülmesini ad alanının bölümleriyle sınırlandırın, böylece algılama özelliğinin hızla ve 10.000 öğeleri sınırının içinde tamamlanabilmesi için</span><span class="sxs-lookup"><span data-stu-id="98b69-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="98b69-124">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98b69-124">EXAMPLES</span></span>

### <span data-ttu-id="98b69-125">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="98b69-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="98b69-126">Bu örnekte, değiştirme algılaması, bir Azure dosya paylaşımının "Data" ve "Reporting\Templates" dizinlerinde çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="98b69-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="98b69-127">Tüm yollar, Azure dosya paylaşımı ad alanının köküne göredir.</span><span class="sxs-lookup"><span data-stu-id="98b69-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="98b69-128">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="98b69-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="98b69-129">Bu örnekte, değişiklik algılama özelliği, arayan komutun değiştiği bilinen bir dosya kümesi için çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="98b69-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="98b69-130">Amaç, Azure dosya eşitlemesi 'nin algılanması ve bu değişiklikleri eşitmaktır.</span><span class="sxs-lookup"><span data-stu-id="98b69-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="98b69-131">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="98b69-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="98b69-132">Bu örnekte, "örnekler" dizininde algılama algılaması çalıştırılır ve alt dizinlerdeki değişiklikleri yinelemeli olarak algılar.</span><span class="sxs-lookup"><span data-stu-id="98b69-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="98b69-133">Yol 10.000 ' den fazla öğe içeriyorsa cmdlet 'in başarısız olacağını unutmayın.</span><span class="sxs-lookup"><span data-stu-id="98b69-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="98b69-134">Yol 10.000 ' den fazla öğe içeriyorsa, bu komutu ad alanının alt kısımlarında çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="98b69-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="98b69-135">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98b69-135">PARAMETERS</span></span>

### <span data-ttu-id="98b69-136">-Iş</span><span class="sxs-lookup"><span data-stu-id="98b69-136">-AsJob</span></span>
<span data-ttu-id="98b69-137">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="98b69-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98b69-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98b69-138">-DefaultProfile</span></span>
<span data-ttu-id="98b69-139">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98b69-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98b69-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="98b69-140">-DirectoryPath</span></span>
<span data-ttu-id="98b69-141">Değişiklik algılamanın gerçekleştirileceği dizin.</span><span class="sxs-lookup"><span data-stu-id="98b69-141">Directory where change detection will be performed.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b69-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98b69-142">-InputObject</span></span>
<span data-ttu-id="98b69-143">Bu nesne, normalde parametre aracılığıyla iletilir.</span><span class="sxs-lookup"><span data-stu-id="98b69-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: ObjectAndDirectoryParameterSet, ObjectAndPathParameterSet
Aliases: CloudEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98b69-144">-Ad</span><span class="sxs-lookup"><span data-stu-id="98b69-144">-Name</span></span>
<span data-ttu-id="98b69-145">Cloudenvseçpunto adı.</span><span class="sxs-lookup"><span data-stu-id="98b69-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="98b69-146">Ad, portalda görüntülenen kolay adın değil, bir GUID.</span><span class="sxs-lookup"><span data-stu-id="98b69-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="98b69-147">Cloudenvseçpointname 'i almak için Get-AzStorageSyncCloudEndpoint cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="98b69-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b69-148">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="98b69-148">-PassThru</span></span>
<span data-ttu-id="98b69-149">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="98b69-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="98b69-150">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="98b69-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="98b69-151">-Yol</span><span class="sxs-lookup"><span data-stu-id="98b69-151">-Path</span></span>
<span data-ttu-id="98b69-152">Değişiklik algılamanın gerçekleştirileceği yol.</span><span class="sxs-lookup"><span data-stu-id="98b69-152">Path where change detection will be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: StringAndPathParameterSet, ResourceIdAndPathParameterSet, ObjectAndPathParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b69-153">-Yinelemeli</span><span class="sxs-lookup"><span data-stu-id="98b69-153">-Recursive</span></span>
<span data-ttu-id="98b69-154">Dizin değişikliği algılamasının özyinelemeli olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="98b69-154">Indication whether directory change detection is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b69-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98b69-155">-ResourceGroupName</span></span>
<span data-ttu-id="98b69-156">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="98b69-156">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b69-157">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="98b69-157">-ResourceId</span></span>
<span data-ttu-id="98b69-158">Cloudenvseçpoint kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="98b69-158">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdAndDirectoryParameterSet, ResourceIdAndPathParameterSet
Aliases: CloudEndpointId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98b69-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="98b69-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="98b69-160">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="98b69-160">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b69-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="98b69-161">-SyncGroupName</span></span>
<span data-ttu-id="98b69-162">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="98b69-162">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98b69-163">-Onay</span><span class="sxs-lookup"><span data-stu-id="98b69-163">-Confirm</span></span>
<span data-ttu-id="98b69-164">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="98b69-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98b69-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98b69-165">-WhatIf</span></span>
<span data-ttu-id="98b69-166">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="98b69-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98b69-167">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="98b69-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98b69-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98b69-168">CommonParameters</span></span>
<span data-ttu-id="98b69-169">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98b69-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98b69-170">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98b69-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98b69-171">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98b69-171">INPUTS</span></span>

### <span data-ttu-id="98b69-172">System. String</span><span class="sxs-lookup"><span data-stu-id="98b69-172">System.String</span></span>

### <span data-ttu-id="98b69-173">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="98b69-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="98b69-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98b69-174">OUTPUTS</span></span>

### <span data-ttu-id="98b69-175">System. void</span><span class="sxs-lookup"><span data-stu-id="98b69-175">System.Void</span></span>

## <span data-ttu-id="98b69-176">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98b69-176">NOTES</span></span>

## <span data-ttu-id="98b69-177">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98b69-177">RELATED LINKS</span></span>
