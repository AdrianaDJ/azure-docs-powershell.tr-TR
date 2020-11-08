---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: b41acc1d10a09febec04b60c397496b97606fb18
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937254"
---
# <span data-ttu-id="ec0c6-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="ec0c6-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="ec0c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec0c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0c6-103">Bir Azure NetApp dosyaları (ANF) anlık görüntüsünün ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ec0c6-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="ec0c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ec0c6-104">SYNTAX</span></span>

### <span data-ttu-id="ec0c6-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ec0c6-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec0c6-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ec0c6-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ec0c6-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec0c6-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec0c6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ec0c6-108">DESCRIPTION</span></span>
<span data-ttu-id="ec0c6-109">**Get-AzNetAppFilesSnapshot** cmdlet 'inin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ec0c6-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="ec0c6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ec0c6-110">EXAMPLES</span></span>

### <span data-ttu-id="ec0c6-111">Örnek 1: anl anlık görüntü alın</span><span class="sxs-lookup"><span data-stu-id="ec0c6-111">Example 1: Get an ANF snapshot</span></span>
```
PS C:\>Get-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume/snapshots/MyAnfSnapshot
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume/MyAnfSnapshot
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes/snapshots
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
SnapshotId        : ca7c4ebd-91cb-0e30-91f5-9154050033df
Created           :
ProvisioningState : Succeeded
```

<span data-ttu-id="ec0c6-112">Bu komut, "MyAnfVolume" biriminden MyAnfSnapshot adındaki anlık görüntüyü alır.</span><span class="sxs-lookup"><span data-stu-id="ec0c6-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="ec0c6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ec0c6-113">PARAMETERS</span></span>

### <span data-ttu-id="ec0c6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ec0c6-114">-AccountName</span></span>
<span data-ttu-id="ec0c6-115">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="ec0c6-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="ec0c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0c6-116">-DefaultProfile</span></span>
<span data-ttu-id="ec0c6-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ec0c6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec0c6-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="ec0c6-118">-Name</span></span>
<span data-ttu-id="ec0c6-119">ANF anlık görüntüsünün adı</span><span class="sxs-lookup"><span data-stu-id="ec0c6-119">The name of the ANF snapshot</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec0c6-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ec0c6-120">-PoolName</span></span>
<span data-ttu-id="ec0c6-121">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="ec0c6-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="ec0c6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec0c6-122">-ResourceGroupName</span></span>
<span data-ttu-id="ec0c6-123">ANF biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="ec0c6-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="ec0c6-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ec0c6-124">-ResourceId</span></span>
<span data-ttu-id="ec0c6-125">ANF anlık görüntüsünün kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ec0c6-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="ec0c6-126">-BirimAdı</span><span class="sxs-lookup"><span data-stu-id="ec0c6-126">-VolumeName</span></span>
<span data-ttu-id="ec0c6-127">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="ec0c6-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="ec0c6-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="ec0c6-128">-VolumeObject</span></span>
<span data-ttu-id="ec0c6-129">Döndürülecek anlık görüntüyü içeren birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="ec0c6-129">The volume object containing the snapshot to return</span></span>

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

### <span data-ttu-id="ec0c6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0c6-130">CommonParameters</span></span>
<span data-ttu-id="ec0c6-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ec0c6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ec0c6-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec0c6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0c6-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ec0c6-133">INPUTS</span></span>

### <span data-ttu-id="ec0c6-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ec0c6-134">System.String</span></span>

### <span data-ttu-id="ec0c6-135">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ec0c6-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ec0c6-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ec0c6-136">OUTPUTS</span></span>

### <span data-ttu-id="ec0c6-137">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="ec0c6-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="ec0c6-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ec0c6-138">NOTES</span></span>

## <span data-ttu-id="ec0c6-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ec0c6-139">RELATED LINKS</span></span>