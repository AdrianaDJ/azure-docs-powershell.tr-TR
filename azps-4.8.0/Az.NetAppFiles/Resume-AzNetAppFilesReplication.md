---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/resume-aznetappfilesreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Resume-AzNetAppFilesReplication.md
ms.openlocfilehash: 95ed2dc354f32229727a3d1b13dbfdfb95fe001a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108958"
---
# <span data-ttu-id="26b6a-101">Resume-AzNetAppFilesReplication</span><span class="sxs-lookup"><span data-stu-id="26b6a-101">Resume-AzNetAppFilesReplication</span></span>

## <span data-ttu-id="26b6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="26b6a-103">Hedef birimdeki bağlantıyı sürdürün/yeniden eşitleyin.</span><span class="sxs-lookup"><span data-stu-id="26b6a-103">Resume/Resync the connection on the destination volume.</span></span> <span data-ttu-id="26b6a-104">İşlem kaynak birimde çalıştırılmışsa, bağlantıyı tersine eşitler ve kaynaktan hedefle eşitlenir.</span><span class="sxs-lookup"><span data-stu-id="26b6a-104">If the operation is ran on the source volume it will reverse-resync the connection and sync from source to destination.</span></span>

## <span data-ttu-id="26b6a-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="26b6a-105">SYNTAX</span></span>

### <span data-ttu-id="26b6a-106">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="26b6a-106">ByFieldsParameterSet (Default)</span></span>
```
Resume-AzNetAppFilesReplication -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26b6a-107">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="26b6a-107">ByResourceIdParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26b6a-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26b6a-108">ByObjectParameterSet</span></span>
```
Resume-AzNetAppFilesReplication -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26b6a-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="26b6a-109">DESCRIPTION</span></span>
<span data-ttu-id="26b6a-110">Hedef birimdeki bağlantıyı sürdürme/yeniden eşitleme</span><span class="sxs-lookup"><span data-stu-id="26b6a-110">Resume/Resync the connection on the destination volume</span></span>

## <span data-ttu-id="26b6a-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="26b6a-111">EXAMPLES</span></span>

### <span data-ttu-id="26b6a-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="26b6a-112">Example 1</span></span>
```powershell
PS C:\> Resume-AnfReplication -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyDestinationAnfVolume"
```

<span data-ttu-id="26b6a-113">Bu komut, "MyDestinationAnfVolume" birimindeki ANF çoğaltma bağlantısını sürdürür.</span><span class="sxs-lookup"><span data-stu-id="26b6a-113">This command resumes the ANF Replication connection on volume "MyDestinationAnfVolume".</span></span>

## <span data-ttu-id="26b6a-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="26b6a-114">PARAMETERS</span></span>

### <span data-ttu-id="26b6a-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="26b6a-115">-AccountName</span></span>
<span data-ttu-id="26b6a-116">Çoğaltma biriminin ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="26b6a-116">The name of the ANF account of the replication volume</span></span>

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

### <span data-ttu-id="26b6a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b6a-117">-DefaultProfile</span></span>
<span data-ttu-id="26b6a-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="26b6a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26b6a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26b6a-119">-InputObject</span></span>
<span data-ttu-id="26b6a-120">Yeniden eşitlenmesi için ANF çoğaltma hedef birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="26b6a-120">The ANF replication destination volume object to resync</span></span>

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

### <span data-ttu-id="26b6a-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="26b6a-121">-Name</span></span>
<span data-ttu-id="26b6a-122">ANF çoğaltma hedef biriminin adı</span><span class="sxs-lookup"><span data-stu-id="26b6a-122">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="26b6a-123">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="26b6a-123">-PassThru</span></span>
<span data-ttu-id="26b6a-124">Belirtilen çoğaltma biriminin yeniden eşitlemediği</span><span class="sxs-lookup"><span data-stu-id="26b6a-124">Return whether resync of the specified replication volume was performed</span></span>

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

### <span data-ttu-id="26b6a-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="26b6a-125">-PoolName</span></span>
<span data-ttu-id="26b6a-126">Çoğaltma biriminin ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="26b6a-126">The name of the ANF pool of the replication volume</span></span>

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

### <span data-ttu-id="26b6a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26b6a-127">-ResourceGroupName</span></span>
<span data-ttu-id="26b6a-128">ANF çoğaltma hedef biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="26b6a-128">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="26b6a-129">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="26b6a-129">-ResourceId</span></span>
<span data-ttu-id="26b6a-130">ANF çoğaltma hedef biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="26b6a-130">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="26b6a-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="26b6a-131">-Confirm</span></span>
<span data-ttu-id="26b6a-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="26b6a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26b6a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26b6a-133">-WhatIf</span></span>
<span data-ttu-id="26b6a-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="26b6a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26b6a-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="26b6a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26b6a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b6a-136">CommonParameters</span></span>
<span data-ttu-id="26b6a-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="26b6a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b6a-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="26b6a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b6a-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="26b6a-139">INPUTS</span></span>

### <span data-ttu-id="26b6a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="26b6a-140">System.String</span></span>

### <span data-ttu-id="26b6a-141">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="26b6a-141">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="26b6a-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="26b6a-142">OUTPUTS</span></span>

### <span data-ttu-id="26b6a-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26b6a-143">System.Boolean</span></span>

## <span data-ttu-id="26b6a-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="26b6a-144">NOTES</span></span>

## <span data-ttu-id="26b6a-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="26b6a-145">RELATED LINKS</span></span>
