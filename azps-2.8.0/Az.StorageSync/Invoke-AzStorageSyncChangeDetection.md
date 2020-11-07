---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: c266b6623463165f14e01e55f0fec4d2d59a581f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934299"
---
# <span data-ttu-id="9f8ee-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="9f8ee-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="9f8ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f8ee-102">SYNOPSIS</span></span>
<span data-ttu-id="9f8ee-103">Bu komut, ad alanları değişikliklerinin algılanmasını el ile başlatmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="9f8ee-104">Tüm paylaşım, alt klasör veya dosya kümesini hedeflenebilir.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="9f8ee-105">Maksimum 10.000 değişiklik algılanabilir.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-105">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="9f8ee-106">Değişiklik kapsamı sizin için biliniyorsa, bu komutun yürütülmesini ad alanının bölümleriyle sınırlandırın, böylece algılamanın hızla ve 10.000 değişiklik sınırının içinde tamamlanabilmesi için</span><span class="sxs-lookup"><span data-stu-id="9f8ee-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="9f8ee-107">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f8ee-107">SYNTAX</span></span>

### <span data-ttu-id="9f8ee-108">StringAndDirectoryParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9f8ee-108">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f8ee-109">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f8ee-109">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f8ee-110">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f8ee-110">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f8ee-111">Resourceıdandpathparameterset</span><span class="sxs-lookup"><span data-stu-id="9f8ee-111">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f8ee-112">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f8ee-112">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f8ee-113">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f8ee-113">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f8ee-114">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f8ee-114">DESCRIPTION</span></span>
<span data-ttu-id="9f8ee-115">Azure dosya eşitlemesi belirli aralıklarla, dosya paylaşımının eşitleme içindeki ad alanını, eşitlenenden başka yollarla denetler. Amaç, bu değişiklikleri ve son olarak bağlı sunuculara eşitlemeyi tanımlamaktır.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-115">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="9f8ee-116">Bu komut, ad alanları değişikliklerinin algılanmasını el ile başlatmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="9f8ee-117">Tüm paylaşım, alt klasör veya dosya kümesini hedeflenebilir.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="9f8ee-118">Değişiklik kapsamı sizin için biliniyorsa, bu komutun yürütülmesini ad alanının bölümleriyle sınırlandırın, böylece algılamanın hızla ve 10.000 değişiklik sınırının içinde tamamlanabilmesi için</span><span class="sxs-lookup"><span data-stu-id="9f8ee-118">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="9f8ee-119">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f8ee-119">EXAMPLES</span></span>

### <span data-ttu-id="9f8ee-120">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9f8ee-120">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="9f8ee-121">Bu örnekte, değiştirme algılaması, bir Azure dosya paylaşımının "Data" ve "Reporting\Templates" dizinlerinde çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-121">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="9f8ee-122">Tüm yollar, Azure dosya paylaşımı ad alanının köküne göredir.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-122">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="9f8ee-123">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="9f8ee-123">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="9f8ee-124">Bu örnekte, değişiklik algılama özelliği, arayan komutun değiştiği bilinen bir dosya kümesi için çalıştırılır.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-124">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="9f8ee-125">Amaç, Azure dosya eşitlemesi 'nin algılanması ve bu değişiklikleri eşitmaktır.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-125">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="9f8ee-126">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="9f8ee-126">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="9f8ee-127">Bu örnekte, "örnekler" dizininde algılama algılaması çalıştırılır ve alt dizinlerdeki değişiklikleri yinelemeli olarak algılar.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-127">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="9f8ee-128">Bu komutun, otomatik olarak durdurulmadan önce en çok 10.000 değişikliği saptayabileceğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-128">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="9f8ee-129">10.000 'den fazla değişiklik olduğundan şüpheleniyorsanız, bu komutu ad alanının alt kısımlarında çalıştırabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-129">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="9f8ee-130">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f8ee-130">PARAMETERS</span></span>

### <span data-ttu-id="9f8ee-131">-Iş</span><span class="sxs-lookup"><span data-stu-id="9f8ee-131">-AsJob</span></span>
<span data-ttu-id="9f8ee-132">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9f8ee-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f8ee-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f8ee-133">-DefaultProfile</span></span>
<span data-ttu-id="9f8ee-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f8ee-135">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="9f8ee-135">-DirectoryPath</span></span>
<span data-ttu-id="9f8ee-136">Değişiklik algılamanın gerçekleştirileceği dizin.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-136">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="9f8ee-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f8ee-137">-InputObject</span></span>
<span data-ttu-id="9f8ee-138">Bu nesne, normalde parametre aracılığıyla iletilir.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-138">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="9f8ee-139">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f8ee-139">-Name</span></span>
<span data-ttu-id="9f8ee-140">Cloudenvseçpunto adı.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-140">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="9f8ee-141">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9f8ee-141">-PassThru</span></span>
<span data-ttu-id="9f8ee-142">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-142">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="9f8ee-143">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-143">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="9f8ee-144">-Yol</span><span class="sxs-lookup"><span data-stu-id="9f8ee-144">-Path</span></span>
<span data-ttu-id="9f8ee-145">Değişiklik algılamanın gerçekleştirileceği yol.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-145">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="9f8ee-146">-Yinelemeli</span><span class="sxs-lookup"><span data-stu-id="9f8ee-146">-Recursive</span></span>
<span data-ttu-id="9f8ee-147">Dizin değişikliği algılamasının özyinelemeli olup olmadığını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-147">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="9f8ee-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f8ee-148">-ResourceGroupName</span></span>
<span data-ttu-id="9f8ee-149">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="9f8ee-150">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9f8ee-150">-ResourceId</span></span>
<span data-ttu-id="9f8ee-151">Cloudenvseçpoint kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9f8ee-151">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="9f8ee-152">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9f8ee-152">-StorageSyncServiceName</span></span>
<span data-ttu-id="9f8ee-153">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-153">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="9f8ee-154">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9f8ee-154">-SyncGroupName</span></span>
<span data-ttu-id="9f8ee-155">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-155">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="9f8ee-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="9f8ee-156">-Confirm</span></span>
<span data-ttu-id="9f8ee-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f8ee-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f8ee-158">-WhatIf</span></span>
<span data-ttu-id="9f8ee-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f8ee-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f8ee-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f8ee-161">CommonParameters</span></span>
<span data-ttu-id="9f8ee-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f8ee-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f8ee-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f8ee-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f8ee-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f8ee-164">INPUTS</span></span>

### <span data-ttu-id="9f8ee-165">System. String</span><span class="sxs-lookup"><span data-stu-id="9f8ee-165">System.String</span></span>

### <span data-ttu-id="9f8ee-166">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9f8ee-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="9f8ee-167">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f8ee-167">OUTPUTS</span></span>

### <span data-ttu-id="9f8ee-168">System. void</span><span class="sxs-lookup"><span data-stu-id="9f8ee-168">System.Void</span></span>

## <span data-ttu-id="9f8ee-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f8ee-169">NOTES</span></span>

## <span data-ttu-id="9f8ee-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f8ee-170">RELATED LINKS</span></span>
