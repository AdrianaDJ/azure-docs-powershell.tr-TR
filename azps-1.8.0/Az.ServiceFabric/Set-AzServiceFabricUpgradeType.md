---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/set-azservicefabricupgradetype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Set-AzServiceFabricUpgradeType.md
ms.openlocfilehash: a82bec40d93b33385dfa9aa2b4a5c5d122e59aa2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759101"
---
# <span data-ttu-id="a6414-101">Set-AzServiceFabricUpgradeType</span><span class="sxs-lookup"><span data-stu-id="a6414-101">Set-AzServiceFabricUpgradeType</span></span>

## <span data-ttu-id="a6414-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6414-102">SYNOPSIS</span></span>
<span data-ttu-id="a6414-103">Kümenin hizmet yapısı yükseltme türünü değiştirin.</span><span class="sxs-lookup"><span data-stu-id="a6414-103">Change the Service Fabric upgrade type of the cluster.</span></span>

## <span data-ttu-id="a6414-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a6414-104">SYNTAX</span></span>

### <span data-ttu-id="a6414-105">Otomatik</span><span class="sxs-lookup"><span data-stu-id="a6414-105">Automatic</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6414-106">El ile</span><span class="sxs-lookup"><span data-stu-id="a6414-106">Manual</span></span>
```
Set-AzServiceFabricUpgradeType [-ResourceGroupName] <String> [-Name] <String> -UpgradeMode <ClusterUpgradeMode>
 -Version <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6414-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a6414-107">DESCRIPTION</span></span>
<span data-ttu-id="a6414-108">Belirli bir hizmet yapısı kodu sürümüyle, yükseltme türünü otomatik veya el ile ayarlamak için **set-AzServiceFabricUpgradeType** kullanın.</span><span class="sxs-lookup"><span data-stu-id="a6414-108">Use **Set-AzServiceFabricUpgradeType** to set upgrade type to automatic or manual with specific Service Fabric code version.</span></span>

## <span data-ttu-id="a6414-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a6414-109">EXAMPLES</span></span>

### <span data-ttu-id="a6414-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a6414-110">Example 1</span></span>
```
PS c:> Set-AzServiceFabricUpgradeType -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster'  -UpgradeMode Automatic
```

<span data-ttu-id="a6414-111">Bu komut küme yükseltme modunu otomatik olarak ayarlar.</span><span class="sxs-lookup"><span data-stu-id="a6414-111">This command will set the cluster upgrade mode to automatic.</span></span>

## <span data-ttu-id="a6414-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a6414-112">PARAMETERS</span></span>

### <span data-ttu-id="a6414-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6414-113">-DefaultProfile</span></span>
<span data-ttu-id="a6414-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a6414-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6414-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="a6414-115">-Name</span></span>
<span data-ttu-id="a6414-116">Kümenin adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="a6414-116">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="a6414-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6414-117">-ResourceGroupName</span></span>
<span data-ttu-id="a6414-118">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a6414-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a6414-119">-UpgradeMode</span><span class="sxs-lookup"><span data-stu-id="a6414-119">-UpgradeMode</span></span>
<span data-ttu-id="a6414-120">Clusterupgrademodu</span><span class="sxs-lookup"><span data-stu-id="a6414-120">ClusterUpgradeMode</span></span>

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

### <span data-ttu-id="a6414-121">-Version</span><span class="sxs-lookup"><span data-stu-id="a6414-121">-Version</span></span>
<span data-ttu-id="a6414-122">Küme kodu sürümü.</span><span class="sxs-lookup"><span data-stu-id="a6414-122">Cluster code version.</span></span>

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

### <span data-ttu-id="a6414-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="a6414-123">-Confirm</span></span>
<span data-ttu-id="a6414-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a6414-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6414-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6414-125">-WhatIf</span></span>
<span data-ttu-id="a6414-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a6414-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a6414-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a6414-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6414-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6414-128">CommonParameters</span></span>
<span data-ttu-id="a6414-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a6414-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6414-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6414-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6414-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a6414-131">INPUTS</span></span>

### <span data-ttu-id="a6414-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a6414-132">System.String</span></span>

### <span data-ttu-id="a6414-133">Microsoft. Azure. Commands. ServiceFabric. modeller. Kümeupgrademode</span><span class="sxs-lookup"><span data-stu-id="a6414-133">Microsoft.Azure.Commands.ServiceFabric.Models.ClusterUpgradeMode</span></span>

## <span data-ttu-id="a6414-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a6414-134">OUTPUTS</span></span>

### <span data-ttu-id="a6414-135">Microsoft. Azure. Commands. ServiceFabric. modeller. PSCluster</span><span class="sxs-lookup"><span data-stu-id="a6414-135">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="a6414-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a6414-136">NOTES</span></span>

## <span data-ttu-id="a6414-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a6414-137">RELATED LINKS</span></span>