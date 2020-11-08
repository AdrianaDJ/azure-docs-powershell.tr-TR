---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098652"
---
# <span data-ttu-id="9649c-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9649c-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="9649c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9649c-102">SYNOPSIS</span></span>
<span data-ttu-id="9649c-103">Bu komut belirtilen sunucu uç noktasını silecek.</span><span class="sxs-lookup"><span data-stu-id="9649c-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="9649c-104">Bu konuma eşitleme hemen durdurulur.</span><span class="sxs-lookup"><span data-stu-id="9649c-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="9649c-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9649c-105">SYNTAX</span></span>

### <span data-ttu-id="9649c-106">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="9649c-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9649c-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="9649c-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9649c-108">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="9649c-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9649c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="9649c-109">DESCRIPTION</span></span>
<span data-ttu-id="9649c-110">Sunucu uç noktasını kaldırmak bozucu bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="9649c-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="9649c-111">Bu sunucu konumu eşitlemeyi durduracak.</span><span class="sxs-lookup"><span data-stu-id="9649c-111">This server location will stop syncing.</span></span> <span data-ttu-id="9649c-112">Bu işlem, eşitleme sorunlarını çözmek için gerçekleştirilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="9649c-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="9649c-113">Bu sunucu konumu (dosyaları dahil) sunucu uç noktasına aynı eşitleme grubuna yeniden eklenirse çakışma dosyalarına ve diğer istenmeyen sonuçlara yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="9649c-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="9649c-114">Bu komut yalnızca yetki alma amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="9649c-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="9649c-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9649c-115">EXAMPLES</span></span>

### <span data-ttu-id="9649c-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9649c-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="9649c-117">Bu komut sunucu uç noktasını kaldıracak.</span><span class="sxs-lookup"><span data-stu-id="9649c-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="9649c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9649c-118">PARAMETERS</span></span>

### <span data-ttu-id="9649c-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="9649c-119">-AsJob</span></span>
<span data-ttu-id="9649c-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="9649c-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9649c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9649c-121">-DefaultProfile</span></span>
<span data-ttu-id="9649c-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9649c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9649c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="9649c-123">-Force</span></span>
<span data-ttu-id="9649c-124">Arz-bu komutun onayını atlamaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="9649c-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="9649c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9649c-125">-InputObject</span></span>
<span data-ttu-id="9649c-126">Normalde ardışık düzen aracılığıyla geçirilen ServerEndpoint giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="9649c-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="9649c-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="9649c-127">-Name</span></span>
<span data-ttu-id="9649c-128">ServerEndpoint adı.</span><span class="sxs-lookup"><span data-stu-id="9649c-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="9649c-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="9649c-129">-PassThru</span></span>
<span data-ttu-id="9649c-130">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="9649c-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="9649c-131">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="9649c-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="9649c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9649c-132">-ResourceGroupName</span></span>
<span data-ttu-id="9649c-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="9649c-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="9649c-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="9649c-134">-ResourceId</span></span>
<span data-ttu-id="9649c-135">ServerEndpoint kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="9649c-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="9649c-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9649c-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="9649c-137">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="9649c-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="9649c-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9649c-138">-SyncGroupName</span></span>
<span data-ttu-id="9649c-139">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="9649c-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="9649c-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="9649c-140">-Confirm</span></span>
<span data-ttu-id="9649c-141">Cmdlet 'i çalıştırmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="9649c-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9649c-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9649c-142">-WhatIf</span></span>
<span data-ttu-id="9649c-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9649c-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9649c-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9649c-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9649c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9649c-145">CommonParameters</span></span>
<span data-ttu-id="9649c-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9649c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9649c-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9649c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9649c-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9649c-148">INPUTS</span></span>

### <span data-ttu-id="9649c-149">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9649c-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="9649c-150">System. String</span><span class="sxs-lookup"><span data-stu-id="9649c-150">System.String</span></span>

## <span data-ttu-id="9649c-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9649c-151">OUTPUTS</span></span>

### <span data-ttu-id="9649c-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="9649c-152">System.Object</span></span>
## <span data-ttu-id="9649c-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9649c-153">NOTES</span></span>

## <span data-ttu-id="9649c-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9649c-154">RELATED LINKS</span></span>