---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 1a04f128326c0b2259b81d6c58c4bc7b0113e9db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267258"
---
# <span data-ttu-id="fb879-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="fb879-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="fb879-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb879-102">SYNOPSIS</span></span>
<span data-ttu-id="fb879-103">Bir Azure NetApp dosyası (ANF) biriminin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="fb879-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="fb879-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fb879-104">SYNTAX</span></span>

### <span data-ttu-id="fb879-105">ByFieldsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fb879-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb879-106">Byresourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="fb879-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb879-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb879-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb879-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fb879-108">DESCRIPTION</span></span>
<span data-ttu-id="fb879-109">**Get-AzNetAppFilesVolume** cmdlet 'inin ayrıntılarını alır.</span><span class="sxs-lookup"><span data-stu-id="fb879-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="fb879-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fb879-110">EXAMPLES</span></span>

### <span data-ttu-id="fb879-111">Örnek 1: ANF sesi edinme</span><span class="sxs-lookup"><span data-stu-id="fb879-111">Example 1: Get an ANF volume</span></span>
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

<span data-ttu-id="fb879-112">Bu komut, "MyAnfPool" havuzundan MyAnfVolume adındaki birimi alır.</span><span class="sxs-lookup"><span data-stu-id="fb879-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="fb879-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fb879-113">PARAMETERS</span></span>

### <span data-ttu-id="fb879-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fb879-114">-AccountName</span></span>
<span data-ttu-id="fb879-115">ANF hesabının adı</span><span class="sxs-lookup"><span data-stu-id="fb879-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="fb879-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb879-116">-DefaultProfile</span></span>
<span data-ttu-id="fb879-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fb879-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb879-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="fb879-118">-Name</span></span>
<span data-ttu-id="fb879-119">ANF biriminin adı</span><span class="sxs-lookup"><span data-stu-id="fb879-119">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb879-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="fb879-120">-PoolName</span></span>
<span data-ttu-id="fb879-121">ANF havuzunun adı</span><span class="sxs-lookup"><span data-stu-id="fb879-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="fb879-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="fb879-122">-PoolObject</span></span>
<span data-ttu-id="fb879-123">Döndürülecek birimi içeren havuz nesnesi</span><span class="sxs-lookup"><span data-stu-id="fb879-123">The pool object containing the volume to return</span></span>

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

### <span data-ttu-id="fb879-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb879-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb879-125">ANF biriminin kaynak grubu</span><span class="sxs-lookup"><span data-stu-id="fb879-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="fb879-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fb879-126">-ResourceId</span></span>
<span data-ttu-id="fb879-127">ANF biriminin kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="fb879-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="fb879-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb879-128">CommonParameters</span></span>
<span data-ttu-id="fb879-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fb879-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb879-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="fb879-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb879-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fb879-131">INPUTS</span></span>

### <span data-ttu-id="fb879-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fb879-132">System.String</span></span>

### <span data-ttu-id="fb879-133">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="fb879-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="fb879-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fb879-134">OUTPUTS</span></span>

### <span data-ttu-id="fb879-135">Microsoft. Azure. Commands. NetAppFiles. modeller. PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="fb879-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="fb879-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fb879-136">NOTES</span></span>

## <span data-ttu-id="fb879-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fb879-137">RELATED LINKS</span></span>
