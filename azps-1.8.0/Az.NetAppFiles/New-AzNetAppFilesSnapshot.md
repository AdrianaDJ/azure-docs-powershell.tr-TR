---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesSnapshot.md
ms.openlocfilehash: bad4c1dfc2317bcc4d03414980cafa73c78949d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760771"
---
# <span data-ttu-id="58cea-101">New-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="58cea-101">New-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="58cea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58cea-102">SYNOPSIS</span></span>
<span data-ttu-id="58cea-103">Yeni bir Azure NetApp dosyaları (ANF) oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58cea-103">Creates a new Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="58cea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="58cea-104">SYNTAX</span></span>

### <span data-ttu-id="58cea-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="58cea-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesSnapshot -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -VolumeName <String> -Name <String> -FileSystemId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58cea-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58cea-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesSnapshot -Name <String> [-Tag <Hashtable>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58cea-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="58cea-107">DESCRIPTION</span></span>
<span data-ttu-id="58cea-108">**New-AzNetAppFilesSnapshot** cmdlet 'i ANF anlık görüntüsü oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58cea-108">The **New-AzNetAppFilesSnapshot** cmdlet creates an ANF snapshot.</span></span>

## <span data-ttu-id="58cea-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="58cea-109">EXAMPLES</span></span>

### <span data-ttu-id="58cea-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="58cea-110">Example 1</span></span>
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
CreationDate      :
ProvisioningState : Succeeded
```

<span data-ttu-id="58cea-111">Bu komut, "MyAnfVolume" birimi içinde yeni TIPF anlık görüntüsü "MyAnfSnapshot" oluşturur.</span><span class="sxs-lookup"><span data-stu-id="58cea-111">This command creates the new ANF snapshot "MyAnfSnapshot" within the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="58cea-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="58cea-112">PARAMETERS</span></span>

### <span data-ttu-id="58cea-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="58cea-113">-AccountName</span></span>
<span data-ttu-id="58cea-114">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="58cea-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="58cea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58cea-115">-DefaultProfile</span></span>
<span data-ttu-id="58cea-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="58cea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58cea-117">-Filesystemıd</span><span class="sxs-lookup"><span data-stu-id="58cea-117">-FileSystemId</span></span>
<span data-ttu-id="58cea-118">Dosya sistemi kimliği</span><span class="sxs-lookup"><span data-stu-id="58cea-118">The file system id</span></span>

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

### <span data-ttu-id="58cea-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="58cea-119">-Location</span></span>
<span data-ttu-id="58cea-120">Kaynağın konumu</span><span class="sxs-lookup"><span data-stu-id="58cea-120">The location of the resource</span></span>

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

### <span data-ttu-id="58cea-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="58cea-121">-Name</span></span>
<span data-ttu-id="58cea-122">ANF anlık görüntüsünün adı</span><span class="sxs-lookup"><span data-stu-id="58cea-122">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58cea-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="58cea-123">-PoolName</span></span>
<span data-ttu-id="58cea-124">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="58cea-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="58cea-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58cea-125">-ResourceGroupName</span></span>
<span data-ttu-id="58cea-126">ANF hesabının kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="58cea-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="58cea-127">Etiketli</span><span class="sxs-lookup"><span data-stu-id="58cea-127">-Tag</span></span>
<span data-ttu-id="58cea-128">Kaynak etiketlerini temsil eden bir Hashtable</span><span class="sxs-lookup"><span data-stu-id="58cea-128">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58cea-129">-BirimAdı</span><span class="sxs-lookup"><span data-stu-id="58cea-129">-VolumeName</span></span>
<span data-ttu-id="58cea-130">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="58cea-130">The name of the ANF volume</span></span>

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

### <span data-ttu-id="58cea-131">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="58cea-131">-VolumeObject</span></span>
<span data-ttu-id="58cea-132">Yeni anlık görüntü nesnesinin birimi</span><span class="sxs-lookup"><span data-stu-id="58cea-132">The volume for the new snapshot object</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58cea-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="58cea-133">-Confirm</span></span>
<span data-ttu-id="58cea-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="58cea-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58cea-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58cea-135">-WhatIf</span></span>
<span data-ttu-id="58cea-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="58cea-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58cea-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="58cea-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58cea-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58cea-138">CommonParameters</span></span>
<span data-ttu-id="58cea-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="58cea-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="58cea-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58cea-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58cea-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="58cea-141">INPUTS</span></span>

### <span data-ttu-id="58cea-142">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="58cea-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="58cea-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="58cea-143">OUTPUTS</span></span>

### <span data-ttu-id="58cea-144">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="58cea-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="58cea-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="58cea-145">NOTES</span></span>

## <span data-ttu-id="58cea-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="58cea-146">RELATED LINKS</span></span>
