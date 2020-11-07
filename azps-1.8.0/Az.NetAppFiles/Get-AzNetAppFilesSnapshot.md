---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 8f34145a65cde73ea1a5b925064c2b9a1d3f92a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93760779"
---
# <span data-ttu-id="ad0f1-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="ad0f1-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="ad0f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad0f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ad0f1-103">Bir Azure NetApp dosyaları (ANF) anlık görüntüsünün ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ad0f1-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="ad0f1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ad0f1-104">SYNTAX</span></span>

### <span data-ttu-id="ad0f1-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ad0f1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ad0f1-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ad0f1-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ad0f1-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad0f1-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad0f1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="ad0f1-108">DESCRIPTION</span></span>
<span data-ttu-id="ad0f1-109">**Get-AzNetAppFilesSnapshot** cmdlet 'inin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="ad0f1-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="ad0f1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ad0f1-110">EXAMPLES</span></span>

### <span data-ttu-id="ad0f1-111">Örnek 1: anl anlık görüntü alın</span><span class="sxs-lookup"><span data-stu-id="ad0f1-111">Example 1: Get an ANF snapshot</span></span>
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
CreationDate      :
ProvisioningState : Succeeded
```

<span data-ttu-id="ad0f1-112">Bu komut, "MyAnfVolume" biriminden MyAnfSnapshot adındaki anlık görüntüyü alır.</span><span class="sxs-lookup"><span data-stu-id="ad0f1-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="ad0f1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ad0f1-113">PARAMETERS</span></span>

### <span data-ttu-id="ad0f1-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="ad0f1-114">-AccountName</span></span>
<span data-ttu-id="ad0f1-115">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="ad0f1-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="ad0f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad0f1-116">-DefaultProfile</span></span>
<span data-ttu-id="ad0f1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ad0f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad0f1-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="ad0f1-118">-Name</span></span>
<span data-ttu-id="ad0f1-119">ANF anlık görüntüsünün adı</span><span class="sxs-lookup"><span data-stu-id="ad0f1-119">The name of the ANF snapshot</span></span>

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

### <span data-ttu-id="ad0f1-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="ad0f1-120">-PoolName</span></span>
<span data-ttu-id="ad0f1-121">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="ad0f1-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="ad0f1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad0f1-122">-ResourceGroupName</span></span>
<span data-ttu-id="ad0f1-123">ANF biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="ad0f1-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="ad0f1-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="ad0f1-124">-ResourceId</span></span>
<span data-ttu-id="ad0f1-125">ANF anlık görüntüsünün kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="ad0f1-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="ad0f1-126">-BirimAdı</span><span class="sxs-lookup"><span data-stu-id="ad0f1-126">-VolumeName</span></span>
<span data-ttu-id="ad0f1-127">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="ad0f1-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="ad0f1-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="ad0f1-128">-VolumeObject</span></span>
<span data-ttu-id="ad0f1-129">Döndürülecek anlık görüntüyü içeren birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="ad0f1-129">The volume object containing the snapshot to return</span></span>

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

### <span data-ttu-id="ad0f1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad0f1-130">CommonParameters</span></span>
<span data-ttu-id="ad0f1-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ad0f1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ad0f1-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad0f1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad0f1-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ad0f1-133">INPUTS</span></span>

### <span data-ttu-id="ad0f1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ad0f1-134">System.String</span></span>

### <span data-ttu-id="ad0f1-135">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="ad0f1-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="ad0f1-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ad0f1-136">OUTPUTS</span></span>

### <span data-ttu-id="ad0f1-137">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="ad0f1-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="ad0f1-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ad0f1-138">NOTES</span></span>

## <span data-ttu-id="ad0f1-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ad0f1-139">RELATED LINKS</span></span>
