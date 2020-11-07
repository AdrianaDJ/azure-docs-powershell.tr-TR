---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 328fd4c798380202b355974cc8d9150e1d138da5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758483"
---
# <span data-ttu-id="33400-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="33400-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="33400-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33400-102">SYNOPSIS</span></span>
<span data-ttu-id="33400-103">Bu komut belirtilen sunucu uç noktasını silecek.</span><span class="sxs-lookup"><span data-stu-id="33400-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="33400-104">Bu konuma eşitleme hemen durdurulur.</span><span class="sxs-lookup"><span data-stu-id="33400-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="33400-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="33400-105">SYNTAX</span></span>

### <span data-ttu-id="33400-106">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="33400-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33400-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="33400-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33400-108">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="33400-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33400-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="33400-109">DESCRIPTION</span></span>
<span data-ttu-id="33400-110">Sunucu uç noktasını kaldırmak bozucu bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="33400-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="33400-111">Bu sunucu konumu eşitlemeyi durduracak.</span><span class="sxs-lookup"><span data-stu-id="33400-111">This server location will stop syncing.</span></span> <span data-ttu-id="33400-112">Bu işlem, eşitleme sorunlarını çözmek için gerçekleştirilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="33400-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="33400-113">Bu sunucu konumu (dosyaları dahil) sunucu uç noktasına aynı eşitleme grubuna yeniden eklenirse çakışma dosyalarına ve diğer istenmeyen sonuçlara yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="33400-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="33400-114">Bu komut yalnızca yetki alma amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="33400-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="33400-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="33400-115">EXAMPLES</span></span>

### <span data-ttu-id="33400-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="33400-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="33400-117">Bu komut sunucu uç noktasını kaldıracak.</span><span class="sxs-lookup"><span data-stu-id="33400-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="33400-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="33400-118">PARAMETERS</span></span>

### <span data-ttu-id="33400-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="33400-119">-AsJob</span></span>
<span data-ttu-id="33400-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="33400-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33400-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33400-121">-DefaultProfile</span></span>
<span data-ttu-id="33400-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="33400-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33400-123">-Force</span><span class="sxs-lookup"><span data-stu-id="33400-123">-Force</span></span>
<span data-ttu-id="33400-124">Arz-bu komutun onayını atlamaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="33400-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="33400-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33400-125">-InputObject</span></span>
<span data-ttu-id="33400-126">Normalde ardışık düzen aracılığıyla geçirilen ServerEndpoint giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="33400-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33400-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="33400-127">-Name</span></span>
<span data-ttu-id="33400-128">ServerEndpoint adı.</span><span class="sxs-lookup"><span data-stu-id="33400-128">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33400-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="33400-129">-PassThru</span></span>
<span data-ttu-id="33400-130">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="33400-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="33400-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33400-131">-ResourceGroupName</span></span>
<span data-ttu-id="33400-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="33400-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="33400-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="33400-133">-ResourceId</span></span>
<span data-ttu-id="33400-134">ServerEndpoint kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="33400-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33400-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="33400-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="33400-136">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="33400-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33400-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="33400-137">-SyncGroupName</span></span>
<span data-ttu-id="33400-138">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="33400-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33400-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="33400-139">-Confirm</span></span>
<span data-ttu-id="33400-140">Cmdlet 'i çalıştırmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="33400-140">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33400-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33400-141">-WhatIf</span></span>
<span data-ttu-id="33400-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="33400-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33400-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="33400-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33400-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33400-144">CommonParameters</span></span>
<span data-ttu-id="33400-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="33400-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33400-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33400-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33400-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="33400-147">INPUTS</span></span>

### <span data-ttu-id="33400-148">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="33400-148">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="33400-149">System. String</span><span class="sxs-lookup"><span data-stu-id="33400-149">System.String</span></span>

## <span data-ttu-id="33400-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="33400-150">OUTPUTS</span></span>

### <span data-ttu-id="33400-151">System. Object</span><span class="sxs-lookup"><span data-stu-id="33400-151">System.Object</span></span>
## <span data-ttu-id="33400-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="33400-152">NOTES</span></span>

## <span data-ttu-id="33400-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="33400-153">RELATED LINKS</span></span>
