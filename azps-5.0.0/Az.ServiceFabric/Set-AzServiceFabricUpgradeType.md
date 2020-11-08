---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: 346bb9cb073488d0112ea08db22fb1f6c387bac9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279453"
---
# <span data-ttu-id="37050-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="37050-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="37050-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37050-102">SYNOPSIS</span></span>
<span data-ttu-id="37050-103">Kümenin hizmet yapısı yükseltme türünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="37050-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="37050-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37050-104">SYNTAX</span></span>

### <span data-ttu-id="37050-105">Otomatik</span><span class="sxs-lookup"><span data-stu-id="37050-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37050-106">El ile</span><span class="sxs-lookup"><span data-stu-id="37050-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37050-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="37050-107">DESCRIPTION</span></span>
<span data-ttu-id="37050-108">Belirli bir hizmet yapısı kodu sürümüyle, yükseltme türünü otomatik veya el ile ayarlamak için **set-AzServiceFabricUpgradeType** kullanın.</span><span class="sxs-lookup"><span data-stu-id="37050-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="37050-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37050-109">EXAMPLES</span></span>

### <span data-ttu-id="37050-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="37050-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="37050-111">Bu komut küme yükseltme modunu otomatik olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="37050-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="37050-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37050-112">PARAMETERS</span></span>

### <span data-ttu-id="37050-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37050-113">-DefaultProfile</span></span>
<span data-ttu-id="37050-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="37050-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37050-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="37050-115">-Name</span></span>
<span data-ttu-id="37050-116">Kümenin adını belirtme</span><span class="sxs-lookup"><span data-stu-id="37050-116">Specify the name of the cluster</span></span>

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

### <span data-ttu-id="37050-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37050-117">-ResourceGroupName</span></span>
<span data-ttu-id="37050-118">Kaynak grubunun adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="37050-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="37050-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="37050-119">-UpgradeMode</span></span>
<span data-ttu-id="37050-120">Clusterupgrademodu</span><span class="sxs-lookup"><span data-stu-id="37050-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="37050-121">-Version</span><span class="sxs-lookup"><span data-stu-id="37050-121">-Version</span></span>
<span data-ttu-id="37050-122">Küme kodu sürümü</span><span class="sxs-lookup"><span data-stu-id="37050-122">Cluster code version</span></span>

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

### <span data-ttu-id="37050-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="37050-123">-Confirm</span></span>
<span data-ttu-id="37050-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="37050-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37050-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37050-125">-WhatIf</span></span>
<span data-ttu-id="37050-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="37050-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37050-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="37050-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37050-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37050-128">CommonParameters</span></span>
<span data-ttu-id="37050-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37050-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37050-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="37050-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37050-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37050-131">INPUTS</span></span>

### <span data-ttu-id="37050-132">System. String</span><span class="sxs-lookup"><span data-stu-id="37050-132">System.String</span></span>

### <span data-ttu-id="37050-133">Microsoft. Azure. Commands. ServiceFabric. modeller. Kümeupgrademode</span><span class="sxs-lookup"><span data-stu-id="37050-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="37050-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37050-134">OUTPUTS</span></span>

### <span data-ttu-id="37050-135">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="37050-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="37050-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37050-136">NOTES</span></span>

## <span data-ttu-id="37050-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37050-137">RELATED LINKS</span></span>
