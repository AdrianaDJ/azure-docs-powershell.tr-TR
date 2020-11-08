---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 41710c328787f542188c828975402696c36f0854
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267519"
---
# <span data-ttu-id="3d95e-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="3d95e-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="3d95e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d95e-102">SYNOPSIS</span></span>
<span data-ttu-id="3d95e-103">Bu komut, ad alanları değişikliklerinin algılanmasını el ile başlatmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3d95e-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="3d95e-104">Tüm paylaşım, alt klasör veya dosya kümesini hedeflenebilir.</span><span class="sxs-lookup"><span data-stu-id="3d95e-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="3d95e-105">Maksimum 10.000 öğe algılanabilir.</span><span class="sxs-lookup"><span data-stu-id="3d95e-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="3d95e-106">Değişiklik kapsamı sizin için biliniyorsa, bu komutun yürütülmesini ad alanının bölümleriyle sınırlandırın, böylece algılama özelliğinin hızla ve 10.000 öğesi sınırının içinde tamamlanabilmesi için</span><span class="sxs-lookup"><span data-stu-id="3d95e-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="3d95e-107">Invoke-AzStorageSyncChangeDetection cmdlet 'i, Azure dosya paylaşımında silinen dosyaları algılayamaz.</span><span class="sxs-lookup"><span data-stu-id="3d95e-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect files that are deleted in the Azure file share.</span></span> <span data-ttu-id="3d95e-108">Dosyalar Azure dosya paylaşımında silinirse, [değişiklik algılama işi](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) çalıştığında algılanır.</span><span class="sxs-lookup"><span data-stu-id="3d95e-108">If files are deleted in the Azure file share, they will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="3d95e-109">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3d95e-109">SYNTAX</span></span>

### <span data-ttu-id="3d95e-110">StringAndDirectoryParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3d95e-110">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d95e-111">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d95e-111">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d95e-112">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d95e-112">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d95e-113">Resourceıdandpathparameterset</span><span class="sxs-lookup"><span data-stu-id="3d95e-113">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d95e-114">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d95e-114">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d95e-115">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="3d95e-115">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d95e-116">Tanım</span><span class="sxs-lookup"><span data-stu-id="3d95e-116">DESCRIPTION</span></span>
<span data-ttu-id="3d95e-117">Azure dosya eşitlemesi belirli aralıklarla, dosya paylaşımının eşitleme içindeki ad alanını, eşitlenenden başka yollarla denetler. Amaç, bu değişiklikleri ve son olarak bağlı sunuculara eşitlemeyi tanımlamaktır.</span><span class="sxs-lookup"><span data-stu-id="3d95e-117">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="3d95e-118">Bu komut, ad alanları değişikliklerinin algılanmasını el ile başlatmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3d95e-118">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="3d95e-119">Tüm paylaşım, alt klasör veya dosya kümesini hedeflenebilir.</span><span class="sxs-lookup"><span data-stu-id="3d95e-119">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="3d95e-120">Değişiklik kapsamı sizin için biliniyorsa, bu komutun yürütülmesini ad alanının bölümleriyle sınırlandırın, böylece algılamanın hızla ve 10.000 değişiklik sınırının içinde tamamlanabilmesi için</span><span class="sxs-lookup"><span data-stu-id="3d95e-120">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="3d95e-121">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3d95e-121">EXAMPLES</span></span>

### <span data-ttu-id="3d95e-122">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3d95e-122">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="3d95e-123">Bu örnekte, değiştirme algılaması, bir Azure dosya paylaşımının "Data" ve "Reporting\Templates" dizinlerinde çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="3d95e-123">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="3d95e-124">Tüm yollar, Azure dosya paylaşımı ad alanının köküne göredir.</span><span class="sxs-lookup"><span data-stu-id="3d95e-124">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="3d95e-125">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="3d95e-125">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="3d95e-126">Bu örnekte, değişiklik algılama özelliği, arayan komutun değiştiği bilinen bir dosya kümesi için çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="3d95e-126">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="3d95e-127">Amaç, Azure dosya eşitlemesi 'nin algılanması ve bu değişiklikleri eşitmaktır.</span><span class="sxs-lookup"><span data-stu-id="3d95e-127">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="3d95e-128">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="3d95e-128">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="3d95e-129">Bu örnekte, "örnekler" dizininde algılama algılaması çalıştırılır ve alt dizinlerdeki değişiklikleri yinelemeli olarak algılar.</span><span class="sxs-lookup"><span data-stu-id="3d95e-129">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="3d95e-130">Bu komutun, otomatik olarak durdurulmadan önce en çok 10.000 değişikliği saptayabileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="3d95e-130">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="3d95e-131">10.000 'den fazla değişiklik olduğundan şüpheleniyorsanız, bu komutu ad alanının alt kısımlarında çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="3d95e-131">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="3d95e-132">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3d95e-132">PARAMETERS</span></span>

