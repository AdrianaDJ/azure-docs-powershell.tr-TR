---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097928"
---
# <span data-ttu-id="183e3-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="183e3-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="183e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="183e3-102">SYNOPSIS</span></span>
<span data-ttu-id="183e3-103">Bu komut, belirli bir depolama eşitleme hizmeti içindeki tüm eşitleme gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="183e3-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="183e3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="183e3-104">SYNTAX</span></span>

### <span data-ttu-id="183e3-105">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="183e3-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="183e3-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="183e3-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="183e3-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="183e3-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="183e3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="183e3-108">DESCRIPTION</span></span>
<span data-ttu-id="183e3-109">Bu komut, belirli bir depolama eşitleme hizmeti içindeki tüm eşitleme gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="183e3-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="183e3-110">Ayrıca, her bir eşitleme grubunun özniteliklerini de listelemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="183e3-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="183e3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="183e3-111">EXAMPLES</span></span>

### <span data-ttu-id="183e3-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="183e3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="183e3-113">Bu komut, belirtilen depolama eşitleme hizmeti 'nde bulunan tüm eşitleme gruplarını alır.</span><span class="sxs-lookup"><span data-stu-id="183e3-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="183e3-114">Belirli bir ad döndürmek için ad belirtin.</span><span class="sxs-lookup"><span data-stu-id="183e3-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="183e3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="183e3-115">PARAMETERS</span></span>

### <span data-ttu-id="183e3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="183e3-116">-DefaultProfile</span></span>
<span data-ttu-id="183e3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="183e3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="183e3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="183e3-118">-Name</span></span>
<span data-ttu-id="183e3-119">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="183e3-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="183e3-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="183e3-120">-ParentObject</span></span>
<span data-ttu-id="183e3-121">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="183e3-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="183e3-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="183e3-122">-ParentResourceId</span></span>
<span data-ttu-id="183e3-123">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="183e3-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="183e3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="183e3-124">-ResourceGroupName</span></span>
<span data-ttu-id="183e3-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="183e3-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="183e3-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="183e3-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="183e3-127">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="183e3-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="183e3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="183e3-128">CommonParameters</span></span>
<span data-ttu-id="183e3-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="183e3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="183e3-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="183e3-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="183e3-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="183e3-131">INPUTS</span></span>

### <span data-ttu-id="183e3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="183e3-132">System.String</span></span>

### <span data-ttu-id="183e3-133">Microsoft. Azure. Commands. Storagesehd. modeller. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="183e3-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="183e3-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="183e3-134">OUTPUTS</span></span>

### <span data-ttu-id="183e3-135">Microsoft. Azure. Commands. Storageseşitleme. model. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="183e3-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="183e3-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="183e3-136">NOTES</span></span>

## <span data-ttu-id="183e3-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="183e3-137">RELATED LINKS</span></span>
