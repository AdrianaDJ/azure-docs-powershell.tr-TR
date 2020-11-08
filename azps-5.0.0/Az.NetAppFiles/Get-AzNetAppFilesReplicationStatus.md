---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: a2345dfe37fd43532739cdfd8000b47fb1e20906
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277610"
---
# <span data-ttu-id="eae2e-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="eae2e-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="eae2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eae2e-102">SYNOPSIS</span></span>
<span data-ttu-id="eae2e-103">Çoğaltmanın durumunu alma</span><span class="sxs-lookup"><span data-stu-id="eae2e-103">Get the status of the replication</span></span>

## <span data-ttu-id="eae2e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eae2e-104">SYNTAX</span></span>

### <span data-ttu-id="eae2e-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eae2e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eae2e-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="eae2e-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eae2e-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eae2e-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eae2e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="eae2e-108">DESCRIPTION</span></span>
<span data-ttu-id="eae2e-109">Çoğaltmanın durumunu alma</span><span class="sxs-lookup"><span data-stu-id="eae2e-109">Get the status of the replication</span></span>

## <span data-ttu-id="eae2e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eae2e-110">EXAMPLES</span></span>

### <span data-ttu-id="eae2e-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eae2e-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="eae2e-112">Bu komut MyVol üzerindeki çoğaltmanın durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="eae2e-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="eae2e-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eae2e-113">PARAMETERS</span></span>

### <span data-ttu-id="eae2e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eae2e-114">-AccountName</span></span>
<span data-ttu-id="eae2e-115">Çoğaltma hedef biriminin ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="eae2e-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="eae2e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eae2e-116">-DefaultProfile</span></span>
<span data-ttu-id="eae2e-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eae2e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eae2e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eae2e-118">-InputObject</span></span>
<span data-ttu-id="eae2e-119">Yineleme durumunu almak için ANF çoğaltma hedef birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="eae2e-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="eae2e-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="eae2e-120">-Name</span></span>
<span data-ttu-id="eae2e-121">ANF çoğaltma hedef biriminin adı</span><span class="sxs-lookup"><span data-stu-id="eae2e-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="eae2e-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="eae2e-122">-PoolName</span></span>
<span data-ttu-id="eae2e-123">Çoğaltma hedef biriminin ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="eae2e-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="eae2e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eae2e-124">-ResourceGroupName</span></span>
<span data-ttu-id="eae2e-125">ANF çoğaltma hedef biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="eae2e-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="eae2e-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="eae2e-126">-ResourceId</span></span>
<span data-ttu-id="eae2e-127">ANF çoğaltma hedef biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="eae2e-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="eae2e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eae2e-128">CommonParameters</span></span>
<span data-ttu-id="eae2e-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eae2e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eae2e-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="eae2e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eae2e-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eae2e-131">INPUTS</span></span>

### <span data-ttu-id="eae2e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="eae2e-132">System.String</span></span>

## <span data-ttu-id="eae2e-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eae2e-133">OUTPUTS</span></span>

### <span data-ttu-id="eae2e-134">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="eae2e-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="eae2e-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eae2e-135">NOTES</span></span>

## <span data-ttu-id="eae2e-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eae2e-136">RELATED LINKS</span></span>
