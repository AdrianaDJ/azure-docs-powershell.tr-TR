---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: f7c1f129d9a5f6f6bdd117597a2943567fb4001d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93758481"
---
# <span data-ttu-id="fa0b4-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fa0b4-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="fa0b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa0b4-102">SYNOPSIS</span></span>
<span data-ttu-id="fa0b4-103">Bu komut, belirtilen eşitleme grubunu silecek.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="fa0b4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa0b4-104">SYNTAX</span></span>

### <span data-ttu-id="fa0b4-105">StringParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa0b4-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa0b4-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="fa0b4-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa0b4-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="fa0b4-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa0b4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa0b4-108">DESCRIPTION</span></span>
<span data-ttu-id="fa0b4-109">Bu komut, belirtilen eşitleme grubunu silecek.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="fa0b4-110">Bir eşitleme grubu yalnızca tüm içerilen uç noktaları silindiğinde kaldırılabilir.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="fa0b4-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa0b4-111">EXAMPLES</span></span>

### <span data-ttu-id="fa0b4-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="fa0b4-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="fa0b4-113">Bu komut, eşitleme grubunu kaldıracak.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="fa0b4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa0b4-114">PARAMETERS</span></span>

### <span data-ttu-id="fa0b4-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="fa0b4-115">-AsJob</span></span>
<span data-ttu-id="fa0b4-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="fa0b4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa0b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa0b4-117">-DefaultProfile</span></span>
<span data-ttu-id="fa0b4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa0b4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fa0b4-119">-Force</span></span>
<span data-ttu-id="fa0b4-120">Arz-bu komutun onayını atlamaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="fa0b4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa0b4-121">-InputObject</span></span>
<span data-ttu-id="fa0b4-122">SyncGroup giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="fa0b4-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="fa0b4-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa0b4-123">-Name</span></span>
<span data-ttu-id="fa0b4-124">SyncGroup adı.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="fa0b4-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="fa0b4-125">-PassThru</span></span>
<span data-ttu-id="fa0b4-126">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="fa0b4-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="fa0b4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa0b4-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa0b4-128">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="fa0b4-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fa0b4-129">-ResourceId</span></span>
<span data-ttu-id="fa0b4-130">SyncGroup kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="fa0b4-130">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="fa0b4-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="fa0b4-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="fa0b4-132">StorageSyncService adı.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="fa0b4-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa0b4-133">-Confirm</span></span>
<span data-ttu-id="fa0b4-134">Cmdlet 'i çalıştırmadan önce onay ister.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-134">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa0b4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa0b4-135">-WhatIf</span></span>
<span data-ttu-id="fa0b4-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa0b4-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa0b4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa0b4-138">CommonParameters</span></span>
<span data-ttu-id="fa0b4-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa0b4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa0b4-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa0b4-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa0b4-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa0b4-141">INPUTS</span></span>

### <span data-ttu-id="fa0b4-142">Microsoft. Azure. Commands. Storageseşitleme. model. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fa0b4-142">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="fa0b4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="fa0b4-143">System.String</span></span>

### <span data-ttu-id="fa0b4-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fa0b4-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fa0b4-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa0b4-145">OUTPUTS</span></span>

### <span data-ttu-id="fa0b4-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="fa0b4-146">System.Object</span></span>
## <span data-ttu-id="fa0b4-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa0b4-147">NOTES</span></span>

## <span data-ttu-id="fa0b4-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa0b4-148">RELATED LINKS</span></span>
