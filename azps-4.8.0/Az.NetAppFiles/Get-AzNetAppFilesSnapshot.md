---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 0f1b6806565a21b106816019c08641e269c4d5a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94108166"
---
# <span data-ttu-id="73e8a-101">Get-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="73e8a-101">Get-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="73e8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73e8a-102">SYNOPSIS</span></span>
<span data-ttu-id="73e8a-103">Bir Azure NetApp dosyaları (ANF) anlık görüntüsünün ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="73e8a-103">Gets details of an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="73e8a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73e8a-104">SYNTAX</span></span>

### <span data-ttu-id="73e8a-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73e8a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73e8a-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="73e8a-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="73e8a-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73e8a-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesSnapshot [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73e8a-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="73e8a-108">DESCRIPTION</span></span>
<span data-ttu-id="73e8a-109">**Get-AzNetAppFilesSnapshot** cmdlet 'inin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="73e8a-109">The **Get-AzNetAppFilesSnapshot** cmdlet gets details of an ANF snapshot.</span></span>

## <span data-ttu-id="73e8a-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73e8a-110">EXAMPLES</span></span>

### <span data-ttu-id="73e8a-111">Örnek 1: anl anlık görüntü alın</span><span class="sxs-lookup"><span data-stu-id="73e8a-111">Example 1: Get an ANF snapshot</span></span>
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

<span data-ttu-id="73e8a-112">Bu komut, "MyAnfVolume" biriminden MyAnfSnapshot adındaki anlık görüntüyü alır.</span><span class="sxs-lookup"><span data-stu-id="73e8a-112">This command gets the snapshot named MyAnfSnapshot from the volume "MyAnfVolume".</span></span>

## <span data-ttu-id="73e8a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73e8a-113">PARAMETERS</span></span>

### <span data-ttu-id="73e8a-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="73e8a-114">-AccountName</span></span>
<span data-ttu-id="73e8a-115">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="73e8a-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="73e8a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73e8a-116">-DefaultProfile</span></span>
<span data-ttu-id="73e8a-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73e8a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73e8a-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="73e8a-118">-Name</span></span>
<span data-ttu-id="73e8a-119">ANF anlık görüntüsünün adı</span><span class="sxs-lookup"><span data-stu-id="73e8a-119">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SnapshotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73e8a-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="73e8a-120">-PoolName</span></span>
<span data-ttu-id="73e8a-121">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="73e8a-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="73e8a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73e8a-122">-ResourceGroupName</span></span>
<span data-ttu-id="73e8a-123">ANF biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="73e8a-123">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="73e8a-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="73e8a-124">-ResourceId</span></span>
<span data-ttu-id="73e8a-125">ANF anlık görüntüsünün kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="73e8a-125">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="73e8a-126">-BirimAdı</span><span class="sxs-lookup"><span data-stu-id="73e8a-126">-VolumeName</span></span>
<span data-ttu-id="73e8a-127">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="73e8a-127">The name of the ANF volume</span></span>

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

### <span data-ttu-id="73e8a-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="73e8a-128">-VolumeObject</span></span>
<span data-ttu-id="73e8a-129">Döndürülecek anlık görüntüyü içeren birim nesnesi</span><span class="sxs-lookup"><span data-stu-id="73e8a-129">The volume object containing the snapshot to return</span></span>

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

### <span data-ttu-id="73e8a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e8a-130">CommonParameters</span></span>
<span data-ttu-id="73e8a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73e8a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e8a-132">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="73e8a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e8a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73e8a-133">INPUTS</span></span>

### <span data-ttu-id="73e8a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="73e8a-134">System.String</span></span>

### <span data-ttu-id="73e8a-135">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="73e8a-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="73e8a-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73e8a-136">OUTPUTS</span></span>

### <span data-ttu-id="73e8a-137">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="73e8a-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="73e8a-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73e8a-138">NOTES</span></span>

## <span data-ttu-id="73e8a-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73e8a-139">RELATED LINKS</span></span>
