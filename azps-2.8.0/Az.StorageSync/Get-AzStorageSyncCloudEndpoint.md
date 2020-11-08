---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: c8ace72aae518de3af27045507fb8c4cfaf72242
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934037"
---
# <span data-ttu-id="1f83b-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f83b-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="1f83b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f83b-102">SYNOPSIS</span></span>
<span data-ttu-id="1f83b-103">Bu komut, verilen eşitleme grubundaki tüm bulut uç noktalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="1f83b-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="1f83b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1f83b-104">SYNTAX</span></span>

### <span data-ttu-id="1f83b-105">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1f83b-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f83b-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f83b-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f83b-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f83b-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f83b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="1f83b-108">DESCRIPTION</span></span>
<span data-ttu-id="1f83b-109">Bu komut, verilen eşitleme grubundaki tüm bulut uç noktalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="1f83b-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="1f83b-110">Her bulut uç noktasının özniteliklerini de listelemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="1f83b-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="1f83b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1f83b-111">EXAMPLES</span></span>

### <span data-ttu-id="1f83b-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="1f83b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="1f83b-113">Bu komut, belirtilen eşitleme grubundaki tüm bulut uç noktalarını alır.</span><span class="sxs-lookup"><span data-stu-id="1f83b-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="1f83b-114">Belirli bir tane döndürmek için-Cloudenvseçpointname belirtin.</span><span class="sxs-lookup"><span data-stu-id="1f83b-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="1f83b-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1f83b-115">PARAMETERS</span></span>

### <span data-ttu-id="1f83b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f83b-116">-DefaultProfile</span></span>
<span data-ttu-id="1f83b-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1f83b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f83b-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="1f83b-118">-Name</span></span>
<span data-ttu-id="1f83b-119">Cloudenvseçpunto adı.</span><span class="sxs-lookup"><span data-stu-id="1f83b-119">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f83b-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1f83b-120">-ParentObject</span></span>
<span data-ttu-id="1f83b-121">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1f83b-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1f83b-122">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="1f83b-122">-ParentResourceId</span></span>
<span data-ttu-id="1f83b-123">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="1f83b-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1f83b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f83b-124">-ResourceGroupName</span></span>
<span data-ttu-id="1f83b-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="1f83b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1f83b-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="1f83b-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="1f83b-127">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="1f83b-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="1f83b-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1f83b-128">-SyncGroupName</span></span>
<span data-ttu-id="1f83b-129">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="1f83b-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="1f83b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f83b-130">CommonParameters</span></span>
<span data-ttu-id="1f83b-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1f83b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f83b-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f83b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f83b-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1f83b-133">INPUTS</span></span>

### <span data-ttu-id="1f83b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1f83b-134">System.String</span></span>

### <span data-ttu-id="1f83b-135">Microsoft. Azure. Commands. Storageseşitleme. model. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="1f83b-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="1f83b-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1f83b-136">OUTPUTS</span></span>

### <span data-ttu-id="1f83b-137">Microsoft. Azure. Commands. Storagesehd. modeller. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="1f83b-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="1f83b-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1f83b-138">NOTES</span></span>

## <span data-ttu-id="1f83b-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1f83b-139">RELATED LINKS</span></span>