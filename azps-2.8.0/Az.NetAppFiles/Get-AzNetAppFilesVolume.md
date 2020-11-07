---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 3d44c9def7dd56fa0d3fa58fd417a738c5db051b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932137"
---
# <span data-ttu-id="e7fd3-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="e7fd3-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="e7fd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="e7fd3-103">Bir Azure NetApp dosyası (ANF) biriminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="e7fd3-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="e7fd3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e7fd3-104">SYNTAX</span></span>

### <span data-ttu-id="e7fd3-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e7fd3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7fd3-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e7fd3-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e7fd3-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e7fd3-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7fd3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e7fd3-108">DESCRIPTION</span></span>
<span data-ttu-id="e7fd3-109">**Get-AzNetAppFilesVolume** cmdlet 'inin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="e7fd3-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="e7fd3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e7fd3-110">EXAMPLES</span></span>

### <span data-ttu-id="e7fd3-111">Örnek 1: ANF sesi edinme</span><span class="sxs-lookup"><span data-stu-id="e7fd3-111">Example 1: Get an ANF volume</span></span>
```
PS C:\>Get-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     :
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="e7fd3-112">Bu komut, "MyAnfPool" havuzundan MyAnfVolume adındaki birimi alır.</span><span class="sxs-lookup"><span data-stu-id="e7fd3-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="e7fd3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e7fd3-113">PARAMETERS</span></span>

### <span data-ttu-id="e7fd3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="e7fd3-114">-AccountName</span></span>
<span data-ttu-id="e7fd3-115">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="e7fd3-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="e7fd3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7fd3-116">-DefaultProfile</span></span>
<span data-ttu-id="e7fd3-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e7fd3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7fd3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="e7fd3-118">-Name</span></span>
<span data-ttu-id="e7fd3-119">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="e7fd3-119">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7fd3-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="e7fd3-120">-PoolName</span></span>
<span data-ttu-id="e7fd3-121">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="e7fd3-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="e7fd3-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="e7fd3-122">-PoolObject</span></span>
<span data-ttu-id="e7fd3-123">Döndürülecek birimi içeren havuz nesnesi</span><span class="sxs-lookup"><span data-stu-id="e7fd3-123">The pool object containing the volume to return</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e7fd3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7fd3-124">-ResourceGroupName</span></span>
<span data-ttu-id="e7fd3-125">ANF biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="e7fd3-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="e7fd3-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e7fd3-126">-ResourceId</span></span>
<span data-ttu-id="e7fd3-127">ANF biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e7fd3-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="e7fd3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7fd3-128">CommonParameters</span></span>
<span data-ttu-id="e7fd3-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e7fd3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e7fd3-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7fd3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7fd3-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e7fd3-131">INPUTS</span></span>

### <span data-ttu-id="e7fd3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="e7fd3-132">System.String</span></span>

### <span data-ttu-id="e7fd3-133">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="e7fd3-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="e7fd3-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e7fd3-134">OUTPUTS</span></span>

### <span data-ttu-id="e7fd3-135">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="e7fd3-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="e7fd3-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e7fd3-136">NOTES</span></span>

## <span data-ttu-id="e7fd3-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e7fd3-137">RELATED LINKS</span></span>