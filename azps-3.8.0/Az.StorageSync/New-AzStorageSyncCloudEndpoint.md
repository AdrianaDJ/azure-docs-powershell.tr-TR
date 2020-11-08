---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098607"
---
# <span data-ttu-id="7ab73-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="7ab73-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="7ab73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ab73-102">SYNOPSIS</span></span>
<span data-ttu-id="7ab73-103">Bu komut, eşitleme grubunda bir Azure dosya eşitlemesi bulut uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ab73-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="7ab73-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ab73-104">SYNTAX</span></span>

### <span data-ttu-id="7ab73-105">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7ab73-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ab73-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ab73-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ab73-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ab73-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ab73-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ab73-108">DESCRIPTION</span></span>
<span data-ttu-id="7ab73-109">Bu komut bir Azure dosya eşitlemesi bulut uç noktası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ab73-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="7ab73-110">Bulut uç noktası, var olan bir Azure dosya paylaşımına başvurudur.</span><span class="sxs-lookup"><span data-stu-id="7ab73-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="7ab73-111">Dosya paylaşımını temsil eder ve eşitleme grubunun tüm dosyalar bölümünü eşitlemeye katılımınızı tanımlar; bulut uç noktası oluşturulmuştur.</span><span class="sxs-lookup"><span data-stu-id="7ab73-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="7ab73-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ab73-112">EXAMPLES</span></span>

### <span data-ttu-id="7ab73-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7ab73-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="7ab73-114">Bulut uç noktası, eşitleme grubunun integral bir üyesidir; bu, "mySyncGroupName" adlı mevcut bir eşitleme grubunun içinde bir örnek oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ab73-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="7ab73-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ab73-115">PARAMETERS</span></span>

### <span data-ttu-id="7ab73-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="7ab73-116">-AsJob</span></span>
<span data-ttu-id="7ab73-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="7ab73-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ab73-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="7ab73-118">-AzureFileShareName</span></span>
<span data-ttu-id="7ab73-119">Depolama hesabı paylaşımı adı (Azure dosya paylaşımı adı)</span><span class="sxs-lookup"><span data-stu-id="7ab73-119">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab73-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ab73-120">-DefaultProfile</span></span>
<span data-ttu-id="7ab73-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ab73-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ab73-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="7ab73-122">-Name</span></span>
<span data-ttu-id="7ab73-123">Bulut uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="7ab73-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="7ab73-124">Azure portalı aracılığıyla oluşturulduğunda, ad, başvurduğu Azure dosyasının adına ayarlanır.</span><span class="sxs-lookup"><span data-stu-id="7ab73-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab73-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7ab73-125">-ParentObject</span></span>
<span data-ttu-id="7ab73-126">Normalde parametre aracılığıyla geçirilen SyncGroup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7ab73-126">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab73-127">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="7ab73-127">-ParentResourceId</span></span>
<span data-ttu-id="7ab73-128">SyncGroup üst kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7ab73-128">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ab73-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab73-129">-ResourceGroupName</span></span>
<span data-ttu-id="7ab73-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7ab73-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab73-131">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="7ab73-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="7ab73-132">Depolama hesabı kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7ab73-132">Storage Account Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab73-133">-Storageaccounttenantıd</span><span class="sxs-lookup"><span data-stu-id="7ab73-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="7ab73-134">Depolama hesabı Kiracı kimliği (Şirket dizin kimliği)</span><span class="sxs-lookup"><span data-stu-id="7ab73-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="7ab73-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="7ab73-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="7ab73-136">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="7ab73-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab73-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="7ab73-137">-SyncGroupName</span></span>
<span data-ttu-id="7ab73-138">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="7ab73-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ab73-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="7ab73-139">-Confirm</span></span>
<span data-ttu-id="7ab73-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7ab73-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ab73-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ab73-141">-WhatIf</span></span>
<span data-ttu-id="7ab73-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7ab73-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ab73-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7ab73-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ab73-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ab73-144">CommonParameters</span></span>
<span data-ttu-id="7ab73-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ab73-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ab73-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ab73-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ab73-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ab73-147">INPUTS</span></span>

### <span data-ttu-id="7ab73-148">Microsoft. Azure. Commands. Storageseşitleme. model. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7ab73-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="7ab73-149">System. String</span><span class="sxs-lookup"><span data-stu-id="7ab73-149">System.String</span></span>

## <span data-ttu-id="7ab73-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ab73-150">OUTPUTS</span></span>

### <span data-ttu-id="7ab73-151">Microsoft. Azure. Commands. Storagesehd. modeller. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="7ab73-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="7ab73-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ab73-152">NOTES</span></span>

## <span data-ttu-id="7ab73-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ab73-153">RELATED LINKS</span></span>
