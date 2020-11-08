---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: dce91ee25cac4a716dc604e38f1ac38e5a3f3f1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278389"
---
# <span data-ttu-id="a26ae-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a26ae-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="a26ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a26ae-102">SYNOPSIS</span></span>
<span data-ttu-id="a26ae-103">Yeni bir Azure NetApp dosyaları (ANF) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a26ae-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="a26ae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a26ae-104">SYNTAX</span></span>

### <span data-ttu-id="a26ae-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a26ae-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a26ae-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a26ae-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a26ae-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a26ae-107">DESCRIPTION</span></span>
<span data-ttu-id="a26ae-108">**Yeni-AzNetAppFilesVolume** cmdlet 'ı BIR ANF birimi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a26ae-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="a26ae-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a26ae-109">EXAMPLES</span></span>

### <span data-ttu-id="a26ae-110">Örnek 1: ANF birimi oluşturma</span><span class="sxs-lookup"><span data-stu-id="a26ae-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="a26ae-111">Bu komut, "MyAnfPool" havuzunda yeni ANF birimi "MyAnfVolume" oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a26ae-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="a26ae-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a26ae-112">PARAMETERS</span></span>

### <span data-ttu-id="a26ae-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a26ae-113">-AccountName</span></span>
<span data-ttu-id="a26ae-114">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="a26ae-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="a26ae-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="a26ae-115">-CreationToken</span></span>
<span data-ttu-id="a26ae-116">Birim için benzersiz bir dosya yolu</span><span class="sxs-lookup"><span data-stu-id="a26ae-116">A unique file path for the volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a26ae-117">-DefaultProfile</span></span>
<span data-ttu-id="a26ae-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a26ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a26ae-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="a26ae-119">-ExportPolicy</span></span>
<span data-ttu-id="a26ae-120">Dışarı aktarma ilkesini temsil eden bir Hashtable dizisi</span><span class="sxs-lookup"><span data-stu-id="a26ae-120">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ae-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="a26ae-121">-Location</span></span>
<span data-ttu-id="a26ae-122">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="a26ae-122">The location of the resource</span></span>

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

### <span data-ttu-id="a26ae-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="a26ae-123">-Name</span></span>
<span data-ttu-id="a26ae-124">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="a26ae-124">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ae-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a26ae-125">-PoolName</span></span>
<span data-ttu-id="a26ae-126">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="a26ae-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="a26ae-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="a26ae-127">-PoolObject</span></span>
<span data-ttu-id="a26ae-128">Yeni birim için havuz</span><span class="sxs-lookup"><span data-stu-id="a26ae-128">The pool for the new volume object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a26ae-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="a26ae-129">-ProtocolType</span></span>
<span data-ttu-id="a26ae-130">Dışarı aktarma ilkesini temsil eden bir Hashtable dizisi</span><span class="sxs-lookup"><span data-stu-id="a26ae-130">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ae-131">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="a26ae-131">-ReplicationObject</span></span>
<span data-ttu-id="a26ae-132">Replication nesnesini temsil eden bir Hashtable dizisi</span><span class="sxs-lookup"><span data-stu-id="a26ae-132">A hashtable array which represents the replication object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ae-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a26ae-133">-ResourceGroupName</span></span>
<span data-ttu-id="a26ae-134">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="a26ae-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="a26ae-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="a26ae-135">-ServiceLevel</span></span>
<span data-ttu-id="a26ae-136">ANF biriminin hizmet düzeyi</span><span class="sxs-lookup"><span data-stu-id="a26ae-136">The service level of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ae-137">-Anlık anlık kimliği</span><span class="sxs-lookup"><span data-stu-id="a26ae-137">-SnapshotId</span></span>
<span data-ttu-id="a26ae-138">Anlık görüntüden birim oluşturma.</span><span class="sxs-lookup"><span data-stu-id="a26ae-138">Create volume from a snapshot.</span></span> <span data-ttu-id="a26ae-139">Anlık görüntüyü tanımlamakta kullanılan UUID v4 veya kaynak tanımlayıcısı</span><span class="sxs-lookup"><span data-stu-id="a26ae-139">UUID v4 or resource identifier used to identify the Snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ae-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a26ae-140">-SubnetId</span></span>
<span data-ttu-id="a26ae-141">Atanmış bir alt ağ için Azure Resource URI 'SI</span><span class="sxs-lookup"><span data-stu-id="a26ae-141">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ae-142">Etiketli</span><span class="sxs-lookup"><span data-stu-id="a26ae-142">-Tag</span></span>
<span data-ttu-id="a26ae-143">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="a26ae-143">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ae-144">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="a26ae-144">-UsageThreshold</span></span>
<span data-ttu-id="a26ae-145">Bayt cinsinden bir dosya sistemi için izin verilen maksimum depolama kotası</span><span class="sxs-lookup"><span data-stu-id="a26ae-145">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ae-146">-Birimtürü</span><span class="sxs-lookup"><span data-stu-id="a26ae-146">-VolumeType</span></span>
<span data-ttu-id="a26ae-147">ANF biriminin türü</span><span class="sxs-lookup"><span data-stu-id="a26ae-147">The type of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a26ae-148">-Onay</span><span class="sxs-lookup"><span data-stu-id="a26ae-148">-Confirm</span></span>
<span data-ttu-id="a26ae-149">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a26ae-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a26ae-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a26ae-150">-WhatIf</span></span>
<span data-ttu-id="a26ae-151">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a26ae-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a26ae-152">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a26ae-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a26ae-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a26ae-153">CommonParameters</span></span>
<span data-ttu-id="a26ae-154">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a26ae-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a26ae-155">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a26ae-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a26ae-156">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a26ae-156">INPUTS</span></span>

### <span data-ttu-id="a26ae-157">System. String</span><span class="sxs-lookup"><span data-stu-id="a26ae-157">System.String</span></span>

### <span data-ttu-id="a26ae-158">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="a26ae-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="a26ae-159">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a26ae-159">OUTPUTS</span></span>

### <span data-ttu-id="a26ae-160">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a26ae-160">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a26ae-161">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a26ae-161">NOTES</span></span>

## <span data-ttu-id="a26ae-162">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a26ae-162">RELATED LINKS</span></span>
