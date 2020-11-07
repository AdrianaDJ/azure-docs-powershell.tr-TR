---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: 2913cbece59687516aa7e2aa83e3cea035218fd8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934313"
---
# <span data-ttu-id="a7fcb-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a7fcb-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="a7fcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="a7fcb-103">Bu komut, belirtilen bir depolama eşitleme hizmeti içinde yeni bir eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="a7fcb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a7fcb-104">SYNTAX</span></span>

### <span data-ttu-id="a7fcb-105">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a7fcb-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7fcb-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7fcb-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7fcb-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7fcb-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7fcb-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a7fcb-108">DESCRIPTION</span></span>
<span data-ttu-id="a7fcb-109">Bu komut, belirtilen bir depolama eşitleme hizmeti içinde yeni bir eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="a7fcb-110">Bir eşitleme grubu, uç noktalar olarak adlandırılan ve uç noktaların herhangi birinde depolanan dosyaları eşitleyen, nokta topolojisini açıklamak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="a7fcb-111">Eşitleme grubu, Azure dosya paylaşımlarına başvuran bulut uç noktaları içerir ve aynı zamanda kaydedilmiş sunucudaki belirli bir yerel yola başvuruda bulunan sunucu uç noktaları içerir.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="a7fcb-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a7fcb-112">EXAMPLES</span></span>

### <span data-ttu-id="a7fcb-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a7fcb-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="a7fcb-114">Bu komut, belirtilen bir depolama eşitleme hizmeti içinde yeni bir eşitleme grubu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="a7fcb-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a7fcb-115">PARAMETERS</span></span>

### <span data-ttu-id="a7fcb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7fcb-116">-DefaultProfile</span></span>
<span data-ttu-id="a7fcb-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7fcb-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a7fcb-118">-Name</span></span>
<span data-ttu-id="a7fcb-119">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-119">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="a7fcb-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a7fcb-120">-ParentObject</span></span>
<span data-ttu-id="a7fcb-121">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="a7fcb-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="a7fcb-122">-ParentResourceId</span></span>
<span data-ttu-id="a7fcb-123">StorageSyncService üst kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a7fcb-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="a7fcb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7fcb-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7fcb-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a7fcb-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="a7fcb-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="a7fcb-127">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="a7fcb-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="a7fcb-128">-Confirm</span></span>
<span data-ttu-id="a7fcb-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7fcb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7fcb-130">-WhatIf</span></span>
<span data-ttu-id="a7fcb-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7fcb-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7fcb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7fcb-133">CommonParameters</span></span>
<span data-ttu-id="a7fcb-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a7fcb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7fcb-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7fcb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7fcb-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a7fcb-136">INPUTS</span></span>

### <span data-ttu-id="a7fcb-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a7fcb-137">System.String</span></span>

### <span data-ttu-id="a7fcb-138">Microsoft. Azure. Commands. Storagesehd. modeller. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="a7fcb-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="a7fcb-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a7fcb-139">OUTPUTS</span></span>

### <span data-ttu-id="a7fcb-140">Microsoft. Azure. Commands. Storageseşitleme. model. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a7fcb-140">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="a7fcb-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a7fcb-141">NOTES</span></span>

## <span data-ttu-id="a7fcb-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a7fcb-142">RELATED LINKS</span></span>
