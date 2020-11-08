---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/restore-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Restore-AzNetAppFilesVolume.md
ms.openlocfilehash: 486bd44d3f48213fde6fb9b6c1d15a5683c1fd82
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94266078"
---
# <span data-ttu-id="a89ad-101">Restore-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a89ad-101">Restore-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="a89ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a89ad-102">SYNOPSIS</span></span>
<span data-ttu-id="a89ad-103">Bir birimi anlık görüntülerinden birine geri yükleme/geri döndürme</span><span class="sxs-lookup"><span data-stu-id="a89ad-103">Restore/Revert a volume to one of its snapshots</span></span>

## <span data-ttu-id="a89ad-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a89ad-104">SYNTAX</span></span>

### <span data-ttu-id="a89ad-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a89ad-105">ByFieldsParameterSet (Default)</span></span>
```
Revert-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-SnapshotId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a89ad-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a89ad-106">ByParentObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89ad-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a89ad-107">ByResourceIdParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a89ad-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a89ad-108">ByObjectParameterSet</span></span>
```
Restore-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a89ad-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="a89ad-109">DESCRIPTION</span></span>
<span data-ttu-id="a89ad-110">Bir birimi anlık görüntü kimliği parametre</span><span class="sxs-lookup"><span data-stu-id="a89ad-110">Restore/Revert a volume to the snapshot specified in the SnapshotId paramter</span></span>

## <span data-ttu-id="a89ad-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a89ad-111">EXAMPLES</span></span>

### <span data-ttu-id="a89ad-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a89ad-112">Example 1</span></span>
```powershell
PS C:\> Restore-AzNetAppFilesVolume -ResourceGroupName "MyRG" -Location "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -SnapshotId 7d6e4069-6c78-6c61-7bf6-c60968e45fbf
```

<span data-ttu-id="a89ad-113">Bu komut, 7d6e4069-6c78-6c61-7bf6-c60968e45fbf 'in anlık görüntüsü olan ses düzeyini geri yükler/</span><span class="sxs-lookup"><span data-stu-id="a89ad-113">This command Restores/Reverts the volume MyVolume to one of its snapshots with the snapshotId of 7d6e4069-6c78-6c61-7bf6-c60968e45fbf</span></span>

## <span data-ttu-id="a89ad-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a89ad-114">PARAMETERS</span></span>

### <span data-ttu-id="a89ad-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a89ad-115">-AccountName</span></span>
<span data-ttu-id="a89ad-116">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="a89ad-116">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ad-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a89ad-117">-DefaultProfile</span></span>
<span data-ttu-id="a89ad-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a89ad-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ad-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a89ad-119">-InputObject</span></span>
<span data-ttu-id="a89ad-120">Kaldırılacak birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="a89ad-120">The volume object to remove</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a89ad-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="a89ad-121">-Name</span></span>
<span data-ttu-id="a89ad-122">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="a89ad-122">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ad-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a89ad-123">-PassThru</span></span>
<span data-ttu-id="a89ad-124">Belirtilen birime başarıyla geri yüklenip geri döndürüldüğünü geri döndürme</span><span class="sxs-lookup"><span data-stu-id="a89ad-124">Return whether the specified volume was successfully restored/reverted</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ad-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a89ad-125">-PoolName</span></span>
<span data-ttu-id="a89ad-126">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="a89ad-126">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ad-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="a89ad-127">-PoolObject</span></span>
<span data-ttu-id="a89ad-128">Kaldırılacak birimi içeren havuz nesnesi</span><span class="sxs-lookup"><span data-stu-id="a89ad-128">The pool object containing the volume to remove</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a89ad-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a89ad-129">-ResourceGroupName</span></span>
<span data-ttu-id="a89ad-130">ANF biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="a89ad-130">The resource group of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ad-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a89ad-131">-ResourceId</span></span>
<span data-ttu-id="a89ad-132">ANF biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="a89ad-132">The resource id of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a89ad-133">-Anlık anlık kimliği</span><span class="sxs-lookup"><span data-stu-id="a89ad-133">-SnapshotId</span></span>
<span data-ttu-id="a89ad-134">Anlık görüntünün anlık görüntülemesi.</span><span class="sxs-lookup"><span data-stu-id="a89ad-134">SnapshotId of the snapshot.</span></span>
<span data-ttu-id="a89ad-135">Anlık görüntüyü tanımlamakta kullanılan UUID v4</span><span class="sxs-lookup"><span data-stu-id="a89ad-135">UUID v4 used to identify the Snapshot</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ad-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="a89ad-136">-Confirm</span></span>
<span data-ttu-id="a89ad-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a89ad-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ad-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a89ad-138">-WhatIf</span></span>
<span data-ttu-id="a89ad-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a89ad-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a89ad-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a89ad-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a89ad-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a89ad-141">CommonParameters</span></span>
<span data-ttu-id="a89ad-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a89ad-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a89ad-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a89ad-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a89ad-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a89ad-144">INPUTS</span></span>

### <span data-ttu-id="a89ad-145">System. String</span><span class="sxs-lookup"><span data-stu-id="a89ad-145">System.String</span></span>

### <span data-ttu-id="a89ad-146">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a89ad-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="a89ad-147">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a89ad-147">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a89ad-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a89ad-148">OUTPUTS</span></span>

### <span data-ttu-id="a89ad-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a89ad-149">System.Boolean</span></span>

## <span data-ttu-id="a89ad-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a89ad-150">NOTES</span></span>

## <span data-ttu-id="a89ad-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a89ad-151">RELATED LINKS</span></span>