### <span data-ttu-id="3d95e-133">-Iş</span><span class="sxs-lookup"><span data-stu-id="3d95e-133">-AsJob</span></span>
<span data-ttu-id="3d95e-134">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3d95e-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d95e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d95e-135">-DefaultProfile</span></span>
<span data-ttu-id="3d95e-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3d95e-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d95e-137">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="3d95e-137">-DirectoryPath</span></span>
<span data-ttu-id="3d95e-138">Değişiklik algılamanın gerçekleştirileceği dizin.</span><span class="sxs-lookup"><span data-stu-id="3d95e-138">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="3d95e-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3d95e-139">-InputObject</span></span>
<span data-ttu-id="3d95e-140">Bu nesne, normalde parametre aracılığıyla iletilir.</span><span class="sxs-lookup"><span data-stu-id="3d95e-140">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="3d95e-141">-Ad</span><span class="sxs-lookup"><span data-stu-id="3d95e-141">-Name</span></span>
<span data-ttu-id="3d95e-142">Cloudenvseçpunto adı.</span><span class="sxs-lookup"><span data-stu-id="3d95e-142">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="3d95e-143">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3d95e-143">-PassThru</span></span>
<span data-ttu-id="3d95e-144">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="3d95e-144">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="3d95e-145">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="3d95e-145">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="3d95e-146">-Yol</span><span class="sxs-lookup"><span data-stu-id="3d95e-146">-Path</span></span>
<span data-ttu-id="3d95e-147">Değişiklik algılamanın gerçekleştirileceği yol.</span><span class="sxs-lookup"><span data-stu-id="3d95e-147">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="3d95e-148">-Yinelemeli</span><span class="sxs-lookup"><span data-stu-id="3d95e-148">-Recursive</span></span>
<span data-ttu-id="3d95e-149">Dizin değişikliği algılamasının özyinelemeli olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3d95e-149">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="3d95e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d95e-150">-ResourceGroupName</span></span>
<span data-ttu-id="3d95e-151">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3d95e-151">Resource Group Name.</span></span>

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

### <span data-ttu-id="3d95e-152">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3d95e-152">-ResourceId</span></span>
<span data-ttu-id="3d95e-153">Cloudenvseçpoint kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3d95e-153">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="3d95e-154">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="3d95e-154">-StorageSyncServiceName</span></span>
<span data-ttu-id="3d95e-155">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="3d95e-155">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="3d95e-156">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3d95e-156">-SyncGroupName</span></span>
<span data-ttu-id="3d95e-157">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="3d95e-157">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="3d95e-158">-Onay</span><span class="sxs-lookup"><span data-stu-id="3d95e-158">-Confirm</span></span>
<span data-ttu-id="3d95e-159">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3d95e-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d95e-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d95e-160">-WhatIf</span></span>
<span data-ttu-id="3d95e-161">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3d95e-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d95e-162">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3d95e-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d95e-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d95e-163">CommonParameters</span></span>
<span data-ttu-id="3d95e-164">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3d95e-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d95e-165">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d95e-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d95e-166">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3d95e-166">INPUTS</span></span>

### <span data-ttu-id="3d95e-167">System. String</span><span class="sxs-lookup"><span data-stu-id="3d95e-167">System.String</span></span>

### <span data-ttu-id="3d95e-168">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3d95e-168">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="3d95e-169">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3d95e-169">OUTPUTS</span></span>

### <span data-ttu-id="3d95e-170">System. void</span><span class="sxs-lookup"><span data-stu-id="3d95e-170">System.Void</span></span>

## <span data-ttu-id="3d95e-171">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3d95e-171">NOTES</span></span>

## <span data-ttu-id="3d95e-172">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3d95e-172">RELATED LINKS</span></span>
