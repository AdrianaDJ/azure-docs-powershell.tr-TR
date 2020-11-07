---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 4c78e636788ea1c91f4ff71b8439f84097503d82
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93934309"
---
# <span data-ttu-id="d035c-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="d035c-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="d035c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d035c-102">SYNOPSIS</span></span>
<span data-ttu-id="d035c-103">Bu komut, belirtilen bulut uç noktasını bir eşitleme grubundan siler.</span><span class="sxs-lookup"><span data-stu-id="d035c-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="d035c-104">En az bir bulut uç noktası olmadan, bu eşitleme grubunda başka sunucu uç noktaları eşitlenebilir.</span><span class="sxs-lookup"><span data-stu-id="d035c-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="d035c-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d035c-105">SYNTAX</span></span>

### <span data-ttu-id="d035c-106">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d035c-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d035c-107">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="d035c-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d035c-108">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="d035c-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d035c-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d035c-109">DESCRIPTION</span></span>
<span data-ttu-id="d035c-110">Bu komut, belirtilen bulut uç noktasını bir eşitleme grubundan siler.</span><span class="sxs-lookup"><span data-stu-id="d035c-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="d035c-111">Azure dosya paylaşımı bulut uç noktası başvuruları bu işlemle değişmeden kalır.</span><span class="sxs-lookup"><span data-stu-id="d035c-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="d035c-112">Bu komut yalnızca yetki alma amaçlıdır.</span><span class="sxs-lookup"><span data-stu-id="d035c-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="d035c-113">Bulut uç noktasını kaldırmak bozucu bir işlemdir.</span><span class="sxs-lookup"><span data-stu-id="d035c-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="d035c-114">Sunucu uç noktaları, en az bir bulut uç noktası olmadan eşitlenemiyor.</span><span class="sxs-lookup"><span data-stu-id="d035c-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="d035c-115">Bu işlem, eşitleme sorunlarını çözmek için gerçekleştirilmemelidir.</span><span class="sxs-lookup"><span data-stu-id="d035c-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="d035c-116">Bu Azure dosya paylaşımı, bulut uç noktası olarak aynı eşitleme grubuna yeniden eklenirse, çakışma dosyalarına ve diğer istenmeyen sonuçlara yol açabilir.</span><span class="sxs-lookup"><span data-stu-id="d035c-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="d035c-117">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d035c-117">EXAMPLES</span></span>

### <span data-ttu-id="d035c-118">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d035c-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="d035c-119">Bu komut, bulut uç noktasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d035c-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="d035c-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d035c-120">PARAMETERS</span></span>

### <span data-ttu-id="d035c-121">-Iş</span><span class="sxs-lookup"><span data-stu-id="d035c-121">-AsJob</span></span>
<span data-ttu-id="d035c-122">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="d035c-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d035c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d035c-123">-DefaultProfile</span></span>
<span data-ttu-id="d035c-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d035c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d035c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="d035c-125">-Force</span></span>
<span data-ttu-id="d035c-126">Arz-bu komutun onayını atlamaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="d035c-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="d035c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d035c-127">-InputObject</span></span>
<span data-ttu-id="d035c-128">Genellikle ardışık düzen aracılığıyla iletilen Cloudenvseçpoint giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="d035c-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d035c-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="d035c-129">-Name</span></span>
<span data-ttu-id="d035c-130">Cloudenvseçpunto adı.</span><span class="sxs-lookup"><span data-stu-id="d035c-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="d035c-131">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="d035c-131">-PassThru</span></span>
<span data-ttu-id="d035c-132">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="d035c-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="d035c-133">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="d035c-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="d035c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d035c-134">-ResourceGroupName</span></span>
<span data-ttu-id="d035c-135">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d035c-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="d035c-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d035c-136">-ResourceId</span></span>
<span data-ttu-id="d035c-137">Cloudenvseçpoint kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="d035c-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="d035c-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="d035c-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="d035c-139">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="d035c-139">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="d035c-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d035c-140">-SyncGroupName</span></span>
<span data-ttu-id="d035c-141">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="d035c-141">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="d035c-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="d035c-142">-Confirm</span></span>
<span data-ttu-id="d035c-143">Cmdlet 'i çalıştırmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="d035c-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d035c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d035c-144">-WhatIf</span></span>
<span data-ttu-id="d035c-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d035c-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d035c-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d035c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d035c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d035c-147">CommonParameters</span></span>
<span data-ttu-id="d035c-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d035c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d035c-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d035c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d035c-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d035c-150">INPUTS</span></span>

### <span data-ttu-id="d035c-151">Microsoft. Azure. Commands. Storagesehd. modeller. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="d035c-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="d035c-152">System. String</span><span class="sxs-lookup"><span data-stu-id="d035c-152">System.String</span></span>

## <span data-ttu-id="d035c-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d035c-153">OUTPUTS</span></span>

### <span data-ttu-id="d035c-154">System. Object</span><span class="sxs-lookup"><span data-stu-id="d035c-154">System.Object</span></span>
## <span data-ttu-id="d035c-155">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d035c-155">NOTES</span></span>

## <span data-ttu-id="d035c-156">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d035c-156">RELATED LINKS</span></span>
