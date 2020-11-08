---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: ebee7b772fc4da3ef14d2273b79b089d57fa317f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938091"
---
# <span data-ttu-id="778f4-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="778f4-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="778f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="778f4-102">SYNOPSIS</span></span>
<span data-ttu-id="778f4-103">Bu komut, belirli bir depolama Eşitleme hizmetine kaydedilen tüm sunucuları listeler.</span><span class="sxs-lookup"><span data-stu-id="778f4-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="778f4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="778f4-104">SYNTAX</span></span>

### <span data-ttu-id="778f4-105">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="778f4-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="778f4-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="778f4-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="778f4-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="778f4-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="778f4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="778f4-108">DESCRIPTION</span></span>
<span data-ttu-id="778f4-109">Bu komut, belirli bir depolama Eşitleme hizmetine kaydedilen tüm sunucuları listeler.</span><span class="sxs-lookup"><span data-stu-id="778f4-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="778f4-110">Ayrıca, her kaydedilmiş sunucunun özniteliklerini de listelemek için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="778f4-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="778f4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="778f4-111">EXAMPLES</span></span>

### <span data-ttu-id="778f4-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="778f4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="778f4-113">Bu komut, belirli bir depolama Eşitleme hizmetine kaydedilen tüm sunucuları alır.</span><span class="sxs-lookup"><span data-stu-id="778f4-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="778f4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="778f4-114">PARAMETERS</span></span>

### <span data-ttu-id="778f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="778f4-115">-DefaultProfile</span></span>
<span data-ttu-id="778f4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="778f4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="778f4-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="778f4-117">-ParentObject</span></span>
<span data-ttu-id="778f4-118">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="778f4-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="778f4-119">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="778f4-119">-ParentResourceId</span></span>
<span data-ttu-id="778f4-120">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="778f4-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="778f4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="778f4-121">-ResourceGroupName</span></span>
<span data-ttu-id="778f4-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="778f4-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="778f4-123">-SunucuKimliği</span><span class="sxs-lookup"><span data-stu-id="778f4-123">-ServerId</span></span>
<span data-ttu-id="778f4-124">RegisteredServer 'in adı.</span><span class="sxs-lookup"><span data-stu-id="778f4-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="778f4-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="778f4-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="778f4-126">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="778f4-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="778f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="778f4-127">CommonParameters</span></span>
<span data-ttu-id="778f4-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="778f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="778f4-129">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="778f4-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="778f4-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="778f4-130">INPUTS</span></span>

### <span data-ttu-id="778f4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="778f4-131">System.String</span></span>

### <span data-ttu-id="778f4-132">Microsoft. Azure. Commands. Storagesehd. modeller. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="778f4-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="778f4-133">System. Guid</span><span class="sxs-lookup"><span data-stu-id="778f4-133">System.Guid</span></span>

## <span data-ttu-id="778f4-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="778f4-134">OUTPUTS</span></span>

### <span data-ttu-id="778f4-135">Microsoft. Azure. Commands. Storages, EHD.</span><span class="sxs-lookup"><span data-stu-id="778f4-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="778f4-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="778f4-136">NOTES</span></span>

## <span data-ttu-id="778f4-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="778f4-137">RELATED LINKS</span></span>