---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94325309"
---
# <span data-ttu-id="088c9-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="088c9-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="088c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="088c9-102">SYNOPSIS</span></span>
<span data-ttu-id="088c9-103">Hedef birimdeki bağlantıyı sürdürün/yeniden eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="088c9-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="088c9-104">İşlem kaynak birimde çalıştırılmışsa, bağlantıyı tersine eşitler ve kaynaktan hedefle eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="088c9-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="088c9-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="088c9-105">SYNTAX</span></span>

### <span data-ttu-id="088c9-106">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="088c9-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="088c9-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="088c9-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="088c9-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="088c9-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="088c9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="088c9-109">DESCRIPTION</span></span>
<span data-ttu-id="088c9-110">Hedef birimdeki bağlantıyı sürdürme/yeniden eşitleme</span><span class="sxs-lookup"><span data-stu-id="088c9-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="088c9-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="088c9-111">EXAMPLES</span></span>

### <span data-ttu-id="088c9-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="088c9-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="088c9-113">Bu komut, "MyDestinationAnfVolume" birimindeki ANF çoğaltma bağlantısını sürdürür.</span><span class="sxs-lookup"><span data-stu-id="088c9-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="088c9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="088c9-114">PARAMETERS</span></span>

### <span data-ttu-id="088c9-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="088c9-115">-AccountName</span></span>
<span data-ttu-id="088c9-116">Çoğaltma biriminin ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="088c9-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="088c9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="088c9-117">-DefaultProfile</span></span>
<span data-ttu-id="088c9-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="088c9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="088c9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="088c9-119">-InputObject</span></span>
<span data-ttu-id="088c9-120">Yeniden eşitlenmesi için ANF çoğaltma hedef birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="088c9-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="088c9-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="088c9-121">-Name</span></span>
<span data-ttu-id="088c9-122">ANF çoğaltma hedef biriminin adı</span><span class="sxs-lookup"><span data-stu-id="088c9-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="088c9-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="088c9-123">-PassThru</span></span>
<span data-ttu-id="088c9-124">Belirtilen çoğaltma biriminin yeniden eşitlemediği</span><span class="sxs-lookup"><span data-stu-id="088c9-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="088c9-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="088c9-125">-PoolName</span></span>
<span data-ttu-id="088c9-126">Çoğaltma biriminin ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="088c9-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="088c9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="088c9-127">-ResourceGroupName</span></span>
<span data-ttu-id="088c9-128">ANF çoğaltma hedef biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="088c9-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="088c9-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="088c9-129">-ResourceId</span></span>
<span data-ttu-id="088c9-130">ANF çoğaltma hedef biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="088c9-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="088c9-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="088c9-131">-Confirm</span></span>
<span data-ttu-id="088c9-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="088c9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="088c9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="088c9-133">-WhatIf</span></span>
<span data-ttu-id="088c9-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="088c9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="088c9-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="088c9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="088c9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="088c9-136">CommonParameters</span></span>
<span data-ttu-id="088c9-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="088c9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="088c9-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="088c9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="088c9-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="088c9-139">INPUTS</span></span>

### <span data-ttu-id="088c9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="088c9-140">System.String</span></span>

### <span data-ttu-id="088c9-141">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="088c9-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="088c9-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="088c9-142">OUTPUTS</span></span>

### <span data-ttu-id="088c9-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="088c9-143">System.Boolean</span></span>

## <span data-ttu-id="088c9-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="088c9-144">NOTES</span></span>

## <span data-ttu-id="088c9-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="088c9-145">RELATED LINKS</span></span>
