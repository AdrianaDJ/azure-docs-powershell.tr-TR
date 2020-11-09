---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/remove-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesReplication.md
ms.openlocfilehash: 04ad7f188a2280dcdf84e8b5c1f45e20edf4d07b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325318"
---
# <span data-ttu-id="604cd-101">Remove-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="604cd-101">Remove-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="604cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="604cd-102">SYNOPSIS</span></span>
<span data-ttu-id="604cd-103">Hedef birimdeki çoğaltma bağlantısını kaldırma/silme ve kaynak çoğaltmaya sürüm gönderme</span><span class="sxs-lookup"><span data-stu-id="604cd-103">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="604cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="604cd-104">SYNTAX</span></span>

### <span data-ttu-id="604cd-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="604cd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="604cd-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="604cd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="604cd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="604cd-107">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="604cd-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="604cd-108">DESCRIPTION</span></span>
<span data-ttu-id="604cd-109">Hedef birimdeki çoğaltma bağlantısını kaldırma/silme ve kaynak çoğaltmaya sürüm gönderme</span><span class="sxs-lookup"><span data-stu-id="604cd-109">Remove/Delete the replication connection on the destination volume, and send release to the source replication</span></span>

## <span data-ttu-id="604cd-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="604cd-110">EXAMPLES</span></span>

### <span data-ttu-id="604cd-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="604cd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="604cd-112">Bu komut, "MyDestinationAnfVolume" birimindeki ANF çoğaltma bağlantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="604cd-112">This command removes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="604cd-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="604cd-113">PARAMETERS</span></span>

### <span data-ttu-id="604cd-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="604cd-114">-AccountName</span></span>
<span data-ttu-id="604cd-115">Çoğaltma biriminin ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="604cd-115">The name of the ANF account of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="604cd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="604cd-116">-DefaultProfile</span></span>
<span data-ttu-id="604cd-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="604cd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="604cd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="604cd-118">-InputObject</span></span>
<span data-ttu-id="604cd-119">Kaldırmak için çoğaltmanın</span><span class="sxs-lookup"><span data-stu-id="604cd-119">The ANF destination volume with the replication to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="604cd-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="604cd-120">-Name</span></span>
<span data-ttu-id="604cd-121">ANF çoğaltma hedef biriminin adı</span><span class="sxs-lookup"><span data-stu-id="604cd-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="604cd-122">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="604cd-122">-PassThru</span></span>
<span data-ttu-id="604cd-123">Belirtilen ANF çoğaltmasının başarıyla kaldırıldığını alma</span><span class="sxs-lookup"><span data-stu-id="604cd-123">Return whether the specified ANF replication was successfully removed</span></span>

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

### <span data-ttu-id="604cd-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="604cd-124">-PoolName</span></span>
<span data-ttu-id="604cd-125">Çoğaltma biriminin ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="604cd-125">The name of the ANF pool of the replication volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="604cd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="604cd-126">-ResourceGroupName</span></span>
<span data-ttu-id="604cd-127">ANF çoğaltma hedef biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="604cd-127">The resource group of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="604cd-128">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="604cd-128">-ResourceId</span></span>
<span data-ttu-id="604cd-129">ANF çoğaltma hedef biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="604cd-129">The resource id of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="604cd-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="604cd-130">-Confirm</span></span>
<span data-ttu-id="604cd-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="604cd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="604cd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="604cd-132">-WhatIf</span></span>
<span data-ttu-id="604cd-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="604cd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="604cd-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="604cd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="604cd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="604cd-135">CommonParameters</span></span>
<span data-ttu-id="604cd-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="604cd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="604cd-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="604cd-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="604cd-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="604cd-138">INPUTS</span></span>

### <span data-ttu-id="604cd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="604cd-139">System.String</span></span>

### <span data-ttu-id="604cd-140">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="604cd-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="604cd-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="604cd-141">OUTPUTS</span></span>

### <span data-ttu-id="604cd-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="604cd-142">System.Boolean</span></span>

## <span data-ttu-id="604cd-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="604cd-143">NOTES</span></span>

## <span data-ttu-id="604cd-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="604cd-144">RELATED LINKS</span></span>
