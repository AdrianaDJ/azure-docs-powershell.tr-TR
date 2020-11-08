---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 9afb334e7c26b49bddcabdbcd1ac4036fc3a77c6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276329"
---
# <span data-ttu-id="3c77a-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c77a-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="3c77a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c77a-102">SYNOPSIS</span></span>
<span data-ttu-id="3c77a-103">Bu komut belirtilen sunucu uç noktasını silecek.</span><span class="sxs-lookup"><span data-stu-id="3c77a-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="3c77a-104">Bu konuma eşitleme hemen durdurulur.</span><span class="sxs-lookup"><span data-stu-id="3c77a-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="3c77a-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3c77a-105">SYNTAX</span></span>

### <span data-ttu-id="3c77a-106">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3c77a-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c77a-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="3c77a-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c77a-108">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="3c77a-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c77a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3c77a-109">DESCRIPTION</span></span>
<span data-ttu-id="3c77a-110">Sunucu uç noktasını kaldırmak bozucu bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="3c77a-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="3c77a-111">Bu sunucu konumu eşitlemeyi durduracak.</span><span class="sxs-lookup"><span data-stu-id="3c77a-111">This server location will stop syncing.</span></span> <span data-ttu-id="3c77a-112">Bu işlem, eşitleme sorunlarını çözmek için gerçekleştirilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="3c77a-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="3c77a-113">Bu sunucu konumu (dosyaları dahil) sunucu uç noktasına aynı eşitleme grubuna yeniden eklenirse çakışma dosyalarına ve diğer istenmeyen sonuçlara yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="3c77a-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="3c77a-114">Bu komut yalnızca yetki alma amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="3c77a-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="3c77a-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3c77a-115">EXAMPLES</span></span>

### <span data-ttu-id="3c77a-116">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3c77a-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="3c77a-117">Bu komut sunucu uç noktasını kaldıracak.</span><span class="sxs-lookup"><span data-stu-id="3c77a-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="3c77a-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3c77a-118">PARAMETERS</span></span>

### <span data-ttu-id="3c77a-119">-Iş</span><span class="sxs-lookup"><span data-stu-id="3c77a-119">-AsJob</span></span>
<span data-ttu-id="3c77a-120">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="3c77a-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c77a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c77a-121">-DefaultProfile</span></span>
<span data-ttu-id="3c77a-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3c77a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c77a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3c77a-123">-Force</span></span>
<span data-ttu-id="3c77a-124">Arz-bu komutun onayını atlamaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="3c77a-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="3c77a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c77a-125">-InputObject</span></span>
<span data-ttu-id="3c77a-126">Normalde ardışık düzen aracılığıyla geçirilen ServerEndpoint giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="3c77a-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="3c77a-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="3c77a-127">-Name</span></span>
<span data-ttu-id="3c77a-128">ServerEndpoint adı.</span><span class="sxs-lookup"><span data-stu-id="3c77a-128">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="3c77a-129">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3c77a-129">-PassThru</span></span>
<span data-ttu-id="3c77a-130">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="3c77a-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="3c77a-131">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="3c77a-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="3c77a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c77a-132">-ResourceGroupName</span></span>
<span data-ttu-id="3c77a-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3c77a-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="3c77a-134">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3c77a-134">-ResourceId</span></span>
<span data-ttu-id="3c77a-135">ServerEndpoint kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="3c77a-135">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="3c77a-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="3c77a-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="3c77a-137">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="3c77a-137">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="3c77a-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="3c77a-138">-SyncGroupName</span></span>
<span data-ttu-id="3c77a-139">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="3c77a-139">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="3c77a-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="3c77a-140">-Confirm</span></span>
<span data-ttu-id="3c77a-141">Cmdlet 'i çalıştırmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="3c77a-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c77a-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c77a-142">-WhatIf</span></span>
<span data-ttu-id="3c77a-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3c77a-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c77a-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3c77a-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c77a-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c77a-145">CommonParameters</span></span>
<span data-ttu-id="3c77a-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3c77a-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c77a-147">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c77a-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c77a-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3c77a-148">INPUTS</span></span>

### <span data-ttu-id="3c77a-149">Microsoft. Azure. Commands. Storagesehd. modeller. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3c77a-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="3c77a-150">System. String</span><span class="sxs-lookup"><span data-stu-id="3c77a-150">System.String</span></span>

## <span data-ttu-id="3c77a-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3c77a-151">OUTPUTS</span></span>

### <span data-ttu-id="3c77a-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="3c77a-152">System.Object</span></span>
## <span data-ttu-id="3c77a-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3c77a-153">NOTES</span></span>

## <span data-ttu-id="3c77a-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3c77a-154">RELATED LINKS</span></span>
