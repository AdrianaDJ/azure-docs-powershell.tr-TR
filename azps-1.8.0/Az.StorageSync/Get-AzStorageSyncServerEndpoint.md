---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b71da416d7609f05d4716090dc8f09bf0ec0b084
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758500"
---
# <span data-ttu-id="f905d-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f905d-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="f905d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f905d-102">SYNOPSIS</span></span>
<span data-ttu-id="f905d-103">Bu komut, belirli bir eşitleme grubundaki tüm sunucu uç noktalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="f905d-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="f905d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f905d-104">SYNTAX</span></span>

### <span data-ttu-id="f905d-105">ObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f905d-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f905d-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f905d-106">StringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f905d-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f905d-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f905d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f905d-108">DESCRIPTION</span></span>
<span data-ttu-id="f905d-109">Bu komut, belirli bir eşitleme grubundaki tüm sunucu uç noktalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="f905d-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="f905d-110">Her sunucu uç noktasının özniteliklerini de listelemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="f905d-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="f905d-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f905d-111">EXAMPLES</span></span>

### <span data-ttu-id="f905d-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f905d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="f905d-113">Bu komut, belirtilen eşitleme grubundaki tüm sunucu uç noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="f905d-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="f905d-114">Belirli bir tane döndürmek için-ServerEndpointName belirtin.</span><span class="sxs-lookup"><span data-stu-id="f905d-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="f905d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f905d-115">PARAMETERS</span></span>

### <span data-ttu-id="f905d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f905d-116">-DefaultProfile</span></span>
<span data-ttu-id="f905d-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f905d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f905d-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f905d-118">-Name</span></span>
<span data-ttu-id="f905d-119">Sunucu uç noktasının adı.</span><span class="sxs-lookup"><span data-stu-id="f905d-119">Name of the server endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f905d-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f905d-120">-ParentObject</span></span>
<span data-ttu-id="f905d-121">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f905d-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="f905d-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="f905d-122">-ParentResourceId</span></span>
<span data-ttu-id="f905d-123">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f905d-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="f905d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f905d-124">-ResourceGroupName</span></span>
<span data-ttu-id="f905d-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f905d-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="f905d-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f905d-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="f905d-127">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="f905d-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="f905d-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f905d-128">-SyncGroupName</span></span>
<span data-ttu-id="f905d-129">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="f905d-129">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f905d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f905d-130">CommonParameters</span></span>
<span data-ttu-id="f905d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f905d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f905d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f905d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f905d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f905d-133">INPUTS</span></span>

### <span data-ttu-id="f905d-134">Microsoft. Azure. Commands. Storageseşitleme. model. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f905d-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="f905d-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f905d-135">System.String</span></span>

## <span data-ttu-id="f905d-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f905d-136">OUTPUTS</span></span>

### <span data-ttu-id="f905d-137">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f905d-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="f905d-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f905d-138">NOTES</span></span>

## <span data-ttu-id="f905d-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f905d-139">RELATED LINKS</span></span>
