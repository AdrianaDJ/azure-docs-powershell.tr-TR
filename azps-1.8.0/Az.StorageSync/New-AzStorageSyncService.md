---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: d2d18a908b53c9a8ab077671b7e2026516d40b17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758486"
---
# <span data-ttu-id="7c74a-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="7c74a-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="7c74a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c74a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c74a-103">Bu komut, kaynak grubunda yeni bir depolama eşitleme hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c74a-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="7c74a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c74a-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c74a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c74a-105">DESCRIPTION</span></span>
<span data-ttu-id="7c74a-106">Depolama eşitleme hizmeti, Azure dosya eşitlemesi için en üst düzey kaynaktır. Bu komut, kaynak grubunda yeni bir depolama eşitleme hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c74a-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="7c74a-107">Kuruluşunuzdaki farklı sunucu gruplarını ayırt etmek için kesinlikle gerekli olan birkaç depolama eşitleme hizmeti oluşturmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="7c74a-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="7c74a-108">Depolama eşitleme hizmeti eşitleme grupları içerir ve ayrıca sunucularınızı kaydettirmek için hedef olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="7c74a-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="7c74a-109">Sunucu yalnızca tek bir depolama Eşitleme hizmetine kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="7c74a-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="7c74a-110">Aynı dosya kümesini eşitlemeye ihtiyaç duyan sunucular varsa, bunları aynı depolama Eşitleme hizmetine kaydettirin.</span><span class="sxs-lookup"><span data-stu-id="7c74a-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="7c74a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c74a-111">EXAMPLES</span></span>

### <span data-ttu-id="7c74a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7c74a-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="7c74a-113">Bu komut, bir depolama eşitleme hizmeti oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7c74a-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="7c74a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c74a-114">PARAMETERS</span></span>

### <span data-ttu-id="7c74a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c74a-115">-DefaultProfile</span></span>
<span data-ttu-id="7c74a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7c74a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c74a-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="7c74a-117">-Location</span></span>
<span data-ttu-id="7c74a-118">Depolama eşitleme hizmeti konumu.</span><span class="sxs-lookup"><span data-stu-id="7c74a-118">Storage Sync Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c74a-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="7c74a-119">-Name</span></span>
<span data-ttu-id="7c74a-120">Depolama eşitleme hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="7c74a-120">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c74a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c74a-121">-ResourceGroupName</span></span>
<span data-ttu-id="7c74a-122">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7c74a-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c74a-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7c74a-123">-Tag</span></span>
<span data-ttu-id="7c74a-124">Depolama eşitleme hizmeti etiketleri.</span><span class="sxs-lookup"><span data-stu-id="7c74a-124">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c74a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c74a-125">CommonParameters</span></span>
<span data-ttu-id="7c74a-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c74a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c74a-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c74a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c74a-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c74a-128">INPUTS</span></span>

### <span data-ttu-id="7c74a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7c74a-129">System.String</span></span>

## <span data-ttu-id="7c74a-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c74a-130">OUTPUTS</span></span>

### <span data-ttu-id="7c74a-131">Microsoft. Azure. Commands. Storagesehd. modeller. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="7c74a-131">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="7c74a-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c74a-132">NOTES</span></span>

## <span data-ttu-id="7c74a-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c74a-133">RELATED LINKS</span></span>