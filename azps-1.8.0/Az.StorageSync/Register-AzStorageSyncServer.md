---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: edfeebf9781c40b44a5a06db407757a5e2f5d2a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758484"
---
# <span data-ttu-id="6dbfb-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="6dbfb-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="6dbfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6dbfb-102">SYNOPSIS</span></span>
<span data-ttu-id="6dbfb-103">Bu komut, bir sunucuyu güven ilişkisi oluşturan bir depolama Eşitleme hizmetine kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="6dbfb-104">PowerShell veya Azure portalı bu sunucuda eşitleme yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="6dbfb-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6dbfb-105">SYNTAX</span></span>

### <span data-ttu-id="6dbfb-106">ObjectParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6dbfb-106">ObjectParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dbfb-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dbfb-107">StringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6dbfb-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="6dbfb-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6dbfb-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="6dbfb-109">DESCRIPTION</span></span>
<span data-ttu-id="6dbfb-110">Bu komut, bir sunucuyu Azure dosya eşitlemesi için en üst düzey kaynağa sahip bir depolama Eşitleme hizmetine kaydeder. Sunucu ve depolama eşitleme hizmeti arasındaki bir güven ilişkisi, güvenli veri aktarımı ve yönetim kanallarının kullanılmasını sağlar.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="6dbfb-111">PowerShell 'i veya Azure portalı bu sunucuda eşitlenecek öğeleri yapılandırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="6dbfb-112">Sunucu yalnızca tek bir depolama Eşitleme hizmetine kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="6dbfb-113">Aynı dosya kümesini eşitlemeye ihtiyaç duyan sunucular varsa, bunları aynı depolama Eşitleme hizmetine kaydettirin.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="6dbfb-114">Komutun, doğrudan veya uzak PowerShell oturumu aracılığıyla kaydettirileceği sunucuda yerel olarak çalıştırılması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="6dbfb-115">Uzak bilgisayar nesnesi kabul edilemiyor.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="6dbfb-116">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6dbfb-116">EXAMPLES</span></span>

### <span data-ttu-id="6dbfb-117">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6dbfb-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="6dbfb-118">Bu komut, bu komutun üzerinde çalışacağı yerel sunucuyu kaydeder.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="6dbfb-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6dbfb-119">PARAMETERS</span></span>

### <span data-ttu-id="6dbfb-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="6dbfb-120">-AsJob</span></span>
<span data-ttu-id="6dbfb-121">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="6dbfb-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6dbfb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dbfb-122">-DefaultProfile</span></span>
<span data-ttu-id="6dbfb-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dbfb-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="6dbfb-124">-ParentObject</span></span>
<span data-ttu-id="6dbfb-125">Normalde parametre aracılığıyla geçirilen StorageSyncService nesnesi.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="6dbfb-126">-Parentresourceıd</span><span class="sxs-lookup"><span data-stu-id="6dbfb-126">-ParentResourceId</span></span>
<span data-ttu-id="6dbfb-127">StorageSyncService üst kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6dbfb-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="6dbfb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6dbfb-128">-ResourceGroupName</span></span>
<span data-ttu-id="6dbfb-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="6dbfb-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="6dbfb-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="6dbfb-131">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="6dbfb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dbfb-132">CommonParameters</span></span>
<span data-ttu-id="6dbfb-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dbfb-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6dbfb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dbfb-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6dbfb-135">INPUTS</span></span>

### <span data-ttu-id="6dbfb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6dbfb-136">System.String</span></span>

### <span data-ttu-id="6dbfb-137">Microsoft. Azure. Commands. Storagesehd. modeller. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="6dbfb-137">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="6dbfb-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6dbfb-138">OUTPUTS</span></span>

### <span data-ttu-id="6dbfb-139">Microsoft. Azure. Commands. Storages, EHD.</span><span class="sxs-lookup"><span data-stu-id="6dbfb-139">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="6dbfb-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6dbfb-140">NOTES</span></span>

## <span data-ttu-id="6dbfb-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6dbfb-141">RELATED LINKS</span></span>