---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/approve-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Approve-AzNetAppFilesReplication.md
ms.openlocfilehash: 9afa4f22de142dba7608d33ed04c972758911aa9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278392"
---
# <span data-ttu-id="02592-101">Approve-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="02592-101">Approve-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="02592-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02592-102">SYNOPSIS</span></span>
<span data-ttu-id="02592-103">Kaynak birimde çoğaltma bağlantısını onayla/yetkilendir</span><span class="sxs-lookup"><span data-stu-id="02592-103">Approve/Authorize replication connection on the source volume</span></span>

## <span data-ttu-id="02592-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="02592-104">SYNTAX</span></span>

### <span data-ttu-id="02592-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="02592-105">ByFieldsParameterSet (Default)</span></span>
```
Approve-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> -DataProtectionVolumeId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02592-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="02592-106">ByResourceIdParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02592-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02592-107">ByObjectParameterSet</span></span>
```
Approve-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02592-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="02592-108">DESCRIPTION</span></span>
<span data-ttu-id="02592-109">Kaynak birimdeki çoğaltma bağlantısını onaylama</span><span class="sxs-lookup"><span data-stu-id="02592-109">Approve the replication connection on the source volume</span></span>

## <span data-ttu-id="02592-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="02592-110">EXAMPLES</span></span>

### <span data-ttu-id="02592-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="02592-111">Example 1</span></span>
```powershell
PS C:\> Approve-AzNetAppFilesReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -DataProtectionVolumeId "MyDestinationVolumeId"

Output:
remoteVolumeResourceId          : resourceId
```

<span data-ttu-id="02592-112">Bu komut, MyAnfVolume 'teki yinelemeyi onaylar.</span><span class="sxs-lookup"><span data-stu-id="02592-112">This command Approves the Replication on MyAnfVolume.</span></span>

## <span data-ttu-id="02592-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="02592-113">PARAMETERS</span></span>

### <span data-ttu-id="02592-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="02592-114">-AccountName</span></span>
<span data-ttu-id="02592-115">Çoğaltma kaynak biriminin ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="02592-115">The name of the ANF account of the replication source volume</span></span>

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

### <span data-ttu-id="02592-116">-Dataprotectionvolumeıd</span><span class="sxs-lookup"><span data-stu-id="02592-116">-DataProtectionVolumeId</span></span>
<span data-ttu-id="02592-117">Hedef veri koruma biriminin dosya sistemi kimliği</span><span class="sxs-lookup"><span data-stu-id="02592-117">The file system id of the destination data protection volume</span></span>

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

### <span data-ttu-id="02592-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02592-118">-DefaultProfile</span></span>
<span data-ttu-id="02592-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="02592-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02592-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02592-120">-InputObject</span></span>
<span data-ttu-id="02592-121">Çoğaltma hedefine yetki veren ANF kaynak birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="02592-121">The ANF source volume object to authorized the replication destination</span></span>

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

### <span data-ttu-id="02592-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="02592-122">-Name</span></span>
<span data-ttu-id="02592-123">ANF çoğaltma kaynak biriminin adı</span><span class="sxs-lookup"><span data-stu-id="02592-123">The name of the ANF replication source volume</span></span>

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

### <span data-ttu-id="02592-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="02592-124">-PassThru</span></span>
<span data-ttu-id="02592-125">Belirtilen birimin çoğaltma yetkilendirmesi gerçekleştirilip gerçekleştirilmeyeceğini döndürme</span><span class="sxs-lookup"><span data-stu-id="02592-125">Return whether replication authorization of the specified volume was performed</span></span>

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

### <span data-ttu-id="02592-126">-PoolName</span><span class="sxs-lookup"><span data-stu-id="02592-126">-PoolName</span></span>
<span data-ttu-id="02592-127">Çoğaltma kaynak biriminin ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="02592-127">The name of the ANF pool of the replication source volume</span></span>

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

### <span data-ttu-id="02592-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02592-128">-ResourceGroupName</span></span>
<span data-ttu-id="02592-129">ANF çoğaltma kaynak biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="02592-129">The resource group of the ANF replication source volume</span></span>

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

### <span data-ttu-id="02592-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="02592-130">-ResourceId</span></span>
<span data-ttu-id="02592-131">ANF çoğaltma kaynak biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="02592-131">The resource id of the ANF replication source volume</span></span>

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

### <span data-ttu-id="02592-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="02592-132">-Confirm</span></span>
<span data-ttu-id="02592-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="02592-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02592-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02592-134">-WhatIf</span></span>
<span data-ttu-id="02592-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="02592-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02592-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="02592-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02592-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02592-137">CommonParameters</span></span>
<span data-ttu-id="02592-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="02592-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02592-139">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="02592-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02592-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="02592-140">INPUTS</span></span>

### <span data-ttu-id="02592-141">System. String</span><span class="sxs-lookup"><span data-stu-id="02592-141">System.String</span></span>

### <span data-ttu-id="02592-142">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="02592-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="02592-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="02592-143">OUTPUTS</span></span>

### <span data-ttu-id="02592-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02592-144">System.Boolean</span></span>

## <span data-ttu-id="02592-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="02592-145">NOTES</span></span>

## <span data-ttu-id="02592-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="02592-146">RELATED LINKS</span></span>
