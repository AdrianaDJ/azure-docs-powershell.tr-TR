---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: c29a1bf4b5b60034a8f38ff8388f36997dbddfc7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104293"
---
# <span data-ttu-id="4dc28-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="4dc28-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="4dc28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dc28-102">SYNOPSIS</span></span>
<span data-ttu-id="4dc28-103">Kümenin hizmet yapısı yükseltme türünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="4dc28-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="4dc28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4dc28-104">SYNTAX</span></span>

### <span data-ttu-id="4dc28-105">Otomatik</span><span class="sxs-lookup"><span data-stu-id="4dc28-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dc28-106">El ile</span><span class="sxs-lookup"><span data-stu-id="4dc28-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dc28-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4dc28-107">DESCRIPTION</span></span>
<span data-ttu-id="4dc28-108">Belirli bir hizmet yapısı kodu sürümüyle, yükseltme türünü otomatik veya el ile ayarlamak için **set-AzServiceFabricUpgradeType** kullanın.</span><span class="sxs-lookup"><span data-stu-id="4dc28-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="4dc28-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4dc28-109">EXAMPLES</span></span>

### <span data-ttu-id="4dc28-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4dc28-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="4dc28-111">Bu komut küme yükseltme modunu otomatik olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4dc28-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="4dc28-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4dc28-112">PARAMETERS</span></span>

### <span data-ttu-id="4dc28-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dc28-113">-DefaultProfile</span></span>
<span data-ttu-id="4dc28-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4dc28-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dc28-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="4dc28-115">-Name</span></span>
<span data-ttu-id="4dc28-116">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="4dc28-116">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc28-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dc28-117">-ResourceGroupName</span></span>
<span data-ttu-id="4dc28-118">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="4dc28-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc28-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="4dc28-119">-UpgradeMode</span></span>
<span data-ttu-id="4dc28-120">Clusterupgrademodu</span><span class="sxs-lookup"><span data-stu-id="4dc28-120">ClusterUpgradeMode</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc28-121">-Version</span><span class="sxs-lookup"><span data-stu-id="4dc28-121">-Version</span></span>
<span data-ttu-id="4dc28-122">Küme kodu sürümü</span><span class="sxs-lookup"><span data-stu-id="4dc28-122">Cluster code version</span></span>

```yaml
Type: System.String
Parameter Sets: Manual
Aliases: ClusterCodeVersion

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dc28-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="4dc28-123">-Confirm</span></span>
<span data-ttu-id="4dc28-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4dc28-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dc28-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dc28-125">-WhatIf</span></span>
<span data-ttu-id="4dc28-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4dc28-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dc28-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4dc28-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dc28-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dc28-128">CommonParameters</span></span>
<span data-ttu-id="4dc28-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4dc28-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dc28-130">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dc28-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dc28-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4dc28-131">INPUTS</span></span>

### <span data-ttu-id="4dc28-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4dc28-132">System.String</span></span>

### <span data-ttu-id="4dc28-133">Microsoft. Azure. Commands. ServiceFabric. modeller. Kümeupgrademode</span><span class="sxs-lookup"><span data-stu-id="4dc28-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="4dc28-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4dc28-134">OUTPUTS</span></span>

### <span data-ttu-id="4dc28-135">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="4dc28-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="4dc28-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4dc28-136">NOTES</span></span>

## <span data-ttu-id="4dc28-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4dc28-137">RELATED LINKS</span></span>
