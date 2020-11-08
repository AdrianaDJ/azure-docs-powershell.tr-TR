---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098654"
---
# <span data-ttu-id="76301-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="76301-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="76301-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76301-102">SYNOPSIS</span></span>
<span data-ttu-id="76301-103">Bu komut, belirtilen eşitleme grubunu silecek.</span><span class="sxs-lookup"><span data-stu-id="76301-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="76301-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76301-104">SYNTAX</span></span>

### <span data-ttu-id="76301-105">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76301-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76301-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="76301-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76301-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="76301-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76301-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="76301-108">DESCRIPTION</span></span>
<span data-ttu-id="76301-109">Bu komut, belirtilen eşitleme grubunu silecek.</span><span class="sxs-lookup"><span data-stu-id="76301-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="76301-110">Bir eşitleme grubu yalnızca tüm içerilen uç noktaları silindiğinde kaldırılabilir.</span><span class="sxs-lookup"><span data-stu-id="76301-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="76301-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76301-111">EXAMPLES</span></span>

### <span data-ttu-id="76301-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="76301-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="76301-113">Bu komut, eşitleme grubunu kaldıracak.</span><span class="sxs-lookup"><span data-stu-id="76301-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="76301-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76301-114">PARAMETERS</span></span>

### <span data-ttu-id="76301-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="76301-115">-AsJob</span></span>
<span data-ttu-id="76301-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="76301-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76301-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76301-117">-DefaultProfile</span></span>
<span data-ttu-id="76301-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="76301-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76301-119">-Force</span><span class="sxs-lookup"><span data-stu-id="76301-119">-Force</span></span>
<span data-ttu-id="76301-120">Arz-bu komutun onayını atlamaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="76301-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76301-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76301-121">-InputObject</span></span>
<span data-ttu-id="76301-122">SyncGroup giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="76301-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76301-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="76301-123">-Name</span></span>
<span data-ttu-id="76301-124">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="76301-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76301-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="76301-125">-PassThru</span></span>
<span data-ttu-id="76301-126">Normal yürütmede, bu cmdlet başarı durumunda değer döndürmez.</span><span class="sxs-lookup"><span data-stu-id="76301-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="76301-127">Geçiş parametresini sağlarsanız, cmdlet başarılı yürütmeden sonra bir ardışık düzene bir değer yazar.</span><span class="sxs-lookup"><span data-stu-id="76301-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="76301-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76301-128">-ResourceGroupName</span></span>
<span data-ttu-id="76301-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="76301-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="76301-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="76301-130">-ResourceId</span></span>
<span data-ttu-id="76301-131">SyncGroup kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="76301-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="76301-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="76301-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="76301-133">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="76301-133">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76301-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="76301-134">-Confirm</span></span>
<span data-ttu-id="76301-135">Cmdlet 'i çalıştırmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="76301-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76301-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76301-136">-WhatIf</span></span>
<span data-ttu-id="76301-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="76301-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76301-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="76301-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76301-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76301-139">CommonParameters</span></span>
<span data-ttu-id="76301-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76301-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76301-141">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76301-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76301-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76301-142">INPUTS</span></span>

### <span data-ttu-id="76301-143">Microsoft. Azure. Commands. Storageseşitleme. model. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="76301-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="76301-144">System. String</span><span class="sxs-lookup"><span data-stu-id="76301-144">System.String</span></span>

### <span data-ttu-id="76301-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="76301-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="76301-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76301-146">OUTPUTS</span></span>

### <span data-ttu-id="76301-147">System. Object</span><span class="sxs-lookup"><span data-stu-id="76301-147">System.Object</span></span>
## <span data-ttu-id="76301-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76301-148">NOTES</span></span>

## <span data-ttu-id="76301-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76301-149">RELATED LINKS</span></span>
