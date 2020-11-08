---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: fb199887edcc3a9895095101870856d15f86ac08
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098604"
---
# <span data-ttu-id="7adbe-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7adbe-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="7adbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7adbe-102">SYNOPSIS</span></span>
<span data-ttu-id="7adbe-103">Bu komut, belirtilen bir depolama eşitleme hizmeti içinde yeni bir eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7adbe-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="7adbe-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7adbe-104">SYNTAX</span></span>

### <span data-ttu-id="7adbe-105">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7adbe-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7adbe-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7adbe-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7adbe-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7adbe-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7adbe-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7adbe-108">DESCRIPTION</span></span>
<span data-ttu-id="7adbe-109">Bu komut, belirtilen bir depolama eşitleme hizmeti içinde yeni bir eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7adbe-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="7adbe-110">Bir eşitleme grubu, uç noktalar olarak adlandırılan ve uç noktaların herhangi birinde depolanan dosyaları eşitleyen, nokta topolojisini açıklamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7adbe-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="7adbe-111">Eşitleme grubu, Azure dosya paylaşımlarına başvuran bulut uç noktaları içerir ve aynı zamanda kaydedilmiş sunucudaki belirli bir yerel yola başvuruda bulunan sunucu uç noktaları içerir.</span><span class="sxs-lookup"><span data-stu-id="7adbe-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="7adbe-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7adbe-112">EXAMPLES</span></span>

### <span data-ttu-id="7adbe-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7adbe-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="7adbe-114">Bu komut, belirtilen bir depolama eşitleme hizmeti içinde yeni bir eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7adbe-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="7adbe-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7adbe-115">PARAMETERS</span></span>

### <span data-ttu-id="7adbe-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7adbe-116">-DefaultProfile</span></span>
<span data-ttu-id="7adbe-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7adbe-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7adbe-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="7adbe-118">-Name</span></span>
<span data-ttu-id="7adbe-119">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="7adbe-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adbe-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7adbe-120">-ParentObject</span></span>
<span data-ttu-id="7adbe-121">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7adbe-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7adbe-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="7adbe-122">-ParentResourceId</span></span>
<span data-ttu-id="7adbe-123">StorageSyncService üst kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7adbe-123">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adbe-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7adbe-124">-ResourceGroupName</span></span>
<span data-ttu-id="7adbe-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7adbe-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adbe-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="7adbe-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="7adbe-127">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="7adbe-127">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7adbe-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="7adbe-128">-Confirm</span></span>
<span data-ttu-id="7adbe-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7adbe-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7adbe-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7adbe-130">-WhatIf</span></span>
<span data-ttu-id="7adbe-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7adbe-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7adbe-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7adbe-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7adbe-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7adbe-133">CommonParameters</span></span>
<span data-ttu-id="7adbe-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7adbe-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7adbe-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7adbe-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7adbe-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7adbe-136">INPUTS</span></span>

### <span data-ttu-id="7adbe-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7adbe-137">System.String</span></span>

### <span data-ttu-id="7adbe-138">Microsoft. Azure. Commands. Storagesehd. modeller. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="7adbe-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="7adbe-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7adbe-139">OUTPUTS</span></span>

### <span data-ttu-id="7adbe-140">Microsoft. Azure. Commands. Storageseşitleme. model. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="7adbe-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="7adbe-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7adbe-141">NOTES</span></span>

## <span data-ttu-id="7adbe-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7adbe-142">RELATED LINKS</span></span>
