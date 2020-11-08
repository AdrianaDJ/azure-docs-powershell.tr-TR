---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277984"
---
# <span data-ttu-id="8ad59-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="8ad59-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="8ad59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ad59-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad59-103">Bu komut, kaynak grubunda depolama eşitleme hizmeti 'ni ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8ad59-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="8ad59-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ad59-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ad59-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ad59-105">DESCRIPTION</span></span>
<span data-ttu-id="8ad59-106">Depolama eşitleme hizmeti, Azure dosya eşitlemesi için en üst düzey kaynaktır. Bu komut, kaynak grubunda depolama eşitleme hizmeti 'ni ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8ad59-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="8ad59-107">Kuruluşunuzdaki farklı sunucu gruplarını ayırt etmek için kesinlikle gerekli olan birkaç depolama eşitleme hizmeti oluşturmanız önerilir.</span><span class="sxs-lookup"><span data-stu-id="8ad59-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="8ad59-108">Depolama eşitleme hizmeti eşitleme grupları içerir ve ayrıca sunucularınızı kaydettirmek için hedef olarak çalışır.</span><span class="sxs-lookup"><span data-stu-id="8ad59-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="8ad59-109">Sunucu yalnızca tek bir depolama Eşitleme hizmetine kaydedilebilir.</span><span class="sxs-lookup"><span data-stu-id="8ad59-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="8ad59-110">Aynı dosya kümesini eşitlemeye ihtiyaç duyan sunucular varsa, bunları aynı depolama Eşitleme hizmetine kaydettirin.</span><span class="sxs-lookup"><span data-stu-id="8ad59-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="8ad59-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ad59-111">EXAMPLES</span></span>

### <span data-ttu-id="8ad59-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8ad59-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="8ad59-113">Bu komut, bir depolama eşitleme hizmeti ayarlar.</span><span class="sxs-lookup"><span data-stu-id="8ad59-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="8ad59-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ad59-114">PARAMETERS</span></span>

### <span data-ttu-id="8ad59-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ad59-115">-DefaultProfile</span></span>
<span data-ttu-id="8ad59-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ad59-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="8ad59-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ad59-117">-Name</span></span>
<span data-ttu-id="8ad59-118">Depolama eşitleme hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="8ad59-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="8ad59-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ad59-119">-ResourceGroupName</span></span>
<span data-ttu-id="8ad59-120">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="8ad59-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="8ad59-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="8ad59-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="8ad59-122">Depolama eşitleme hizmeti IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="8ad59-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="8ad59-123">Etiketli</span><span class="sxs-lookup"><span data-stu-id="8ad59-123">-Tag</span></span>
<span data-ttu-id="8ad59-124">Depolama eşitleme hizmeti etiketleri.</span><span class="sxs-lookup"><span data-stu-id="8ad59-124">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ad59-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ad59-125">-Confirm</span></span>
<span data-ttu-id="8ad59-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ad59-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ad59-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ad59-127">-WhatIf</span></span>
<span data-ttu-id="8ad59-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ad59-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ad59-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8ad59-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ad59-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad59-130">CommonParameters</span></span>
<span data-ttu-id="8ad59-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ad59-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad59-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ad59-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad59-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ad59-133">INPUTS</span></span>

### <span data-ttu-id="8ad59-134">System. String</span><span class="sxs-lookup"><span data-stu-id="8ad59-134">System.String</span></span>

## <span data-ttu-id="8ad59-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ad59-135">OUTPUTS</span></span>

### <span data-ttu-id="8ad59-136">Microsoft. Azure. Commands. Storagesehd. modeller. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="8ad59-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="8ad59-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ad59-137">NOTES</span></span>

## <span data-ttu-id="8ad59-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ad59-138">RELATED LINKS</span></span>
