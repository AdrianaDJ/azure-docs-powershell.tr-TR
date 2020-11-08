---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 1fe8da5c9ee899b7aa1a77a9fbb0ac7a2bf3b35c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278394"
---
# <span data-ttu-id="31aae-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="31aae-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="31aae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31aae-102">SYNOPSIS</span></span>
<span data-ttu-id="31aae-103">Yeni bir Azure NetApp dosyaları (ANF) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31aae-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="31aae-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="31aae-104">SYNTAX</span></span>

### <span data-ttu-id="31aae-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="31aae-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> [-FileSystemId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31aae-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="31aae-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31aae-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="31aae-107">DESCRIPTION</span></span>
<span data-ttu-id="31aae-108">**New-AzNetAppFilesSnapshot** cmdlet 'i ANF anlık görüntüsü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31aae-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="31aae-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="31aae-109">EXAMPLES</span></span>

### <span data-ttu-id="31aae-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="31aae-110">Example 1</span></span>
```
PS C:\>New-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -SnapshotName "MyAnfSnapshot" -FileSystemId "3e2773a7-2a72-d003-0637-1a8b1fa3eaaf"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="31aae-111">Bu komut, "MyAnfVolume" birimi içinde yeni TIPF anlık görüntüsü "MyAnfSnapshot" oluşturur.</span><span class="sxs-lookup"><span data-stu-id="31aae-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="31aae-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="31aae-112">PARAMETERS</span></span>

### <span data-ttu-id="31aae-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="31aae-113">-AccountName</span></span>
<span data-ttu-id="31aae-114">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="31aae-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="31aae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31aae-115">-DefaultProfile</span></span>
<span data-ttu-id="31aae-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="31aae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31aae-117">-Filesystemıd</span><span class="sxs-lookup"><span data-stu-id="31aae-117">-FileSystemId</span></span>
<span data-ttu-id="31aae-118">Dosya sistemi kimliği</span><span class="sxs-lookup"><span data-stu-id="31aae-118">The file system id</span></span>

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

### <span data-ttu-id="31aae-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="31aae-119">-Location</span></span>
<span data-ttu-id="31aae-120">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="31aae-120">The location of the resource</span></span>

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

### <span data-ttu-id="31aae-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="31aae-121">-Name</span></span>
<span data-ttu-id="31aae-122">ANF anlık görüntüsünün adı</span><span class="sxs-lookup"><span data-stu-id="31aae-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31aae-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="31aae-123">-PoolName</span></span>
<span data-ttu-id="31aae-124">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="31aae-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="31aae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31aae-125">-ResourceGroupName</span></span>
<span data-ttu-id="31aae-126">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="31aae-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="31aae-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="31aae-127">-Tag</span></span>
<span data-ttu-id="31aae-128">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="31aae-128">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="31aae-129">-BirimAdı</span><span class="sxs-lookup"><span data-stu-id="31aae-129">-VolumeName</span></span>
<span data-ttu-id="31aae-130">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="31aae-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="31aae-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="31aae-131">-VolumeObject</span></span>
<span data-ttu-id="31aae-132">Yeni anlık görüntü nesnesinin birimi</span><span class="sxs-lookup"><span data-stu-id="31aae-132">The volume for the new snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31aae-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="31aae-133">-Confirm</span></span>
<span data-ttu-id="31aae-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="31aae-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31aae-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31aae-135">-WhatIf</span></span>
<span data-ttu-id="31aae-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="31aae-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31aae-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="31aae-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31aae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31aae-138">CommonParameters</span></span>
<span data-ttu-id="31aae-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="31aae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31aae-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="31aae-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31aae-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="31aae-141">INPUTS</span></span>

### <span data-ttu-id="31aae-142">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="31aae-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="31aae-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="31aae-143">OUTPUTS</span></span>

### <span data-ttu-id="31aae-144">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="31aae-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="31aae-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="31aae-145">NOTES</span></span>

## <span data-ttu-id="31aae-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="31aae-146">RELATED LINKS</span></span>
